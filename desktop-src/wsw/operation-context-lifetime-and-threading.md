---
title: Durata e threading del contesto dell'operazione
description: La durata del contesto dell'operazione, rappresentata da un \_ handle di contesto dell'operazione WS \_ , determina la durata delle proprietà in esso contenute.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Durata del contesto dell'operazione e servizi Web di threading per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734879"
---
# <a name="operation-context-lifetime-and-threading"></a>Durata e threading del contesto dell'operazione

La durata del contesto dell'operazione, rappresentata da un handle di [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) , determina la durata delle proprietà in esso contenute. Un contesto deve pertanto essere utilizzato solo entro la durata dell'operazione del [servizio](service-operation.md) o il callback a cui è stato fornito. Il ciclo di vita di una chiamata sincrona è l'esecuzione della funzione stessa. Per una chiamata asincrona, la durata termina dopo il completamento della chiamata asincrona. Il modello di servizio non fornisce alcuna garanzia sul contesto dopo il completamento della chiamata. Il comportamento di basarsi sul contesto dell'operazione o su una delle relative proprietà oltre la sua durata non è definito.


Vedere anche l'esempio di calcolatore basato sulla sessione, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Modello di threading

Il contesto dell'operazione supporta il threading libero. Tuttavia, ciò è vero per il contesto dell'operazione e non per le proprietà in esso contenute.

Quando si registra un callback di annullamento per un'operazione del servizio tramite la funzione [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , si noti che la prima registrazione avrà esito positivo. l'impostazione del callback di annullamento più volte, tuttavia, avrà esito negativo.

 

 




