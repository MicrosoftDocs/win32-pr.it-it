---
title: Attivazione e disattivazione della ritrasmissione
description: Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla funzione SnmpSetRetransmitMode. La nuova modalità di ritrasmissione si applica alle chiamate successive alla funzione SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc7624977b4959911cc4128c9a75ac70fac7031bfb853c4b31db34d0987b4d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885671"
---
# <a name="turning-retransmission-on-and-off"></a>Attivazione e disattivazione della ritrasmissione

Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla [**funzione SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) La nuova modalità di ritrasmissione si applica alle chiamate successive alla [**funzione SnmpSendMsg.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)

Quando l'applicazione chiama **SnmpSetRetransmitMode** con il valore della modalità di ritrasmissione SNMPAPI \_ ON, l'implementazione Di Microsoft WinSNMP avvia l'esecuzione dei criteri di ritrasmissione dell'applicazione. La nuova modalità di ritrasmissione non influisce sui messaggi SNMP in sospeso. Un messaggio in attesa è un messaggio che non ha risposta nel momento in cui l'applicazione modifica la modalità di ritrasmissione.

Quando l'applicazione WinSNMP chiama la [**funzione SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con il valore della modalità di ritrasmissione SNMPAPI OFF, l'implementazione interrompe l'esecuzione dei criteri di \_ ritrasmissione. L'implementazione annulla i tentativi di ritrasmissione per i messaggi SNMP in sospeso. Ciò è dovuto al fatto che l'implementazione potrebbe non essere in grado di gestire tutte le richieste e le operazioni SNMP in sospeso più le nuove richieste, prima che un timeout dell'applicazione o un contatore dei tentativi segnali un evento.

 

 




