---
description: In questa sezione viene descritto come scrivere una trasformazione Media Foundation personalizzata (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Scrittura di un MFT personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882214"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="bbbeb-103">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="bbbeb-103">Writing a Custom MFT</span></span>

<span data-ttu-id="bbbeb-104">In questa sezione viene descritto come scrivere una trasformazione Media Foundation personalizzata (MFT).</span><span class="sxs-lookup"><span data-stu-id="bbbeb-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="bbbeb-105">Elenco di controllo MFT</span><span class="sxs-lookup"><span data-stu-id="bbbeb-105">MFT Checklist</span></span>

<span data-ttu-id="bbbeb-106">Quando si implementa un MFT personalizzato, utilizzare l'elenco di controllo seguente per determinare i requisiti:</span><span class="sxs-lookup"><span data-stu-id="bbbeb-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbbeb-107">Tutte le MFTs</span><span class="sxs-lookup"><span data-stu-id="bbbeb-107">All MFTs</span></span></td>
<td><span data-ttu-id="bbbeb-108">Tutti MFTs devono implementare <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="bbbeb-109">Negli argomenti seguenti vengono fornite ulteriori informazioni sull'implementazione di questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="bbbeb-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="bbbeb-110"><a href="basic-mft-processing-model.md">Modello di elaborazione MFT di base</a></span><span class="sxs-lookup"><span data-stu-id="bbbeb-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="bbbeb-111"><a href="time-stamps-and-durations.md">Timestamp e durate</a></span><span class="sxs-lookup"><span data-stu-id="bbbeb-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="bbbeb-112"><a href="handling-stream-changes.md">Gestione delle modifiche dei flussi</a></span><span class="sxs-lookup"><span data-stu-id="bbbeb-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbbeb-113">Codificatori e decodificatori</span><span class="sxs-lookup"><span data-stu-id="bbbeb-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="bbbeb-114">Requisiti: vedere <a href="implementing-a-codec-mft.md">implementazione di un codec MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="bbbeb-115">Consigliato: implementare <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> o <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>per supportare le notifiche di qualità del servizio (QoS).</span><span class="sxs-lookup"><span data-stu-id="bbbeb-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbbeb-116">Decodificatori video e processori video</span><span class="sxs-lookup"><span data-stu-id="bbbeb-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="bbbeb-117">Facoltativo: supporta l'accelerazione video DirectX.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="bbbeb-118"><a href="direct3d-aware-mfts.md">MFTs compatibili con Direct3D</a></span><span class="sxs-lookup"><span data-stu-id="bbbeb-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="bbbeb-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporto di DXVA 2,0 in Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="bbbeb-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbbeb-120">Codec hardware</span><span class="sxs-lookup"><span data-stu-id="bbbeb-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="bbbeb-121">Vedere <a href="hardware-mfts.md">hardware MFTS</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbbeb-122">Per rendere la MFT individuabile dalle applicazioni...</span><span class="sxs-lookup"><span data-stu-id="bbbeb-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="bbbeb-123">Vedere <a href="registering-and-enumerating-mfts.md">registrazione ed enumerazione di MFTS</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbbeb-124">Elaborazione asincrona dei dati</span><span class="sxs-lookup"><span data-stu-id="bbbeb-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="bbbeb-125">Il modello MFT predefinito usa chiamate sincrone (bloccanti) per elaborare i dati.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="bbbeb-126">Per alcuni MFTs, l'elaborazione asincrona può essere più efficiente.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="bbbeb-127">Tuttavia, è anche più complesso da implementare.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="bbbeb-128">Per altre informazioni, vedere <a href="asynchronous-mfts.md">MFTS asincrono</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbbeb-129">Controllo della frequenza, modalità di trick o riproduzione inversa</span><span class="sxs-lookup"><span data-stu-id="bbbeb-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="bbbeb-130">Vedere <a href="implementing-rate-control.md">implementazione del controllo della frequenza</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbbeb-131">Se il MFT crea dei thread...</span><span class="sxs-lookup"><span data-stu-id="bbbeb-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="bbbeb-132">Implementare l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bbbeb-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bbbeb-133">Se il MFT presenta restrizioni di licenza...</span><span class="sxs-lookup"><span data-stu-id="bbbeb-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="bbbeb-134">Prendere in considerazione l'uso del meccanismo Field-of-use.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="bbbeb-135">Vedere il <a href="field-of-use-restrictions.md">campo relativo alle restrizioni di utilizzo</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbbeb-136">Se si sta trasportando un oggetto DMO (DirectX Media Object) esistente...</span><span class="sxs-lookup"><span data-stu-id="bbbeb-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="bbbeb-137">Vedere <a href="comparison-of-mfts-and-dmos.md">confronto tra MFTS e DMOS</a>.</span><span class="sxs-lookup"><span data-stu-id="bbbeb-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bbbeb-138">Questa sezione contiene i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="bbbeb-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="bbbeb-139">Timestamp e durate</span><span class="sxs-lookup"><span data-stu-id="bbbeb-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="bbbeb-140">Gestione delle modifiche dei flussi</span><span class="sxs-lookup"><span data-stu-id="bbbeb-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="bbbeb-141">Implementazione di un codec MFT</span><span class="sxs-lookup"><span data-stu-id="bbbeb-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="bbbeb-142">MFTs compatibili con Direct3D</span><span class="sxs-lookup"><span data-stu-id="bbbeb-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="bbbeb-143">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="bbbeb-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="bbbeb-144">Meriti codec</span><span class="sxs-lookup"><span data-stu-id="bbbeb-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="bbbeb-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbbeb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbbeb-146">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bbbeb-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




