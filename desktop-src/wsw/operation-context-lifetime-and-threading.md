---
title: Durata e threading del contesto dell'operazione
description: La durata del contesto dell'operazione, rappresentata da un handle WS OPERATION CONTEXT, determina la \_ durata delle proprietà in esso \_ contenute.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Durata del contesto dell'operazione e servizi Web di threading per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd2748f797e43bab750f4e02409e62e6293b39cb44d4cfd3626f86099502fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344831"
---
# <a name="operation-context-lifetime-and-threading"></a>Durata e threading del contesto dell'operazione

La durata del contesto dell'operazione, rappresentata da un handle [WS \_ OPERATION \_ CONTEXT,](ws-operation-context.md) determina la durata delle proprietà in esso contenute. Pertanto, un contesto deve essere utilizzato solo entro la durata dell'operazione [del](service-operation.md) servizio o del callback a cui il relativo oggetto è stato fornito. La durata di una chiamata sincrona è l'esecuzione della funzione stessa. Per una chiamata asincrona, la durata termina dopo il completamento della chiamata asincrona. Il modello di servizio non offre alcuna garanzia sul contesto dopo il completamento della chiamata. Il comportamento di basarsi sul contesto dell'operazione o su una delle relative proprietà oltre la sua durata non è definito.


Vedere anche l'esempio di calcolatrice basata sulla [sessione, SessionfullCalculatorServiceExample.](sessionfullcalculatorserviceexample.md)

## <a name="threading-model"></a>Modello di threading

Il contesto dell'operazione supporta il threading free, tuttavia questo vale per il contesto dell'operazione stesso e non si applica ad alcuna delle proprietà in esso contenute.

Quando si registra un callback di annullamento per un'operazione del servizio tramite la [**funzione WsRegisterOperationForCancel,**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) si noti che la prima registrazione avrà esito positivo. L'impostazione del callback di annullamento più volte, tuttavia, avrà esito negativo.

 

 




