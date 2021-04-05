---
title: Chiusura e pulizia
description: Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulitura seguenti.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044819"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="48db3-103">Chiusura e pulizia</span><span class="sxs-lookup"><span data-stu-id="48db3-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="48db3-104">Per terminare correttamente un'applicazione, è necessario eseguire le operazioni di pulizia seguenti:</span><span class="sxs-lookup"><span data-stu-id="48db3-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="48db3-105">Rimuovere tutti gli URL registrati dal gruppo di URL chiamando la funzione [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) per annullare la registrazione degli URL registrati in precedenza nella chiamata a [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span><span class="sxs-lookup"><span data-stu-id="48db3-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="48db3-106">Chiudere il gruppo di URL chiamando la funzione [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) .</span><span class="sxs-lookup"><span data-stu-id="48db3-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="48db3-107">Tutti i gruppi di URL creati in una sessione del server devono essere chiusi prima di chiudere la sessione del server.</span><span class="sxs-lookup"><span data-stu-id="48db3-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="48db3-108">Chiudere la sessione del server chiamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span><span class="sxs-lookup"><span data-stu-id="48db3-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="48db3-109">Chiudere l'handle per la coda delle richieste chiamando [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span><span class="sxs-lookup"><span data-stu-id="48db3-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="48db3-110">Terminare le risorse create dall'API del server HTTP chiamando la funzione [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) con le impostazioni dei flag corrispondenti per ogni chiamata effettuata originariamente dall'applicazione a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="48db3-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="48db3-111">Ognuna di queste chiamate termina tutte le risorse create nella chiamata a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="48db3-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




