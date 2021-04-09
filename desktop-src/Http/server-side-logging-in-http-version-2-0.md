---
title: Registrazione Server-Side
description: La registrazione lato server è disponibile in un gruppo di URL o in una sessione del server.
ms.assetid: e1fcd87f-382a-42bf-b53f-1e1cb1dbbfc5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b76548b296bcdbd343e4e259e0cf3c87537ef5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856493"
---
# <a name="server-side-logging"></a><span data-ttu-id="bf387-103">Registrazione Server-Side</span><span class="sxs-lookup"><span data-stu-id="bf387-103">Server-Side Logging</span></span>

<span data-ttu-id="bf387-104">La registrazione lato server è disponibile in un gruppo di URL o in una sessione del server.</span><span class="sxs-lookup"><span data-stu-id="bf387-104">Server-side logging is available on a URL group or server session.</span></span> <span data-ttu-id="bf387-105">Quando la registrazione è abilitata in una sessione del server, funziona come forma centralizzata di registrazione per tutti i gruppi di URL nella sessione del server.</span><span class="sxs-lookup"><span data-stu-id="bf387-105">When logging is enabled on a server session, it functions as centralized form of logging for all the URL groups under the server session.</span></span> <span data-ttu-id="bf387-106">Quando la registrazione è abilitata in un gruppo di URL, la registrazione viene eseguita solo sulle richieste indirizzate al gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="bf387-106">When logging is enabled on a URL group, logging is performed only on requests that are routed to the URL Group.</span></span> <span data-ttu-id="bf387-107">L'API server HTTP supporta i tipi di registrazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf387-107">The following types of logging are supported by the HTTP Server API:</span></span>

-   <span data-ttu-id="bf387-108">[Registrazione W3C](w3c-logging.md): disponibile nel gruppo URL e sessione del server.</span><span class="sxs-lookup"><span data-stu-id="bf387-108">[W3C logging](w3c-logging.md): Available on the server session and URL group.</span></span>
-   <span data-ttu-id="bf387-109">[Registrazione NCSA](ncsa-logging.md): disponibile nel gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="bf387-109">[NCSA logging](ncsa-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="bf387-110">[Registrazione IIS](iis-logging.md): disponibile nel gruppo URL.</span><span class="sxs-lookup"><span data-stu-id="bf387-110">[IIS logging](iis-logging.md): Available on the URL group.</span></span>
-   <span data-ttu-id="bf387-111">[Registrazione binaria centralizzata](centralized-binary-logging.md): disponibile nella sessione del server.</span><span class="sxs-lookup"><span data-stu-id="bf387-111">[Centralized binary logging](centralized-binary-logging.md): Available on the server session.</span></span>

<span data-ttu-id="bf387-112">Per sfruttare i vantaggi della funzionalità di registrazione HTTP, l'applicazione consente di abilitare e configurare un tipo di registrazione nella sessione del server o nel gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="bf387-112">To take advantage of the HTTP logging feature, the application enables and configures one type of logging on the server session or URL group.</span></span> <span data-ttu-id="bf387-113">Per ulteriori informazioni, vedere [configurazione e abilitazione della registrazione lato server](configuring-and-enabling-server-side-logging.md)</span><span class="sxs-lookup"><span data-stu-id="bf387-113">For more information, see [Configuring and Enabling Server Side Logging](configuring-and-enabling-server-side-logging.md)</span></span>

 

 




