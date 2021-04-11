---
title: Contesto (servizi Web Windows)
description: Un contesto viene utilizzato nelle operazioni del servizio del modello di servizio e nei callback per passare i dati sullo stato pertinente all'operazione del servizio o al callback quando viene richiamato.
ms.assetid: 44283854-96df-4e6b-8464-3df685896f07
keywords:
- Servizi Web di contesto per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7edd1f8c93bbf4fd4b4d5feea5b2219bc522ea
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "103956089"
---
# <a name="context-windows-web-services"></a><span data-ttu-id="ca736-106">Contesto (servizi Web Windows)</span><span class="sxs-lookup"><span data-stu-id="ca736-106">Context (Windows Web Services)</span></span>

<span data-ttu-id="ca736-107">Un contesto viene utilizzato nelle operazioni del [servizio](service-operation.md) del modello di servizio e nei callback per passare i dati sullo stato pertinente all'operazione del servizio o al callback quando viene richiamato.</span><span class="sxs-lookup"><span data-stu-id="ca736-107">A context is used in Service Model [service operations](service-operation.md) and callbacks to pass relevant state data to the service operation or callback when it is invoked.</span></span> <span data-ttu-id="ca736-108">Una struttura del [ \_ \_ contesto dell'operazione WS](ws-operation-context.md) fa riferimento a un contesto.</span><span class="sxs-lookup"><span data-stu-id="ca736-108">A context is referenced by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) structure.</span></span> <span data-ttu-id="ca736-109">È possibile recuperare le proprietà di un contesto con la funzione [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) , come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="ca736-109">The properties of a context can be retrieved with the [**WsGetOperationContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty) function, as illustrated in the following code.</span></span>

``` syntax
WS_MESSAGE* requestMessage = NULL;
HRESULT hr = WsGetOperationContextProperty (
                context, 
                WS_OPERATION_CONTEXT_PROPERTY_INPUT_MESSAGE, 
                &requestMessage, 
                sizeof(requestMessage),
                error);
```

<span data-ttu-id="ca736-110">Non tutte le proprietà di contesto sono disponibili in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="ca736-110">Not all the context properties are available at any given time.</span></span> <span data-ttu-id="ca736-111">Vedere la documentazione relativa alla proprietà di contesto relativa alla disponibilità di una proprietà specifica in un'operazione di callback o di [servizio](service-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ca736-111">See the context property documentation regarding availability of a specific property in a callback or a [service operation](service-operation.md).</span></span>

<span data-ttu-id="ca736-112">Per ulteriori informazioni su come gestire la durata e il threading del contesto dell'operazione, vedere l'argomento relativo alla [durata e al threading del contesto dell'operazione](operation-context-lifetime-and-threading.md) .</span><span class="sxs-lookup"><span data-stu-id="ca736-112">For more information on how to maintain operation context lifetime and threading, see the [Operation Context Lifetime and Threading](operation-context-lifetime-and-threading.md) topic.</span></span>

<span data-ttu-id="ca736-113">L'enumerazione seguente fa parte del contesto:</span><span class="sxs-lookup"><span data-stu-id="ca736-113">The following enumeration is part of the context:</span></span>

-   [<span data-ttu-id="ca736-114">**\_ID della \_ proprietà di contesto dell'operazione WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ca736-114">**WS\_OPERATION\_CONTEXT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_operation_context_property_id)

<span data-ttu-id="ca736-115">La funzione seguente fa parte del contesto:</span><span class="sxs-lookup"><span data-stu-id="ca736-115">The following function is part of the context:</span></span>

-   [<span data-ttu-id="ca736-116">**WsGetOperationContextProperty**</span><span class="sxs-lookup"><span data-stu-id="ca736-116">**WsGetOperationContextProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetoperationcontextproperty)

<span data-ttu-id="ca736-117">Il seguente handle fa parte del contesto:</span><span class="sxs-lookup"><span data-stu-id="ca736-117">The following handle is part of the context:</span></span>

-   [<span data-ttu-id="ca736-118">\_contesto dell'operazione WS \_</span><span class="sxs-lookup"><span data-stu-id="ca736-118">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)

 

 




