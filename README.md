💼 Automação Comercial e Funil de Vendas NR-1 (Riscos Psicossociais)
🎯 1. Objetivos do Projeto
O objetivo principal deste projeto é automatizar e estruturar a operação comercial de prospecção, qualificação e fechamento de contratos para empresas que buscam conformidade com a NR-1 (Gerenciamento de Riscos Psicossociais e Ergonomia em SST).

A solução integra um ecossistema prático composto por:

Automação de Processos: Fluxo inteligente construído em n8n (self-hosted) para captação de leads, roteamento por etapas e gestão de cadência.

Qualificação Dinâmica: Diagnóstico prévio baseado em um checklist de 19 questões (19Qs) com classificação de riscos por semáforo (Verde, Amarelo, Vermelho).

Gestão Comercial (CRM): Planilhas estruturadas para acompanhamento de leads (Indústria Exemplo Ltda, Comércio ABC, etc.) e régua de relacionamento do Dia 0 ao Dia 10.

Blindagem Probatória: Argumentação jurídica voltada à prevenção de passivos trabalhistas e notificações do Ministério Público do Trabalho (MPT).

⚙️ 2. Arquitetura e Testes do Fluxo no n8n
O fluxo desenvolvido no n8n foi estruturado em blocos modulares para garantir escalabilidade e controle total da operação:

Webhook de Entrada (Webhook Entradas Lead NR-1): Captura em tempo real os dados de formulários e páginas de captação (Nome, Empresa, Telefone, E-mail e Etapa).

Roteamento Inteligente (Switch Etapa do Funil): Analisa a propriedade recebida e direciona o fluxo automaticamente para:

Trilha de Portfólio: Envio de materiais institucionais.

Trilha de Pré-Auditoria: Processamento do checklist de 19Qs e cálculo da exposição ao risco.

Trilha de Régua de Cadência: Agendamento de mensagens de follow-up (Dias 0, 2, 5 e 10).

Trilha de Proposta/Contrato: Automação para fechamento comercial.

✅ 3. Validações Operacionais
Validação do Webhook: Testado via requisições POST com payloads em JSON simulando a entrada de novos leads no funil.

Validação do Switch: Comprovado o roteamento correto para os nós de portfólio, cadência e geração de propostas com base nas regras lógicas configuradas.

Validação Comercial: Alinhamento perfeito entre as trilhas do n8n e os dados controlados na planilha de prospecção e cadência.

⚠️ 4. Dificuldades Técnicas e Lições Aprendidas (Pivot de Arquitetura)
Durante a fase de testes práticos, o projeto enfrentou desafios específicos relacionados à integração com canais externos de mensageria:

API do WhatsApp (Sandbox da Meta):

Dificuldade: A API oficial apresentou restrições rígidas de conformidade geográfica para números de destino no Brasil (+55) em contas de teste, além de exigir que o usuário iniciasse a janela de conversa enviando uma mensagem prévia.

Solução / Decisão Técnica: Para evitar bloqueios e garantir a estabilidade imediata da entrega, optamos por suspender a dependência direta da Sandbox da Meta, centralizando a robustez do projeto na automação interna do n8n (gestão de dados, planilhas e e-mails) e na execução comercial direta.
