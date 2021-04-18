---
title: Attivazione e disattivazione della ritrasmissione
description: Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla funzione SnmpSetRetransmitMode. La nuova modalità di ritrasmissione si applica alle chiamate successive alla funzione SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297943"
---
# <a name="turning-retransmission-on-and-off"></a>Attivazione e disattivazione della ritrasmissione

Un'applicazione può impostare la modalità di ritrasmissione con una chiamata alla funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . La nuova modalità di ritrasmissione si applica alle chiamate successive alla funzione [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .

Quando l'applicazione chiama **SnmpSetRetransmitMode** con il valore della modalità di ritrasmissione snmpapi \_ on, l'implementazione di Microsoft WinSNMP inizia l'esecuzione dei criteri di ritrasmissione dell'applicazione. La nuova modalità di ritrasmissione non influisce sui messaggi SNMP in attesa. Un messaggio in attesa è uno senza risposta al momento in cui l'applicazione modifica la modalità di ritrasmissione.

Quando l'applicazione WinSNMP chiama la funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) con il valore della modalità di ritrasmissione snmpapi \_ off, l'implementazione interrompe l'esecuzione dei criteri di ritrasmissione. L'implementazione Annulla i tentativi di ritrasmissione per i messaggi SNMP in attesa. Ciò è dovuto al fatto che l'implementazione di non può gestire tutte le richieste e le operazioni SNMP in attesa, oltre alle nuove richieste, prima che un contatore di timeout dell'applicazione o di ripetizione segnali un evento.

 

 




