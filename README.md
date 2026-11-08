# WV Orçamentos

Demonstração de portfólio da WV.LAB, desenvolvida por Wandley Vitor com assistência de IA. Organiza pedidos, propostas e próximos retornos de prestadores de serviços.

## Experimente online

**[Abrir WV Orçamentos](https://wv-orcamentos.pages.dev/)**

A demonstração é pública e começa com seis exemplos fictícios. Cada visitante mantém seus próprios registros no navegador; os dados não são compartilhados entre visitantes.

## Funcionalidades

- Cadastro e edição de atendimentos com cliente, serviço, itens e condições.
- Etapas Novo, Orçado, Aprovado, Em execução, Concluído e Perdido.
- Quantidades inteiras e valores monetários calculados em centavos.
- Próximos retornos, busca e filtro por etapa.
- Prévia de proposta com impressão ou salvamento como PDF pelo navegador.
- Persistência no localStorage e backup JSON com validação de importação.
- Seis atendimentos fictícios para explorar e restauração com confirmação.

## Executar

Requer Python 3 para um servidor estático ou outro servidor HTTP local. Na raiz: `python -m http.server 8765 --bind 127.0.0.1 --directory dist`. Abra http://127.0.0.1:8765. Não há dependências de build. Fontes externas são opcionais; há fontes de sistema como alternativa.

## Validação realizada

Em 8 de novembro de 2026, as verificações de sintaxe JavaScript passaram. Foram conferidos conversão de centavos, soma com quantidades, rejeição de valores negativos e casas decimais excessivas, data impossível, quantidade fracionária e identificadores duplicados no backup, além de ida e volta de backup no modelo. No navegador, um atendimento de teste com 3 × R$ 89,90 mostrou R$ 269,70 e permaneceu após recarregar.

Não houve teste completo de todas as combinações de navegador, importação pela interface ou diálogo de impressão do sistema. Esta versão não é uma implantação para dados de clientes.

## Limites

Os dados ficam apenas no navegador e podem ser perdidos ao limpar seu armazenamento. Não há login, controle de acesso por usuário, servidor de dados, sincronização, mensagens automáticas, pagamentos ou aceite eletrônico. Exportação não faz backup automático. Importação combina identificadores e substitui correspondências após confirmação. Use dados fictícios na demonstração.

Esta é uma ferramenta de acompanhamento manual. Uma proposta aprovada no painel não equivale a aceite jurídico ou recebimento. A maturidade comercial depende de validação com usuários e de arquitetura, segurança e suporte adequados ao uso contratado.

## Estrutura

- dist/index.html: estrutura e formulários.
- dist/style.css: interface adaptável.
- dist/model.js: regras de valores, datas e backup.
- dist/app.js: fluxo da interface, persistência e impressão.
