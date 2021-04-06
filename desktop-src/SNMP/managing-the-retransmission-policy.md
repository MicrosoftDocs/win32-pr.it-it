---
title: Gestione dei criteri di ritrasmissione
description: L'applicazione WinSNMP può richiedere che l'implementazione di Microsoft WinSNMP esegua i criteri di ritrasmissione dell'applicazione. Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045044"
---
# <a name="managing-the-retransmission-policy"></a>Gestione dei criteri di ritrasmissione

L'applicazione WinSNMP può richiedere che l'implementazione di Microsoft WinSNMP esegua i criteri di ritrasmissione dell'applicazione. Quando l'implementazione gestisce la ritrasmissione, usa il periodo di timeout e i valori del numero di tentativi nel database.

L'implementazione identifica la modalità di ritrasmissione predefinita in un valore restituito dalla funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante l'inizializzazione. La modalità può essere uno dei valori seguenti.



| Valore        | Significato                                                                      |
|--------------|------------------------------------------------------------------------------|
| SNMPAPI \_  | L'implementazione sta eseguendo i criteri di ritrasmissione dell'applicazione.     |
| SNMPAPI \_ disattivato | L'implementazione non esegue i criteri di ritrasmissione dell'applicazione. |



 

Un'applicazione WinSNMP può recuperare in qualsiasi momento la modalità di ritrasmissione corrente attiva per l'implementazione chiamando la funzione [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) . L'API WinSNMP fornisce altre [funzioni di database](winsnmp-functions.md) che semplificano la gestione dei criteri di ritrasmissione.

In qualsiasi momento durante l'esecuzione del programma, l'applicazione WinSNMP può regolare l'esecuzione dei criteri eseguendo uno dei passaggi seguenti:

-   Richiedere che l'implementazione avvii o arresti l'esecuzione dei criteri di ritrasmissione chiamando la funzione [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) . Per ulteriori informazioni, vedere [attivazione e disattivazione della ritrasmissione](turning-retransmission-on-and-off.md).
-   Modificare il periodo di timeout e i valori del numero di tentativi nel database di implementazione. Per ulteriori informazioni, vedere [modifica del criterio di ritrasmissione](changing-the-retransmission-policy.md).
-   Chiamare la funzione [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) per annullare il ciclo di ritrasmissione e rilasciare le strutture di dati interne associate a una singola richiesta di messaggio SNMP. Per ulteriori informazioni, vedere [annullamento della ritrasmissione](canceling-retransmission.md).

L'applicazione può eseguire i propri criteri di ritrasmissione. In questo caso, l'esecuzione può essere basata sui valori nel database.

 

 




