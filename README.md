# Letra Bonita - Gerador de Folhas de Caligrafia

![Captura de Tela do Projeto](https://via.placeholder.com/800x450?text=Captura+de+Tela+do+Projeto)
*(Substitua esta imagem por uma captura de tela real do seu projeto em funcionamento)*

## Descrição do Projeto

O "Letra Bonita" é um aplicativo web interativo que permite aos usuários gerar e imprimir folhas de caligrafia personalizadas. Ideal para estudantes, entusiastas da caligrafia ou qualquer pessoa que queira praticar sua escrita de forma organizada.

Com este gerador, você tem controle total sobre o texto de prática, o estilo das linhas-guia e as fontes. Uma funcionalidade integrada de Inteligência Artificial permite gerar citações famosas baseadas em temas específicos para preencher suas folhas, tornando a prática mais interessante e variada. As folhas podem ser impressas diretamente do navegador, suportando múltiplas páginas automaticamente.

## Recursos

* **Texto de Prática Personalizável:** Insira qualquer texto que desejar para praticar.
* **Geração de Citações por IA:**
    * Preencha suas folhas com citações famosas geradas por Inteligência Artificial (via Gemini API).
    * Escolha um tema para as citações (ex: "amor", "sucesso", "filosofia").
    * Citações filosóficas padrão são fornecidas por padrão.
* **Configurações de Fonte Flexíveis:**
    * Escolha entre uma variedade de fontes de caligrafia (Dancing Script, Great Vibes, Allura, Pacifico, Caveat, Indie Flower, Shadows Into Light, Permanent Marker, Roboto).
    * Ajuste o tamanho da fonte em tempo real.
    * Opção de **Texto Tracejado** (padrão ativado) para facilitar a prática de traçado.
* **Linhas-Guia Avançadas:**
    * Defina o tipo de linha principal (sólida, tracejada, pontilhada).
    * Linhas intermediárias (altura-x, ascendente, descendente) sempre pontilhadas para melhor orientação.
    * Ajuste o ângulo de inclinação das linhas-guia.
    * Controle a altura-X (altura das letras minúsculas sem ascendentes/descendentes).
    * Personalize a cor das linhas.
* **Layout de Página Adaptável:**
    * Escolha entre tamanhos de página A4 e Carta.
    * Defina a orientação da página (retrato ou paisagem), com adaptação automática das pautas.
* **Impressão Otimizada:**
    * Pré-visualização em tempo real do seu design.
    * Impressão direta do navegador.
    * Suporte automático a **múltiplas páginas** para textos longos.
    * Opção para "Abrir SVG para Imprimir" em uma nova janela para uma experiência de impressão mais limpa e controlada.
* **Gerenciamento de API Key:**
    * Insira e salve sua própria chave de API Gemini localmente no navegador (`localStorage`) para reutilização.
    * Limpeza fácil da chave salva.

## Como Usar

1.  **Acesse o Aplicativo:** Abra o `index.html` em seu navegador ou acesse a página do projeto no GitHub Pages.
2.  **Texto de Prática:** Digite ou cole o texto que deseja praticar na área "Texto de Prática".
3.  **Gerar Citações (Opcional):**
    * Se você quiser que a IA preencha o texto, vá em "Configurações da API Gemini" e insira sua chave de API (veja a seção abaixo).
    * Em "Gerador de Citações (IA)", digite um tema ou deixe em branco para citações filosóficas.
    * Clique em "Gerar Citações".
4.  **Ajuste de Fonte:** Selecione a "Família da Fonte", "Tamanho da Fonte" e marque/desmarque "Texto Tracejado".
5.  **Ajuste das Linhas-Guia:** Configure o "Tipo de Linha Principal", "Ângulo de Inclinação", "Altura-X" e "Cor da Linha".
6.  **Layout de Página:** Escolha o "Tamanho da Página" e a "Orientação".
7.  **Imprimir:**
    * Clique em "Imprimir Folha" para imprimir diretamente a pré-visualização atual do aplicativo.
    * **Recomendado:** Clique em "Abrir SVG para Imprimir" para abrir uma nova janela/aba com apenas a folha de caligrafia, otimizada para impressão. O diálogo de impressão do navegador será aberto automaticamente.

## Configuração da API Key Gemini (Importante!)

Para utilizar a funcionalidade de geração de citações por IA, você precisará de uma chave de API do Google Gemini.

1.  **Obtenha sua Chave de API:**
    * Visite [Google AI Studio - Obter chave de API](https://aistudio.google.com/apikey).
    * Siga as instruções para criar e copiar sua chave.
2.  **Insira e Salve no Aplicativo:**
    * No painel "Configurações da API Gemini" do aplicativo, cole sua chave no campo "Sua Chave de API Gemini".
    * Clique no botão "Salvar".
    * Sua chave será armazenada no `localStorage` do seu navegador e será carregada automaticamente em futuras visitas.
    * **(Atenção):** Armazenar chaves de API diretamente no frontend não é totalmente seguro para aplicações de produção. Para este projeto pessoal/demonstração, é aceitável, mas esteja ciente dos riscos.

## Como Rodar Localmente

1.  **Clone o Repositório:**
    ```bash
    git clone [https://github.com/](https://github.com/)<seu-usuario>/Letra-Bonita.git
    ```
2.  **Navegue até a Pasta:**
    ```bash
    cd Letra-Bonita
    ```
3.  **Abra no Navegador:**
    * Simplesmente abra o arquivo `index.html` em seu navegador preferido (ex: `file:///caminho/para/Letra-Bonita/index.html`).
    * Para garantir que o `localStorage` funcione corretamente em alguns navegadores (como o Chrome), pode ser necessário rodar um servidor local simples (ex: `npx live-server` ou `python -m http.server`).

## Como Publicar no GitHub Pages

1.  **Crie um Repositório:** Siga os passos de criação de repositório no GitHub.
2.  **Faça o Upload:** Envie o arquivo `index.html` (e quaisquer outros arquivos se você os tiver separado) para a branch `main` (ou `master`) do seu repositório.
3.  **Ative o GitHub Pages:** Vá para "Settings" (Configurações) do seu repositório > "Pages" > selecione a branch `main` (ou `master`) e a pasta `/(root)` como origem. Salve.
4.  Seu site estará disponível em `https://<seu-usuario>.github.io/Letra-Bonita/` (substitua `<seu-usuario>` pelo seu nome de usuário GitHub).

## Tecnologias Utilizadas

* **HTML5:** Estrutura da página.
* **CSS3 (com Tailwind CSS):** Estilização e responsividade.
* **JavaScript (ES6+):** Lógica interativa, geração de SVG, integração com API.
* **SVG:** Para renderização precisa das folhas de caligrafia.
* **Google Fonts:** Para as opções de fontes de caligrafia.
* **Gemini API (Google AI Studio):** Para geração de citações.
* **localStorage:** Para armazenamento local da API Key.

## Contribuição

Contribuições são bem-vindas! Se você tiver ideias para melhorias, novas funcionalidades ou correções de bugs, sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

## Licença

Este projeto está licenciado sob a Licença MIT.

---

Espero que esta descrição e `README.md` sejam úteis para o seu projeto!
