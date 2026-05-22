# SafeGuard Industrial
**Sistema de Gestão Proativa de EPIs e Segurança em Campo**

Projeto desenvolvido para o **Challenge 2026 — Metaindustria**, uma parceria entre a **FIAP** e a **SPI Integração** (Maio de 2026).

---

## 🏭 Contexto e Problema
O setor industrial brasileiro passa por uma transformação impulsionada pela Metaindústria, onde o chão de fábrica passa a ser monitorado gerando dados operacionais massivos. No entanto, a gestão de segurança ainda opera num modelo punitivo e reativo.

Isso gera problemas graves, como:
* **Conformidade seletiva:** Operadores usam EPIs apenas quando o supervisor está presente.
* **Ineficiência manual:** Registros em papel sujeitos a fraudes e alta carga administrativa para os supervisores.
* **Ação reativa:** Reação a acidentes já ocorridos, sem capacidade preventiva, gerando custos bilionários para o país.

## 💡 A Solução
O SafeGuard Industrial é uma plataforma construída sobre três pilares fundamentais: Monitoramento Contínuo, Inteligência Preventiva e Gestão Integrada.

### Funcionalidades Principais
* **Monitoramento em Tempo Real:** Utiliza câmeras com visão computacional (YOLOv8) para detectar ausência de EPIs obrigatórios, além de sensores RFID/NFC para registro automático de check-in/out.
* **Sistema de Alertas Inteligentes:** Envio de alertas ao operador via dispositivo wearable (vibração e LED) e notificação push ao supervisor contendo foto do incidente. Caso o alerta não seja reconhecido em 5 minutos, ocorre o escalonamento automático para o gestor.
* **Analytics e Inteligência Operacional:** Dashboards gerenciais de conformidade em tempo real, relatórios automatizados (NR-6, ISO 45001) e predição de riscos operacionais.

## 👥 Para Quem Construímos (Personas)
* **Carlos (Operador de Campo):** Busca alertas preventivos para não esquecer de utilizar os equipamentos ao transitar entre diferentes zonas.
* **Fernanda (Supervisora de Segurança):** Precisa de visão em tempo real e automação de alertas para conseguir monitorar e auditar o trabalho de múltiplos operadores.
* **Roberto (Gestor Industrial):** Necessita de dados confiáveis e KPIs em tempo real para evitar multas, manter conformidade regulatória e subsidiar relatórios executivos.

## 🛠️ Stack Tecnológica
Nossa arquitetura prioriza performance de edge computing, maturidade empresarial e tecnologias open-source:

* **Backend:** Java 21 + Spring Boot 3
* **Frontend (Web/Mobile):** React 18 + TypeScript / React Native
* **Bancos de Dados:** PostgreSQL 16 (Relacional/Auditoria) e TimescaleDB (Séries Temporais IoT)
* **Mensageria e Cache:** Apache Kafka e Redis
* **Visão Computacional:** Python + OpenCV + YOLOv8
* **Infraestrutura:** Docker + Kubernetes (On-premise para segurança industrial)

## 📂 Estrutura do Repositório
```text
safeguard-industrial/
├── README.md                    # Visão geral, proposta, personas, tecnologias
├── docs/                       
│   └── requisitos.md            # RF, RNF, personas, restrições, matriz de rastreabilidade
├── diagrams/                   
│   ├── casos-de-uso.md          # UC: código PlantUML + descrições completas
│   ├── atividades.md            # Atividades: código PlantUML + narrativa de cenários
│   ├── classes.md               # Classes: código PlantUML + descrições de entidades
│   ├── casos-de-uso.png         # Figura 1 — renderizada
│   ├── atividades.png           # Figura 2 — renderizada
│   └── classes.png              # Figura 3 — renderizada
├── src/                         # Código-fonte (Sprint 2+)
└── sprint-reviews/             
    └── sprint1-review


```
Vitor Saccardo da Silva 
RM 555611
