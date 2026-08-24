---
name: ui-minimalista
versao: 1.0.0
description: Competência de domínio para interfaces minimalistas leves, legíveis e responsivas, derivada de evidência observável do projeto externo fladmorty1987/ui-minimalista e mantida no fork debianlima/ui-minimalista.
---

# UI Minimalista

## Origem e procedência
- upstream externo: `fladmorty1987/ui-minimalista`;
- commit de origem reconciliado: `811c48df847e29c74a1d11c22cbcfb98211a4c48`;
- fork mantido: `debianlima/ui-minimalista`;
- derivação: competência criada por nós a partir da análise do projeto externo; o upstream não continha `SKILL.md`;
- licença: o README upstream declara MIT; não havia arquivo `LICENSE` no commit reconciliado, portanto essa limitação deve permanecer registrada.

## Problema que resolve
Dar a projetos com telas, formulários, landing pages e componentes uma referência mínima de UI que privilegie simplicidade estrutural, carregamento leve, legibilidade, foco visual e baixo acoplamento a frameworks.

## Decisões observadas no upstream
- estrutura HTML pequena e sem dependências JavaScript obrigatórias;
- layout centralizado por flexbox;
- poucos elementos estruturais (`header`, `main`, `footer`);
- botão com estado `hover`, transição curta e cantos discretos;
- cores de alto contraste para regiões estruturais;
- intenção declarada de componentes leves, flexíveis e personalizáveis.

Esses itens são evidência do projeto analisado, não regras universais de design.

## Regras da competência
1. Começar pela menor estrutura capaz de comunicar hierarquia e ação principal.
2. Evitar dependência visual que não tenha função observável no contrato da tela.
3. Preservar semântica HTML, navegação por teclado e foco visível.
4. Tratar responsividade, contraste e performance como portões, não como preferências.
5. Componente só entra quando reutilização ou clareza justificar a abstração.
6. CSS base deve permanecer fácil de sobrescrever pelo projeto consumidor.
7. Não impor paleta, tipografia ou framework como identidade fixa da competência.

## Como usar em projeto
A skill de projeto apenas `referencia` esta competência. A versão fica congelada na unidade; atualização futura exige leitura do delta e reconciliação incremental antes de avançar `versao_fixada`.

Contextos típicos: `frontend`, `tela`, `componente`, `formulario`, `landing`.

## Portões
- axe: sem violação crítica/seríssima;
- teclado: `Tab` percorre elementos interativos e foco permanece visível;
- Lighthouse: `LCP < 2.5 s` e `CLS < 0.1` no ambiente declarado;
- peso: dentro do orçamento declarado pelo contrato do projeto;
- HTML/CSS: sem erro estrutural que invalide semântica ou parsing.

Portão indisponível produz `não verificado`; não promover artefato consumidor a `aceito` por aparência visual apenas.

## Como modificar sem perder aprendizado
Antes de normalizar qualquer mudança do upstream ou do fork:
1. inventariar upstream/fork e commits;
2. ler o delta;
3. preservar decisões ainda válidas;
4. registrar substituições explícitas;
5. obter `DELTA_INVENTORY=PASS` e `LEARNING_PRESERVED=PASS`;
6. só então normalizar esta skill e atualizar consumidores.

## Armadilhas observáveis
- transformar minimalismo em ausência de acessibilidade;
- usar somente `hover` para comunicar estado;
- assumir que framework pesado é necessário para tela simples;
- copiar cores/exemplos do upstream como identidade obrigatória;
- declarar MIT pelo README como se um arquivo `LICENSE` tivesse sido verificado;
- atualizar a skill no iffcloud sem ler o delta do fork/upstream.
