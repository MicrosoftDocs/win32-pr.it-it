---
title: Serializzazione dinamica del buffer
description: Quando si utilizza lo stile del buffer dinamico di serializzazione, il buffer di marshalling viene allocato dallo stub e i dati vengono codificati in questo buffer e passati di nuovo all'utente. Quando si esegue l'unmarshalling, si fornisce il buffer che contiene i dati.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c1b97124c502e48c4d3ba18e424770bc936496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471259"
---
# <a name="dynamic-buffer-serialization"></a>Serializzazione dinamica del buffer

Quando si utilizza lo stile del buffer dinamico di serializzazione, il buffer di marshalling viene allocato dallo stub e i dati vengono codificati in questo buffer e passati di nuovo all'utente. Quando si esegue l'unmarshalling, si fornisce il buffer che contiene i dati.

Lo stile del buffer dinamico della serializzazione usa le routine seguenti:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La funzione [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) alloca la memoria necessaria per l'handle di codifica e quindi la Inizializza. L'applicazione può chiamare [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) per reinizializzare l'handle. Chiama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle. Per creare un handle di decodifica corrispondente all'handle di codifica del buffer dinamico, usare [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

 

 




