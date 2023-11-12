---
title: "CAP 이론이란?"
categories:
  - Software Engineering
tags:
  - CAP Theorem
  - System Design
  - Distributed Systems
toc: true
toc_sticky: true
toc_label: "CAP Theorem"
toc_icon: "book"
---

## 서론
CAP 이론은 분산 시스템의 일관성(Consistency), 가용성(Availability), 파티션 허용성(Partition Tolerance) 간의 균형을 설명하는 컴퓨터 과학의 중요한 이론입니다. 이는 네트워크를 통해 연결된 여러 노드로 이루어진 분산 시스템이 어떻게 동작해야 하는지에 대한 원칙을 제시합니다.

## CAP 이론: 분산 시스템 설계의 균형과 선택

### 1. 일관성(Consistency)
- 모든 노드가 동시에 동일한 데이터에 대해 일관된 결과를 보여야 합니다.

### 2. 가용성(Availability)
- 모든 요청에 대해 항상 응답할 수 있어야 합니다.

### 3. 파티션 허용성(Partition Tolerance)
- 네트워크 분할이 발생하더라도 시스템은 계속해서 동작할 수 있어야 합니다.

CAP 이론은 이 세 가지 요소 중에서 두 가지만 선택할 수 있다는 원칙을 제시합니다. 네트워크 분할이 발생하면 한 노드에서 다른 노드로의 통신이 불가능해지기 때문에 모든 노드가 항상 동일한 데이터를 가지고 있을 수 없습니다. 이로 인해 일관성과 가용성 중 하나를 희생하고 파티션 허용성을 보장해야 합니다.

### 사례
#### 1. 금융 거래 시스템

**일관성 우선:**
- 네트워크 파티션이 발생하면 ATM 간의 통신이 불가능하므로, 은행은 일관성을 우선시하며 파티션이 해결될 때까지 입출금을 중지합니다.
- 잔액 일관성을 유지하며 고객 서비스는 이용 불가능하지만, 네트워크 복구 시에는 잔액의 마이너스 상태를 방지할 수 있습니다.

**가용성 우선:**
- 네트워크 파티션이 발생하더라도 고객은 ATM을 통해 입출금을 계속할 수 있습니다. 이는 가용성을 우선시 하는 전략입니다.
- 파티션이 해결될 때까지 잔액이 일치하지 않을 수 있으며, 고객은 두 ATM에서 잔액을 인출할 수 있습니다. 그러나 네트워크 복구 시에는 잔액의 일관성이 깨질 수 있습니다.

#### 소셜 미디어 플랫폼

**일관성 우선:**
- 두 사용자가 동일한 게시물에 동시에 댓글을 작성할 때, 파티션이 해결될 때까지 댓글이 다른 사용자에게 표시되지 않습니다.
- 이 경우 일관성을 중시하며, 사용자는 파티션이 해결될 때까지 댓글 기능을 사용할 수 없을 수 있습니다.

**가용성 우선:**
- 소셜 네트워크 플랫폼에서는 가용성을 우선시할 수 있습니다. 사용자는 댓글이 표시되지 않더라도 다른 기능을 계속 사용할 수 있습니다.
- 파티션이 해결될 때까지 사용자에게 불편함을 최소화하며, 일관성이 일시적으로 희생될 수 있습니다.

### 소프트웨어 설계에 유용한 점

#### 선택의 기준 제시
CAP 이론은 설계자에게 일관성과 가용성 중 어떤 측면을 중요시할지에 대한 고려를 강요합니다. 시스템의 목적과 요구 사항에 따라 어떤 특성을 우선시해야 하는지 결정할 수 있도록 도와줍니다.

#### 절충안 고려
CAP 이론은 설계 과정에서 높은 수준의 절충안을 고려하도록 유도합니다. 어떤 상황에서는 일관성이 더 중요하고, 다른 상황에서는 가용성이 더 중요할 수 있습니다. 이를 고려하여 시스템을 설계할 필요가 있습니다.

#### 분산 시스템 설계에 대한 이해
CAP 이론을 이해하면 분산 시스템이 어떻게 동작해야 하는지에 대한 전반적인 이해를 얻을 수 있습니다. 이는 대규모 시스템을 설계하고 관리하는 데 도움이 됩니다.

## 결론

CAP 이론은 분산 시스템 설계자에게 중요한 고려 사항을 제시하고, 어떤 상황에서든 높은 수준의 절충을 고려할 수 있도록 도와줍니다. 그러나 현실 세계에서는 더 복잡한 상황이 있기 때문에 이 이론을 단순한 가이드로만 사용하는 것이 아니라 각각의 상황에 맞게 적절히 조정하여 사용해야 합니다. 따라서 CAP 이론은 분산 시스템 설계에 있어서 네트워크 분할 시 어떻게 대응할지에 대한 출발점을 제공하지만, 항상 신중한 고려와 현실적인 접근이 필요합니다.