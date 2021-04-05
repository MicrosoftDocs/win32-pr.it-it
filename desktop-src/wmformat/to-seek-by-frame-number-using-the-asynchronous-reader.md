---
title: Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono
description: Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- Formato di sistemi avanzati (ASF), ricerca per numero di frame
- ASF (Advanced Systems Format), ricerca per numero di frame
- ASF (Advanced Systems Format), Reader asincroni
- ASF (formato avanzato dei sistemi), Reader asincroni
- Reader asincroni, ricerca per numero di frame
- flussi video, ricerca per numero di frame
- flussi video, lettori asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046291"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="1f223-110">Per eseguire la ricerca in base al numero di frame utilizzando il Reader asincrono</span><span class="sxs-lookup"><span data-stu-id="1f223-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="1f223-111">L'oggetto Reader asincrono può essere utilizzato per cercare i numeri di frame dei flussi video in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f223-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="1f223-112">Per usare la ricerca basata su frame, il file caricato nel lettore deve essere indicizzato in base al frame.</span><span class="sxs-lookup"><span data-stu-id="1f223-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="1f223-113">Ogni singolo flusso video può essere indicizzato.</span><span class="sxs-lookup"><span data-stu-id="1f223-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="1f223-114">Per determinare se un flusso è stato indicizzato in base al frame, è possibile controllare l' \_ attributo g wszWMNumberOfFrames nell'intestazione del file chiamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="1f223-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="1f223-115">Per cercare i dati in un file ASF in base al numero di frame usando il Reader asincrono, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="1f223-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="1f223-116">Ottenere un puntatore all'interfaccia [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) dell'oggetto Reader chiamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="1f223-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="1f223-117">Per impostare il numero e la durata del fotogramma iniziale, chiamare [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="1f223-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="1f223-118">È necessario specificare il numero di flusso di un flusso video indicizzato con frame.</span><span class="sxs-lookup"><span data-stu-id="1f223-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="1f223-119">Il lettore sincronizza il resto degli output con l'ora di presentazione del frame specificato del flusso specificato e inizia a consegnare gli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="1f223-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="1f223-120">Gestire gli esempi normalmente nell'implementazione del metodo **IWMReaderCallback:: OnSample** .</span><span class="sxs-lookup"><span data-stu-id="1f223-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f223-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f223-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f223-122">**Lettura di file con il lettore asincrono**</span><span class="sxs-lookup"><span data-stu-id="1f223-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1f223-123">**Lettura dei metadati durante la riproduzione**</span><span class="sxs-lookup"><span data-stu-id="1f223-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="1f223-124">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="1f223-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




