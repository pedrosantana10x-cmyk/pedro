<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Adote um Amigo - I Love so Pet</title>
    <link rel="stylesheet" href="style.css"> 
</head>
<style>
/* CSS do Estilo Pastel (Mantido embutido para execução imediata) */
:root {
    --pastel-green: #C8E6C9; /* Verde Hortelã Pastel */
    --pastel-brown: #EFEBE9; /* Bege/Creme Pastel */
    --pastel-grey: #CFD8DC;  /* Azul-Acinzentado Claro Pastel */
    --dark-text: #546E7A;    /* Texto Muted (Azul-Acinzentado Escuro) */
    --border-color: #A79F9B; /* Cor de borda Muted */
}

/* Estilos Gerais do Corpo */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: var(--pastel-brown);
    color: var(--dark-text);
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

/* Cabeçalho */
header {
    background-color: var(--pastel-green);
    color: var(--dark-text);
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h1 {
    margin: 0;
    font-size: 2.2em;
}

/* Containers de Seção */
.manager, .flex-container {
    max-width: 600px;
    margin: 30px auto;
    padding: 30px;
    background-color: var(--pastel-grey);
    border-radius: 12px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

/* Estilos do Formulário */
.manager form {
    display: flex;
    flex-direction: column;
}

legend {
    font-weight: 600;
    margin-bottom: 25px;
    font-size: 1.2em;
    color: var(--dark-text);
    text-align: center;
}

label {
    margin-top: 15px;
    margin-bottom: 5px;
    font-weight: 500;
}

input[type="text"], 
input[type="email"], 
input[type="tel"],
select {
    padding: 12px;
    margin-bottom: 20px;
    border: 1px solid var(--border-color);
    border-radius: 6px;
    box-sizing: border-box; 
    background-color: #ffffff; 
    color: var(--dark-text);
    transition: border-color 0.3s ease;
}

input[type="text"]:focus, 
input[type="email"]:focus, 
input[type="tel"]:focus,
select:focus {
    border-color: var(--pastel-green);
    outline: none;
}

/* Botão de Envio */
input[type="submit"] {
    background-color: var(--pastel-green);
    color: var(--dark-text);
    padding: 15px 20px;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    font-size: 1.1em;
    font-weight: bold;
    transition: background-color 0.3s ease, transform 0.1s ease;
    margin-top: 20px;
}

input[type="submit"]:hover {
    background-color: #A5D6A7;
}

input[type="submit"]:active {
    transform: translateY(1px);
}

/* Estilo para a tag P */
.flex-container p {
    text-align: center;
    font-style: italic;
    color: var(--dark-text);
    padding-top: 15px;
    margin-top: 15px;
    border-top: 1px solid var(--border-color);
}

#selecao {
    padding: 12px;
}

.toggle-btn {
    background-color: var(--pastel-green);
    color: var(--dark-text);
    padding: 15px;
    margin: 8px 0;
    border: none;
    border-radius: 6px;
    width: 100%;
    text-align: left;
    font-size: 1.1em;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.toggle-btn:hover {
    background-color: #A5D6A7;
}

/* Estilos para o Conteúdo Colapsável */
.collapse-content {
    padding: 0 15px; /* Padding ajustado para melhor transição */
    background-color: var(--pastel-brown);
    border-radius: 0 0 6px 6px;
    margin-bottom: 10px;
    /* Estilo principal para esconder o conteúdo por padrão */
    max-height: 0; 
    overflow: hidden;
    transition: max-height 0.4s ease-out, padding 0.4s ease-out;
}

/* Estilo para mostrar o conteúdo */
.collapse-content.active {
    max-height: 800px; /* Aumentado para acomodar a tabela */
    padding: 15px;
}

.collapse-content p {
    margin-top: 0;
    font-style: normal;
    text-align: left;
    border-top: none; 
}

/* Estilos para os Botões de Sub-Opção */
.sub-btn {
    background-color: var(--pastel-grey);
    color: var(--dark-text);
    padding: 10px 15px;
    border: 1px solid var(--border-color);
    border-radius: 4px;
    margin-right: 10px;
    margin-top: 10px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.sub-btn:hover {
    background-color: #B0BEC5;
}

/* Estilo especial para o botão de Denúncia */
.den-btn {
    background-color: #FFCDD2;
}

.den-btn:hover {
    background-color: #E57373; 
}

/* Estilos para a Tabela de Exemplo */
#tabela-exemplar {
    width: 100%; /* Ajustado para 100% dentro do container colapsado */
    margin: 20px 0; 
    border-collapse: collapse;
    background-color: #FFFFFF;
    border: 1px solid var(--border-color);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
    border-radius: 8px;
    overflow: hidden;
}

/* Cabeçalho da Tabela */
#tabela-exemplar thead th {
    background-color: var(--pastel-green);
    color: var(--dark-text);
    padding: 10px;
    text-align: left;
    font-weight: bold;
    border-bottom: 2px solid var(--border-color);
}

/* Células de Dados e Cabeçalho */
#tabela-exemplar th, 
#tabela-exemplar td {
    padding: 8px 10px;
    border: 1px solid #E0E0E0;
    font-size: 0.9em;
}

/* Estilo para Linhas Ímpares (Fundo Zebrado) */
#tabela-exemplar tbody tr:nth-child(odd) {
    background-color: var(--pastel-brown); 
}

/* Estilo para Linhas Pares (Fundo Cinza/Branco) */
#tabela-exemplar tbody tr:nth-child(even) {
    background-color: #FFFFFF;
}

/* Rodapé da Tabela */
#tabela-exemplar tfoot td {
    background-color: var(--pastel-grey);
    color: var(--dark-text);
    text-align: center;
    font-size: 0.8em;
    padding: 8px;
}
</style>
<body>
    <header>
        <h1> I Love so Pet 🐶❤️🐱</h1>
    </header>
    
    <section class="manager">
        <form action="https://docs.google.com/forms/d/e/1FAIpQLSd8XtgSddbb-XldIOfUYHFJrCwMsIZ2Nz5-_T-VvC6ce6HvDg/formResponse" name="formulario_cadastro" onsubmit="return validateForm()" method="post" target="_blank">
            <legend>Preencha as lacunas para encontrar seu novo amigo e dê um lar para ele.🏡</legend>
            <label for="nome">Nome:</label>
            <input type="text" name="fname" placeholder="Seu nome completo" required>
            <label for="email">E-mail:</label>
            <input type="email" name="femail" placeholder="seu.email@exemplo.com" required>
            <label for="Ncelular">Celular:</label>
            <input type="tel" name="fnumber" placeholder="(XX) XXXXX-XXXX" required>
            <input type="submit" value="Enviar Cadastro e Continuar">
        </form>
    </section>
    
    <div class="flex-container">
        <h2>Precisa de Ajuda? Clique e Selecione:</h2>
        
        <option class="toggle-btn" data-target="adocao-collapse">Casas de Adoção 🏡</option>
        <div id="adocao-collapse" class="collapse-content">
            <p>Encontre ONGs próximas a você.</p>
            <button class="sub-btn">Encontrar ONGs</button>
            <button class="sub-btn">Quero ser voluntário</button>
        </div>

        <option class="toggle-btn" data-target="petshop-collapse">Petshop 🛁</option>
        <div id="petshop-collapse" class="collapse-content">
            <p>Agendamento de banho e tosa.</p>
            <button class="sub-btn">Agendar Serviço</button>
            <button class="sub-btn">Ver Catálogo</button>
        </div>

        <form action="https://www.webdenuncia.sp.gov.br/depa" target="_blank">
        <option class="toggle-btn" data-target="denuncia-collapse">Denúncias 🚨</option>
        <div id="denuncia-collapse" class="collapse-content">
            <p>Ajude a combater maus-tratos.</p>
            <button class="sub-btn den-btn" >Fazer Denúncia</button>
        </div>
        </form>
        
        <p>Queremos pedir seu apoio para darmos continuidade e amplificação de nossa causa de adoção. Cada ajuda importa! 💖</p>
    </div>

    <script>
        // Função de Validação do Formulário
        function validateForm(){
            let x = document.forms["formulario_cadastro"]["fname"].value;
            let y = document.forms["formulario_cadastro"]["femail"].value;
            let z = document.forms["formulario_cadastro"]["fnumber"].value;

            if (x == "" || y == "" || z == ""){
                alert("Por favor, preencha completamente todas as lacunas do formulário de cadastro.");
                return false;
            }
            // Se tudo estiver preenchido, retorna true para prosseguir com o submit (redirecionamento)
            return true;
        }

        // Script para a funcionalidade de Colapso (Accordion)
        document.addEventListener('DOMContentLoaded', function() {
            const toggleoptions = document.querySelectorAll('.toggle-btn');

            toggleoptions.forEach(button => {
                button.addEventListener('click', function() {
                    const targetId = this.getAttribute('data-target');
                    const targetElement = document.getElementById(targetId);

                    // Colapsa todos os outros painéis primeiro
                    document.querySelectorAll('.collapse-content').forEach(content => {
                        if (content.id !== targetId) {
                            content.classList.remove('active');
                        }
                    });

                    // Alterna a classe 'active' no painel clicado
                    targetElement.classList.toggle('active');
                });
            });
        });
    </script>
</body>
</html>
