---
title: "인터넷은 어떻게 동작하는가?"
categories:
  - Network
tags:
  - Internet
  - Networking
toc: true
toc_sticky: true
toc_label: "인터넷은 어떻게 동작하는가?"
toc_icon: "internet"
---

인터넷은 전세계의 컴퓨터가 서로 연결된 네트워크로 표준화된 프로토콜(TCP/IP)을 통해 통신하는 것입니다.

- 즉, 수많은 TCP/IP 프로토콜을 사용하는 독립된 네트워크들을 하나로 연결하여 만들어진 거대한 글로벌 네트워크입니다.

## 인터넷은 어떻게 동작하는가?
인터넷은 가상의 공간이라고 생각할 수 있지만, 실제로는 다양한 종류의 와이어(광섬유, 구리, 위성 통신, 이동 통신망 등)을 통해 데이터를 전송하는 거대한 시스템입니다. 인터넷은 컴퓨터와 서버 간에 통신을 가능하게 하며, 모든 서버는 고유한 IP 주소를 가지고 있습니다. 이 IP 주소는 컴퓨터를 식별하기 위한 우편 주소와 유사한 역할을 합니다. 하지만 이러한 숫자 형식의 IP 주소는 기억하기 어려우므로, 우리는 도메인 이름(예: google.com)을 사용하여 서버를 식별합니다.

우리가 집에 있는 컴퓨터는 직접적으로 인터넷에 연결되어 있지 않습니다. 대부분의 경우, 우리는 인터넷 서비스 제공업체(ISP)를 통해 인터넷에 연결됩니다. 이런 이유로 우리 컴퓨터를 클라이언트라고 부릅니다.

데이터를 인터넷을 통해 주고받는 과정에서, 컴퓨터에서 다른 컴퓨터로 정보를 보내는 방법을 살펴봅시다. 예를 들어, 웹 페이지를 요청하거나 이메일을 보낼 때, 데이터는 작은 패킷으로 분할되어 전송됩니다. 이러한 패킷들은 인터넷을 통해 도착합니다. 이때, 패킷은 순서대로 재조립되어 우리가 볼 수 있는 형태로 표시됩니다.

패킷이 전송되는 과정에서 라우터라고 불리는 장치가 사용됩니다. 라우터는 데이터 패킷을 목적지로 안내하는 역할을 합니다. 데이터 패킷은 라우터를 통과하여 최적의 경로를 찾아 목적지에 도달합니다. 이러한 과정을 통해 인터넷을 통해 데이터가 안정적으로 전송되고 통신이 이루어집니다. 

> 참고: https://www.youtube.com/watch?v=7_LPdttKXPc 