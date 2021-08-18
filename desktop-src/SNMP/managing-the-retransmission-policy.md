---
title: Gestione dei criteri di ritrasmissione
description: L'applicazione WinSNMP può richiedere che l'implementazione Microsoft WinSNMP esempi i criteri di ritrasmissione dell'applicazione. Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63737f8cb4a0fcdb8c6e3824d07cbc7c592c1f7e9813e8751197fcd1d64ad786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009429"
---
# <a name="managing-the-retransmission-policy"></a>Gestione dei criteri di ritrasmissione

L'applicazione WinSNMP può richiedere che l'implementazione Microsoft WinSNMP esempi i criteri di ritrasmissione dell'applicazione. Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.

L'implementazione identifica la modalità di ritrasmissione predefinita in un valore restituito dalla [**funzione SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante l'inizializzazione. La modalità può essere uno dei valori seguenti.



| Valore        | Significato                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_ ON  | L'implementazione esegue i criteri di ritrasmissione dell'applicazione.     |
| SNMPAPI \_ OFF | L'implementazione non esegue i criteri di ritrasmissione dell'applicazione. |



 

Un'applicazione WinSNMP può recuperare in qualsiasi momento la modalità di ritrasmissione corrente attiva per l'implementazione chiamando la [**funzione SnmpGetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) L'API WinSNMP fornisce altre [funzioni di database che](winsnmp-functions.md) semplificano la gestione dei criteri di ritrasmissione.

In qualsiasi momento durante l'esecuzione del programma, l'applicazione WinSNMP può modificare l'esecuzione dei criteri eseguendo uno dei passaggi seguenti:

-   Richiedere all'implementazione di avviare o arrestare l'esecuzione dei criteri di ritrasmissione chiamando la [**funzione SnmpSetRetransmitMode.**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) Per altre informazioni, vedere Attivazione e disattivazione [della ritrasmissione](turning-retransmission-on-and-off.md).
-   Modificare il periodo di timeout e i valori del numero di tentativi nel database dell'implementazione. Per altre informazioni, vedere [Modifica dei criteri di ritrasmissione](changing-the-retransmission-policy.md).
-   Chiamare la [**funzione SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) per annullare il ciclo di ritrasmissione e rilasciare strutture di dati interne associate a una singola richiesta di messaggio SNMP. Per altre informazioni, vedere [Annullamento della ritrasmissione](canceling-retransmission.md).

L'applicazione può eseguire i propri criteri di ritrasmissione. In questo caso, l'esecuzione può essere basata o meno sui valori nel database.

 

 




