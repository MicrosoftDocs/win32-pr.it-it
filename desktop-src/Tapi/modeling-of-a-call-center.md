---
description: I provider di servizi possono esporre ogni risorsa nel PBX come un dispositivo a linee e possibilmente un dispositivo telefonico associato.
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: Modellazione di un Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401568"
---
# <a name="modeling-of-a-call-center"></a>Modellazione di un Call Center

I provider di servizi possono esporre ogni risorsa nel PBX come un dispositivo a linee e possibilmente un dispositivo telefonico associato. I terminali che supportano più aspetti della chiamata possono eseguire questa operazione tramite più indirizzi, esattamente come nel controllo delle chiamate del primo gruppo. Infatti, la visualizzazione di terze parti di un dispositivo è identica a quella della prima parte; le applicazioni nel server possono visualizzare e controllare tutti i dispositivi di terze parti, mentre un singolo PC client connesso al server può visualizzare solo i dispositivi resi visibili tramite i controlli di accesso gestiti da TAPISRV sul server. È anche possibile modellare risorse diverse dai terminali come dispositivi lineari. Ad esempio, una coda o un punto di route ACD verrebbe modellato come un dispositivo a linee che può avere molte chiamate attive; un server IVR, un server di posta vocale o un set di porte di composizione predittiva può essere modellato anche come un dispositivo a linee che supporta più chiamate.

All'interno di questo modello, lo stato del dispositivo e le chiamate a cui è stato eseguito il monitoraggio possono essere monitorati anche se i messaggi TAPI esistenti, ad esempio la [**riga \_ LINEDEVSTATE**](line-linedevstate.md), la [**riga \_ ADDRESSSTATE**](line-addressstate.md), la [**riga \_ CALLSTATE**](line-callstate.md)e la [**riga \_ CALLINFO**](line-callinfo.md), e i dettagli ottenuti tramite funzioni come [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)e [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo). Ogni volta che un oggetto TAPI viene gestito tramite un'applicazione di terze parti in esecuzione sul server, il risultato è identico a quello che si sarebbe verificato se lo stesso oggetto fosse stato utilizzato in modo analogo da un'applicazione di prima entità in esecuzione su un computer client associato a tale dispositivo. Le indicazioni sullo stato inviate dal provider di servizi server che controllano l'infrastruttura di commutazione (o il commutatore) vengono recapitate sia alle applicazioni in esecuzione sul server sia a quelle in esecuzione su client autorizzati associati.

 

 



