---
title: Serializzazione dinamica del buffer
description: Quando si usa lo stile di serializzazione del buffer dinamico, il buffer di marshalling viene allocato dallo stub e i dati vengono codificati in questo buffer e passati all'utente. Quando si esegue l'unmarsshaling, si specifica il buffer che contiene i dati.
ms.assetid: d2c3805b-47bf-4bca-b904-9414e26dde68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea47a87a9d2e566dcfb033b0c9e9403ae72081afe0a1554337dbacfef9c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021681"
---
# <a name="dynamic-buffer-serialization"></a>Serializzazione dinamica del buffer

Quando si usa lo stile di serializzazione del buffer dinamico, il buffer di marshalling viene allocato dallo stub e i dati vengono codificati in questo buffer e passati all'utente. Quando si esegue l'unmarsshaling, si specifica il buffer che contiene i dati.

Lo stile del buffer dinamico della serializzazione usa le routine seguenti:

-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

La [**funzione MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) alloca la memoria necessaria per l'handle di codifica e quindi la inizializza. L'applicazione può chiamare [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) per reinizializzare l'handle. Chiama [**MesHandleFree per**](/windows/desktop/api/Midles/nf-midles-meshandlefree) liberare la memoria dell'handle. Per creare un handle di decodifica corrispondente all'handle di codifica del buffer dinamico, [**usare MesDecodeBufferHandleCreate.**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)

 

 




