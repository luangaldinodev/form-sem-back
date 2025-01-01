# Documentação do Projeto de Formulário Sem Back-End com FormSubmit

## Introdução


Este projeto consiste em um formulário de contato simples implementado em HTML e CSS, utilizando o serviço FormSubmit para envio de dados diretamente para um e-mail específico, sem a necessidade de configurar um back-end.

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos principais:

- **index.html:** Arquivo principal que define o formulário de contato.

- **obrigado.html:** Página de confirmação exibida após o envio do formulário.

- **style.css:** Estilos principais aplicados ao formulário e à página de confirmação.

- **responsivo.css:** Arquivo para ajustes responsivos.

## Detalhes de Implementação

### index.html

Este é o arquivo principal onde o formulário é definido. O FormSubmit é configurado como o destino do formulário por meio do atributo action.

**Destaques do código:**

```

<form action="https://formsubmit.co/seuemail@dominio.com" method="post">
    <label for="nome">Seu nome:</label>
    <input required type="text" name="nome" id="nome">

    <label for="email">Seu E-mail:</label>
    <input required type="email" name="email" id="email">

    <label for="assunto">Assunto:</label>
    <input type="text" name="assunto" id="assunto">

    <label for="mensagem">Mensagem:</label>
    <textarea required minlength="20" name="mensagem" id="mensagem"></textarea>

    <input type="submit" value="Enviar">
    <input type="hidden" name="_next" value="http://127.0.0.1:5500/obrigado.html">
</form>

```

- O atributo action envia os dados para o FormSubmit.

- Campos obrigatórios (nome, e-mail e mensagem) foram configurados com o atributo required.

- O campo _next especifica a URL para redirecionamento após o envio bem-sucedido.

### obrigado.html

Página simples para confirmar que o envio do formulário foi bem-sucedido.

**Destaques do código:**

```
<section class="obrigado">
    <form class="form">
        <h2 class="obrigado-title">Formulário enviado com sucesso!</h2>
        <a class="obrigado-btn" href="index.html">Voltar</a>
    </form>
</section>
```

- Um botão leva o usuário de volta à página inicial.

### style.css

Define os estilos para a interface do usuário.

**Destaques do estilo:**

- Uso de variáveis CSS para cores:

```
:root {
    --cor-1: #191414;
    --cor-2: #ffffff;
    --cor-3: #cccccc;
    --cor-4: #999999;
    --cor-5: #1ED760;
    --cor-6: #db2525;
}
```

**Estilização do formulário:**

```
.form {
    display: flex;
    flex-direction: column;
    background-color: var(--cor-1);
    padding: 2rem;
    border-radius: 1rem;
    box-shadow: 0 0 1rem rgba(0, 0, 0, 0.6);
}

.formulario-enviar {
    background-color: var(--cor-5);
    color: var(--cor-2);
    border: none;
    border-radius: 0.5rem;
    padding: 0.8rem;
    font-weight: 600;
}
```

## Como Utilizar

1. Substitua seuemail@dominio.com pelo endereço de e-mail que deverá receber as mensagens.

2. Ajuste o valor do campo _next para o URL onde a página "https://seudominio/obrigado.html" estará hospedada.

3. Abra o arquivo index.html em um navegador para acessar o formulário.

4. Envie a primeira requisição para a ativação do formulário.

## Como Modificar

1. Acesse o site "https://formsubmit.co/".

2. Leia a documentação na seção "Advanced Features" e siga os passos descritos.



## Considerações Finais

Este projeto é uma solução simples e eficiente para formulários sem back-end. Ideal para pequenos sites ou landing pages. Lembre-se de verificar a política de uso do FormSubmit para garantir conformidade com suas regras de envio.
