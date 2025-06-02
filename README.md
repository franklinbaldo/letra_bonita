# Letra Bonita - Gerador de Folhas de Caligrafia



**Demo ao Vivo:** [Acesse o Letra Bonita aqui!](https://franklinbaldo.github.io/letra_bonita/)

## Descrição do Projeto

O "Letra Bonita" é um aplicativo web interativo, moderno e intuitivo, desenvolvido para auxiliar na prática da caligrafia. Ele permite que usuários de todos os níveis criem e imprimam folhas de caligrafia personalizadas, com controle total sobre cada aspecto da sua sessão de prática. Seja para aprimorar a letra, experimentar novos estilos ou simplesmente relaxar, o Letra Bonita oferece as ferramentas necessárias.

## Recursos Principais

* **Texto de Prática Totalmente Personalizável:** Insira qualquer conteúdo textual que desejar para suas sessões de prática.
* **Geração de Citações com IA (Gemini API):**
    * Preencha suas folhas instantaneamente com citações famosas geradas por Inteligência Artificial.
    * Especifique um tema (ex: "amor", "sucesso", "natureza") ou utilize a opção padrão para citações filosóficas.
    * A API Key é gerenciável localmente no navegador, garantindo conveniência e privacidade.
* **Controle Detalhado da Fonte:**
    * Vasta seleção de fontes de caligrafia e script do Google Fonts (Dancing Script, Great Vibes, Allura, Pacifico, Caveat, Indie Flower, Shadows Into Light, Permanent Marker, Roboto).
    * Ajuste preciso do tamanho da fonte em tempo real.
    * Opção de **Texto Tracejado** (ativado por padrão) para facilitar o aprendizado e o traçado.
* **Linhas-Guia Avançadas para Orientação Perfeita:**
    * Defina o estilo da linha de base (principal): sólida, tracejada ou pontilhada.
    * Linhas intermediárias (altura-x, ascendente e descendente) são sempre **pontilhadas**, fornecendo um guia visual claro sem sobrecarregar.
    * Ajuste o ângulo de inclinação das linhas-guia para praticar diferentes estilos caligráficos.
    * Controle milimétrico da altura-X (altura das letras minúsculas).
    * Personalize a cor de todas as linhas.
* **Layout de Página Flexível e Preciso:**
    * Escolha entre tamanhos de página padrão: A4 (210 x 297 mm) e Carta (215.9 x 279.4 mm).
    * Defina a orientação da página: Retrato ou Paisagem, com adaptação automática e precisa de todas as pautas.
* **Impressão Otimizada e Multipágina:**
    * Pré-visualização em tempo real que se ajusta perfeitamente.
    * Suporte automático a **múltiplas páginas** para textos longos, garantindo que todo o conteúdo seja impresso.
    * Opção "Abrir SVG para Imprimir" que abre uma nova janela/aba com a folha de caligrafia em SVG otimizado para impressão (garantindo nitidez e proporções corretas).
* **Totalmente Front-end:** Desenvolvido apenas com HTML, CSS e JavaScript, tornando-o leve e fácil de hospedar.

## Como Usar

1.  **Acesse o Aplicativo:** Abra o arquivo `index.html` em seu navegador ou visite o projeto em seu GitHub Pages.
2.  **Texto de Prática:** Digite ou cole o texto que deseja praticar na área designada.
3.  **Configurar Chave de API (Para Citações):**
    * Se você deseja usar o gerador de citações por IA, vá até o painel "Configurações da API Gemini".
    * Insira sua chave de API Gemini (gratuita, pode ser obtida em [aistudio.google.com/apikey](https://aistudio.google.com/apikey)).
    * Clique em "Salvar". Sua chave será guardada localmente para futuras visitas.
4.  **Gerar Citações (Opcional):**
    * No painel "Gerador de Citações (IA)", você pode digitar um tema (ex: "amor", "sucesso") ou deixar o campo em branco para obter citações filosóficas padrão.
    * Clique em "Gerar Citações" para preencher o campo de texto de prática.
5.  **Ajuste o Design:**
    * Utilize os painéis "Definições de Fonte", "Linhas-Guia" e "Layout de Página" para personalizar completamente sua folha de caligrafia. A pré-visualização à direita será atualizada em tempo real.
6.  **Imprimir:**
    * Clique em **"Imprimir Folha"** para imprimir a página atual do aplicativo (que inclui a pré-visualização).
    * **Recomendado para melhor qualidade de impressão:** Clique em **"Abrir SVG para Imprimir"**. Isso abrirá uma nova aba/janela com a folha de caligrafia pura, otimizada para impressão. O diálogo de impressão do navegador será acionado automaticamente.

## Como Rodar Localmente

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/franklinbaldo/letra_bonita.git](https://github.com/franklinbaldo/letra_bonita.git)
    ```
2.  **Navegue até a Pasta do Projeto:**
    ```bash
    cd letra_bonita
    ```
3.  **Abra no Navegador:**
    * Simplesmente abra o arquivo `index.html` em seu navegador web (ex: `file:///caminho/para/letra_bonita/index.html`).
    * Para garantir que as funcionalidades que dependem de APIs e `localStorage` funcionem sem restrições de CORS (Cross-Origin Resource Sharing) em alguns navegadores, é recomendado rodar um servidor web local simples (ex: usando a extensão "Live Server" no VS Code, ou comandos como `npx live-server` ou `python -m http.server`).

## Como Publicar no GitHub Pages

1.  **Crie seu Repositório:** Se você ainda não o fez, crie um novo repositório público no GitHub.
2.  **Faça o Upload:** Envie o arquivo `index.html` (que contém todo o HTML, CSS e JavaScript) para a branch `main` (ou `master`) do seu repositório.
3.  **Ative o GitHub Pages:**
    * No seu repositório GitHub, vá para `Settings` (Configurações).
    * No menu lateral, clique em `Pages`.
    * Em "Build and deployment", selecione `Deploy from a branch` (Implantar a partir de um branch).
    * Escolha a branch `main` (ou `master`) e a pasta `/(root)` (raiz).
    * Clique em `Save` (Salvar).
4.  Seu site estará disponível publicamente em `https://<seu-usuario>.github.io/<nome-do-repositorio>/` (substitua `<seu-usuario>` pelo seu nome de usuário GitHub e `<nome-do-repositorio>` pelo nome do seu repositório, que no seu caso é `letra_bonita`).

## Tecnologias Utilizadas

* **HTML5:** Estrutura semântica do aplicativo.
* **CSS3:** Estilização geral e regras de impressão.
* **Tailwind CSS:** Framework CSS para design responsivo e eficiente.
* **JavaScript (ES6+):** Lógica interativa, manipulação do DOM, geração dinâmica de SVG, gerenciamento de estado e chamadas de API.
* **SVG (Scalable Vector Graphics):** Para renderização de alta precisão das linhas-guia e texto, garantindo qualidade de impressão.
* **Google Fonts:** Para a vasta seleção de fontes de caligrafia.
* **Gemini API (Google AI Studio):** Para a funcionalidade de geração de citações inteligentes.
* **localStorage:** Para persistência local da chave de API do usuário.

## Contribuição

Contribuições são **muito bem-vindas**! Se você tiver ideias para novas funcionalidades, melhorias no código, otimizações ou correções de bugs, por favor:

1.  Abra uma *issue* para discutir sua sugestão.
2.  Faça um *fork* do repositório.
3.  Crie uma nova *branch* para sua feature (`git checkout -b feature/sua-feature`).
4.  Faça suas alterações e commite-as (`git commit -m 'feat: Adiciona nova funcionalidade X'`).
5.  Envie suas alterações para o *fork* (`git push origin feature/sua-feature`).
6.  Abra um *Pull Request* descrevendo suas mudanças.

## Licença

Este projeto está licenciado sob a Licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
