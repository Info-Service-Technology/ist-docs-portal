# MEDGEST

![Logo do MEDGEST](../assets/medgest-logo.jpg)

**Gestão Medicamentos**

> **Situação: em desenvolvimento.** Esta página descreve um protótipo e um escopo planejado; não representa disponibilidade para uso operacional.

## Visão geral

O MEDGEST está sendo desenvolvido para apoiar profissionais responsáveis pelo estoque de medicamentos em instituições com uma ou mais unidades. A visão do produto inclui controle de estoque por unidade, lotes e validade, transferências interunidades com aprovação e rastreabilidade e análises consolidadas.

## Estado atual

A versão de desenvolvimento contém uma interface React/Vite, uma API Flask local para autenticação e uma conta de demonstração de uso estritamente local. O painel usa dados fictícios mantidos em memória. Neste estágio, o MEDGEST não se conecta a bases hospitalares, não altera estoques reais, não executa transferências e não está implantado em staging ou produção.

Não use a demonstração com dados reais de medicamentos, instituições, profissionais, pacientes ou operações. A conta de teste não deve ser utilizada em ambientes compartilhados, staging ou produção.

## Escopo em planejamento

- Estoque e lotes por instituição/unidade, com controle de acesso no escopo autorizado.
- Fluxo de transferência entre unidades, incluindo estados de solicitação, aprovação, despacho, trânsito, conferência e recebimento.
- Trilha de auditoria e relatórios operacionais, sujeitos à definição das fontes de verdade e regras de atualização de saldo.
- Integração analítica das fontes operacionais existentes; a proposta em discussão considera data lake em S3, processamento com AWS Glue/PySpark e zonas Bronze, Silver e Gold. Essa arquitetura ainda não foi aprovada nem implantada.
- Avaliação de rota para movimentação entre unidades; o uso de Google Maps e qualquer rastreamento contínuo ainda precisam ser definidos.

Itens desta seção são intenções de planejamento, não funcionalidades disponíveis.

## Segurança e privacidade

A demonstração deve usar dados sintéticos. O produto não está autorizado para tratar dados reais de saúde ou apoiar decisões operacionais. Requisitos de autenticação, autorização, segregação entre instituições/unidades, auditoria, retenção e integração devem ser definidos e validados antes de qualquer uso real. Não foi feita avaliação formal da LGPD ou dos requisitos aplicáveis da ANVISA, nem homologação ou integração com a RNDS. Deploy AWS por Terraform e pipelines GitHub Actions para homologação/produção também não foram implementados ou executados. Esta documentação não constitui certificação de conformidade legal ou de segurança.

## Histórico

Não há release pública do MEDGEST. Mudanças futuras devem ser rastreáveis por Issues, commits, PRs e releases, com validações e implantação registradas. A publicação desta página no IST Docs Portal também depende de revisão e aprovação próprias.
