
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validação de Formulário - Velho Oeste</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <form id="formulario" onsubmit="return validarFormulario(event)">
        <!-- Campo Nome -->
        <h1>Formulário de Cadastro</h1>
        <label for="nome">Nome (somente letras, 3 a 120 caracteres):</label>
        <input type="text" id="nome" name="nome" minlength="3" maxlength="120" pattern="[A-Za-zÀ-ÿ\s]+" required>
        <span class="erro" id="erro-nome"></span>
        <br>

        <!-- Campo Data de Nascimento -->
        <label for="dataNascimento">Data de Nascimento (DD/MM/AAAA):</label>
        <input type="text" id="dataNascimento" name="dataNascimento" placeholder="DD/MM/AAAA" pattern="\d{2}/\d{2}/\d{4}" required>
        <span class="erro" id="erro-dataNascimento"></span>
        <br>

        <!-- Campo Mês -->
        <label for="mes">Mês (deve estar entre 1 e 12):</label>
        <input type="number" id="mes" name="mes" min="1" max="12" required>
        <span class="erro" id="erro-mes"></span>
        <br>

        <!-- Botão de Enviar -->
        <button type="submit">Enviar</button>
    </form>

    <script src="script.js"></script>
</body>
</html>
