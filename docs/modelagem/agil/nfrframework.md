# NFR Framework

## Introdução

O **NFR Framework** é uma abordagem para representar e analisar [Requisitos Não-Funcionais](../../elicitacao/req_elicitados.md), oferecendo uma estrutura formal para armazenar tanto o desenho quanto o racional por trás do processo de design de requisitos. Seu objetivo é auxiliar desenvolvedores na implementação de soluções personalizadas, considerando:

- Características do domínio e do sistema em questão;
- Requisitos funcionais e não-funcionais;
- Prioridades e carga de trabalho.

Esses fatores determinam a escolha das alternativas de desenvolvimento mais adequadas para cada sistema. Para isso, o framework utiliza grafos chamados **Softgoal Interdependency Graphs (SIGs)**, nos quais os *softgoals* representam objetivos abstratos de satisfação imprecisa.<a id="anchor_1" href="#REF1">[1]</a>

## Softgoal Interdependency Graph (SIG)

O **Softgoal Interdependency Graph (SIG)** é uma ferramenta gráfica utilizada pelo *NFR Framework* para representar decisões de projeto relacionadas a *softgoals* — objetivos com critérios de satisfação vagos ou imprecisos. Cada nó do grafo representa um *softgoal*, enquanto as arestas indicam relações de decomposição ou de contribuição entre eles. <a id="anchor_1" href="#REF1">[1]</a>

### Tipos de Softgoal

Para compreender o funcionamento do SIG, é essencial entender os diferentes tipos de *softgoal*:

1. **Softgoals NFR**  
   Representam diretamente os Requisitos Não-Funcionais. São organizados hierarquicamente e agrupados em catálogos temáticos (como desempenho, segurança, usabilidade, etc.).

2. **Softgoals de Operacionalização**  
   Correspondem a soluções concretas (operações, processos, estruturas de dados, restrições) que visam satisfazer *softgoals* NFR ou outros de operacionalização.

3. **Softgoals de Afirmação**  
   São registros em linguagem natural que expressam justificativas de projeto ou fatores do domínio, como carga de trabalho, decisões de priorização e contexto organizacional.

A figura 1 mostra a representação dos tipos de *softgoals* que estão presentes em um NRF Framework:

<p align="center"><i>Figura 1: Tipos das Softgoals</i></p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/tipos.png" width="600">
</p>

<font size="3"><p style="text-align: center"> Fonte: (SILVA, 2019)</p></font>

### Interdependências

As interdependências no SIG definem as associações entre os *softgoals* e se dividem em dois tipos principais:

#### Decomposições

A decomposição permite subdividir *softgoals* em objetivos mais específicos, facilitando a análise e a priorização. Pode ocorrer em todos os tipos de *softgoal*:

- **NFR**: Fragmenta objetivos amplos em partes menores, reduzindo ambiguidades.
- **Operacionalização**: Refina uma solução geral em alternativas específicas.
- **Afirmação**: Serve para afirmar ou refutar justificativas de projeto.
- **Priorização**: Permite atribuir diferentes níveis de prioridade entre *softgoals* do mesmo tipo.

A figura 2 ilustra essas diferentes formas de decomposição dentro do NFR Framework:

<p align="center"><i>Figura 2: Tipos de Decomposição das Softgoals</i></p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/tabela2.png" width="600">
</p>

<font size="3"><p style="text-align: center"> Fonte: (SILVA, 2019)</p></font>

#### Contribuições

Contribuições indicam como um *softgoal* impacta outro. Podem ser:

- **AND**: Todos os derivados devem ser satisfeitos para satisfazer o *softgoal* principal.
- **OR**: A satisfação de ao menos um derivado é suficiente.
- **MAKE (++):** Contribuição totalmente positiva.
- **BREAK (--):** Contribuição totalmente negativa.
- **HELP (+):** Contribuição levemente positiva.
- **HURT (-):** Contribuição levemente negativa.
- **UNKNOWN (?)**: Contribuição desconhecida.
- **EQUALS**: Correlação direta entre os níveis de satisfação.
- **SOME**: A contribuição é conhecida, mas sua intensidade é incerta. <a id="anchor_2" href="#REF2">[2]</a>

## Procedimento de Avaliação no NFR Framework

O **procedimento de avaliação** determina o grau em que os requisitos não funcionais (softgoals) são satisfeitos por um conjunto de decisões. Dessa forma, ele verifica se cada softgoal ou interdependência do Softgoal Interdependency Graph (SIG) foi suficientemente atendido.<a id="anchor_2" href="#REF2">[2]</a>

### Tipos de rótulos usados

- ✓ **Satisfeito**: O requisito não funcional é plenamente satisfeito.
- 𝒲+ **Fracamente satisfeito**: Satisfação parcial; impacto positivo, mas menos forte que ✓.
- X **Negado**: O requisito não é satisfeito e pode até contradizer os objetivos do sistema.
- 𝒲- **Fracamente negado**: Negação parcial; impacto negativo, mas mais brando que X.
- 🗲 **Conflitante**: Há conflitos entre requisitos; coexistem aspectos positivos e negativos.
- u **Indeterminado**: Não há dados suficientes para determinar o impacto entre os requisitos.

<p align="center"><i>Figura 3: Tipos de rótulos utilizados pelos softgoals</i></p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/tabela3.png" width="600">
</p>

<font size="3"><p style="text-align: center"> Fonte: (SILVA, 2019)</p></font>


<p align="center"><b>Tabela</b> — Histórico de Contribuições</p>

| O que foi feito                                  | Autor(es)                                                                                                  | Data de Criação |
| ------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- | --------------- |
| Adição das tabela modelo de RNF                  | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025      |
| Adição das tabela modelo Cartão de Especificação | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025      |
| Adição de tabela Compatibilidade                 | [João Marcos Moraes](https://github.com/JJOAOMARCOSS)                                                      | 28/05/2025      |
| Adição de tabela Segurança                       | [Luiza da Silva Pugas](https://github.com/Luizaxx)                                                         | 28/05/2025      |
| Adição de tabela Usabilidade                     | [Lucas Mendonça](https://github.com/lucasarruda9)                                                          | 28/05/2025      |
| Adição de tabela Acessibilidade                  | [Ana Victória Guedes da Costa](https://github.com/navicg)                                                  | 28/05/2025      |
| Adição de tabela Desempenho                      | [Artur Mendonça Arruda](https://github.com/ArtyMend07)                                                     | 28/05/2025      |
| Adição de tabela Responsividade                  | [Gabriel Lopes](https://github.com/BrzGab)                                                                 | 28/05/2025      |
| Adição de tabela Confiabilidade                  | [Karoline Luz da Conceição](https://github.com/KarolineLuz)                                                | 28/05/2025      |
| Adição de tabela Autonomia/Offline               | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025      |
| Adição de tabela Aparência                       | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025      |

<font size="3"><p style="text-align: center">Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

## Priorização MoSCoW

Para organizar e definir a importância relativa dos requisitos não-funcionais identificados, este projeto utiliza a técnica de priorização [**MoSCoW**](../../elicitacao/tec_priorizacao/moscow.md).

O método **MoSCoW** categoriza os requisitos em quatro grupos principais:

- **Must have (M)** → Essenciais para o sucesso do sistema. Sem eles, o projeto falha.
- **Should have (S)** → Importantes, mas não críticos. Sua ausência pode ser contornada temporariamente.
- **Could have (C)** → Desejáveis, porém opcionais. Podem ser incluídos se houver tempo e recursos.
- **Won’t have this time (W)** → Fora do escopo atual. Requisitos que foram deliberadamente deixados para versões futuras.

### Aplicação no NFR Framework

No contexto deste projeto, a priorização **MoSCoW** será usada para:

1. **Atribuir prioridades aos softgoals NFR e aos requisitos relacionados**, complementando os valores numéricos de prioridade já indicados nos cartões de especificação.
2. **Guiar decisões de implementação**, ajudando a equipe a entender quais requisitos não-funcionais são indispensáveis, quais podem ser adiados e quais são opcionais.
3. **Registrar as decisões nos Softgoal Interdependency Graphs (SIGs)**, utilizando as tags **M / S / C / W** nos nós e/ou nas legendas, para manter rastreabilidade visual das prioridades.

Essa priorização também será documentada nas tabelas de especificação, adicionando uma coluna e a anotação que indique a categoria **MoSCoW** de cada requisito.

## Metodologia

1. Definição dos temas principais: Usabilidade, Desempenho, Segurança, Acessibilidade, Confiabilidade.
2. Modelagem com o NFR Framework, representando os requisitos não funcionais como softgoals.
3. Construção dos Softgoal Interdependency Graphs (SIGs) no Draw.io para cada tema.
4. Análise de contribuições e conflitos entre softgoals (por exemplo: trade-offs entre desempenho e segurança).
5. Aplicação do procedimento de avaliação, atribuindo rótulos como satisfeito, fracamente satisfeito, negado, fracamente negado, conflitante ou indeterminado para cada softgoal.
6. Validação final com revisão bibliográfica e feedback da equipe, garantindo alinhamento com o estado da arte.


## Tabela de Requisitos Não Funcionais 

| ID    | Descrição                                                                                                                                     | Rastreabilidade                                                                                                                                  | Implementado |
| ----- | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| RNF01 | O sistema deve ser compatível com vários dispositivos como Android e iOS.                                                                     | <a href="/elicitacao/tec_elicitacao/analise_documentos/#anchor_AD">AD09</a>                                                                      | Sim          |
| RNF02 | O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD).                                                             | <a href="/elicitacao/tec_elicitacao/analise_documentos/#anchor_AD">AD10</a>                                                                      | Sim          |
| RNF03 | O sistema deve possuir uma interface simples, limpa e com ícones ilustrativos                                                                 | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN01</a>                                                                         | Sim          |
| RNF04 | O aplicativo deve permitir acessibilidade para pessoas idosas ou com deficiência visual                                                       | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN02</a>                                                                         | Não          |
| RNF05 | O sistema deve funcionar mesmo em dispositivos com baixa capacidade de hardware                                                               | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN04</a>                                                                         | Sim          |
| RNF06 | A navegação deve ser rápida e fluida entre telas, sem necessidade de redirecionamentos excessivos                                             | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN05</a>                                                                         | Não          |
| RNF07 | O sistema deve carregar as informações de forma otimizada, reduzindo tempo de resposta                                                        | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN06</a>                                                                         | Sim          |
| RNF08 | O layout deve ser responsivo para diferentes tamanhos de tela                                                                                 | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN07</a>, <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT22</a> | Sim          |
| RNF09 | O sistema deve ter compatibilidade com leitores de tela                                                                                       | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN08</a>                                                                         | Sim          |
| RNF10 | O app deve conter linguagem clara e acessível, adequada a diferentes níveis de escolaridade                                                   | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN09</a>                                                                         | Não          |
| RNF11 | O aplicativo deve ser mais autoexplicativo, com uma navegação intuitiva e menos dependência de redirecionamentos externos.                    | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN01</a> <a href="/elicitacao/tec_elicitacao/analise_documentos/#anchor_AD">AD11</a>  | Não          |
| RNF12 | O aplicativo deve garantir que as informações exibidas sejam atualizadas e reflitam fielmente a realidade, especialmente em saúde e educação. | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN02</a>                                                                              | Sim          |
| RNF13 | O aplicativo deve apresentar estabilidade, evitando travamentos ou falhas de carregamento, especialmente em redes móveis.                     | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN03</a>                                                                              | Não          |
| RNF14 | O aplicativo deve garantir proteção de dados pessoais, reforçando a confiança do usuário quanto à privacidade e segurança.                    | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN04</a>                                                                              | Sim          |
| RNF15 | O aplicativo deve melhorar a performance do processo de login, permitindo uma experiência mais fluida.                                        | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN05</a>                                                                              | Não          |
| RNF16 | O aplicativo deve considerar a usabilidade para usuários idosos, garantindo que o design e as funcionalidades sejam acessíveis.               | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN06</a>                                                                              | Não          |
| RNF17 | O aplicativo deve fornecer suporte para acessibilidade, incluindo recursos para daltônicos e deficientes visuais.                             | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN07</a>, <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT19</a>      | Não          |
| RNF18 | O aplicativo deve ter uma aparência profissional e confiável para transmitir segurança aos usuários.                                          | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN08</a>                                                                              | Não          |
| RNF19 | O aplicativo deve ser compatível com as versões mais recentes dos sistemas Android e iOS.                                                     | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT15</a>                                                                           | Sim          |
| RNF20 | As funcionalidades principais devem responder em, no máximo, dois segundos para garantir boa experiência.                                     | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT16</a>                                                                           | Sim          |
| RNF21 | A interface deve ser simples, objetiva e utilizar linguagem acessível a usuários com diferentes níveis de escolaridade.                       | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT17</a>                                                                           | Sim          |
| RNF22 | O sistema deve proteger as informações pessoais com criptografia de dados e autenticação segura.                                              | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT18</a>                                                                           | Sim          |
| RNF23 | Deve funcionar em modo offline para consulta de registros ou informações previamente acessadas.                                               | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT20</a>                                                                           | Não          |
| RNF24 | As imagens capturadas pelo usuário devem ser otimizadas para upload rápido mesmo em conexões móveis.                                          | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT21</a>                                                                           | Sim          |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ( [João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

## Taxonomia

A taxonomia é um esquema de classificação que organiza termos e suas relações no contexto de uma área de conhecimento. Segundo Usman et al. (2017), **“taxonomias contribuem para amadurecer um campo de conhecimento, permitindo descrever seus elementos e evoluindo ao longo do tempo ao incorporar novos conhecimentos”**<a id="anchor_2" href="#REF2">[2]</a>.

<p align="center"><b>Tabela</b> — Taxonomia</p>

| Softgoal            | RNFs Relacionados                        |
| ------------------- | ---------------------------------------- |
| *Segurança*         | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF02</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF14</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF22</a>                      |
| *Usabilidade*       | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF03</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF10</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF11</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF16</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF21</a>        |
| *Acessibilidade*    | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF04</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF09</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF17</a>                     |
| *Desempenho*        | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF06</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF07</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF13</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF15</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF20</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF24</a> |
| *Confiabilidade*    | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF01</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF08</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF12</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF18</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF19</a>, <a href="/elicitacao/req_elicitados/#anchor_RF">RNF23</a> |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ( [João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

A taxonomia apresentada nesta tabela organiza os Softgoals (objetivos de qualidade não-funcionais) do sistema e relaciona cada um com os Requisitos Não-Funcionais correspondentes. Essa classificação ajuda a estruturar os critérios que devem ser atendidos para garantir aspectos importantes do software, como compatibilidade, segurança, usabilidade, acessibilidade, desempenho, entre outros.
A Figura 3 ilustra a representação visual dessa taxonomia, facilitando a compreensão das relações entre os Softgoals e seus respectivos Requisitos não funcionais.

<p align="center">
  <img src="/assets/modelagem/nfr/Taxonomia.drawio.png" width="600">
</p>
<p align="center"><i>Figura 3: Taxonomia</i></p>

## Cartões de Especificação

Os cartões de especificação a seguir, Tabelas de 1 a 10, foram utilizados para definir os Requisitos Não-Funcionais a serem utilizados na confecção dos NFR Frameworks.<a id="anchor_2" href="#REF2">[2]</a>

<p align="center"><b>Tabela 1</b> — Cartão de Especificação modelo</p>

| *Item*                  | *Descrição*                                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | Um número sequencial                                                                                        |
| *Classificação*         | Classificação do RNF conforme taxonomia                                                                     |
| *Descrição*             | Declaração única do significado do requisito                                                                |
| *Justificativa*         | Justificativa sobre a criação do requisito                                                                  |
| *Origem*                | Origem do requisito (stakeholder, norma, etc.)                                                              |
| *Critério de Aceitação* | Métrica do requisito que possa ser testada e validada                                                       |
| *Dependências*          | Requisitos relacionados e estruturas dependentes                                                            |
| *Prioridade*            | Categoria de prioridade: **M** (Must have), **S** (Should have), **C** (Could have), **W** (Won’t have) |
| *Conflitos*             | Requisitos conflitantes com este                                                                            |
| *História*              | Data de criação e de modificação                                                                            |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ( [João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

----------

<p align="center"><b>Tabela 2</b> — Cartão de Especificação 2</p>

| *Item*                  | *Descrição*                                                                                  |
| ----------------------- | -------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF02</a>                                    |
| *Classificação*         | Segurança                                                                                    |
| *Descrição*             | O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD).            |
| *Justificativa*         | Garantir a proteção legal dos dados pessoais dos usuários e evitar penalidades legais.       |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/analise_documentos/#anchor_AD">AD10</a>                                        |
| *Critério de Aceitação* | O sistema deve demonstrar conformidade com os princípios e obrigações da LGPD em auditorias. |
| *Dependências*          | RNF14 (Proteção de dados), RNF22 (Autenticação segura).                                      |
| *Prioridade*            | **M** (Must have)                                                                            |
| *Conflitos*             | Pode exigir ajustes em funcionalidades para reduzir coleta ou armazenamento de dados.        |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                      |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

----

<p align="center"><b>Tabela 3</b> — Cartão de Especificação 3</p>

| *Item*                  | *Descrição*                                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF14</a>                                                   |
| *Classificação*         | Segurança                                                                                                   |
| *Descrição*             | O sistema deve garantir proteção de dados pessoais, reforçando a confiança do usuário quanto à privacidade. |
| *Justificativa*         | A proteção de dados é essencial para manter a confiança dos usuários e evitar vazamentos ou ataques.        |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN04</a>                                                           |
| *Critério de Aceitação* | Implementação de criptografia em repouso e em trânsito, políticas de acesso restrito e logs de auditoria.   |
| *Dependências*          | RNF02 (Conformidade LGPD), RNF22 (Autenticação segura), RNF15 (Performance de login).                       |
| *Prioridade*            | **M** (Must have)                                                                                           |
| *Conflitos*             | Pode impactar a performance do sistema, especialmente no processo de login e acesso a dados sensíveis.      |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                     |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

---

<p align="center"><b>Tabela 4</b> — Cartão de Especificação 4</p>

| *Item*                  | *Descrição*                                                                                                  |
| ----------------------- | ------------------------------------------------------------------------------------------------------------ |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF22</a>                                                    |
| *Classificação*         | Segurança                                                                                                    |
| *Descrição*             | O sistema deve usar autenticação segura, preferencialmente integrada ao gov.br, para proteger o acesso.      |
| *Justificativa*         | Autenticação robusta é necessária para evitar acessos não autorizados e fraudes.                             |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT18</a>                                            |
| *Critério de Aceitação* | Implementação de autenticação integrada ao gov.br, uso de protocolos seguros (OAuth, SAML) e logs de acesso. |
| *Dependências*          | RNF14 (Proteção de dados), RNF15 (Performance de login).                                                     |
| *Prioridade*            | **M** (Must have)                                                                                            |
| *Conflitos*             | Pode aumentar a complexidade de implementação e gerar impacto na experiência do usuário (tempo de login).    |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                      |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

## NFR01: Segurança

Este SIG (Softgoal Interdependency Graph) foi elaborado a partir de requisitos não funcionais relacionados à portabilidade do sistema. Esses requisitos garantem que o sistema seja acessível em diferentes ambientes.

## Requisitos: 
Requisitos utilizados para desenvolver o SIG da Figura 1:

### Tabela de Requisitos Relacionados à LGPD

| **Código** | **Descrição**                                                                                                                             |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| RNF02      | O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD).                                                         |
| RNF14      | O aplicativo deve garantir proteção de dados pessoais, reforçando a confiança do usuário quanto à privacidade e segurança.               |
| RNF22      | O sistema deve proteger as informações pessoais com criptografia de dados e autenticação segura.                                          |

<p align="center"><i>Figura 4: SIG: Segurança </i></p>

<p align="center">
  <img src="https://i.ibb.co/Hf9MwG4L/image.png" width="600">
</p>

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>

### Propagação dos Impactos

A Tabela X, apresentada a seguir, mostra a avaliação da propagação dos impactos representados na imagem acima.

### Tabela X: Tabela de Impactos

| **NFR**                                | **Impacto** | **Avaliador**     |
|----------------------------------------|-------------|-------------------|
| Portabilidade                          | ✔           | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)    |
| Manter as mesmas funcionalidades       | ⩗/+         | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)     |
| Disponibilidade em outras plataformas  | ⩗/+         | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)    |



### Tabela X: Tabela de Impactos - Segurança

| *NFR*                        | *Impacto* | *Avaliador*           |
|-----------------------------|-----------|------------------------|
| Conformidade com a LGPD     | ✔         | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)    |
| Proteção de dados           | ⩗/+       | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)    |
| Autenticar de forma segura  | ⩗/+       | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)     |
| Criptografar dados          | ⩗/+       | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)     |
| Satisfação do usuário       | ⩗/+       | [Luiza da Silva Pugas](https://github.com/Luizaxx) e [João Marcos](https://github.com/JJOAOMARCOSS)    |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([João Marcos](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx), 2025)</p></font>


**Vídeo 1** - Validação e Priorização de NFR com usuário por [Luiza da Silva Pugas](https://github.com/Luizaxx)

<p style="text-align: center"><iframe width="560" height="315" src="https://youtube.com/embed/xOqd3H6dOds" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe></p>

<p style="text-align: center"><a href="https://youtu.be/xOqd3H6dOds" target="_blank">Clique aqui para assistir no YouTube</a></p>

| **Nome** | **Função** | **Data** | **Hora** |
|:---------:|:------------------------:|:--------:|:--------:|
| [Luiza da Silva Pugas](https://github.com/Luizaxx) | Elaborador dos NFR | 01/06/2025 | 14:30 |
| Nívea Cecília | Cidadã | 01/06/2025 | 14:30 |


## Termo de consentimento de imagem 
Este documento confirma que a cidadã Nívea Cecília forneceu seu consentimento formal para o uso de sua imagem, conforme os termos estabelecidos.

O termo foi assinado e encontra-se disponível no seguinte arquivo: [PDF](docs/assets/termo-img/Assinatura Nivea .pdf)
---

<p align="center"><b>Tabela 3</b> — Cartão de Especificação 3</p>

| *Item*                  | *Descrição*                                                                                                           |
| ----------------------- | --------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF03</a> / <a href="/elicitacao/req_elicitados/#anchor_RF">RNF10</a> / <a href="/elicitacao/req_elicitados/#anchor_RF">RNF11</a> / <a href="/elicitacao/req_elicitados/#anchor_RF">RNF16</a> / <a href="/elicitacao/req_elicitados/#anchor_RF">RNF21</a>                                                                                |
| *Classificação*         | Usabilidade                                                                                                           |
| *Descrição*             | O sistema deve ser intuitivo, acessível, com linguagem clara e apropriada a diferentes perfis de usuários.            |
| *Justificativa*         | Uma boa usabilidade aumenta a adesão ao aplicativo e reduz a curva de aprendizado dos usuários.                       |
| *Origem*                | Análise documental, brainstorming e entrevistas com usuários.                                                         |
| *Critério de Aceitação* | Interface limpa e clara, compatível com leitores de tela, linguagem acessível, responsividade, e navegação intuitiva. |
| *Dependências*          | RNF08 (Responsividade), RNF17 (Acessibilidade)                                                                        |
| *Prioridade*            |  **M** (Must have)                                                                                                           |
| *Conflitos*             | Pode exigir mais tempo de design e testes com usuários reais.                                                         |
| *História*              | Criado em 28/05/2025 – Última modificação em 28/05/2025                                                               |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Lucas Mendonça](https://github.com/lucasarruda9), 2025)</p></font>

------

<p align="center"><b>Tabela 10</b> — Cartão de Especificação 10</p>

| *Item*                  | *Descrição*                                                                                                                  |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF04</a>                                                                    |
| *Classificação*         | Acessibilidade                                                                                                               |
| *Descrição*             | O aplicativo deve permitir acessibilidade para pessoas idosas ou com deficiência visual.                                     |
| *Justificativa*         | Garante que o sistema seja inclusivo para públicos com diferentes necessidades e limitações físicas.                         |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN02</a>                                                         |
| *Critério de Aceitação* | Testes mostrando compatibilidade com recursos de acessibilidade do sistema operacional, como ajustes de tamanho e contraste. |
| *Dependências*          | RNF03 (Interface intuitiva), RNF11 (Linguagem acessível).                                                                    |
| *Prioridade*            | **M** (Must have)                                                                                                            |
| *Conflitos*             | Pode exigir ajustes adicionais no design visual e maior atenção em testes especializados.                                    |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                                      |



<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Ana Victória Guedes da Costa](https://github.com/navicg) e [Karoline Luz da Conceição](https://github.com/KarolineLuz), 2025)</p></font>

---

<p align="center"><b>Tabela 11</b> — Cartão de Especificação 11</p>

| *Item*                  | *Descrição*                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF09</a>                                                                 |
| *Classificação*         | Acessibilidade                                                                                                            |
| *Descrição*             | O sistema deve ter compatibilidade com leitores de tela para atender usuários com deficiência visual.                     |
| *Justificativa*         | Permite o uso do sistema por usuários cegos ou com baixa visão, garantindo acesso à informação.                           |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN08</a>                                                      |
| *Critério de Aceitação* | Testes com leitores de tela como TalkBack (Android) e VoiceOver (iOS), garantindo leitura correta dos elementos e fluxos. |
| *Dependências*          | RNF03 (Interface intuitiva), RNF11 (Linguagem acessível).                                                                 |
| *Prioridade*            | **M** (Must have)                                                                                                         |
| *Conflitos*             | Pode limitar certas escolhas visuais, exigindo atenção na marcação semântica e descrição de imagens.                      |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                                   |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Ana Victória Guedes da Costa](https://github.com/navicg) e [Karoline Luz da Conceição](https://github.com/KarolineLuz), 2025)</p></font>

---

<p align="center"><b>Tabela 12</b> — Cartão de Especificação 12</p>

| *Item*                  | *Descrição*                                                                                                                |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF17</a>                                                                  |
| *Classificação*         | Acessibilidade                                                                                                             |
| *Descrição*             | O aplicativo deve fornecer suporte para daltônicos e outros tipos de deficiência visual.                                   |
| *Justificativa*         | Assegura que os elementos visuais sejam acessíveis a diferentes tipos de deficiência, ampliando o público-alvo do sistema. |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN07</a>, <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT19</a>                                                       |
| *Critério de Aceitação* | Testes de contraste, inclusão de ícones não baseados apenas em cor, e modos de exibição adaptados.                         |
| *Dependências*          | RNF03 (Interface intuitiva), RNF11 (Linguagem acessível).                                                                  |
| *Prioridade*            | **M** (Must have)                                                                                                          |
| *Conflitos*             | Pode exigir ajustes detalhados no design de cores, contrastes e elementos gráficos.                                        |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                                    |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Ana Victória Guedes da Costa](https://github.com/navicg) e [Karoline Luz da Conceição](https://github.com/KarolineLuz), 2025)</p></font>

---

<p align="center"><b>Tabela 13</b> — Cartão de Especificação 13</p>

| *Item*                  | *Descrição*                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF06</a>                                                 |
| *Classificação*         | Desempenho                                                                                                |
| *Descrição*             | A navegação deve ser rápida e fluida entre telas, sem necessidade de redirecionamentos excessivos.        |
| *Justificativa*         | Garante que os usuários tenham uma experiência ágil e sem interrupções ao usar o sistema.                 |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN05</a>                                                           |
| *Critério de Aceitação* | O tempo de transição entre telas deve ser inferior a dois segundos, sem redirecionamentos desnecessários. |
| *Dependências*          | RNF08 (Responsividade), RNF01 (Compatibilidade).                                                          |
| *Prioridade*            | **S** (Should have)                                                                                       |
| *Conflitos*             | Pode exigir otimizações e adaptações específicas para diferentes dispositivos ou plataformas.             |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                   |



<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 14</b> — Cartão de Especificação 14</p>

| *Item*                  | *Descrição*                                                                                                 |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF07</a>                                                   |
| *Classificação*         | Desempenho                                                                                                  |
| *Descrição*             | O sistema deve carregar as informações de forma otimizada, reduzindo o tempo de resposta.                   |
| *Justificativa*         | Minimiza o tempo de espera do usuário, tornando a interação mais eficiente.                                 |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN06</a>                                                             |
| *Critério de Aceitação* | As principais informações devem ser carregadas em até dois segundos, mesmo sob condições de rede moderadas. |
| *Dependências*          | RNF06 (Navegação fluida), RNF08 (Responsividade).                                                           |
| *Prioridade*            | **S** (Should have)                                                                                         |
| *Conflitos*             | Otimizações de carregamento podem impactar o consumo de recursos do dispositivo.                            |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                     |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 15</b> — Cartão de Especificação 15</p>

| *Item*                  | *Descrição*                                                                                                               |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF13</a>                                                                 |
| *Classificação*         | Desempenho                                                                                                                |
| *Descrição*             | O aplicativo deve apresentar estabilidade, evitando travamentos ou falhas de carregamento, especialmente em redes móveis. |
| *Justificativa*         | Garante que o sistema funcione bem mesmo em condições adversas de conexão, evitando perda de confiança do usuário.        |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN03</a>                                                                           |
| *Critério de Aceitação* | Testes de estabilidade mostrando menos de 1% de falhas em redes móveis durante sessões prolongadas.                       |
| *Dependências*          | RNF05 (Baixo hardware), RNF20 (Tempo de resposta rápido).                                                                 |
| *Prioridade*            | **S** (Should have)                                                                                                       |
| *Conflitos*             | Requer testes detalhados e ajustes específicos para diferentes condições de rede.                                         |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                                   |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 16</b> — Cartão de Especificação 16</p>

| *Item*                  | *Descrição*                                                                                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------ |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF15</a>                                                          |
| *Classificação*         | Desempenho                                                                                                         |
| *Descrição*             | O aplicativo deve melhorar a performance do processo de login, permitindo uma experiência mais fluida.             |
| *Justificativa*         | O login é um ponto crítico da experiência, e sua eficiência impacta diretamente a satisfação do usuário.           |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN05</a>                                                                              |
| *Critério de Aceitação* | O login deve ser concluído em menos de três segundos em 90% das tentativas, considerando diferentes tipos de rede. |
| *Dependências*          | RNF22 (Autenticação segura), RNF14 (Proteção de dados).                                                            |
| *Prioridade*            | **S** (Should have)                                                                                                |
| *Conflitos*             | Melhorar performance pode limitar certos mecanismos de segurança mais robustos.                                    |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                            |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 17</b> — Cartão de Especificação 17</p>

| *Item*                  | *Descrição*                                                                                               |
| ----------------------- | --------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF20</a>                                                 |
| *Classificação*         | Desempenho                                                                                                |
| *Descrição*             | As funcionalidades principais devem responder em, no máximo, dois segundos para garantir boa experiência. |
| *Justificativa*         | A resposta rápida mantém o usuário engajado e reduz a sensação de lentidão no uso do aplicativo.          |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT16</a>                                                              |
| *Critério de Aceitação* | Medição de tempo de resposta com limite de dois segundos para as funções críticas.                        |
| *Dependências*          | RNF07 (Carregamento otimizado), RNF06 (Navegação fluida).                                                 |
| *Prioridade*            | **S** (Should have)                                                                                       |
| *Conflitos*             | Pode demandar otimizações agressivas, impactando legibilidade ou modularidade do código.                  |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                   |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 18</b> — Cartão de Especificação 18</p>

| *Item*                  | *Descrição*                                                                                           |
| ----------------------- | ----------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF24</a>                                             |
| *Classificação*         | Desempenho                                                                                            |
| *Descrição*             | As imagens capturadas pelo usuário devem ser otimizadas para upload rápido, mesmo em conexões móveis. |
| *Justificativa*         | Reduzir tempo de upload e evitar frustração, especialmente em regiões com internet limitada.          |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT21</a>                                                          |
| *Critério de Aceitação* | Upload concluído em menos de cinco segundos para imagens até 5MB em redes móveis padrão.              |
| *Dependências*          | RNF13 (Estabilidade), RNF05 (Baixo hardware).                                                         |
| *Prioridade*            | **S** (Should have)                                                                                   |
| *Conflitos*             | Compressão agressiva pode impactar a qualidade visual das imagens.                                    |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                               |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Artur Mendonça Arruda](https://github.com/ArtyMend07), 2025)</p></font>

---

<p align="center"><b>Tabela 19</b> — Cartão de Especificação 19</p>

| *Item*                  | *Descrição*                                                                                                         |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF01</a>                                                           |
| *Classificação*         | Confiabilidade                                                                                                      |
| *Descrição*             | O sistema deve ser compatível com vários dispositivos, como Android e iOS.                                          |
| *Justificativa*         | Garante que o sistema funcione corretamente em diferentes ambientes, aumentando seu alcance e robustez.             |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/analise_documentos/#anchor_AD">AD09</a>                                                                                    |
| *Critério de Aceitação* | Funcionalidade completa testada e validada em pelo menos 95% dos dispositivos Android e iOS mais usados no mercado. |
| *Dependências*          | RNF08 (Responsividade), RNF19 (Compatibilidade com versões).                                                        |
| *Prioridade*            | **M** (Must have)                                                                                                   |
| *Conflitos*             | Pode aumentar a complexidade de testes e a necessidade de manutenção contínua.                                      |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                             |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

<p align="center"><b>Tabela 20</b> — Cartão de Especificação 20</p>

| *Item*                  | *Descrição*                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF08</a>                                                     |
| *Classificação*         | Confiabilidade                                                                                                |
| *Descrição*             | O layout deve ser responsivo para diferentes tamanhos de tela.                                                |
| *Justificativa*         | Assegura uma boa experiência em dispositivos variados, prevenindo falhas de visualização e uso.               |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/brainstorming/#anchor_BRN">BRN07</a>, <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT22</a>                                                                  |
| *Critério de Aceitação* | Interface validada em telas de diferentes tamanhos (smartphones, tablets, desktops) com 100% de legibilidade. |
| *Dependências*          | RNF01 (Compatibilidade), RNF19 (Versões Android/iOS).                                                         |
| *Prioridade*            | **M** (Must have)                                                                                             |
| *Conflitos*             | Pode exigir adaptações específicas por plataforma e aumentar o esforço de design.                             |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                       |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

<p align="center"><b>Tabela 21</b> — Cartão de Especificação 21</p>

| *Item*                  | *Descrição*                                                                                                   |
| ----------------------- | ------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF12</a>                                                     |
| *Classificação*         | Confiabilidade                                                                                                |
| *Descrição*             | O aplicativo deve garantir que as informações exibidas estejam atualizadas e reflitam fielmente a realidade.  |
| *Justificativa*         | Evita decisões erradas baseadas em dados desatualizados, essencial para áreas críticas como saúde e educação. |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN02</a>                                                                                                  |
| *Critério de Aceitação* | Os dados sensíveis devem ser atualizados automaticamente de fontes confiáveis a cada 24h.                     |
| *Dependências*          | RNF13 (Estabilidade), RNF22 (Segurança).                                                                      |
| *Prioridade*            | **M** (Must have)                                                                                             |
| *Conflitos*             | Necessidade de sincronização frequente pode impactar desempenho em conexões lentas.                           |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                       |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

<p align="center"><b>Tabela 22</b> — Cartão de Especificação 22</p>

| *Item*                  | *Descrição*                                                                                                     |
| ----------------------- | --------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF18</a>                                                       |
| *Classificação*         | Confiabilidade                                                                                                  |
| *Descrição*             | O aplicativo deve ter uma aparência profissional e confiável para transmitir segurança aos usuários.            |
| *Justificativa*         | A aparência impacta a percepção de qualidade e credibilidade, essencial para aceitação do sistema.              |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/entrevista/#anchor_EN">EN08</a>                                                                                |
| *Critério de Aceitação* | Testes de percepção com usuários mostrando pelo menos 85% de avaliação positiva quanto à confiabilidade visual. |
| *Dependências*          | RNF03 (Interface intuitiva), RNF21 (Design acessível).                                                          |
| *Prioridade*            | **M** (Must have)                                                                                               |
| *Conflitos*             | Pode aumentar custos de design e refinamento visual.                                                            |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                         |


<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

<p align="center"><b>Tabela 23</b> — Cartão de Especificação 23</p>

| *Item*                  | *Descrição*                                                                                       |
| ----------------------- | ------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF19</a>                                         |
| *Classificação*         | Confiabilidade                                                                                    |
| *Descrição*             | O aplicativo deve ser compatível com as versões mais recentes dos sistemas Android e iOS.         |
| *Justificativa*         | Garante que o sistema esteja atualizado e funcione corretamente nos dispositivos mais usados.     |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT15</a>                                                                  |
| *Critério de Aceitação* | Testes confirmando funcionamento total nas três versões mais recentes dos sistemas Android e iOS. |
| *Dependências*          | RNF01 (Compatibilidade), RNF08 (Responsividade).                                                  |
| *Prioridade*            | **M** (Must have)                                                                                 |
| *Conflitos*             | Pode exigir atualizações frequentes e adaptações rápidas a mudanças de sistema operacional.       |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                           |



<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

<p align="center"><b>Tabela 24</b> — Cartão de Especificação 24</p>

| *Item*                  | *Descrição*                                                                                                       |
| ----------------------- | ----------------------------------------------------------------------------------------------------------------- |
| *Nr Requisito*          | <a href="/elicitacao/req_elicitados/#anchor_RF">RNF23</a>                                                         |
| *Classificação*         | Confiabilidade                                                                                                    |
| *Descrição*             | O aplicativo deve funcionar em modo offline para consulta de registros ou informações previamente acessadas.      |
| *Justificativa*         | Permite uso contínuo mesmo em condições de rede instáveis, aumentando a confiabilidade do sistema.                |
| *Origem*                | <a href="/elicitacao/tec_elicitacao/integracao/#anchor_INTT">INT20</a>                                                                                       |
| *Critério de Aceitação* | As principais funcionalidades devem permanecer acessíveis offline, com sincronização automática ao voltar online. |
| *Dependências*          | RNF12 (Dados atualizados), RNF13 (Estabilidade).                                                                  |
| *Prioridade*            | **M** (Must have)                                                                                                 |
| *Conflitos*             | Sincronização offline pode gerar desafios técnicos e de consistência de dados.                                    |
| *História*              | Criado em 28/05/2025 – Última modificação em 31/05/2025                                                           |

<font size="3"><p style="text-align: center"> Fonte: Elaborado pelos autores ([Gabriel Lopes](https://github.com/BrzGab), 2025)</p></font>

---

## Diagramas e Análises





## Bibliografia

> PAIM, F. R. S., CASTRO, J. F. B. Enhancing Data Warehouse Design with the NFR Framework. Centro de Informática UFPE, Recife, 2019. Disponível em: <http://wer.inf.puc-rio.br/WERpapers/artigos/artigos_WER02/paim.pdf>. Acesso em: 22/05/2025

## Referências Bibliográficas

> <a id="REF1" href="#anchor_1">1.</a>CHUNG, L., NIXON, B. A., YU, E., MYLOPOULOS, J. Non-functional requirementsin software engineering. Springer Science & Business Media: [S.l.], 2000. v. 5.

<div style="text-align: center">
<img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/nfrchung.png" >
</div>

<div style="text-align: center">
<img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/nfrchung2.png" >
</div>
 
> <a id="REF2" href="#anchor_2">2.</a>SILVA, Reinaldo Antônio. NFR4ES: Um Catálogo de Requisitos Não-Funcionais para Sistemas Embarcados. Centro de Informática UFPE, Recife, 2019. Disponível em: <https://repositorio.ufpe.br/handle/123456789/34150>. Acesso em: 22/05/2025.

<div style="text-align: center">
<img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/nfrreinaldo2.png" >
</div>

<div style="text-align: center">
<img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/nfrreinaldo.jpeg" >
</div>

<div style="text-align: center">
<img src="https://raw.githubusercontent.com/Requisitos-de-Software/2025.1-e-GDF/refs/heads/docs/nfr/docs/assets/nfr/nfrcartaodeespecifica%C3%A7%C3%A3o.png" >
</div>


## Histórico de Versões

| Versão | Descrição                            | Autor(es)                                                                                         | Data       | Revisor(es)                                                                                                 | Data de Revisão |
| ------ | ------------------------------------ | ------------------------------------------------------------------------------------------------- | ---------- | ----------------------------------------------------------------------------------------------------------- | --------------- |
| 1.0    | Criação da página e introdução | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) | 23/05/2025 | [Luiza da Silva Pugas](https://github.com/Luizaxx) | 23/05/2025      |
| 1.1    | Adição das tabela modelo de RNF | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.2    | Adição das tabela modelo Cartão de Especificação | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.3    | Adição de tabela Compatibilidade | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.4    | Adição de tabela Segurança | [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.5    | Adição de tabela Usabilidade | [Lucas Mendonça](https://github.com/lucasarruda9) | 28/05/2025 | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) | 03/06/2025      |
| 1.6    | Adição de tabela Acessibilidade | [Ana Victória Guedes da Costa](https://github.com/navicg) | 28/05/2025 | [Luiza da Silva Pugas](https://github.com/Luizaxx) | 03/06/2025      |
| 1.7    | Adição de tabela Desempenho | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 28/05/2025 | [Ana Victória Guedes da Costa](https://github.com/navicg) | 03/06/2025      |
| 1.8    | Adição de tabela Responsividade | [Gabriel Lopes](https://github.com/BrzGab) | 28/05/2025 | [Artur Mendonça Arruda](https://github.com/ArtyMend07) | 03/06/2025      |
| 1.9    | Adição de tabela Confiabilidade | [Karoline Luz da Conceição](https://github.com/KarolineLuz) | 28/05/2025 | [Gabriel Lopes](https://github.com/BrzGab) | 03/06/2025      |
| 1.10    | Adição de tabela Autonomia/Offline | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.11    | Adição de tabela Aparência | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) e [Luiza da Silva Pugas](https://github.com/Luizaxx) | 28/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
| 1.12    | Arruamndo as tabelas diminuindo com base na taxonomia | [João Marcos Moraes](https://github.com/JJOAOMARCOSS) | 31/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 03/06/2025      |
