---
description: Questa sezione descrive Transmission Control Protocol/Internet Protocol funzioni, strutture di dati e controlli (TCP/IP).
ms.assetid: ff92750b-453e-4328-821c-1098de8e6125
title: Allegato TCP/IP di Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a5cc403f0ff7f7e6b1daeb979ae9b7ec6ab3c3bed455843cec7ae4f43469975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822365"
---
# <a name="winsock-tcpip-annex"></a>Allegato TCP/IP di Winsock

Questa sezione descrive Transmission Control Protocol/Internet Protocol funzioni, strutture di dati e controlli (TCP/IP).



| Elemento          | Descrizione                                                                                                                                 |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Nome/i del protocollo | TCP, UDP                                                                                                                                    |
| Descrizione      | Fornisce servizi di trasporto sul livello di rete IP: UDP per datagrammi inaffidabili, TCP per flussi di byte affidabili e orientati alla connessione. |
| Famiglia di indirizzi   | **AF \_ INET**, **AF \_ INET6**                                                                                                                 |
| File di intestazione      | *Ws2tcpip.h*                                                                                                                                |



 

Sono disponibili due tipi di servizi di trasporto di base: datagrammi non affidabili (UDP) e flussi di byte orientati alla connessione affidabili (TCP). Inoltre, è facoltativamente supportato un socket non elaborato. I socket non elaborati consentono a un'applicazione di comunicare tramite protocolli diversi da TCP e UDP, ad esempio ICMP. I socket non elaborati sono supportati nelle famiglie di indirizzi **AF \_ INET** e **AF \_ INET6** con alcune limitazioni.

Questa sezione illustra le estensioni di Winsock specifiche dei protocolli TCP/IP. Descrive anche gli aspetti delle funzioni Winsock di base che richiedono una considerazione speciale o che possono presentare un comportamento univoco quando si usa TCP/IP.

 

 



