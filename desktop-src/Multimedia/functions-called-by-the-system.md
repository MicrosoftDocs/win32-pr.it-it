---
title: Funzioni chiamate dal sistema
description: Funzioni chiamate dal sistema
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- audio multimediale, funzioni ACM
- audio, funzioni ACM
- Gestione compressione audio (ACM), funzioni
- ACM (Gestione compressione audio), funzioni
- Funzioni ACM
- funzioni callback
- Gestione compressione audio (ACM), funzioni di callback
- ACM (Gestione compressione audio), funzioni di callback
- procedure Hook
- procedure per i driver
- Gestione compressione audio (ACM), procedure Hook
- ACM (Gestione compressione audio), procedure Hook
- Gestione compressione audio (ACM), procedure per i driver
- ACM (Gestione compressione audio), procedure per i driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299677"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="30e20-117">Funzioni chiamate dal sistema</span><span class="sxs-lookup"><span data-stu-id="30e20-117">Functions Called by the System</span></span>

<span data-ttu-id="30e20-118">Il sistema chiama tre tipi diversi di funzioni definite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="30e20-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="30e20-119">Le funzioni di callback sono funzioni nell'applicazione chiamate dal sistema in risposta a una richiesta effettuata da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="30e20-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="30e20-120">Le procedure Hook consentono a un'applicazione di gestire la personalizzazione delle finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="30e20-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="30e20-121">Una procedura di driver è l'implementazione del proprio codec, convertitore o filtro di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="30e20-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="30e20-122">Le funzioni di callback hanno i nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="30e20-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="30e20-123">**acmDriverEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="30e20-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="30e20-124">**acmFilterEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="30e20-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="30e20-125">**acmFilterTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="30e20-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="30e20-126">**acmFormatEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="30e20-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="30e20-127">**acmFormatTagEnumCallback**</span><span class="sxs-lookup"><span data-stu-id="30e20-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="30e20-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="30e20-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="30e20-129">La maggior parte delle funzioni di enumerazione in ACM utilizza funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="30e20-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="30e20-130">Ad esempio, quando si chiama una funzione di enumerazione, l'ACM enumera gli elementi chiamando ripetutamente l'applicazione tramite la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="30e20-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="30e20-131">Alcune funzioni non possono essere chiamate dall'interno di queste funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="30e20-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="30e20-132">Le funzioni che non possono essere chiamate modificano le strutture ACM interne utilizzate dalle funzioni di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="30e20-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="30e20-133">Le funzioni seguenti non devono essere chiamate dall'interno di una funzione di callback:</span><span class="sxs-lookup"><span data-stu-id="30e20-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="30e20-134">**acmDriverAdd**</span><span class="sxs-lookup"><span data-stu-id="30e20-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="30e20-135">**acmDriverPriority**</span><span class="sxs-lookup"><span data-stu-id="30e20-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="30e20-136">**acmDriverRemove**</span><span class="sxs-lookup"><span data-stu-id="30e20-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="30e20-137">Il sistema chiama le funzioni seguenti per consentire a un'applicazione di gestire la personalizzazione delle finestre di dialogo:</span><span class="sxs-lookup"><span data-stu-id="30e20-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="30e20-138">**acmFilterChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="30e20-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="30e20-139">**acmFormatChooseHookProc**</span><span class="sxs-lookup"><span data-stu-id="30e20-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="30e20-140">La funzione seguente viene specificata come prototipo che consente a un'applicazione di utilizzare un codec, un convertitore o un filtro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="30e20-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="30e20-141">Una funzione conforme a questo prototipo può essere passata come argomento alla funzione [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="30e20-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="30e20-142">**acmDriverProc**</span><span class="sxs-lookup"><span data-stu-id="30e20-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 