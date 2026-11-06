# Studio AI — Vídeos de treinamento e testes de ERP produzidos por IA

> Um estúdio formado por duas IAs especializadas que trabalham em sequência: a primeira **opera um sistema ERP como uma pessoa faria** para testar funcionalidades e gravar vídeos narrados de treinamento; a segunda **adiciona animações** que ilustram o que a narração explica. O resultado é um vídeo pronto para entrega, sem edição manual.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=for-the-badge&logo=anthropic&logoColor=white)
![AI Agents](https://img.shields.io/badge/AI_Agents-412991?style=for-the-badge&logo=robotframework&logoColor=white)

**Projeto interno, desenvolvido na WK Sistemas.** Este repositório apresenta o conceito e os resultados. A implementação não é pública.

---

## O problema

Produzir vídeos de treinamento de um sistema é um trabalho manual e repetitivo: percorrer as telas, gravar, narrar, legendar, animar e editar. Quando o sistema muda ou o texto precisa de ajuste, boa parte do trabalho recomeça.

Testar novas funcionalidades segue a mesma lógica: abrir telas, preencher campos e conferir resultados, várias vezes.

## A ideia

Dividir o trabalho entre **duas IAs, cada uma especialista em uma etapa**, conduzidas por linguagem natural.

| IA | Papel | O que entrega |
| --- | --- | --- |
| **REC** | Opera o sistema de verdade, com o cursor e as telas reais | Vídeo narrado da aula ou da demonstração, ou o resultado de cada cenário de teste com evidências |
| **Motion** | Assiste ao vídeo pronto e decide onde uma animação ajuda a explicar | O mesmo vídeo, com animações e textos curtos sincronizados à fala |

A pessoa descreve o que precisa, e as IAs cuidam do restante.

---

## Como um vídeo é produzido

<p align="center"><img src="docs/fluxo-conceitual.png" alt="Fluxo conceitual de produção de um vídeo" width="820"></p>

**REC: a gravação**

1. **Conteúdo.** O texto narrado sai do material didático oficial. Nada é inventado.
2. **Roteiro.** A IA transforma o conteúdo em um passo a passo no sistema.
3. **Ensaio.** O roteiro é executado sem gravar, para encontrar problemas antes da gravação.
4. **Gravação.** O sistema é operado de verdade enquanto a tela é gravada, com narração, destaque dos cliques, aproximação nas áreas importantes e proteção de dados pessoais.

**Motion: as animações**

5. **Leitura do vídeo.** A IA identifica em que momento cada palavra é dita e quando a tela está parada ou em movimento.
6. **Escolha dos momentos.** Animações entram só quando a narração explica um conceito e a tela não mostra nada importante. Durante cliques, menus e trocas de tela, a tela fala por si.
7. **Animação.** Textos curtos e ícones surgem no instante da palavra-chave, com o fundo desfocado para dar foco, e somem antes de a tela voltar a se mexer.

**Acabamento**

8. **Legenda e entrega.** A legenda entra por último, para nunca ficar coberta, e o vídeo é conferido antes de chegar ao cliente.

---

## Princípios do projeto

- **Cada IA faz uma coisa bem.** Gravar e animar são etapas separadas, com regras próprias, e podem evoluir de forma independente.
- **Ensaiar antes de gravar.** Erros aparecem no ensaio, não no vídeo pronto.
- **Conferir o resultado da ação, não só a aparência da tela.** Um teste só passa quando o efeito esperado realmente aconteceu.
- **Fidelidade ao conteúdo.** Tudo o que a narração diz tem origem no material oficial.
- **A animação nunca disputa atenção com o sistema.** Ela aparece só nos momentos conceituais, uma ideia por vez, e nunca enquanto algo se move na tela.
- **O original é preservado.** As animações são uma camada por cima: a voz e a qualidade da imagem continuam exatamente como foram gravadas.
- **Identidade visual consistente.** Todos os vídeos seguem o mesmo padrão de cores, tipografia e movimento.
- **Segurança.** Uso apenas em ambiente de demonstração, sem dados reais expostos e com proteção automática de informações pessoais.

---

## Resultados

- **Em uso real:** vídeos de treinamento já entregues para o material didático da empresa.
- **Do conteúdo ao vídeo final sem edição manual:** gravação, narração, animações e legenda produzidas pelas IAs.
- **Uma ferramenta, várias demandas:** vídeos de aula, demonstrações de novas funcionalidades e testes.
- **Padronização:** todos os vídeos seguem a mesma qualidade, independentemente da máquina ou de quem opera.
- **Transferível:** a documentação permitiu que outra pessoa da equipe passasse a usar a ferramenta.

---

## Competências aplicadas

Automação de processos · Agentes de IA · Orquestração de múltiplas IAs · Python · Automação de interface · Processamento de vídeo · Motion design · Garantia de qualidade · Documentação técnica

---

## Autor

**Guilherme Babel Machado** · [LinkedIn](https://www.linkedin.com/in/guilherme-babel-machado-25a4531ba) · [GitHub](https://github.com/Babelg)
