---
title: Per cercare i marcatori
description: Per cercare i marcatori
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Formato di sistemi avanzati (ASF), ricerca di marcatori
- ASF (formato avanzato dei sistemi), ricerca di marcatori
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- Reader asincroni, ricerca di marcatori
- lettori asincroni, marcatori
- marcatori, ricerca
- indicatori, Reader asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299526"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="f4a8e-113">Per cercare i marcatori</span><span class="sxs-lookup"><span data-stu-id="f4a8e-113">To Seek to Markers</span></span>

<span data-ttu-id="f4a8e-114">Un marcatore è una posizione denominata in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="f4a8e-115">È possibile avviare la riproduzione solo dalla posizione di un marcatore utilizzando il Reader asincrono.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="f4a8e-116">È possibile iniziare la riproduzione in corrispondenza di un marcatore attenendosi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="f4a8e-117">Chiamare **IWMReader:: QueryInterface** per ottenere un puntatore all'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="f4a8e-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="f4a8e-118">Recuperare il numero totale di marcatori nel file chiamando [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span><span class="sxs-lookup"><span data-stu-id="f4a8e-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="f4a8e-119">Scorrere i marcatori utilizzando il numero di marcatori recuperato nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="f4a8e-120">Recuperare il nome e l'ora di ogni marcatore chiamando [**IWMHeaderInfo:: Getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) per ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="f4a8e-121">Salvare l'indice del marcatore desiderato.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="f4a8e-122">Chiamare **IWMReader:: QueryInterface** per ottenere un puntatore all'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .</span><span class="sxs-lookup"><span data-stu-id="f4a8e-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="f4a8e-123">Specificare il marcatore da cui iniziare la riproduzione chiamando [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span><span class="sxs-lookup"><span data-stu-id="f4a8e-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="f4a8e-124">È necessario passare l'indice del marcatore desiderato, salvato nel passaggio 3.</span><span class="sxs-lookup"><span data-stu-id="f4a8e-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="f4a8e-125">Gestire gli esempi normalmente nell'implementazione del metodo [**IWMReaderCallback:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="f4a8e-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4a8e-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f4a8e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4a8e-127">**Indicatori**</span><span class="sxs-lookup"><span data-stu-id="f4a8e-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="f4a8e-128">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="f4a8e-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="f4a8e-129">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="f4a8e-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




