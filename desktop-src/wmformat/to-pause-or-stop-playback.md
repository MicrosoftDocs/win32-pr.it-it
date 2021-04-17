---
title: Per sospendere o arrestare la riproduzione
description: Per sospendere o arrestare la riproduzione
ms.assetid: 8e43ea80-36c7-4530-8ed3-dfdb64a3a2e3
keywords:
- Formato Advanced Systems (ASF), sospensione della riproduzione
- ASF (formato avanzato dei sistemi), sospensione della riproduzione
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Formato Advanced Systems (ASF), arresto della riproduzione
- ASF (formato avanzato dei sistemi), arresto della riproduzione
- ASF (Advanced Systems Format), sospensione o arresto della riproduzione
- ASF (formato avanzato dei sistemi), sospensione o arresto della riproduzione
- lettori asincroni, sospensione della riproduzione
- lettori asincroni, arresto della riproduzione
- lettori asincroni, sospensione o arresto della riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728ce4c58f9198f605764d0f19d0d5f55c7f6c6b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104516597"
---
# <a name="to-pause-or-stop-playback"></a><span data-ttu-id="f75a5-114">Per sospendere o arrestare la riproduzione</span><span class="sxs-lookup"><span data-stu-id="f75a5-114">To Pause or Stop Playback</span></span>

<span data-ttu-id="f75a5-115">Quando si chiama [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) per iniziare la riproduzione di un file, il Reader asincrono continuerà l'elaborazione nei propri thread distinti fino a quando non viene raggiunta la fine del file.</span><span class="sxs-lookup"><span data-stu-id="f75a5-115">When you call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) to begin playing a file, the asynchronous reader will continue processing in its own separate threads until the end of the file is reached.</span></span> <span data-ttu-id="f75a5-116">È possibile sospendere o arrestare il recapito degli esempi usando rispettivamente i metodi [**IWMReader::P ause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) o [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) .</span><span class="sxs-lookup"><span data-stu-id="f75a5-116">You can pause or stop the delivery of samples using the [**IWMReader::Pause**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-pause) or [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop) methods respectively.</span></span>

## <a name="pausing"></a><span data-ttu-id="f75a5-117">Sospensione</span><span class="sxs-lookup"><span data-stu-id="f75a5-117">Pausing</span></span>

<span data-ttu-id="f75a5-118">Quando si chiama **IWMReader::P ause** per sospendere la riproduzione di un file, il lettore tiene traccia della posizione corrente nel file.</span><span class="sxs-lookup"><span data-stu-id="f75a5-118">When you call **IWMReader::Pause** to pause playback of a file, the reader keeps track of the current position in the file.</span></span> <span data-ttu-id="f75a5-119">Per riprendere la riproduzione dopo la sospensione, chiamare [**IWMReader:: Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span><span class="sxs-lookup"><span data-stu-id="f75a5-119">To resume playing after pausing, call [**IWMReader::Resume**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-resume).</span></span> <span data-ttu-id="f75a5-120">La riproduzione riprenderà dal punto in cui è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="f75a5-120">Playback will resume from the point at which it paused.</span></span>

## <a name="stopping"></a><span data-ttu-id="f75a5-121">Stopping</span><span class="sxs-lookup"><span data-stu-id="f75a5-121">Stopping</span></span>

<span data-ttu-id="f75a5-122">Quando si chiama **IWMReader:: Stop** per interrompere la riproduzione di un file, il lettore non tiene traccia delle informazioni sullo stato di avanzamento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f75a5-122">When you call **IWMReader::Stop** to halt playback of a file, the reader does not keep track of any information about the progress of playback.</span></span> <span data-ttu-id="f75a5-123">Per usare **Interrompi** e versioni successive per tornare al punto di arresto, è necessario salvare l'ora di presentazione dell'ultimo esempio recapitato e usarlo nella chiamata a **IWMReader:: Start**.</span><span class="sxs-lookup"><span data-stu-id="f75a5-123">To use **Stop** and later return to the stopping point you must save the presentation time of the last sample delivered and use it in your call to **IWMReader::Start**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f75a5-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f75a5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f75a5-125">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="f75a5-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="f75a5-126">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="f75a5-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




