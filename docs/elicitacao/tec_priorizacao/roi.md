# Roi

## Introdução


A técnica ROI (Return on Investment ou Retorno sobre Investimento) é uma abordagem que visa avaliar a relação entre o benefício esperado de um requisito e o custo estimado para sua implementação. No contexto do projeto de requisitos do eGDF, esta técnica nos ajudará a priorizar os requisitos que trarão maior valor aos usuários considerando os recursos necessários para implementá-los.

## Metodologia

Para aplicar a técnica ROI, seguimos os seguintes passos:

1. **Avaliação do Benefício (1-5):**
   - 1: Benefício muito baixo
   - 2: Benefício baixo
   - 3: Benefício moderado
   - 4: Benefício alto
   - 5: Benefício muito alto

2. **Avaliação do Custo (1-5):**
   - 1: Custo muito baixo
   - 2: Custo baixo
   - 3: Custo moderado
   - 4: Custo alto
   - 5: Custo muito alto

3. **Cálculo do ROI:**
   - ROI = Benefício / Custo

4. **Classificação da Prioridade:**
   - Alta: ROI ≥ 2
   - Média: 1 < ROI < 2
   - Baixa: ROI ≤ 1

## Link da gravação
[Link para a gravação da reunião](https://youtu.be/eH5Uf2jb0g8)

## Priorização dos Requisitos

### Requisitos Funcionais

<p style="text-align: center"><b>Tabela 1:</b> Priorização dos Requisitos Funcionais</p>

| Requisitos | ID | Descrição | Benefício (1-5) | Custo (1-5) | ROI | Prioridade |
|------------|----|-----------|-----------------|-------------|-----|------------|
| RF01 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR01</a>, <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD01</a> | O usuário deve conseguir realizar login de forma simples e rápida | 5 | 2 | 2.5 | Alta |
| RF02 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR02</a> | O usuário deve conseguir acessar funcionalidades mesmo com pouca familiaridade com tecnologia | 5 | 3 | 1.67 | Média |
| RF03 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR03</a> | O usuário deve poder receber notificações personalizadas com base em sua localização | 4 | 3 | 1.33 | Média |
| RF04 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR04</a> | O usuário deve poder consultar agendamentos e serviços em um único local centralizado | 5 | 2 | 2.5 | Alta |
| RF05 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR05</a>, <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD05</a>, <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT13</a> | O usuário deve ter acesso a um assistente virtual com acessibilidade por voz | 4 | 4 | 1 | Baixa |
| RF06 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR06</a> | O usuário deve poder acessar tutoriais passo a passo sobre como usar o app | 4 | 2 | 2 | Alta |
| RF07 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR07</a>, <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN08</a>, <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD08</a> | O usuário deve poder alterar o tamanho da fonte e o contraste de cores | 4 | 2 | 2 | Alta |
| RF08 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR08</a> | O aplicativo deve permitir modo escuro | 3 | 2 | 1.5 | Média |
| RF09 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR10</a> | O usuário deve poder acessar e visualizar notícias relevantes | 3 | 2 | 1.5 | Média |
| RF10 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR11</a> | O usuário deve poder gerar relatórios e visualizar comprovantes de agendamentos | 4 | 2 | 2 | Alta |
| RF11 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR12</a> | O aplicativo deve permitir a integração com serviços de saúde, educação e mobilidade | 5 | 4 | 1.25 | Média |
| RF12 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR13</a> | O usuário deve poder alterar o idioma do aplicativo | 3 | 3 | 1 | Baixa |
| RF13 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR14</a> | O usuário deve poder personalizar suas preferências e perfis para recomendações de serviços | 4 | 3 | 1.33 | Média |
| RF14 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR15</a> | O aplicativo deve permitir o envio de mensagens curtas sobre vencimentos e lembretes importantes | 4 | 2 | 2 | Alta |
| RF15 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR16</a> | O usuário deve poder acessar um menu com as principais funções logo na tela inicial | 5 | 2 | 2.5 | Alta |
| RF16 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR17</a> | O usuário deve poder acessar informações de agendamento e reagendamento de forma centralizada | 4 | 2 | 2 | Alta |
| RF17 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR18</a> | O usuário deve poder utilizar chatbot para tirar dúvidas | 3 | 3 | 1 | Baixa |
| RF18 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR19</a> | O aplicativo deve permitir notificações por categorias como saúde, educação, transporte | 4 | 2 | 2 | Alta |
| RF19 | <a href="../../tec_elicitacao/brainstorming/#anchor_BS">BR20</a> | O usuário deve conseguir compartilhar ou salvar informações importantes | 4 | 2 | 2 | Alta |
| RF20 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN01</a> | O aplicativo permite a visualização da localização dos ônibus em tempo real | 5 | 4 | 1.25 | Média |
| RF21 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN02</a> | O aplicativo fornece links para serviços externos de forma eficiente | 3 | 2 | 1.5 | Média |
| RF22 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN03</a>, <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT07</a> | O aplicativo oferece funcionalidades para consulta de informações educacionais | 4 | 3 | 1.33 | Média |
| RF23 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN04</a> | O aplicativo permite autenticação segura através da plataforma gov.br | 5 | 3 | 1.67 | Média |
| RF24 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN05</a> | O aplicativo facilita o acesso a serviços relacionados a impostos | 5 | 3 | 1.67 | Média |
| RF25 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN06</a> | O aplicativo implementa funcionalidades adicionais na área educacional | 4 | 3 | 1.33 | Média |
| RF26 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN09</a> | O aplicativo deve permitir que usuários reportem problemas da cidade | 4 | 3 | 1.33 | Média |
| RF27 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN10</a>, <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT05</a> | O aplicativo deve fornecer acesso a números de serviços de emergência | 5 | 1 | 5 | Alta |
| RF28 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN11</a> | O aplicativo deve oferecer uma seção de suporte ao usuário | 4 | 2 | 2 | Alta |
| RF29 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD02</a> | O sistema deve permitir que o usuário solicite serviços públicos | 5 | 3 | 1.67 | Média |
| RF30 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD03</a> | O sistema deve permitir o usuário utilizar um mapa para localizar serviços | 4 | 3 | 1.33 | Média |
| RF31 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD04</a> | O sistema deve permitir que o usuário visualize status das solicitações | 4 | 2 | 2 | Alta |
| RF32 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD06</a> | O sistema deve permitir que o usuário confirme resolução de problemas | 4 | 2 | 2 | Alta |
| RF33 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD07</a> | O sistema deve permitir que o usuário exclua seus dados | 5 | 2 | 2.5 | Alta |
| RF34 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT01</a> | Permitir o registro de ocorrências de infraestrutura urbana | 4 | 3 | 1.33 | Média |
| RF35 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT02</a> | Disponibilizar categorias pré-definidas para ocorrências | 3 | 2 | 1.5 | Média |
| RF36 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT03</a> | Permitir selecionar tipo de serviço (implantação, limpeza ou reparo) | 3 | 2 | 1.5 | Média |
| RF37 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT04</a> | Possibilitar adição de descrição, imagem e localização GPS | 4 | 2 | 2 | Alta |
| RF38 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT06</a> | Disponibilizar agendamento de serviços de saúde pública | 5 | 3 | 1.67 | Média |
| RF39 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT08</a> | Oferecer acesso a serviços de transporte público | 5 | 3 | 1.67 | Média |
| RF40 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT09</a> | Permitir agendamentos em serviços sociais | 4 | 3 | 1.33 | Média |
| RF41 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT10</a> | Disponibilizar emissão de tributos e documentos fiscais | 5 | 3 | 1.67 | Média |
| RF42 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT11</a> | Fornecer histórico de interações do usuário | 4 | 2 | 2 | Alta |
| RF43 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT12</a> | Apresentar feed de notícias atualizadas | 3 | 2 | 1.5 | Média |
| RF44 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT13</a> | Integrar assistente virtual com respostas automáticas | 4 | 4 | 1 | Baixa |
| RF45 | <a href="../../tec_elicitacao/introspeccao/#anchor_INT">INT14</a> | Fornecer mapa com localização de serviços públicos | 4 | 3 | 1.33 | Média |

<p style="text-align: center"><b>Fonte:</b> Artur, 2025</p>

### Requisitos Não Funcionais

<p style="text-align: center"><b>Tabela 2:</b> Priorização dos Requisitos Não Funcionais</p>

| Requisitos | ID | Descrição | Benefício (1-5) | Custo (1-5) | ROI | Prioridade |
|------------|----|-----------|-----------------|-------------|-----|------------|
| RNF01 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD09</a> | O sistema deve ser compatível com vários dispositivos como Android e iOS | 5 | 4 | 1.25 | Média |
| RNF02 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD10</a> | O sistema deve estar em conformidade com a Lei Geral de Proteção de Dados (LGPD) | 5 | 3 | 1.67 | Média |
| RNF03 | <a href="../../tec_elicitacao/analise_documentos/#anchor_AD">AD11</a> | O sistema deve ter uma interface intuitiva | 5 | 2 | 2.5 | Alta |
| RNF04 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN01</a> | O sistema deve possuir uma interface simples, limpa e com ícones ilustrativos | 4 | 2 | 2 | Alta |
| RNF05 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN02</a> | O aplicativo deve permitir acessibilidade para pessoas idosas ou com deficiência visual | 5 | 3 | 1.67 | Média |
| RNF06 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN04</a> | O sistema deve funcionar em hardware limitado | 4 | 3 | 1.33 | Média |
| RNF07 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN05</a> | A navegação deve ser rápida e fluida | 5 | 3 | 1.67 | Média |
| RNF08 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN06</a> | O sistema deve ter carregamento otimizado | 4 | 3 | 1.33 | Média |
| RNF09 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN07</a>, <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT22</a> | O layout deve ser responsivo | 4 | 3 | 1.33 | Média |
| RNF10 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN08</a> | O sistema deve ter compatibilidade com leitores | 5 | 3 | 1.67 | Média |
| RNF11 | <a href="../../tec_elicitacao/brainstorming/#anchor_BRN">BRN09</a> | O app deve ter linguagem clara e acessível | 5 | 2 | 2.5 | Alta |
| RNF12 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN01</a> | O aplicativo deve ser autoexplicativo | 4 | 2 | 2 | Alta |
| RNF13 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN02</a> | As informações devem ser atualizadas e precisas | 5 | 3 | 1.67 | Média |
| RNF14 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN03</a> | O aplicativo deve ter estabilidade | 5 | 3 | 1.67 | Média |
| RNF15 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN04</a> | O aplicativo deve garantir proteção de dados | 5 | 3 | 1.67 | Média |
| RNF16 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN05</a> | O processo de login deve ter boa performance | 4 | 3 | 1.33 | Média |
| RNF17 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN06</a> | O design deve ser acessível para idosos | 5 | 3 | 1.67 | Média |
| RNF18 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN07</a>, <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT19</a> | Deve ter recursos para daltônicos e deficientes | 5 | 3 | 1.67 | Média |
| RNF19 | <a href="../../tec_elicitacao/entrevista/#anchor_EN">EN08</a> | Deve ter aparência profissional e confiável | 4 | 2 | 2 | Alta |
| RNF20 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT15</a> | Compatível com Android e iOS recentes | 5 | 4 | 1.25 | Média |
| RNF21 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT16</a> | Resposta em máximo dois segundos | 5 | 3 | 1.67 | Média |
| RNF22 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT17</a> | Interface simples e linguagem acessível | 5 | 2 | 2.5 | Alta |
| RNF23 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT18</a> | Proteção com criptografia e autenticação | 5 | 3 | 1.67 | Média |
| RNF24 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT20</a> | Funcionamento offline para consultas | 4 | 4 | 1 | Baixa |
| RNF25 | <a href="../../tec_elicitacao/integracao/#anchor_INTT">INT21</a> | Otimização de imagens para upload | 3 | 2 | 1.5 | Média |

<p style="text-align: center"><b>Fonte:</b> Artur, 2025</p>

## Resultados

Com base na priorização realizada, podemos observar que:

1. **Requisitos Funcionais:**
   - Alta Prioridade: 16 requisitos (35.6%)
   - Média Prioridade: 24 requisitos (53.3%)
   - Baixa Prioridade: 5 requisitos (11.1%)

2. **Requisitos Não Funcionais:**
   - Alta Prioridade: 6 requisitos (24%)
   - Média Prioridade: 18 requisitos (72%)
   - Baixa Prioridade: 1 requisito (4%)

### Analise das Informações:

1. A maioria dos requisitos funcionais e não funcionais tem prioridade média, indicando um bom equilíbrio entre benefício e custo.

2. Os requisitos de alta prioridade estão principalmente relacionados a:
   - Usabilidade básica (login, menu principal)
   - Funcionalidades essenciais (agendamentos, serviços de emergência)
   - Acessibilidade (fonte, contraste)
   - Interface do usuário (simplicidade, intuitividade)

3. Os requisitos de baixa prioridade geralmente envolvem:
   - Funcionalidades avançadas (assistente virtual, modo offline)
   - Recursos que requerem alto custo de implementação

<p style="text-align: center"><b>Figura 1:</b> Distribuição de Prioridades - Requisitos Funcionais</p>

<table align="center">
<tr><th colspan="3">Distribuição de Prioridades - RFs</th></tr>
<tr>
    <td bgcolor="#90EE90" width="35.6%">Alta (35.6%)</td>
    <td bgcolor="#FFFFE0" width="53.3%">Média (53.3%)</td>
    <td bgcolor="#FFB6C1" width="11.1%">Baixa (11.1%)</td>
</tr>
</table>

<p style="text-align: center"><b>Figura 2:</b> Distribuição de Prioridades - Requisitos Não Funcionais</p>

<table align="center">
<tr><th colspan="3">Distribuição de Prioridades - RNFs</th></tr>
<tr>
    <td bgcolor="#90EE90" width="24%">Alta (24%)</td>
    <td bgcolor="#FFFFE0" width="72%">Média (72%)</td>
    <td bgcolor="#FFB6C1" width="4%">Baixa (4%)</td>
</tr>
</table>

<p style="text-align: center"><b>Fonte:</b> Artur, 2025</p>

## Bibliografia

> WIEGERS, Karl; BEATTY, Joy. "Software Requirements". Microsoft Press, 2013.

> SOMMERVILLE, Ian. "Engenharia de Software". 9ª edição, Pearson, 2011.

> The Standish Group. "CHAOS Report". 2020.

## Histórico de Versão

| Versão | Descrição                             | Autor(es)                                       | Data       | Revisor(es)                                   | Data de Revisão |
|--------|----------------------------------------|--------------------------------------------------|------------|-----------------------------------------------|-----------------|
| 1.0    | Criação da documentação do ROI | [Artur Mendonça](https://github.com/ArtyMend07)        | 04/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 04/05/2025      |
| 1.1    | Correção de nome | [Artur Mendonça](https://github.com/ArtyMend07)        | 04/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 04/05/2025      |
| 2.0    | Adição de hyperlinks de rastreabilidade nas tabelas de requisitos | [Artur Mendonça](https://github.com/ArtyMend07)        | 15/05/2025 | [Lucas Mendonça](https://github.com/lucasarruda9) | 16/05/2025      |