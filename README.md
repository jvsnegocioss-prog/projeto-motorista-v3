# Projeto Motorista — protótipo PWA

Protótipo v2 para controle de ganhos, despesas, metas, cadastro de múltiplos veículos e análise manual de ofertas para Uber, 99 e inDrive.

## Arquivos
- `index.html`: aplicativo
- `manifest.webmanifest`: configuração instalável
- `sw.js`: cache básico para uso offline
- `icon-192.png` e `icon-512.png`: ícones

## Publicar para teste no GitHub Pages
1. Crie um repositório NOVO para este projeto, separado dos seus outros aplicativos.
2. Envie os arquivos extraídos diretamente para a raiz do repositório (não deixe o `index.html` dentro de uma subpasta).
3. Em Settings → Pages, selecione Deploy from a branch, branch `main`, pasta `/(root)`.
4. Abra o endereço HTTPS gerado no Safari do iPhone.
5. No Safari, toque em Compartilhar → Adicionar à Tela de Início.

## Limitações desta versão
- O nome é provisório; não é o nome comercial final.
- A imagem da oferta pode ser selecionada, mas o OCR automático ainda não foi implementado.
- É possível cadastrar vários veículos e selecionar qual está em uso; a análise utiliza consumo, combustível e manutenção do veículo selecionado.
- A análise é baseada nos campos digitados e nos custos configurados.
- Os dados ficam no armazenamento local do navegador/aparelho. Exportar backup regularmente; não há sincronização em nuvem nesta versão.
- A estimativa não inclui automaticamente todos os custos fixos, impostos ou períodos sem passageiro.
- Esta versão não se conecta às APIs de Uber, 99 ou inDrive e não aceita/recusa corridas automaticamente.
- Antes de uso comercial, realizar testes, revisão de segurança, acessibilidade e compatibilidade.


## Versão 3 — leitura de capturas
- Permite escolher uma captura de tela da galeria/arquivos e tentar reconhecer texto usando Tesseract.js carregado pela internet.
- Sugere valor, km e minutos quando consegue identificar os padrões; o motorista deve conferir os campos antes de calcular.
- O reconhecimento não aceita nem recusa corridas e pode falhar em capturas de baixa qualidade. O formulário manual continua disponível.
