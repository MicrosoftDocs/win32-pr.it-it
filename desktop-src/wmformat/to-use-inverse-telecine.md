---
title: Per usare il telecine inverso
description: Per usare il telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, telecine inversa
- Windows Media Format SDK, telecine
- ASF (Advanced Systems Format), telecine inversa
- ASF (formato avanzato dei sistemi), telecine inversa
- Formato di sistemi avanzati (ASF), telecine
- ASF (formato avanzato dei sistemi), telecine
- Telecine inversa
- telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299521"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="cd6d3-111">Per usare il telecine inverso</span><span class="sxs-lookup"><span data-stu-id="cd6d3-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="cd6d3-112">La telecine è il processo di conversione di film, che include 24 fotogrammi al secondo, in video, con 60 campi (metà fotogrammi) al secondo.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="cd6d3-113">Questo processo inserisce le immagini da ogni fotogramma di film in più campi video.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="cd6d3-114">Quando si codifica digitalmente un video creato da un film usando la telecine, il processo di compressione può causare la qualità degli artefatti di movimento e di altre riduzioni.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="cd6d3-115">Per evitare di influire sulla qualità dell'output digitale, il codec Windows Media Video 9 supporta la telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="cd6d3-116">Quando si usa la telecine inversa, il codec ricostruisce i 24 fotogrammi originali al secondo dal video di input prima di codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="cd6d3-117">Per utilizzare la telecine inversa, è necessario:</span><span class="sxs-lookup"><span data-stu-id="cd6d3-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="cd6d3-118">Usare un profilo con un flusso video impostato su 24 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="cd6d3-119">Conosce la configurazione del campo del video di input.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="cd6d3-120">Per utilizzare la telecine per un input per il writer, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="cd6d3-121">Configurare il writer come di consueto.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-121">Set up the writer as usual.</span></span> <span data-ttu-id="cd6d3-122">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="cd6d3-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="cd6d3-123">Prima di iniziare a scrivere esempi, ottenere un puntatore all'interfaccia [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) chiamando **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="cd6d3-124">Identificare il flusso da ricostruire chiamando [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per il numero di input desiderato.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="cd6d3-125">Passare g \_ wszDeinterlaceMode come impostazione e WM \_ DM \_ deinterlacciare \_ INVERSETELECINE come valore.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="cd6d3-126">Chiamare nuovamente **SetInputSetting** per impostare g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="cd6d3-127">Scrivere il file come di consueto.</span><span class="sxs-lookup"><span data-stu-id="cd6d3-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd6d3-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd6d3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd6d3-129">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="cd6d3-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="cd6d3-130">**Interfaccia IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="cd6d3-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="cd6d3-131">**Interfaccia IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="cd6d3-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




