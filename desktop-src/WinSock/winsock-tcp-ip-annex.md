---
description: In questa sezione vengono descritte le funzioni, le strutture di dati e i controlli Transmission Control Protocol/Internet Protocol (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Allegato TCP/IP Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4fd86a016ed80d9c71ac1647323508cb4dc7b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226479"
---
# <a name="winsock-tcpip-annex"></a>Allegato TCP/IP Winsock

In questa sezione vengono descritte le funzioni, le strutture di dati e i controlli Transmission Control Protocol/Internet Protocol (TCP/IP).



| Elemento          | Descrizione                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i protocollo | TCP, UDP                                                                                                                                    |
| Descrizione      | Fornisce servizi di trasporto sul livello di rete IP: UDP per datagrammi non affidabili, TCP per flussi di byte affidabili e orientati alla connessione. |
| Famiglia di indirizzi   | **AF \_ INET**, **AF \_ INET6**                                                                                                                 |
| File di intestazione      | *Ws2tcpip. h*                                                                                                                                |



 

Sono disponibili due tipi di servizi di trasporto di base: datagrammi non affidabili (UDP) e orientato alla connessione affidabile-flussi di byte (TCP). Inoltre, è facoltativamente supportato un socket non elaborato. I socket RAW consentono a un'applicazione di comunicare tramite protocolli diversi da TCP e UDP, ad esempio ICMP. I socket raw sono supportati nelle famiglie di indirizzi **AF \_ inet** e **AF \_ INET6** con alcune limitazioni.

In questa sezione vengono illustrate le estensioni di Winsock specifiche per i protocolli TCP/IP. Vengono inoltre descritti gli aspetti delle funzioni Winsock di base che richiedono una particolare attenzione o che possono presentare un comportamento univoco quando si utilizza TCP/IP.

 

 



