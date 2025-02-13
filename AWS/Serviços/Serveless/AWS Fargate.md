# AWS Fargate
## Visão Geral

O AWS Fargate é um serviço de computação em contêineres que permite executar contêineres sem gerenciar servidores ou clusters. Ele é compatível com o Amazon Elastic Container Service (ECS) e o Amazon Elastic Kubernetes Service (EKS), oferecendo uma maneira simples e eficiente de executar aplicações em contêineres.

**Link Oficial:** [AWS Fargate](https://aws.amazon.com/fargate/)

## Casos de Uso Comuns

- **Execução de Microsserviços:** Execução de aplicações baseadas em microsserviços sem a necessidade de gerenciar infraestrutura.
- **Aplicações Web:** Hospedagem de aplicações web em contêineres com escalabilidade automática.
- **Processamento de Dados:** Execução de tarefas de processamento de dados em contêineres.
- **Ambientes de Desenvolvimento e Teste:** Criação de ambientes de desenvolvimento e teste isolados e escaláveis.

## Principais Recursos

- **Gerenciamento Automático de Infraestrutura:** Elimina a necessidade de provisionar, configurar e escalar servidores.
- **Integração com ECS e EKS:** Compatível com Amazon ECS e Amazon EKS para orquestração de contêineres.
- **Escalabilidade Automática:** Escalabilidade automática com base na demanda.
- **Segurança Integrada:** Isolamento de tarefas em nível de kernel e integração com AWS IAM para controle de acesso.

## Benefícios

- **Simplicidade:** Elimina a complexidade de gerenciar servidores e clusters.
- **Escalabilidade:** Escalabilidade automática para atender à demanda das aplicações.
- **Custo-Efetivo:** Paga apenas pelos recursos de computação e memória utilizados.
- **Segurança:** Isolamento de tarefas e integração com serviços de segurança da AWS.

## Limitações

- **Custos para Cargas de Trabalho Intensivas:** Para cargas de trabalho intensivas em computação, os custos podem ser mais altos comparados a instâncias EC2 gerenciadas manualmente.
- **Limitações de Personalização:** Menos flexibilidade em termos de personalização de hardware e configurações de baixo nível.
- **Compatibilidade:** Requer uso de ECS ou EKS para orquestração de contêineres.

## Integrações

- Amazon ECS
- Amazon EKS
- [[AWS Identity and Access Management (IAM)]]
- Amazon CloudWatch
- AWS Load Balancer

## Exemplos de Uso

```yaml
# Exemplo de definição de tarefa no Amazon ECS com Fargate
version: '3'
services:
  web:
    image: nginx
    ports:
      - "80:80"
    deploy:
      resources:
        limits:
          cpus: '0.5'
          memory: '512M'
```

## Melhores Práticas

- **Monitoramento:** Utilize o Amazon CloudWatch para monitorar o desempenho e a saúde das tarefas em execução no Fargate.
- **Segurança:** Implemente políticas de IAM restritivas e utilize segredos do AWS Secrets Manager para gerenciar credenciais.
- **Otimização de Recursos:** Ajuste os limites de CPU e memória para otimizar custos e desempenho.
- **Integração Contínua:** Integre o Fargate com pipelines de CI/CD para automatizar a implantação de contêineres.

## Custos

- **Cobrança por Uso:** Paga-se pelo uso de CPU e memória alocados para as tarefas em execução.
- **Free Tier:** Inclui um limite gratuito de horas de uso de CPU e memória mensalmente.

## Links Úteis

- [Documentação Oficial do AWS Fargate](https://docs.aws.amazon.com/fargate/)
- [Amazon ECS](https://aws.amazon.com/ecs/)
- [Amazon EKS](https://aws.amazon.com/eks/)
- [AWS Pricing Calculator](https://calculator.aws/)

## Notas Adicionais

- O AWS Fargate é ideal para equipes que desejam focar no desenvolvimento de aplicações sem se preocupar com a infraestrutura subjacente.
- Para cargas de trabalho que requerem alto desempenho ou personalização de hardware, considere o uso de instâncias EC2 gerenciadas manualmente.

---