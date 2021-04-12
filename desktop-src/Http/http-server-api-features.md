---
title: Funzionalità dell'API del server HTTP
description: In questo argomento sono supportate e non supportate le funzionalità dell'API del server HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Funzionalità dell'API del server HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331916"
---
# <a name="http-server-api-features"></a><span data-ttu-id="b62bb-104">Funzionalità dell'API del server HTTP</span><span class="sxs-lookup"><span data-stu-id="b62bb-104">HTTP Server API Features</span></span>

<span data-ttu-id="b62bb-105">Negli elenchi seguenti vengono descritte le funzionalità supportate e non supportate dell'API del server HTTP.</span><span class="sxs-lookup"><span data-stu-id="b62bb-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="b62bb-106">Funzionalità supportate</span><span class="sxs-lookup"><span data-stu-id="b62bb-106">Features Supported</span></span>

<span data-ttu-id="b62bb-107">HTTP supporta le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="b62bb-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="b62bb-108">Funzionalità server HTTP v 1.0 e v 1.1.</span><span class="sxs-lookup"><span data-stu-id="b62bb-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="b62bb-109">Secure Sockets Layer 3,0 (SSL) con supporto per i certificati client e server.</span><span class="sxs-lookup"><span data-stu-id="b62bb-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="b62bb-110">Memorizzazione nella cache dei frammenti di dati da utilizzare nelle risposte successive.</span><span class="sxs-lookup"><span data-stu-id="b62bb-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="b62bb-111">Supporto per indirizzi IPv6 e IPv4.</span><span class="sxs-lookup"><span data-stu-id="b62bb-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="b62bb-112">Prenotazioni degli spazi dei nomi URL per la sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b62bb-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="b62bb-113">Handle true per tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b62bb-113">True handles for all objects.</span></span>
-   <span data-ttu-id="b62bb-114">Modelli I/O sincroni e asincroni.</span><span class="sxs-lookup"><span data-stu-id="b62bb-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="b62bb-115">Supporto per WOW64 in computer che eseguono Windows a 64 bit a partire da Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="b62bb-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="b62bb-116">Funzionalità non supportate</span><span class="sxs-lookup"><span data-stu-id="b62bb-116">Features Not Supported</span></span>

<span data-ttu-id="b62bb-117">L'API server HTTP non supporta le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="b62bb-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="b62bb-118">L'API server HTTP non esegue l'autenticazione client o server in base al contenuto delle intestazioni della richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="b62bb-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="b62bb-119">Qualsiasi autenticazione necessaria deve essere implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b62bb-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="b62bb-120">WOW64 nei computer che eseguono Windows a 64 bit non è supportato in Windows Server 2003 e Windows XP con Service Pack 2 (SP2) e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b62bb-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="b62bb-121">L'API server HTTP non supporta la registrazione di richieste e risposte HTTP.</span><span class="sxs-lookup"><span data-stu-id="b62bb-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="b62bb-122">L'API server HTTP non suddivide le risposte HTTP in uscita.</span><span class="sxs-lookup"><span data-stu-id="b62bb-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="b62bb-123">Se necessario, l'applicazione deve implementare la suddivisione in blocchi della risposta.</span><span class="sxs-lookup"><span data-stu-id="b62bb-123">The application must implement response chunking if required.</span></span>

 

 




