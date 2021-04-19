---
description: Questo documento descrive la progettazione e l'uso delle classi di base MSP. L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori troverà l'attività di creazione di un MSP basato su DirectShow per TAPI 3 New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classi base MSP di TAPI 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317644"
---
# <a name="tapi-3-msp-base-classes"></a><span data-ttu-id="d504e-104">Classi base MSP di TAPI 3</span><span class="sxs-lookup"><span data-stu-id="d504e-104">TAPI 3 MSP Base Classes</span></span>

<span data-ttu-id="d504e-105">Questo documento descrive la progettazione e l'uso delle classi di base MSP.</span><span class="sxs-lookup"><span data-stu-id="d504e-105">This document describes the design and use of the MSP Base Classes.</span></span> <span data-ttu-id="d504e-106">L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori troverà l'attività di creazione di un MSP basato su DirectShow per la nuova MSPI di TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="d504e-106">Use of these classes is not required, but most developers will find they simplify the task of building a DirectShow-based MSP for TAPI 3's new MSPI.</span></span>

<span data-ttu-id="d504e-107">Il codice sorgente per le classi base MSP si trova nella directory Samples di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d504e-107">Source code for the MSP base classes can be found in the Samples directory of the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="d504e-108">Si presuppone una certa familiarità con COM, ATL, DirectShow e C++.</span><span class="sxs-lookup"><span data-stu-id="d504e-108">Familiarity with COM, ATL, DirectShow, and C++ is assumed.</span></span> <span data-ttu-id="d504e-109">Il lettore deve inoltre conoscere il materiale generale in [informazioni sul provider di servizi multimediali (msp)](about-the-media-service-provider-msp-.md) e in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span><span class="sxs-lookup"><span data-stu-id="d504e-109">The reader must also know the general material in [About the Media Service Provider (MSP)](about-the-media-service-provider-msp-.md) and in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).</span></span>

<span data-ttu-id="d504e-110">Per Windows 2000 è necessario ATL 2,1.</span><span class="sxs-lookup"><span data-stu-id="d504e-110">ATL 2.1 is required for Windows 2000.</span></span> <span data-ttu-id="d504e-111">A partire da Windows XP, vengono compilati sia ATL 2,1 che 3,0.</span><span class="sxs-lookup"><span data-stu-id="d504e-111">Starting with Windows XP, both ATL 2.1 and 3.0 will compile.</span></span>

<span data-ttu-id="d504e-112">Librerie di classi base MSP (disponibili nell'SDK):</span><span class="sxs-lookup"><span data-stu-id="d504e-112">MSP Base Class Libraries (available in the SDK):</span></span>

-   <span data-ttu-id="d504e-113">Mspbase. lib</span><span class="sxs-lookup"><span data-stu-id="d504e-113">Mspbase.lib</span></span>
-   <span data-ttu-id="d504e-114">Mspid. lib</span><span class="sxs-lookup"><span data-stu-id="d504e-114">Mspid.lib</span></span>
-   <span data-ttu-id="d504e-115">Strmbase. lib</span><span class="sxs-lookup"><span data-stu-id="d504e-115">Strmbase.lib</span></span>
-   <span data-ttu-id="d504e-116">Tmuid. lib</span><span class="sxs-lookup"><span data-stu-id="d504e-116">Tmuid.lib</span></span>
    > [!Note]  
    > <span data-ttu-id="d504e-117">È necessario utilizzare il collegamento dinamico anziché quello statico.</span><span class="sxs-lookup"><span data-stu-id="d504e-117">Dynamic rather than static linking should be used.</span></span>

     

<span data-ttu-id="d504e-118">File di intestazione della classe di base MSP (disponibili nell'SDK):</span><span class="sxs-lookup"><span data-stu-id="d504e-118">MSP Base Class Header Files (available in the SDK):</span></span>

-   <span data-ttu-id="d504e-119">Mspaddr. h</span><span class="sxs-lookup"><span data-stu-id="d504e-119">Mspaddr.h</span></span>
-   <span data-ttu-id="d504e-120">Mspbase. h</span><span class="sxs-lookup"><span data-stu-id="d504e-120">Mspbase.h</span></span>
-   <span data-ttu-id="d504e-121">Mspcall. h</span><span class="sxs-lookup"><span data-stu-id="d504e-121">Mspcall.h</span></span>
-   <span data-ttu-id="d504e-122">Msplog. h</span><span class="sxs-lookup"><span data-stu-id="d504e-122">Msplog.h</span></span>
-   <span data-ttu-id="d504e-123">Mspstrm. h</span><span class="sxs-lookup"><span data-stu-id="d504e-123">Mspstrm.h</span></span>
-   <span data-ttu-id="d504e-124">Mspterm. h</span><span class="sxs-lookup"><span data-stu-id="d504e-124">Mspterm.h</span></span>
-   <span data-ttu-id="d504e-125">Mspthrd. h</span><span class="sxs-lookup"><span data-stu-id="d504e-125">Mspthrd.h</span></span>
-   <span data-ttu-id="d504e-126">Msptmac. h</span><span class="sxs-lookup"><span data-stu-id="d504e-126">Msptmac.h</span></span>
-   <span data-ttu-id="d504e-127">Msptmvc. h</span><span class="sxs-lookup"><span data-stu-id="d504e-127">Msptmvc.h</span></span>
-   <span data-ttu-id="d504e-128">Msptrmvc. h</span><span class="sxs-lookup"><span data-stu-id="d504e-128">Msptrmvc.h</span></span>
-   <span data-ttu-id="d504e-129">Msptrmac. h</span><span class="sxs-lookup"><span data-stu-id="d504e-129">Msptrmac.h</span></span>
-   <span data-ttu-id="d504e-130">Msptrmar. h</span><span class="sxs-lookup"><span data-stu-id="d504e-130">Msptrmar.h</span></span>
-   <span data-ttu-id="d504e-131">Msputils. h</span><span class="sxs-lookup"><span data-stu-id="d504e-131">Msputils.h</span></span>

<span data-ttu-id="d504e-132">File di origine della classe di base MSP (disponibili negli esempi di SDK):</span><span class="sxs-lookup"><span data-stu-id="d504e-132">MSP Base Class Source Files (available in the SDK Samples):</span></span>

-   <span data-ttu-id="d504e-133">Mspaddr. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-133">Mspaddr.cpp</span></span>
-   <span data-ttu-id="d504e-134">Mspcall. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-134">Mspcall.cpp</span></span>
-   <span data-ttu-id="d504e-135">Msplog. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-135">Msplog.cpp</span></span>
-   <span data-ttu-id="d504e-136">Mspstrm. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-136">Mspstrm.cpp</span></span>
-   <span data-ttu-id="d504e-137">Mspterm. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-137">Mspterm.cpp</span></span>
-   <span data-ttu-id="d504e-138">Mspthrd. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-138">Mspthrd.cpp</span></span>
-   <span data-ttu-id="d504e-139">Msptrmac. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-139">Msptrmac.cpp</span></span>
-   <span data-ttu-id="d504e-140">Msptrmar. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-140">Msptrmar.cpp</span></span>
-   <span data-ttu-id="d504e-141">Msptrmvc. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-141">Msptrmvc.cpp</span></span>
-   <span data-ttu-id="d504e-142">Msputils. cpp</span><span class="sxs-lookup"><span data-stu-id="d504e-142">Msputils.cpp</span></span>

 

 



