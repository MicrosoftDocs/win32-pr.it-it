---
title: Panoramica dell'immissione del nome del servizio
description: La voce servizio del nome è costituita da tre sezioni distinte.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc3855f586582b013bc47b11eb058ae461014f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298941"
---
# <a name="an-overview-of-the-name-service-entry"></a>Panoramica dell'immissione del nome del servizio

La voce servizio del nome è costituita da tre sezioni distinte. La prima sezione è per le interfacce (UUID + Version), la seconda sezione contiene gli UUID degli oggetti e la terza sezione è per gli handle di associazione. Specificare un nome per la voce che fungerà da metodo per identificarlo.

Quando si chiama [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), il server specifica il nome della voce in cui inserire le informazioni esportate. Questa interfaccia appena esportata viene quindi aggiunta alla sezione Interface della voce del servizio Name. Rimangono anche tutte le interfacce già presenti nella voce servizio del nome. Questo stesso processo viene seguito per gli UUID degli oggetti e gli handle di associazione.

Il client chiama [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) per cercare un handle di binding appropriato. Vengono estratti il nome della voce, l'handle dell'interfaccia e l'UUID di un oggetto. Che limitano le voci da cui vengono restituiti gli handle di associazione. Se una voce corrisponde ai criteri di ricerca, tutti gli handle di binding in tale voce vengono restituiti da [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext).

 

 




