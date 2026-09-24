# Bikcraft

Site de bicicletas elétricas: home, lista de bicicletas com uma página para cada modelo
(Nimbus, Magic e Nebula), seguros, orçamento, contato e termos de uso. HTML, CSS e JavaScript
puro, sem framework e sem backend.

## Como rodar

Abra o `index.html` no navegador. Sem instalação e sem servidor.

O CSS que a página carrega é o `css/style.min.css`. Os arquivos de cada seção ficam em `css/`,
e o `css/style.css` só os importa na ordem certa — mexer neles não muda nada na tela até o
minificado ser atualizado.

## Decisões

Cores e tipografia ficam em `css/utilidades/` como classes (`cor-5`, `font-1-l`), então cada
página monta o visual combinando classes em vez de escrever CSS novo para cada seção. O menu do
topo vira botões com fundo escuro abaixo de 800px, porque a lista de links ficava apertada no
celular.

As animações de entrada saem do `simple-anime.js` em `js/plugins/`. O resto das interações é
JavaScript escrito na mão, em `js/script.js`: item do menu ativo pela URL, perguntas frequentes
que abrem e fecham, troca da imagem principal na galeria do modelo (só acima de 1000px) e itens
do orçamento pré-marcados pelos parâmetros da URL, como em `orcamento.html?tipo=seguro&produto=prata`.

## O que não tem

O formulário de contato é só front-end: o `js/formluario.js` faz um POST para `enviar.php`,
arquivo que não está no repositório. Rodando a página direto no navegador, o envio falha e
aparece "Erro no envio". Sem servidor com PHP, não tem como mensagem chegar a lugar nenhum.
