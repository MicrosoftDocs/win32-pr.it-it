---
title: Scenario di applicazione amministrativa
description: Le applicazioni amministrative chiamano un subset di funzioni MGM correlate all'enumerazione di voci di inoltring multicast (MFE) e statistiche MFE.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c7d69b88503f7a4af18f0ab4650923a2845f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298401"
---
# <a name="administrative-application-scenario"></a>Scenario di applicazione amministrativa

Le applicazioni amministrative chiamano un subset di funzioni MGM correlate all'enumerazione di voci di inoltring multicast (MFE) e statistiche MFE. Non è necessario che un'applicazione si registri con il gestore del gruppo multicast per usare queste funzioni (ovvero, l'applicazione non necessita di un handle).

## <a name="enumerating-mfes"></a>Enumerazione di MFE

Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione tra un'applicazione amministrativa e il gestore del gruppo multicast. Nella prima colonna sono descritte le azioni eseguite dall'applicazione amministrativa e le risposte dell'applicazione amministrativa al gestore del gruppo multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast all'applicazione amministrativa. La terza colonna presenta informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.



| Azione applicazione amministrativa                                                                                                                                                                                      | Azione gestione gruppi multicast                                                                                                                                                                                                                                                              | Note                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ottenere uno o più MFE utilizzando la funzione [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) .                                                                                                                                   | Restituisce il numero di MFE appropriato per il buffer fornito dal client. Se non è possibile restituire alcun MFE nel buffer fornito, restituire \_ l'errore \_ buffer insufficiente e la dimensione del buffer necessaria per restituire un MFE.<br/>                                                              | I client possono anche recuperare le statistiche MFE usando le funzioni statistiche corrispondenti, [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) e [**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats). |
| Se \_ \_ viene ricevuto un errore di buffer insufficiente, chiamare di nuovo la funzione [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) usando un buffer delle dimensioni indicate.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Continuare a chiamare la funzione [**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) , fornendo come uno dei parametri l'ultimo MFE restituito dalla chiamata precedente alla funzione [**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) . | Restituisce il numero di MFE appropriato per il buffer fornito dal client. Se non è possibile restituire alcun MFE nel buffer fornito, restituire \_ l'errore \_ buffer insufficiente e la dimensione del buffer necessaria per un MFE.<br/> Restituisce \_ un errore \_ \_ se non restano altri elementi MFE.<br/> |                                                                                                                                                                                                 |
| Continuare l'enumerazione fino a \_ quando \_ non \_ viene ricevuto alcun altro elemento.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Usare le funzioni [**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) e [**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) per recuperare un MFE specifico o un set specifico di statistiche MFE.

 

 

 





