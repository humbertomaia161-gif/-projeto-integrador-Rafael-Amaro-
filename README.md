# Catálogo de Celulares Custo-Benefício 2026

Site com celulares de bom custo-benefício em 2026, organizados por faixa de preço (até R$ 7.000). Dá para buscar, filtrar, ordenar, favoritar, comparar até 3 modelos, ver detalhes, assistir a um vídeo de apresentação e sugerir um celular.

Projeto da disciplina **Desenvolvimento Front-End para Web**, construído aula a aula.

**Site publicado:** https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/ (troque pelo link real após o deploy)

## Faixas de preço

| Faixa | Preço | Situação |
|---|---|---|
| Entrada | até R$ 1.500 | 3 modelos |
| Intermediário | R$ 1.500 a R$ 3.000 | 7 modelos |
| Intermediário superior | R$ 3.000 a R$ 5.000 | em pesquisa |
| Premium acessível | R$ 5.000 a R$ 7.000 | em pesquisa |

## Funcionalidades

- Filtro por faixa (botões e menu), busca por nome e ordenação por nota ou preço
- Favoritos salvos no `localStorage` (continuam após recarregar a página)
- Comparador de até 3 celulares, com tabela acessível
- Modal de detalhes (Bootstrap)
- Gráfico de notas em Canvas e selo em SVG
- Vídeo com MP4 e WebM, poster e legendas em português
- Formulário de sugestões com validação nativa e lista salva no navegador

## Tecnologias

HTML5 semântico, CSS3, JavaScript puro e Bootstrap 5.3.3 (via CDN, precisa de internet).

## Como rodar

Abra o `index.html` no navegador (ou use a extensão Live Server no VS Code).

## Estrutura

```
├── index.html
├── css/style.css
├── js/dados.js        (fichas dos celulares)
├── js/main.js         (lógica e interatividade)
├── assets/images/logo.svg
├── assets/media/      (vídeo, poster e legendas)
├── docs/entregas-por-aula.md
├── .gitignore
└── README.md
```

## Sobre os dados

Preços e fichas vêm de testes e listas publicados pelo Oficina da Net em jul/2026 e out/2026. Os preços mudam com frequência, então confira nas lojas. A nota é uma avaliação própria do catálogo (0 a 10), baseada em preço, tela, bateria, desempenho e atualizações.

Fontes:
- https://www.oficinadanet.com.br/topsmartphones/64420-top-10-celulares-ate-1500
- https://www.oficinadanet.com.br/topsmartphones/73012-melhores-celulares-custo-beneficio-outubro

## Autor

[Seu nome aqui]

Avaliação do Projeto Integrador: Catálogo de Celulares
Visão geral

O projeto apresenta boa qualidade técnica e organização acima do esperado para a atividade. O código é limpo, seguro e bem estruturado, com interatividade completa e atenção à acessibilidade. Alguns itens específicos do checklist da Aula 11 ainda podem ser complementados.

Nota estimada: 8,0 de 10 para o checklist da atividade, e cerca de 9,0 considerando o projeto como um todo.

Pontos fortes
Manipulação segura do DOM: os elementos são criados com createElement, textContent e append, por meio de uma função auxiliar reutilizável. Não há uso de innerHTML.
Boas práticas de JavaScript: uso de const e let (sem var), código dentro de DOMContentLoaded, um único ouvinte de eventos na lista (event delegation) e localStorage protegido com try/catch.
Cuidado com os dados: o sort é aplicado sempre em cópias do array, o que evita o Erro 4.
Dados coerentes: o array tem 10 celulares com várias propriedades, e a contagem por faixa no README confere com os dados.
Acessibilidade e semântica: labels, regiões aria-live, link de salto, foco visível e respeito a prefers-reduced-motion.
Estrutura do repositório: README organizado, .gitignore adequado, vídeo com dois formatos, poster e legendas.
Pontos a complementar

Estes itens fazem parte do checklist da atividade e não foram encontrados nos arquivos:

Resumo com reduce: o código usa map e filter, mas não há reduce. A atividade pede uma linha de resumo na página (total, média ou contagem), por exemplo “Preço médio da lista exibida”.
Parâmetro com valor padrão: nenhuma função possui esse recurso. Um exemplo simples seria formatarNota(nota, casas = 1).
Função de processamento: hoje existem funções que classificam e formatam, mas nenhuma que calcule algo. Uma função como calcularCustoBeneficio(nota, preco) completaria o padrão processar → classificar → mostrar.
Dados originais preservados: a linha que acrescenta faixa aos objetos de CELULARES altera o array de origem. O recomendado é gerar novos objetos com map: { ...celular, faixa: classificarFaixa(celular.preco) }.
Verificação de elementos nulos: falta confirmar que a área de resultado foi encontrada antes de usá-la, por exemplo if (!lista) return;.
Uso de classList: a classe da faixa é aplicada por className. Trocar por classList.add atende ao checklist sem alterar o resultado visual.
Testes no Console: como as funções estão dentro do DOMContentLoaded, não podem ser chamadas pelo Console. Mover as funções de cálculo para fora desse bloco facilita o teste e a separação entre cálculo e página.

