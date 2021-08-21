---
title: Panoramica della voce name service
description: La voce name service è costituita da tre sezioni distinte.
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7982cef018ec91435c647000031ae42a25e2e2bb315a20623ac75e610197e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073561"
---
# <a name="an-overview-of-the-name-service-entry"></a>Panoramica della voce name service

La voce name service è costituita da tre sezioni distinte. La prima sezione è per le interfacce (UUID + versione), la seconda sezione contiene gli UUID dell'oggetto e la terza sezione per gli handle di associazione. Specificare un nome per la voce che verrà utilizzato come modo per identificarla.

Quando si [**chiama RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta), il server specifica il nome della voce in cui inserire le informazioni esportate. Questa interfaccia appena esportata viene quindi aggiunta alla sezione interface della voce name service. Rimangono anche tutte le interfacce già presenti nella voce del servizio dei nomi. Questo stesso processo viene seguito per gli UUID degli oggetti e gli handle di associazione.

Il client chiama [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (o [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) per cercare un handle di associazione appropriato. Vengono estratti il nome della voce, l'handle di interfaccia e un UUID dell'oggetto. Limitano le voci da cui vengono restituiti gli handle di associazione. Se una voce corrisponde ai criteri di ricerca, tutti gli handle di associazione in tale voce vengono restituiti da [**RpcNsBindingImportNext.**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)

 

 




