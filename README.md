# 📌 Resumo do Laboratório – Criando Máquinas Virtuais na Azure

Este repositório contém o resumo das lições aprendidas no laboratório **Microsoft Azure – Criando Máquinas Virtuais** da DIO.

---

## 🚀 Benefícios da Nuvem
- **Escalabilidade:** aumentar ou reduzir recursos conforme a demanda.
- **Flexibilidade:** criar e configurar VMs sob medida para diferentes necessidades.
- **Alta disponibilidade:** manter os serviços online mesmo diante de falhas.
- **Segurança:** replicação e backup para proteção contra perda de dados.

---

## 📊 SLA – Service Level Agreement (Acordo de Nível de Serviço)

O **SLA** define o percentual de disponibilidade garantida pelo provedor de nuvem.  
Um SLA mais alto significa **menor tempo de inatividade**, garantindo maior confiabilidade para serviços críticos.

| SLA      | Tempo de inatividade por semana | Tempo de inatividade por mês | Tempo de inatividade por ano |
|----------|---------------------------------|------------------------------|------------------------------|
| 99%      | 1,68 hora                       | 7,2 horas                    | 3,65 dias                    |
| 99,9%    | 10,1 minutos                    | 43,2 minutos                 | 8,76 horas                   |
| 99,95%   | 5 minutos                       | 21,6 minutos                 | 4,38 horas                   |
| 99,99%   | 1,01 minuto                     | 4,32 minutos                 | 52,56 minutos                 |
| 99,999%  | 6 segundos                      | 25,9 segundos                | 5,26 minutos                  |

💡 **Uso prático:**  
- **SLA baixo (99% a 99,9%)**: aceitável para sistemas internos ou não críticos, onde a interrupção não causa grandes prejuízos.  
- **SLA alto (99,99% ou mais)**: indicado para sistemas de missão crítica, como e-commerce, bancos, saúde e aplicações que exigem disponibilidade quase total.

---

## 🌍 Escolha de Zonas

Ao criar uma VM, é possível escolher entre:
- **Zona única:** hospedada em um único datacenter. Menor custo, mas menor resiliência.
- **Múltiplas zonas:** réplica em diferentes zonas da mesma região. Maior resiliência e disponibilidade.

---

## 📦 Estratégias de Replicação na Azure

A replicação é fundamental para garantir disponibilidade e recuperação de dados em caso de falha. A Azure oferece quatro estratégias principais:

1. **LRS – Locally Redundant Storage**  
   - Replicação local dentro de um único datacenter.  
   - Protege contra falhas de hardware no mesmo local.  
   - **Quando usar:** cenários de baixo custo e onde a perda regional não seja um risco crítico.

2. **ZRS – Zone-Redundant Storage**  
   - Replicação entre múltiplas zonas de disponibilidade na mesma região.  
   - Protege contra falhas físicas em um datacenter inteiro.  
   - **Quando usar:** aplicações que precisam de alta disponibilidade dentro da mesma região.

3. **GRS – Geo-Redundant Storage**  
   - Replicação entre regiões geográficas diferentes.  
   - Garante recuperação de desastres em nível regional.  
   - **Quando usar:** backup de dados essenciais e proteção contra falhas regionais.

4. **GZRS – Geo-Zone-Redundant Storage**  
   - Combina ZRS + GRS.  
   - Replicação entre zonas e entre regiões.  
   - **Quando usar:** serviços críticos que exigem máxima disponibilidade e resiliência contra falhas locais e regionais.

---

## 🛠 Como escolher o serviço ideal

1. **Defina a criticidade da aplicação:**  
   - Quanto mais crítico, maior deve ser o SLA e mais robusta a estratégia de replicação.

2. **Avalie o orçamento:**  
   - Soluções com alta redundância e SLA elevado custam mais.  
   - Não pague por disponibilidade que não será usada.

3. **Considere a localização dos usuários:**  
   - Múltiplas zonas e replicações geográficas podem reduzir latência e melhorar experiência.

4. **Planeje a recuperação de desastres (DRP):**  
   - Escolha entre LRS, ZRS, GRS e GZRS com base no nível de risco que você precisa mitigar.

---

✍️ **Resumo final:**  
Ao criar máquinas virtuais na Azure, entender **SLA**, **zonas** e **estratégias de replicação** é essencial para equilibrar custo, desempenho e disponibilidade. A escolha correta garante que seu serviço se mantenha estável mesmo diante de falhas e imprevistos.
