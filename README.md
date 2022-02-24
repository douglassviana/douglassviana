<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulário</title>
</head>
<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');

    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Poppins', sans-serif;
        font-size: 100%;
        color: #202020;
        line-height: 1.5;
    }
    
    body {
        background: #333333;
    }

    .content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50% , -50%);
        background-color: #FFF;
        width: 720px;
        padding: 30px;
        box-shadow: 0px 10px 20px;
        border-radius: 10px;
    }

    .row {
        padding: 5px;
    }

    .buttons {
        text-align: center;
    }

    fieldset {
        border-radius: 10px;
        padding: 30px;
        margin-bottom: 20px;
        border-color: #1e9aff
    }

    legend {
        font-size: 2rem;
        padding-left: 10px;
        padding-right: 10px;
        border-radius: 10px;
        color: #FFF;
        background: #1e9aff;
        background: linear-gradient(80deg, rgba(30,154,255,1) 0%, rgb(46, 196, 255) 100%);
        font-weight: bold;
        font-family: 'Poppins', sans-serif;
    }

    label:not([for="casado"], [for="solteiro"], [for="java"], [for="php"], [for="csharp"]) {
        display: inline-block;
        width: 120px;
    }

    input {
        padding: 2px;
        outline: none;
    }

    input[id="nome"],
    input[id="sobrenome"],
    input[id="email"] {
        width: 480px;
    }

    input[id="dtnasc"] {
        width: 180px;
    }

    input[type="text"],
    input[type="date"],
    input[type="number"],
    input[type="email"] {
        border: none;
        border-bottom: 2px solid #c2cbce;
        transition: 500ms all;
    }

    input[type="text"]:focus,
    input[type="date"]:focus,
    input[type="number"]:focus,
    input[type="email"]:focus {
        color: #1e9aff;
        font-weight: 600;
        letter-spacing: 1px;
        border-color: #1e9aff;
    }

    textarea {
        padding: 10px;
        resize: none;
        outline: none;
        width: 100%;
    }

    input[type="radio"],
    input[type="checkbox"] {
        margin-top: 10px;
        margin-bottom: 10px;
    }

    input::-webkit-outer-spin-button,
    input::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }

    input[type="submit"],
    input[type="reset"] {
        margin-inline: 15px;
        padding: 5px 10px;
        background-color: #1e9aff;
        border: none;
        border-radius: 5px;
        color: #fff;
        transition: 0.3s all ease-in-out;
    }

    input[type="submit"]:hover,
    input[type="reset"]:hover {
        transform: scale(1.1);
        cursor: pointer;
    }

</style>

<body>
    <div class="content">
        <form action="">
            <fieldset>
                <legend>Dados Pessoais</legend>
                <div class="row">
                    <label for="nome">Nome:</label>
                    <input type="text" id="nome" name="nome" placeholder="Digite seu nome" autocomplete="off" required>
                </div>
                <div class="row">
                    <label for="sobrenome">Sobrenome:</label>
                    <input type="text" id="sobrenome" name="sobrenome" placeholder="Digite seu sobrenome" autocomplete="off"
                        required>
                </div>
                <div class="row">
                    <label for="email">E-mail:</label>
                    <input type="email" id="email" name="email" placeholder="Digite seu e-mail" autocomplete="off" required>
                </div>
                <div class="row">
                    <label for="dtnasc">Data de Nascimento:</label>
                    <input type="date" id="dtnasc" name="dtnasc">
                </div>
                <div class="row">
                    <label for="">Estado Civil:</label>
                    <input type="radio" value="Casado" id="casado" name="estadocivil">
                    <label for="casado">Casado</label>
                    <input type="radio" value="Solteiro" id="solteiro" name="estadocivil">
                    <label for="solteiro">Solteiro</label>
                </div>
                <div class="row"></div>
            </fieldset>
            <div class="buttons">
                <input type="submit">
                <input type="reset" value="Limpar">
            </div>
        </form>
    </div>
</body>

</html>
