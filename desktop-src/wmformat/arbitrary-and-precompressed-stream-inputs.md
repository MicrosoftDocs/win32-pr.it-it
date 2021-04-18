---
title: Input di flusso arbitrario e precompresso
description: Input di flusso arbitrario e precompresso
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), input di flusso arbitrario
- ASF (formato avanzato dei sistemi), input di flusso arbitrario
- profili, input di flussi arbitrari
- codec, input di flusso arbitrari
- Advanced Systems Format (ASF), input di flusso precompressi
- ASF (Advanced Systems Format), input di flusso precompressi
- profili, input di flusso precompressi
- codec, input di flusso precompressi
- input di flusso precompressi
- input di flusso arbitrari
- flussi, input di flusso arbitrari
- flussi, input di flusso precompressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299509"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="22624-115">Input di flusso arbitrario e precompresso</span><span class="sxs-lookup"><span data-stu-id="22624-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="22624-116">Solo gli input che devono essere compressi da uno dei codec Windows Media hanno più input possibili.</span><span class="sxs-lookup"><span data-stu-id="22624-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="22624-117">Gli altri tipi di input possibili sono input arbitrari e input precompressi.</span><span class="sxs-lookup"><span data-stu-id="22624-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="22624-118">I requisiti per i formati di input per questi tipi sono descritti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="22624-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="22624-119">Input di flusso arbitrari</span><span class="sxs-lookup"><span data-stu-id="22624-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="22624-120">Gli input per i tipi di flusso arbitrari sono identici ai formati di flusso descritti nel profilo.</span><span class="sxs-lookup"><span data-stu-id="22624-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="22624-121">Non è necessario impostare i formati di input per questi tipi.</span><span class="sxs-lookup"><span data-stu-id="22624-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="22624-122">Input di flusso precompressi</span><span class="sxs-lookup"><span data-stu-id="22624-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="22624-123">Quando si copia un flusso da un file a un altro, si passano esempi già compressi.</span><span class="sxs-lookup"><span data-stu-id="22624-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="22624-124">In questo caso, è necessario impostare l'oggetto proprietà di input su **null** per informare il writer che non è necessario convalidare i dati passati.</span><span class="sxs-lookup"><span data-stu-id="22624-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="22624-125">Per impostare il formato di input su **null**, chiamare [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passare **null** come secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="22624-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="22624-126">Quando si chiama questo metodo con un parametro **null** , è necessario effettuare la chiamata prima di chiamare [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="22624-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="22624-127">Quando si usano flussi precompressi, è necessario copiare manualmente le informazioni sul codec nell'intestazione del file prima di scrivere.</span><span class="sxs-lookup"><span data-stu-id="22624-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="22624-128">Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore.</span><span class="sxs-lookup"><span data-stu-id="22624-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="22624-129">Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso del flusso precompresso.</span><span class="sxs-lookup"><span data-stu-id="22624-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="22624-130">Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal reader.</span><span class="sxs-lookup"><span data-stu-id="22624-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22624-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="22624-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22624-132">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="22624-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




