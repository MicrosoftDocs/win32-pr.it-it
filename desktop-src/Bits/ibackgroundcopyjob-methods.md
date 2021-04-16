---
title: Metodi metodo ibackgroundcopyjob (BITS)
description: L'interfaccia metodo ibackgroundcopyjob espone i metodi seguenti. | Metodi metodo ibackgroundcopyjob (BITS)
ms.assetid: CB1C6D64-416A-4F31-AC9D-B3C1A6818034
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a7ebeeefa90c90435f1294d78c4816cf77be3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530625"
---
# <a name="ibackgroundcopyjob-methods-bits"></a><span data-ttu-id="91fa5-104">Metodi metodo ibackgroundcopyjob (BITS)</span><span class="sxs-lookup"><span data-stu-id="91fa5-104">IBackgroundCopyJob Methods (BITS)</span></span>

<span data-ttu-id="91fa5-105">L'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91fa5-105">The [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91fa5-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="91fa5-106">In this section</span></span>

-   [<span data-ttu-id="91fa5-107">**Metodo AddFile**</span><span class="sxs-lookup"><span data-stu-id="91fa5-107">**AddFile Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfile)
-   [<span data-ttu-id="91fa5-108">**Metodo AddFileSet**</span><span class="sxs-lookup"><span data-stu-id="91fa5-108">**AddFileSet Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-addfileset)
-   [<span data-ttu-id="91fa5-109">**Metodo Cancel**</span><span class="sxs-lookup"><span data-stu-id="91fa5-109">**Cancel Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel)
-   [<span data-ttu-id="91fa5-110">**Metodo complete**</span><span class="sxs-lookup"><span data-stu-id="91fa5-110">**Complete Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete)
-   [<span data-ttu-id="91fa5-111">**Metodo EnumFiles**</span><span class="sxs-lookup"><span data-stu-id="91fa5-111">**EnumFiles Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-enumfiles)
-   [<span data-ttu-id="91fa5-112">**Metodo GetDescription**</span><span class="sxs-lookup"><span data-stu-id="91fa5-112">**GetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdescription)
-   [<span data-ttu-id="91fa5-113">**Metodo GetDisplayName**</span><span class="sxs-lookup"><span data-stu-id="91fa5-113">**GetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getdisplayname)
-   [<span data-ttu-id="91fa5-114">**Metodo GetError**</span><span class="sxs-lookup"><span data-stu-id="91fa5-114">**GetError Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterror)
-   [<span data-ttu-id="91fa5-115">**Metodo GetErrorCount**</span><span class="sxs-lookup"><span data-stu-id="91fa5-115">**GetErrorCount Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-geterrorcount)
-   [<span data-ttu-id="91fa5-116">**Metodo GetId**</span><span class="sxs-lookup"><span data-stu-id="91fa5-116">**GetId Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getid)
-   [<span data-ttu-id="91fa5-117">**Metodo GetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="91fa5-117">**GetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getminimumretrydelay)
-   [<span data-ttu-id="91fa5-118">**Metodo GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="91fa5-118">**GetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnoprogresstimeout)
-   [<span data-ttu-id="91fa5-119">**Metodo GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="91fa5-119">**GetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyflags)
-   [<span data-ttu-id="91fa5-120">**Metodo GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="91fa5-120">**GetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getnotifyinterface)
-   [<span data-ttu-id="91fa5-121">**Metodo GetOwner**</span><span class="sxs-lookup"><span data-stu-id="91fa5-121">**GetOwner Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getowner)
-   [<span data-ttu-id="91fa5-122">**Metodo GetPriority**</span><span class="sxs-lookup"><span data-stu-id="91fa5-122">**GetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getpriority)
-   [<span data-ttu-id="91fa5-123">**Metodo getProgress**</span><span class="sxs-lookup"><span data-stu-id="91fa5-123">**GetProgress Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress)
-   [<span data-ttu-id="91fa5-124">**Metodo GetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="91fa5-124">**GetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getproxysettings)
-   [<span data-ttu-id="91fa5-125">**Metodo GetState**</span><span class="sxs-lookup"><span data-stu-id="91fa5-125">**GetState Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate)
-   [<span data-ttu-id="91fa5-126">**Metodo gettimes**</span><span class="sxs-lookup"><span data-stu-id="91fa5-126">**GetTimes Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettimes)
-   [<span data-ttu-id="91fa5-127">**Metodo GetType**</span><span class="sxs-lookup"><span data-stu-id="91fa5-127">**GetType Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-gettype)
-   [<span data-ttu-id="91fa5-128">**Resume (metodo)**</span><span class="sxs-lookup"><span data-stu-id="91fa5-128">**Resume Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
-   [<span data-ttu-id="91fa5-129">**Metodo sedescription**</span><span class="sxs-lookup"><span data-stu-id="91fa5-129">**SetDescription Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdescription)
-   [<span data-ttu-id="91fa5-130">**Sedisplayname (metodo)**</span><span class="sxs-lookup"><span data-stu-id="91fa5-130">**SetDisplayName Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setdisplayname)
-   [<span data-ttu-id="91fa5-131">**Metodo SetMinimumRetryDelay**</span><span class="sxs-lookup"><span data-stu-id="91fa5-131">**SetMinimumRetryDelay Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay)
-   [<span data-ttu-id="91fa5-132">**Metodo SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="91fa5-132">**SetNoProgressTimeout Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout)
-   [<span data-ttu-id="91fa5-133">**Metodo SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="91fa5-133">**SetNotifyFlags Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)
-   [<span data-ttu-id="91fa5-134">**Metodo SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="91fa5-134">**SetNotifyInterface Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)
-   [<span data-ttu-id="91fa5-135">**Metodo SetPriority**</span><span class="sxs-lookup"><span data-stu-id="91fa5-135">**SetPriority Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setpriority)
-   [<span data-ttu-id="91fa5-136">**Metodo SetProxySettings**</span><span class="sxs-lookup"><span data-stu-id="91fa5-136">**SetProxySettings Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)
-   [<span data-ttu-id="91fa5-137">**Suspend (metodo)**</span><span class="sxs-lookup"><span data-stu-id="91fa5-137">**Suspend Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-suspend)
-   [<span data-ttu-id="91fa5-138">**Metodo TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="91fa5-138">**TakeOwnership Method**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-takeownership)

 

 




