# 🐾 Sistema de Gerenciamento de Clínica Veterinária

> Projeto Prático Baseado em Problemas (PBL)  
> Unidade Curricular: Arquitetura e Modelagem de Sistemas  
> Professor: Abraão de Oliveira Ferreira  

## 📌 Sobre o Sistema

O Sistema de Gerenciamento de Clínica Veterinária foi desenvolvido para centralizar, simplificar e automatizar a rotina operacional e clínica de uma clínica veterinária. A aplicação atende desde o cadastro de tutores e seus animais até o agendamento de consultas, acompanhamento de prontuários médicos e envio automatizado de lembretes.

## 🛠️ Funcionalidades Principais (Escopo)

- RF01 – Gestão de Tutores: Cadastro e atualização dos dados pessoais e de contato dos proprietários.
- RF02 – Gestão de Pets: Registro dos animais vinculados aos seus respectivos tutores.
- RF03 – Agendamento Online: Marcação de consultas e exames com validação automática de horários.
- RF04 – Histórico Clínico Digital: Prontuário centralizado com exames, tratamentos, vacinas e triagem.
- RF05 – Lembretes e Notificações: Envio automático de confirmações e alertas de consulta por e-mail e SMS.

## 🏛️ Arquitetura e Tecnologias

- Arquitetura em Camadas: Organização em Apresentação, Aplicação, Domínio e Infraestrutura
- Padrão de Persistência: Repository Pattern acoplado ao banco de dados relacional PostgreSQL.
- Processamento Reativo: Arquitetura orientada a eventos (Event-Driven) para envio assíncrono de notificações via AWS EventBridge.
- Containerização: Gerenciamento do ambiente de desenvolvimento via Docker e Docker Compose.
## 📁 Estrutura do Repositório

clinica-veterinaria-pbl/
├── .env.example                  # Modelo de variáveis de ambiente sem dados sensíveis
├── .gitignore                    # Regras de exclusão do Git (senhas, builds e caches)
├── README.md                     # Documentação principal e guia de início do projeto
├── docs/                         # ARTEFATOS DE ENGENHARIA E MODELAGEM
│   ├── requisitos/               # Requisitos Funcionais (RF01-RF05), RNF e Regras de Negócio
│   ├── modelagem/                # Diagramas UML (Classes, Sequência, Estados) e links do Figma
│   └── arquitetura/              # Decisões de Banco, Camadas e Matriz de Rastreabilidade
├── src/                          # CÓDIGO-FONTE POR MÓDULOS DE DOMÍNIO
│   ├── tutores/                  # Módulo de Gestão de Tutores (RF01)
│   ├── pets/                     # Módulo de Gestão de Pets (RF02)
│   ├── agendamentos/             # Módulo de Agendamentos Online (RF03)
│   ├── historico/                # Módulo de Prontuário e Triagem Clínica (RF04)
│   ├── notificacoes/             # Módulo Reativo de Eventos e Mensageria (RF05)
│   └── autenticacao/             # Módulo de Login, Perfis de Acesso e LGPD (RNF01)
└── tests/                        # SUÍTE DE TESTES AUTOMATIZADOS
    ├── unit/                     # Testes Unitários de Serviços e Regras
    └── integration/              # Testes de Integração com Banco e Barramento
