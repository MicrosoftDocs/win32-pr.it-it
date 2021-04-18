---
title: Assegnazione di formati di output
description: Assegnazione di formati di output
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, assegnazione di formati di output
- Formato di sistemi avanzati (ASF), assegnazione di formati di output
- ASF (Advanced Systems Format), assegnazione di formati di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri e formati di output, assegnazione
- codec, numeri di output e formati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299506"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="a30ae-110">Assegnazione di formati di output</span><span class="sxs-lookup"><span data-stu-id="a30ae-110">Assigning Output Formats</span></span>

<span data-ttu-id="a30ae-111">Alcuni codec possono decomprimere i dati multimediali digitali in diversi formati non compressi.</span><span class="sxs-lookup"><span data-stu-id="a30ae-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="a30ae-112">È possibile trovare tutti i formati supportati per un output specifico usando il Reader asincrono o il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="a30ae-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="a30ae-113">Per esaminare tutti i formati disponibili per un output, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="a30ae-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="a30ae-114">Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="a30ae-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="a30ae-115">Laddove i nomi di interfaccia variano, i metodi di lettura sincrona sono elencati tra parentesi dopo i metodi del lettore asincrono.</span><span class="sxs-lookup"><span data-stu-id="a30ae-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="a30ae-116">Creare un oggetto Reader e caricare un file per la lettura.</span><span class="sxs-lookup"><span data-stu-id="a30ae-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="a30ae-117">Per ulteriori informazioni, vedere [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md) (o [per creare un reader sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="a30ae-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="a30ae-118">Determinare l'output per il quale si desidera trovare i formati disponibili.</span><span class="sxs-lookup"><span data-stu-id="a30ae-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="a30ae-119">Se non si conosce già l'output che si desidera utilizzare, è possibile identificare gli output nel file utilizzando le procedure descritte in [per identificare i numeri di output](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="a30ae-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="a30ae-120">Recuperare il numero totale di formati disponibili per l'output desiderato chiamando [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (o [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span><span class="sxs-lookup"><span data-stu-id="a30ae-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="a30ae-121">Scorrere i formati disponibili uno alla volta, eseguendo i passaggi seguenti per ognuno di essi:</span><span class="sxs-lookup"><span data-stu-id="a30ae-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="a30ae-122">Recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per il formato di output corrente chiamando [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) o [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="a30ae-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="a30ae-123">Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per il formato di output effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="a30ae-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="a30ae-124">Eseguire la prima chiamata per ottenere la dimensione della struttura, quindi allocare la memoria per l'oggetto e passare un puntatore alla memoria allocata alla seconda chiamata.</span><span class="sxs-lookup"><span data-stu-id="a30ae-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="a30ae-125">Trovare il sottotipo di supporto del formato di output in **WM \_ media \_ Type. sottotipo**.</span><span class="sxs-lookup"><span data-stu-id="a30ae-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="a30ae-126">Per video, se il sottotipo corrente è il formato che si vuole usare per l'output, interrompere il ciclo.</span><span class="sxs-lookup"><span data-stu-id="a30ae-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="a30ae-127">In caso contrario, passare all'iterazione successiva.</span><span class="sxs-lookup"><span data-stu-id="a30ae-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="a30ae-128">Per l'audio, è necessario controllare i valori nella struttura **WAVEFORMATEX** in base ai requisiti.</span><span class="sxs-lookup"><span data-stu-id="a30ae-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="a30ae-129">**WM \_ MEDIA \_ Type. pbFormat** punta alla struttura **WAVEFORMATEX** per gli output audio.</span><span class="sxs-lookup"><span data-stu-id="a30ae-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="a30ae-130">Dopo aver individuato l'output desiderato, impostarlo per l'uso con il lettore chiamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (o [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="a30ae-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="a30ae-131">È necessario passare un puntatore all'interfaccia **IWMOutputMediaProps** ottenuta nel primo passaggio del ciclo.</span><span class="sxs-lookup"><span data-stu-id="a30ae-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a30ae-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a30ae-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a30ae-133">**Interfaccia IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a30ae-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="a30ae-134">**Interfaccia IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="a30ae-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="a30ae-135">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="a30ae-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="a30ae-136">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="a30ae-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="a30ae-137">**Uso degli output**</span><span class="sxs-lookup"><span data-stu-id="a30ae-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




