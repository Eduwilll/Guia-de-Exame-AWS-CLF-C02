---
title: AWS Identity and Access Management (IAM)
tags:
  - aws
  - cloud
  - infra
url: https://aws.amazon.com/pt/iam/
criado: 2025-02-12
atualizado: Wednesday 12th February 2025 19:26:41
---
# AWS Identity and Access Management (IAM)
## Visão Geral

O AWS Identity and Access Management (IAM) é um serviço que ajuda a gerenciar de forma segura o acesso aos serviços e recursos da AWS. Ele permite criar e gerenciar usuários, grupos e permissões, garantindo que apenas pessoas e recursos autorizados possam acessar os serviços da AWS.

**Link Oficial:** [AWS IAM](https://aws.amazon.com/iam/)

## Casos de Uso Comuns

- **Gerenciamento de Usuários:** Criação e gerenciamento de usuários e suas credenciais de acesso.
- **Controle de Acesso:** Definição de permissões granulares para usuários, grupos e roles.
- **Segurança de Recursos:** Proteção de recursos da AWS com políticas de acesso detalhadas.
- **Integração com Serviços AWS:** Uso de roles para permitir que serviços da AWS acessem recursos entre si.

## Principais Recursos

- **Usuários e Grupos:** Criação e gerenciamento de usuários e grupos para organizar permissões.
- **Roles:** Definição de roles para permitir que serviços da AWS e aplicações acessem recursos.
- **Políticas de Acesso:** Criação de políticas JSON para definir permissões granulares.
- **Multi-Factor Authentication (MFA):** Adição de uma camada extra de segurança com autenticação de dois fatores.
- **Auditoria e Monitoramento:** Integração com AWS CloudTrail para auditoria e monitoramento de atividades.

## Benefícios

- **Segurança:** Controle de acesso granular para proteger recursos da AWS.
- **Facilidade de Uso:** Interface simples para gerenciar usuários, grupos e permissões.
- **Escalabilidade:** Suporta grandes organizações com milhares de usuários e recursos.
- **Conformidade:** Ajuda a atender requisitos de conformidade com auditoria de acesso.

## Limitações

- **Complexidade de Configuração:** Configuração inicial pode ser complexa para ambientes muito grandes.
- **Limitações de Políticas:** Políticas de IAM têm limites de tamanho e complexidade.
- **Gerenciamento de Credenciais:** Requer gerenciamento cuidadoso de credenciais de acesso.

## Integrações

- [[Amazon S3]]
- [[Amazon EC2]]
- [[AWS Lambda]]
- [[AWS CloudTrail]]
- [[AWS Organizations]]

## Exemplos de Uso
```json
// Exemplo de uma política IAM para permitir acesso somente leitura ao Amazon S3
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:Get*",
        "s3:List*"
      ],
      "Resource": "*"
    }
  ]
}
```

## Melhores Práticas

- **Princípio do Menor Privilégio:** Conceda apenas as permissões necessárias para realizar uma tarefa.
- **Uso de Roles:** Utilize roles para conceder permissões temporárias a serviços e aplicações.
- **MFA:** Habilite MFA para contas de usuário com permissões elevadas.
- **Monitoramento:** Use o AWS CloudTrail para monitorar atividades e acessos.
- **Revisão Regular:** Revise regularmente as permissões e políticas para garantir que estejam atualizadas.
    

## Custos

- **Gratuito:** O AWS IAM é um serviço gratuito, sem custos adicionais para criação e gerenciamento de usuários, grupos e políticas.
- **Custos de Serviços AWS:** Os custos associados aos serviços da AWS utilizados continuam aplicáveis.
- **Free Tier:** Não há free tier específico para o AWS IAM, mas o serviço em si não tem custos adicionais.
    

## Links Úteis

- [Documentação Oficial do AWS IAM](https://docs.aws.amazon.com/iam/)
- [AWS CloudTrail](https://aws.amazon.com/cloudtrail/)
- [AWS Organizations](https://aws.amazon.com/organizations/)
- [AWS Pricing Calculator](https://calculator.aws/)

## Notas Adicionais

- O AWS IAM é ideal para organizações que precisam gerenciar e proteger o acesso aos serviços e recursos da AWS de forma segura e eficiente.
- Para ambientes complexos, considere o uso do AWS Organizations em conjunto com o AWS IAM para gerenciar permissões em escala.

---