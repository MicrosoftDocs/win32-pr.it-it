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
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="2d0d5-106">Durata e threading del contesto dell'operazione</span><span class="sxs-lookup"><span data-stu-id="2d0d5-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="2d0d5-107">La durata del contesto dell'operazione, rappresentata da un handle di [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) , determina la durata delle proprietà in esso contenute.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="2d0d5-108">Un contesto deve pertanto essere utilizzato solo entro la durata dell'operazione del [servizio](service-operation.md) o il callback a cui è stato fornito.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="2d0d5-109">Il ciclo di vita di una chiamata sincrona è l'esecuzione della funzione stessa.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="2d0d5-110">Per una chiamata asincrona, la durata termina dopo il completamento della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="2d0d5-111">Il modello di servizio non fornisce alcuna garanzia sul contesto dopo il completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="2d0d5-112">Il comportamento di basarsi sul contesto dell'operazione o su una delle relative proprietà oltre la sua durata non è definito.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="2d0d5-113">Vedere anche l'esempio di calcolatore basato sulla sessione, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="2d0d5-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="2d0d5-114">Modello di threading</span><span class="sxs-lookup"><span data-stu-id="2d0d5-114">Threading Model</span></span>

<span data-ttu-id="2d0d5-115">Il contesto dell'operazione supporta il threading libero. Tuttavia, ciò è vero per il contesto dell'operazione e non per le proprietà in esso contenute.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="2d0d5-116">Quando si registra un callback di annullamento per un'operazione del servizio tramite la funzione [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , si noti che la prima registrazione avrà esito positivo. l'impostazione del callback di annullamento più volte, tuttavia, avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="2d0d5-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




