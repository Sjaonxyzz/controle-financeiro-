# Livro-Caixa

Site estático de controle financeiro pessoal — entradas, saídas, categorias e histórico de lançamentos. Um único arquivo (`index.html`), sem backend, sem build, pronto para o GitHub Pages.

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex.: `livro-caixa`).
2. Suba o arquivo `index.html` para a raiz do repositório (pode arrastar e soltar pela interface web do GitHub, em **Add file → Upload files**).
3. Vá em **Settings → Pages**.
4. Em **Source**, selecione a branch `main` e a pasta `/ (root)`. Salve.
5. Em alguns minutos o site estará no ar em `https://SEU-USUARIO.github.io/livro-caixa/`.

Não há nenhuma etapa de build — é HTML/CSS/JS puro em um único arquivo.

## Como funciona

- **Categorias**: existem categorias padrão para entradas e saídas; você pode adicionar novas categorias direto no formulário, escolhendo "+ Nova categoria…".
- **Entradas e saídas**: cada lançamento tem tipo, descrição, categoria, valor e data. Clique em um lançamento na tabela para editá-lo ou excluí-lo.
- **Preenchimento autônomo**:
  - A data já vem preenchida com o dia atual.
  - Ao digitar uma descrição já usada antes (ex.: "mercado"), o formulário sugere automaticamente a mesma categoria e o último valor.
  - As opções de categoria mudam sozinhas conforme você alterna entre Entrada e Saída.
- **Saldo e resumo**: o painel lateral mostra o saldo atual, total de entradas/saídas e um gráfico de barras simples com as saídas por categoria.
- **Dados salvos no navegador**: tudo fica em `localStorage`, ou seja, é local a cada navegador/computador — nada é enviado para nenhum servidor.
- **Backup**: use "Exportar backup (.json)" para salvar seus dados e "Importar backup (.json)" para restaurá-los em outro navegador ou dispositivo. Há também exportação em CSV para abrir em planilhas.

## Limitações

Por ser um site 100% estático, os dados não sincronizam automaticamente entre dispositivos — é preciso exportar e importar o backup manualmente. Se no futuro você quiser sincronização entre aparelhos, seria necessário adicionar um backend ou um serviço como Firebase/Supabase.
