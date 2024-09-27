# POC-3-Program-Boys
O que são Media Queries? <br>
As media queries são uma técnica do CSS que permite aplicar estilos diferentes a um documento dependendo de características do dispositivo em que ele está sendo exibido. Elas são fundamentais para o design responsivo, que garante que sua aplicação ou site funcione bem em uma variedade de dispositivos e tamanhos de tela.

Como Funcionam as Media Queries <br>
As media queries utilizam a regra @media para definir condições sob as quais os estilos CSS devem ser aplicados. Essas condições podem se basear em características como a largura da tela, a altura, a orientação e o tipo de mídia (como impressão).

<strong>Sintaxe Básica</strong>

@media (condição) {
    /* Estilos CSS */
}

Regras Comuns de Media Queries

1. Impressão <br>
Para aplicar estilos específicos apenas durante a impressão, você pode usar:

@media print {
    /* Estilos para impressão */
}

Esses estilos podem ocultar elementos desnecessários, alterar fontes ou ajustar a disposição para facilitar a leitura no papel.

2. Larguras de Dispositivos<br>
As media queries podem ser configuradas para diferentes tamanhos de tela. Aqui estão exemplos para smartphones, tablets e desktops:

- Smartphones (até 600px)

@media (max-width: 600px) {
    /* Estilos para smartphones */
}

- Tablets (entre 601px e 1024px)

@media (min-width: 601px) and (max-width: 1024px) {
    /* Estilos para tablets */
}

- Desktops (acima de 1024px)

@media (min-width: 1025px) {
    /* Estilos para desktops */
}

3. Disposição dos Dispositivos<br>
As media queries também permitem que você detecte a orientação do dispositivo, seja em modo retrato (portrait) ou paisagem (landscape).

- Retrato

@media (orientation: portrait) {
    /* Estilos para dispositivos em modo retrato */
}

- Paisagem

@media (orientation: landscape) {
    /* Estilos para dispositivos em modo paisagem */
}

Exemplos Completos <br>
Aqui está um exemplo completo de media queries que abrange impressão, tamanhos de dispositivos e orientações:

/* Estilos gerais */
body {
    font-family: Arial, sans-serif;
}

/* Impressão */
@media print {
    body {
        font-size: 12pt;
    }
    .no-print {
        display: none;
    }
}

/* Smartphones */
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}

/* Tablets */
@media (min-width: 601px) and (max-width: 1024px) {
    body {
        background-color: lightgreen;
    }
}

/* Desktops */
@media (min-width: 1025px) {
    body {
        background-color: lightcoral;
    }
}

/* Modo retrato */
@media (orientation: portrait) {
    .sidebar {
        display: none;
    }
}

/* Modo paisagem */
@media (orientation: landscape) {
    .sidebar {
        display: block;
    }
}

Conclusão

As media queries são uma ferramenta poderosa para criar designs responsivos e acessíveis. Ao utilizar as regras mencionadas, você pode garantir que seu site seja funcional e visualmente atraente em uma ampla gama de dispositivos e condições de uso.
