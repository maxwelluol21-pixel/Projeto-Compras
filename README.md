# Base de procurement

A fonte oficial do portal é a planilha pública do Google Sheets configurada em `index.html`, aba `BASE_DASHBOARD`.

Requisitos:
- a aba deve permanecer pública;
- a URL deve apontar para a planilha correta;
- o portal carrega a base automaticamente ao abrir e a cada 1 minutos;
- em produção, o fallback local fica desativado por padrão para evitar dados fictícios silenciosos.

A planilha aceita colunas como fornecedor, categoria, tipo, descrição, proposta inicial, percentual negociado, proposta final e saving/cost avoid. O portal normaliza o cabeçalho, transforma as linhas em registros e recalcula indicadores, gráficos e tabelas em tempo real.

Se a planilha não estiver acessível, o portal exibe uma mensagem profissional e não inventa dados. Para testes locais controlados, basta ativar `allowLocalFallback` na configuração do `DATA_SOURCE_CONFIG` no `index.html` e fornecer um arquivo real exportado da planilha.
