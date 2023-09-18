let menuControle = true;

const tarefas = [];

function criarTarefa(titulo, descricao) {
    return {
        titulo: titulo,
        descricao: descricao,
        status: "pendente"
    };
}

function criarTarefas(titulo, descricao) {
    tarefas.push({
        titulo: titulo,
        descricao: descricao,
        status: "pendente"
    });
}

function editar() {
    let numeroTarefaEditar = Number(prompt("Digite o número da tarefa que deseja editar:"));

    numeroTarefaEditar -= 1;

    if (numeroTarefaEditar >= 0 && numeroTarefaEditar < tarefas.length) {
        let opcaoDeEdicao = prompt("O que você deseja editar (titulo, descrição ou status)?");

        if (opcaoDeEdicao === "titulo") {
            let novoTitulo = prompt("Digite o novo título:");
            tarefas[numeroTarefaEditar].titulo = novoTitulo;
        } else if (opcaoDeEdicao === "descrição") {
            let novaDescricao = prompt("Digite a nova descrição:");
            tarefas[numeroTarefaEditar].descricao = novaDescricao;
        } else if (opcaoDeEdicao === "status") {
            let novoStatus = prompt("Digite o novo Status:");
            tarefas[numeroTarefaEditar].status = novoStatus;
        } else {
            console.log("Opção de edição inválida.");
        }
        console.log("Tarefa editada com sucesso.");
    } else {
        console.log("Número de tarefa inválido.");
    }
}

function excluir() {
    let numeroTarefaExcluir = Number(prompt("Qual tarefa você deseja deletar?"));

    numeroTarefaExcluir -= 1;

    if (numeroTarefaExcluir >= 0 && numeroTarefaExcluir < tarefas.length) {
        tarefas.splice(numeroTarefaExcluir, 1);
        console.log("Tarefa deletada com sucesso.");
    } else {
        console.log("Tarefa não encontrada.");
    }
}

function exibirMenu() {
    console.log("Selecione uma opção:");
    console.log("1. Opção 1 para criar uma tarefa");
    console.log("2. Opção 2 para editar");
    console.log("3. Opção 3 para excluir");
    console.log("4. Opção 4 para mostrar a lista");
}

while (menuControle) {
    exibirMenu();
    const escolha2 = prompt("Digite o número da opção desejada. Digite 0 para mostrar a sua lista:");

    if (escolha2 === "1") {
        const titulo = prompt("Título da tarefa:");
        const descricao = prompt("Descrição da tarefa:");
        criarTarefas(titulo, descricao);
    } else if (escolha2 === "2") {
        editar();
    } else if (escolha2 === "3") {
        excluir();
    } else if (escolha2 === "4") {
        console.log(tarefas);
    } else {
        console.log("Opção inválida.");
        menuControle = false;
    }
}

