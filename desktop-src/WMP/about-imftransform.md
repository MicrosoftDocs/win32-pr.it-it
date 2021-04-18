---
title: Informazioni su IMFTransform
description: Informazioni su IMFTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
- Plug-in di Windows Media Player, interfaccia IMFTransform
- plug-in, interfaccia IMFTransform
- plug-in per l'elaborazione di segnali digitali, interfaccia IMFTransform
- Plug-in DSP, interfaccia IMFTransform
- Interfaccia IMFTransform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297797"
---
# <a name="about-imftransform"></a><span data-ttu-id="533a0-113">Informazioni su IMFTransform</span><span class="sxs-lookup"><span data-stu-id="533a0-113">About IMFTransform</span></span>

<span data-ttu-id="533a0-114">L'interfaccia **IMFTransform** è una delle interfacce che devono essere implementate da un plug-in DSP a doppia modalità.</span><span class="sxs-lookup"><span data-stu-id="533a0-114">The **IMFTransform** interface is one of the interfaces that must be implemented by a dual-mode DSP plug-in.</span></span> <span data-ttu-id="533a0-115">Windows Media Player chiama i metodi dell'interfaccia **IMFTransform** per fornire i dati al plug-in e recuperare i dati elaborati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="533a0-115">Windows Media Player calls the methods of the **IMFTransform** interface to provide data to the plug-in and to retrieve processed data back from the plug-in.</span></span> <span data-ttu-id="533a0-116">Per la documentazione completa dell'interfaccia **IMFTransform** , vedere la sezione Media Foundation della Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="533a0-116">For complete documentation of the **IMFTransform** interface, see the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="533a0-117">I metodi di **IMFTransform** possono essere categorizzati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="533a0-117">The methods of **IMFTransform** can be categorized as follows.</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="533a0-118">Metodi che gestiscono la negoziazione del formato</span><span class="sxs-lookup"><span data-stu-id="533a0-118">Methods That Handle Format Negotiation</span></span>

<span data-ttu-id="533a0-119">Windows Media Player chiama i metodi seguenti per ottenere informazioni sui formati di dati supportati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="533a0-119">Windows Media Player calls the following methods to get information about the data formats supported by the plug-in.</span></span>

-   <span data-ttu-id="533a0-120">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="533a0-120">**GetStreamCount**</span></span>
-   <span data-ttu-id="533a0-121">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="533a0-121">**GetStreamLimits**</span></span>
-   <span data-ttu-id="533a0-122">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="533a0-122">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="533a0-123">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="533a0-123">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="533a0-124">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="533a0-124">**GetInputAvailableType**</span></span>
-   <span data-ttu-id="533a0-125">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="533a0-125">**GetOutputAvailableType**</span></span>
-   <span data-ttu-id="533a0-126">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="533a0-126">**SetInputType**</span></span>
-   <span data-ttu-id="533a0-127">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="533a0-127">**SetOutputType**</span></span>
-   <span data-ttu-id="533a0-128">**GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="533a0-128">**GetAttributes**</span></span>
-   <span data-ttu-id="533a0-129">**GetInputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="533a0-129">**GetInputStreamAttributes**</span></span>
-   <span data-ttu-id="533a0-130">**GetOutputStreamAttributes**</span><span class="sxs-lookup"><span data-stu-id="533a0-130">**GetOutputStreamAttributes**</span></span>
-   <span data-ttu-id="533a0-131">**GetStreamIDs**</span><span class="sxs-lookup"><span data-stu-id="533a0-131">**GetStreamIDs**</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="533a0-132">Metodi che specificano o recuperano informazioni sullo stato</span><span class="sxs-lookup"><span data-stu-id="533a0-132">Methods That Specify or Retrieve State Information</span></span>

<span data-ttu-id="533a0-133">Windows Media Player chiama i metodi seguenti per ottenere o impostare i valori correlati allo stato corrente del plug-in.</span><span class="sxs-lookup"><span data-stu-id="533a0-133">Windows Media Player calls the following methods to get or set values related to the current state of the plug-in.</span></span>

-   <span data-ttu-id="533a0-134">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="533a0-134">**SetInputType**</span></span>
-   <span data-ttu-id="533a0-135">**SetOutputType**</span><span class="sxs-lookup"><span data-stu-id="533a0-135">**SetOutputType**</span></span>
-   <span data-ttu-id="533a0-136">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="533a0-136">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="533a0-137">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="533a0-137">**GetOutputCurrentType**</span></span>
-   <span data-ttu-id="533a0-138">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="533a0-138">**GetInputStatus**</span></span>
-   <span data-ttu-id="533a0-139">**AddInputStreams**</span><span class="sxs-lookup"><span data-stu-id="533a0-139">**AddInputStreams**</span></span>
-   <span data-ttu-id="533a0-140">**DeleteInputStreams**</span><span class="sxs-lookup"><span data-stu-id="533a0-140">**DeleteInputStreams**</span></span>
-   <span data-ttu-id="533a0-141">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="533a0-141">**GetOutputStatus**</span></span>
-   <span data-ttu-id="533a0-142">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="533a0-142">**SetOutputBounds**</span></span>

> [!Note]  
> <span data-ttu-id="533a0-143">**SetInputType** e **SetOutputType** vengono usati sia per la negoziazione del formato sia per la specifica e il recupero delle informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="533a0-143">**SetInputType** and **SetOutputType** are used both for format negotiation and for specifying and retrieving state information.</span></span>

 

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="533a0-144">Metodi che gestiscono il buffering e l'elaborazione dei dati</span><span class="sxs-lookup"><span data-stu-id="533a0-144">Methods That Handle Buffering and Processing Data</span></span>

<span data-ttu-id="533a0-145">Windows Media Player chiama i metodi seguenti per avviare i vari processi eseguiti dal plug-in per eseguire l'elaborazione del segnale digitale.</span><span class="sxs-lookup"><span data-stu-id="533a0-145">Windows Media Player calls the following methods to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span>

-   <span data-ttu-id="533a0-146">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="533a0-146">**ProcessInput**</span></span>
-   <span data-ttu-id="533a0-147">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="533a0-147">**ProcessOutput**</span></span>
-   <span data-ttu-id="533a0-148">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="533a0-148">**ProcessMessage**</span></span>
-   <span data-ttu-id="533a0-149">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="533a0-149">**ProcessEvent**</span></span>

## <a name="related-topics"></a><span data-ttu-id="533a0-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="533a0-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="533a0-151">**Interfacce obbligatorie**</span><span class="sxs-lookup"><span data-stu-id="533a0-151">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




