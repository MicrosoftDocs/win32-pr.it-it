---
title: Scenario di applicazione amministrativa
description: Le applicazioni amministrative chiamano un subset di funzioni MGM correlate all'enumerazione delle voci di inoltro multicast (MFE) e delle statistiche MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791916"
---
# <a name="administrative-application-scenario"></a>Scenario di applicazione amministrativa

Le applicazioni amministrative chiamano un subset di funzioni MGM correlate all'enumerazione delle voci di inoltro multicast (MFE) e delle statistiche MFE. Un'applicazione non deve eseguire la registrazione con il gestore di gruppi multicast per usare queste funzioni, ovvero l'applicazione non richiede un handle.

## <a name="enumerating-mfes"></a>Enumerazione di MFE

La tabella seguente riepiloga una serie di passaggi in un'interazione tra un'applicazione amministrativa e il gestore di gruppi multicast. La prima colonna descrive le azioni eseguite dall'applicazione amministrativa e le risposte dell'applicazione amministrativa al gestore di gruppi multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast all'applicazione amministrativa. La terza colonna presenta eventuali informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.



| Azione dell'applicazione amministrativa                                                                                                                                                                                      | Azione di gestione del gruppo multicast                                                                                                                                                                                                                                                              | Note                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ottenere uno o più MFE usando la [**funzione MgmGetFirstMfe.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)                                                                                                                                   | Restituisce tutti gli MFE che rientrano nel buffer fornito dal client. Se non è possibile restituire alcun MFE nel buffer fornito, restituire ERROR INSUFFICIENT BUFFER e le dimensioni del buffer necessarie per restituire \_ \_ un MFE.<br/>                                                              | I client possono anche recuperare le statistiche MFE usando le funzioni statistiche [**corrispondenti, MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) e [**MgmGetNextMfeStats.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats) |
| Se viene ricevuto l'errore ERROR INSUFFICIENT BUFFER, chiamare di nuovo la funzione \_ \_ [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) usando un buffer delle dimensioni indicate.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Continuare a chiamare la funzione [**MgmGetNextMfe,**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) fornendo come uno dei parametri l'ultima funzione MFE restituita dalla chiamata precedente alla [**funzione MgmGetFirstMfe.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) | Restituisce tutti gli MFE che rientrano nel buffer fornito dal client. Se non è possibile restituire alcun MFE nel buffer fornito, restituisce ERROR INSUFFICIENT BUFFER e la dimensione del buffer necessaria per \_ \_ un MFE.<br/> Restituisce ERROR \_ NO MORE ITEMS quando non rimangono altri \_ \_ MFE.<br/> |                                                                                                                                                                                                 |
| Continuare l'enumerazione fino a quando \_ non viene ricevuto ERROR NO MORE \_ \_ ITEMS.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Usare le [**funzioni MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) e [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) per recuperare un MFE specifico o un set specifico di statistiche MFE.

 

 

 





