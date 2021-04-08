---
title: Cache in modalità kernel
description: .
ms.assetid: f9a46ff4-779b-4b3a-b8f5-1ae10a3c0a61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9264535a58c033d66fd3fcc39988a292afc2a27f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045254"
---
# <a name="kernel-mode-cache"></a><span data-ttu-id="90ee3-103">Cache in modalità kernel</span><span class="sxs-lookup"><span data-stu-id="90ee3-103">Kernel Mode Cache</span></span>

<span data-ttu-id="90ee3-104">L'API server HTTP versione 2,0 consente alle applicazioni di memorizzare nella cache le risposte con contenuto statico in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="90ee3-104">The HTTP Server version 2.0 API allows applications to cache responses with static content in kernel mode.</span></span> <span data-ttu-id="90ee3-105">Si ottengono prestazioni migliori quando le richieste vengono gestite dalla cache del kernel senza passare alla modalità utente.</span><span class="sxs-lookup"><span data-stu-id="90ee3-105">Increased performance is achieved when requests are served from the kernel cache without transitioning to user mode.</span></span>

<span data-ttu-id="90ee3-106">L'API server HTTP applica le configurazioni di proprietà appropriate a tutte le richieste gestite dalla cache del kernel, incluse le risposte di registrazione.</span><span class="sxs-lookup"><span data-stu-id="90ee3-106">The HTTP Server API applies the appropriate property configurations to all requests served from the kernel cache, including logging responses.</span></span> <span data-ttu-id="90ee3-107">Le richieste che richiedono l'autenticazione, tuttavia, non verranno gestite dalla cache.</span><span class="sxs-lookup"><span data-stu-id="90ee3-107">Requests that require authentication, however, will not be served from the cache.</span></span>

<span data-ttu-id="90ee3-108">L'API server HTTP limita la cache in modalità kernel alle richieste che soddisfano le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="90ee3-108">The HTTP Server API limits the kernel mode cache to requests that meet the following conditions:</span></span>

-   <span data-ttu-id="90ee3-109">Il verbo della richiesta è GET e viene ricevuta l'intera richiesta.</span><span class="sxs-lookup"><span data-stu-id="90ee3-109">The request verb is GET and the entire request is received.</span></span>
-   <span data-ttu-id="90ee3-110">La richiesta non deve avere un corpo entità.</span><span class="sxs-lookup"><span data-stu-id="90ee3-110">The request must not have an entity body.</span></span>
-   <span data-ttu-id="90ee3-111">Il protocollo HTTP è la versione 1,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="90ee3-111">The HTTP protocol is version 1.0 or later.</span></span>
-   <span data-ttu-id="90ee3-112">L'intestazione "translate: f" non è presente.</span><span class="sxs-lookup"><span data-stu-id="90ee3-112">The "Translate: f " header is not present.</span></span>
-   <span data-ttu-id="90ee3-113">Si prevede che le intestazioni diverse da "Expect: 100-continue" non siano presenti.</span><span class="sxs-lookup"><span data-stu-id="90ee3-113">Expect headers other than "Expect: 100-Continue" are not present.</span></span>
-   <span data-ttu-id="90ee3-114">L'intestazione dell'autorizzazione non è presente.</span><span class="sxs-lookup"><span data-stu-id="90ee3-114">The authorization header is not present.</span></span>
-   <span data-ttu-id="90ee3-115">Le intestazioni Range e If-Range non sono presenti.</span><span class="sxs-lookup"><span data-stu-id="90ee3-115">The Range and If-Range headers are not present.</span></span>

<span data-ttu-id="90ee3-116">Oltre alle limitazioni per la richiesta, la risposta deve soddisfare anche le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="90ee3-116">In addition to the restrictions on the request, the response must also meet the following conditions:</span></span>

-   <span data-ttu-id="90ee3-117">Per impostazione predefinita, le dimensioni della risposta sono limitate a 256 KB.</span><span class="sxs-lookup"><span data-stu-id="90ee3-117">Response size is limited to 256 KB, by default.</span></span> <span data-ttu-id="90ee3-118">Per modificare le dimensioni della risposta memorizzata nella cache, impostare il valore del registro di sistema **UriMaxUriBytes** sul numero di byte richiesto.</span><span class="sxs-lookup"><span data-stu-id="90ee3-118">To change the size of the response that is cached, set the **UriMaxUriBytes** registry value to the required number of bytes.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       System
          CurrentControlSet
             Services
                HTTP
                   Parameters
                      UriMaxUriBytes
    ```

-   <span data-ttu-id="90ee3-119">L'intera risposta deve essere fornita in una singola chiamata a [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span><span class="sxs-lookup"><span data-stu-id="90ee3-119">The entire response must be provided in a single call to [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse).</span></span>
-   <span data-ttu-id="90ee3-120">L'intestazione della data nella risposta non deve essere evitata.</span><span class="sxs-lookup"><span data-stu-id="90ee3-120">The date header on the response must not be suppressed.</span></span>
-   <span data-ttu-id="90ee3-121">Se è presente l'intestazione Last-modified, il valore dell'intestazione deve avere la sintassi corretta.</span><span class="sxs-lookup"><span data-stu-id="90ee3-121">If the last-modified header is present, the value of the header must have the correct syntax.</span></span> <span data-ttu-id="90ee3-122">Il valore di ora in questa intestazione viene usato per la verifica del controllo della cache.</span><span class="sxs-lookup"><span data-stu-id="90ee3-122">The time value in this header is used for cache control verification.</span></span>
-   <span data-ttu-id="90ee3-123">Lo spazio disponibile nella cache in modalità kernel è sufficiente per archiviare la risposta.</span><span class="sxs-lookup"><span data-stu-id="90ee3-123">The kernel mode cache has enough space left to store the response.</span></span>

<span data-ttu-id="90ee3-124">Per impostazione predefinita, la cache di risposta in modalità kernel è abilitata.</span><span class="sxs-lookup"><span data-stu-id="90ee3-124">By default, kernel mode response cache is enabled.</span></span> <span data-ttu-id="90ee3-125">Se una o più condizioni per la richiesta o la risposta elencate in precedenza non vengono soddisfatte, la risposta verrà inviata, ma non verrà memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="90ee3-125">If any of the conditions for the request or response listed above are not met, the response will be sent, but it will not be cached.</span></span> <span data-ttu-id="90ee3-126">Nell'API del server HTTP versione 2,0, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) include un parametro facoltativo *pCachePolicy* per passare la struttura dei [**\_ \_ criteri della cache HTTP**](/windows/desktop/api/Http/ns-http-http_cache_policy) .</span><span class="sxs-lookup"><span data-stu-id="90ee3-126">In HTTP Server version 2.0 API, [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) includes an optional *pCachePolicy* parameter to pass the [**HTTP\_CACHE\_POLICY**](/windows/desktop/api/Http/ns-http-http_cache_policy) structure.</span></span> <span data-ttu-id="90ee3-127">Per configurare la cache, le applicazioni utilizzano la struttura dei criteri di cache.</span><span class="sxs-lookup"><span data-stu-id="90ee3-127">Applications use the cache policy structure to configure the cache.</span></span>

 

 




