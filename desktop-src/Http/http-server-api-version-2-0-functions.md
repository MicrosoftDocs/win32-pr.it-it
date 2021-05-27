---
title: Funzioni dell'API server HTTP versione 2.0
description: L'API server HTTP versione 2.0 fornisce le funzioni seguenti.
ms.assetid: 12daffca-b403-4f06-8037-206f90e33252
keywords:
- Funzioni dell'API server HTTP versione 2.0
- Funzioni HTTP, API server HTTP versione 2.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e4d5c09c001caa58d43c1e61d800f66b39706b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549076"
---
# <a name="http-server-api-version-20-functions"></a><span data-ttu-id="26193-105">Funzioni dell'API server HTTP versione 2.0</span><span class="sxs-lookup"><span data-stu-id="26193-105">HTTP Server API version 2.0 functions</span></span>

<span data-ttu-id="26193-106">L'API server HTTP versione 2.0 fornisce le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="26193-106">The HTTP Server API version 2.0 provides the following functions.</span></span>

| <span data-ttu-id="26193-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="26193-107">Function</span></span> | <span data-ttu-id="26193-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26193-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="26193-109">**HttpDelegateRequestEx**</span><span class="sxs-lookup"><span data-stu-id="26193-109">**HttpDelegateRequestEx**</span></span>](/windows/win32/api/http/nf-http-httpdelegaterequestex) | <span data-ttu-id="26193-110">Delega una richiesta dalla coda di richieste di origine alla coda di richieste di destinazione.</span><span class="sxs-lookup"><span data-stu-id="26193-110">Delegates a request from the source request queue to the target request queue.</span></span> |
| [<span data-ttu-id="26193-111">**HttpFindUrlGroupId**</span><span class="sxs-lookup"><span data-stu-id="26193-111">**HttpFindUrlGroupId**</span></span>](/windows/win32/api/http/nf-http-httpfindurlgroupid) | <span data-ttu-id="26193-112">Recupera un ID gruppo DI URL per un URL e una coda di richieste.</span><span class="sxs-lookup"><span data-stu-id="26193-112">Retrieves a URL group ID for a URL and a request queue.</span></span> |
| [<span data-ttu-id="26193-113">**HttpIsFeatureSupported**</span><span class="sxs-lookup"><span data-stu-id="26193-113">**HttpIsFeatureSupported**</span></span>](/windows/win32/api/http/nf-http-httpisfeaturesupported) | <span data-ttu-id="26193-114">Verifica se una particolare funzionalità è supportata.</span><span class="sxs-lookup"><span data-stu-id="26193-114">Checks whether a particular feature is supported.</span></span> |

## <a name="server-session"></a><span data-ttu-id="26193-115">Sessione del server</span><span class="sxs-lookup"><span data-stu-id="26193-115">Server session</span></span>

| <span data-ttu-id="26193-116">Funzione</span><span class="sxs-lookup"><span data-stu-id="26193-116">Function</span></span> | <span data-ttu-id="26193-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26193-117">Description</span></span> |
|-|-|
| [<span data-ttu-id="26193-118">**HttpCloseServerSession**</span><span class="sxs-lookup"><span data-stu-id="26193-118">**HttpCloseServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseserversession) | |
| [<span data-ttu-id="26193-119">**HttpCreateServerSession**</span><span class="sxs-lookup"><span data-stu-id="26193-119">**HttpCreateServerSession**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateserversession) | |
| [<span data-ttu-id="26193-120">**HttpQueryServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-120">**HttpQueryServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty) | |
| [<span data-ttu-id="26193-121">**HttpSetServerSessionProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-121">**HttpSetServerSessionProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) | |

## <a name="url-groups"></a><span data-ttu-id="26193-122">Gruppi di URL</span><span class="sxs-lookup"><span data-stu-id="26193-122">URL Groups</span></span>

| <span data-ttu-id="26193-123">Funzione</span><span class="sxs-lookup"><span data-stu-id="26193-123">Function</span></span> | <span data-ttu-id="26193-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26193-124">Description</span></span> |
|-|-|
| [<span data-ttu-id="26193-125">**HttpAddUrlToUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="26193-125">**HttpAddUrlToUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) | |
| [<span data-ttu-id="26193-126">**HttpCreateUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="26193-126">**HttpCreateUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) | |
| [<span data-ttu-id="26193-127">**HttpCloseUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="26193-127">**HttpCloseUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) | |
| [<span data-ttu-id="26193-128">**Proprietà HttpQueryUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-128">**HttpQueryUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty) | |
| [<span data-ttu-id="26193-129">**HttpRemoveUrlFromUrlGroup**</span><span class="sxs-lookup"><span data-stu-id="26193-129">**HttpRemoveUrlFromUrlGroup**</span></span>](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) | |
| [<span data-ttu-id="26193-130">**Proprietà HttpSetUrlGroupProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-130">**HttpSetUrlGroupProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) | |

## <a name="request-queue"></a><span data-ttu-id="26193-131">Coda richiesta</span><span class="sxs-lookup"><span data-stu-id="26193-131">Request Queue</span></span>

| <span data-ttu-id="26193-132">Funzione</span><span class="sxs-lookup"><span data-stu-id="26193-132">Function</span></span> | <span data-ttu-id="26193-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26193-133">Description</span></span> |
|-|-|
| [<span data-ttu-id="26193-134">**HttpCloseRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="26193-134">**HttpCloseRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcloserequestqueue) | |
| [<span data-ttu-id="26193-135">**HttpCreateRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="26193-135">**HttpCreateRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) | |
| [<span data-ttu-id="26193-136">**HttpQueryRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-136">**HttpQueryRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) | |
| [<span data-ttu-id="26193-137">**HttpSetRequestQueueProperty**</span><span class="sxs-lookup"><span data-stu-id="26193-137">**HttpSetRequestQueueProperty**</span></span>](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) | |
| [<span data-ttu-id="26193-138">**HttpShutdownRequestQueue**</span><span class="sxs-lookup"><span data-stu-id="26193-138">**HttpShutdownRequestQueue**</span></span>](/windows/desktop/api/Http/nf-http-httpshutdownrequestqueue) | |
| [<span data-ttu-id="26193-139">**HttpWaitForDemandStart**</span><span class="sxs-lookup"><span data-stu-id="26193-139">**HttpWaitForDemandStart**</span></span>](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) | |

## <a name="related-topics"></a><span data-ttu-id="26193-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26193-140">Related topics</span></span>

[<span data-ttu-id="26193-141">Strutture dell'API server HTTP versione 2.0</span><span class="sxs-lookup"><span data-stu-id="26193-141">HTTP Server API version 2.0 structures</span></span>](http-server-api-version-2-0-structures.md)
