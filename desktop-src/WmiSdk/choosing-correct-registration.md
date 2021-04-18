---
description: WMI supporta diversi modelli di threading a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio la classe o la proprietà.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Scelta della registrazione corretta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313201"
---
# <a name="choosing-correct-registration"></a><span data-ttu-id="323ed-103">Scelta della registrazione corretta</span><span class="sxs-lookup"><span data-stu-id="323ed-103">Choosing Correct Registration</span></span>

<span data-ttu-id="323ed-104">WMI supporta diversi modelli di threading a seconda della modalità di hosting del provider e del tipo di funzionalità del provider, ad esempio la [classe](writing-a-class-provider.md) o la [Proprietà](writing-a-property-provider.md).</span><span class="sxs-lookup"><span data-stu-id="323ed-104">WMI supports different threading models depending on how the provider is hosted and the type of provider functionality, such as [Class](writing-a-class-provider.md) or [Property](writing-a-property-provider.md).</span></span> <span data-ttu-id="323ed-105">I [*provider disaccoppiati*](gloss-d.md) , ad esempio, non supportano tutti i tipi di funzionalità del provider.</span><span class="sxs-lookup"><span data-stu-id="323ed-105">For example, [*decoupled providers*](gloss-d.md) do not support all the types of provider functionality.</span></span> <span data-ttu-id="323ed-106">Per altre informazioni sui diversi modelli di hosting e su come configurarli, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="323ed-106">For more information about different hosting models and how to configure them, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="in-process-providers"></a><span data-ttu-id="323ed-107">Provider di In-Process</span><span class="sxs-lookup"><span data-stu-id="323ed-107">In-Process Providers</span></span>

<span data-ttu-id="323ed-108">I provider in-process vengono eseguiti in un processo host condiviso Wmiprvse.exe.</span><span class="sxs-lookup"><span data-stu-id="323ed-108">In-process providers run in a shared host process, Wmiprvse.exe.</span></span> <span data-ttu-id="323ed-109">La maggior parte dei tipi di provider in-process utilizza il modello di Apartment a thread multipli (MTA).</span><span class="sxs-lookup"><span data-stu-id="323ed-109">Most in-process provider types use the multithreaded apartment (MTA) model.</span></span>

<span data-ttu-id="323ed-110">Il modello MTA è supportato per i seguenti tipi di funzionalità del provider:</span><span class="sxs-lookup"><span data-stu-id="323ed-110">The MTA model is supported for the following types of provider functionality:</span></span>

-   [<span data-ttu-id="323ed-111">Provider di classi</span><span class="sxs-lookup"><span data-stu-id="323ed-111">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="323ed-112">Provider di istanze</span><span class="sxs-lookup"><span data-stu-id="323ed-112">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="323ed-113">Provider di metodi</span><span class="sxs-lookup"><span data-stu-id="323ed-113">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="323ed-114">Provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="323ed-114">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="323ed-115">Provider di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-115">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="323ed-116">Provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-116">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="323ed-117">Il modello di Apartment a thread singolo (STA) è supportato per alcuni tipi di funzionalità del provider:</span><span class="sxs-lookup"><span data-stu-id="323ed-117">The single-threaded apartment (STA) model is supported for some types of provider functionality:</span></span>

-   [<span data-ttu-id="323ed-118">Provider di istanze</span><span class="sxs-lookup"><span data-stu-id="323ed-118">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="323ed-119">Provider di metodi</span><span class="sxs-lookup"><span data-stu-id="323ed-119">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="323ed-120">Provider di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-120">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="323ed-121">Provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-121">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a><span data-ttu-id="323ed-122">Provider out-of-process</span><span class="sxs-lookup"><span data-stu-id="323ed-122">Out-of-Process Providers</span></span>

<span data-ttu-id="323ed-123">I provider ospitati in un altro host del servizio condiviso supportano le funzionalità del provider seguenti:</span><span class="sxs-lookup"><span data-stu-id="323ed-123">Providers that are hosted in a different shared service host support the following provider functionality:</span></span>

-   [<span data-ttu-id="323ed-124">Provider di classi</span><span class="sxs-lookup"><span data-stu-id="323ed-124">Class Provider</span></span>](writing-a-class-provider.md)
-   [<span data-ttu-id="323ed-125">Provider di istanze</span><span class="sxs-lookup"><span data-stu-id="323ed-125">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="323ed-126">Provider di metodi</span><span class="sxs-lookup"><span data-stu-id="323ed-126">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="323ed-127">Provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="323ed-127">Property Provider</span></span>](writing-a-property-provider.md)
-   [<span data-ttu-id="323ed-128">Provider di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-128">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="323ed-129">Provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-129">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

<span data-ttu-id="323ed-130">Per ulteriori informazioni sugli host dei servizi condivisi, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="323ed-130">For more information about shared service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="decoupled-providers"></a><span data-ttu-id="323ed-131">Provider disaccoppiati</span><span class="sxs-lookup"><span data-stu-id="323ed-131">Decoupled Providers</span></span>

<span data-ttu-id="323ed-132">I provider disaccoppiati sono ospitati in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="323ed-132">Decoupled providers are hosted in an application.</span></span> <span data-ttu-id="323ed-133">Per ulteriori informazioni, vedere [incorporamento di un provider in un'applicazione](incorporating-a-provider-in-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="323ed-133">For more information, see [Incorporating a Provider in an Application](incorporating-a-provider-in-an-application.md).</span></span> <span data-ttu-id="323ed-134">I provider creati utilizzando WMI nel .NET Framework sono disaccoppiati.</span><span class="sxs-lookup"><span data-stu-id="323ed-134">Providers created using WMI in the .NET Framework are decoupled.</span></span> <span data-ttu-id="323ed-135">I provider disaccoppiati supportano le funzionalità del provider seguenti:</span><span class="sxs-lookup"><span data-stu-id="323ed-135">Decoupled providers support the following provider functionality:</span></span>

-   [<span data-ttu-id="323ed-136">Provider di istanze</span><span class="sxs-lookup"><span data-stu-id="323ed-136">Instance Provider</span></span>](writing-an-instance-provider.md)
-   [<span data-ttu-id="323ed-137">Provider di metodi</span><span class="sxs-lookup"><span data-stu-id="323ed-137">Method Provider</span></span>](writing-a-method-provider.md)
-   [<span data-ttu-id="323ed-138">Provider di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-138">Event Provider</span></span>](writing-an-event-provider.md)
-   [<span data-ttu-id="323ed-139">Provider di consumer di eventi</span><span class="sxs-lookup"><span data-stu-id="323ed-139">Event Consumer Provider</span></span>](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a><span data-ttu-id="323ed-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="323ed-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="323ed-141">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="323ed-141">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="323ed-142">Hosting e sicurezza del provider</span><span class="sxs-lookup"><span data-stu-id="323ed-142">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



