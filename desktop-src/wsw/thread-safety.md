---
title: Thread safety
description: Tutte le funzioni in questa API sono sicure da chiamare simultaneamente da thread diversi. Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Servizi Web di thread safety per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734850"
---
# <a name="thread-safety"></a><span data-ttu-id="5c4bf-107">Thread safety</span><span class="sxs-lookup"><span data-stu-id="5c4bf-107">Thread Safety</span></span>

<span data-ttu-id="5c4bf-108">Tutte le funzioni in questa API sono sicure da chiamare simultaneamente da thread diversi.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="5c4bf-109">Tuttavia, ogni oggetto passato come parametro alle funzioni ha un comportamento di threading specifico, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="5c4bf-110">Gli handle seguenti sono a thread singolo e non supportano operazioni simultanee per una particolare istanza:</span><span class="sxs-lookup"><span data-stu-id="5c4bf-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="5c4bf-111">\_heap WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="5c4bf-112">\_messaggio WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="5c4bf-113">\_buffer WS XML \_</span><span class="sxs-lookup"><span data-stu-id="5c4bf-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="5c4bf-114">\_lettore XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="5c4bf-115">\_writer XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="5c4bf-116">\_errore WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="5c4bf-117">\_contesto dell'operazione WS \_</span><span class="sxs-lookup"><span data-stu-id="5c4bf-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="5c4bf-118">\_criteri WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="5c4bf-119">\_metadati WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="5c4bf-120">\_token di sicurezza WS \_</span><span class="sxs-lookup"><span data-stu-id="5c4bf-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="5c4bf-121">\_contesto di sicurezza WS \_</span><span class="sxs-lookup"><span data-stu-id="5c4bf-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="5c4bf-122">Gli handle seguenti sono a thread libero e supportano operazioni simultanee per una particolare istanza:</span><span class="sxs-lookup"><span data-stu-id="5c4bf-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="5c4bf-123">\_canale WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="5c4bf-124">\_listener WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="5c4bf-125">\_host del servizio WS \_</span><span class="sxs-lookup"><span data-stu-id="5c4bf-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="5c4bf-126">\_proxy servizio \_ WS</span><span class="sxs-lookup"><span data-stu-id="5c4bf-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="5c4bf-127">Per tutti questi handle, il Threading viene definito in termini di operazioni (non chiamate di funzione).</span><span class="sxs-lookup"><span data-stu-id="5c4bf-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="5c4bf-128">Un'operazione è definita diversamente per le funzioni richiamate in modo sincrono rispetto alle funzioni richiamate in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5c4bf-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="5c4bf-129">Per le funzioni richiamate in modo sincrono, l'operazione è in sospeso durante l'esecuzione della funzione.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="5c4bf-130">Per le funzioni richiamate in modo asincrono, se la funzione restituisce un codice restituito diverso da **WS \_ S \_ Async** , l'operazione è in sospeso durante l'esecuzione della funzione.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="5c4bf-131">Se la funzione restituisce **WS \_ S \_ Async** , tuttavia, l'operazione è in sospeso fino a quando non viene richiamato il [**\_ \_ callback di WS asincrono**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="5c4bf-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="5c4bf-132">Per ulteriori informazioni sulla chiamata di funzioni in modo asincrono, vedere l'argomento relativo al [modello asincrono](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="5c4bf-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="5c4bf-133">Per i codici di errore, vedere [valori restituiti dei servizi Web Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5c4bf-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="5c4bf-134">Il mancato completamento del contratto di threading per un oggetto comporterà un comportamento indefinito.</span><span class="sxs-lookup"><span data-stu-id="5c4bf-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




