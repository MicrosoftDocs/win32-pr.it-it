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
# <a name="dynamic-buffer-serialization"></a><span data-ttu-id="802e1-104">Serializzazione dinamica del buffer</span><span class="sxs-lookup"><span data-stu-id="802e1-104">Dynamic Buffer Serialization</span></span>

<span data-ttu-id="802e1-105">Quando si utilizza lo stile del buffer dinamico di serializzazione, il buffer di marshalling viene allocato dallo stub e i dati vengono codificati in questo buffer e passati di nuovo all'utente.</span><span class="sxs-lookup"><span data-stu-id="802e1-105">When using the dynamic buffer style of serialization, the marshalling buffer is allocated by the stub, and the data is encoded into this buffer and passed back to you.</span></span> <span data-ttu-id="802e1-106">Quando si esegue l'unmarshalling, si fornisce il buffer che contiene i dati.</span><span class="sxs-lookup"><span data-stu-id="802e1-106">When unmarshaling, you supply the buffer that contains the data.</span></span>

<span data-ttu-id="802e1-107">Lo stile del buffer dinamico della serializzazione usa le routine seguenti:</span><span class="sxs-lookup"><span data-stu-id="802e1-107">The dynamic buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="802e1-108">**MesEncodeDynBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="802e1-108">**MesEncodeDynBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [<span data-ttu-id="802e1-109">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="802e1-109">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="802e1-110">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="802e1-110">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="802e1-111">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="802e1-111">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="802e1-112">La funzione [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) alloca la memoria necessaria per l'handle di codifica e quindi la Inizializza.</span><span class="sxs-lookup"><span data-stu-id="802e1-112">The [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate) function allocates the memory needed for the encoding handle and then initializes it.</span></span> <span data-ttu-id="802e1-113">L'applicazione può chiamare [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) per reinizializzare l'handle.</span><span class="sxs-lookup"><span data-stu-id="802e1-113">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle.</span></span> <span data-ttu-id="802e1-114">Chiama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) per liberare la memoria dell'handle.</span><span class="sxs-lookup"><span data-stu-id="802e1-114">It calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="802e1-115">Per creare un handle di decodifica corrispondente all'handle di codifica del buffer dinamico, usare [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="802e1-115">To create a decoding handle corresponding to the dynamic buffer encoding handle, use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

 

 




