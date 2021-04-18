---
title: Per identificare i numeri di output
description: Per identificare i numeri di output
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media Format SDK, identificazione dei numeri di output
- ASF (Advanced Systems Format), identificazione dei numeri di output
- ASF (Advanced Systems Format), identificazione dei numeri di output
- ASF (Advanced Systems Format), numeri di output e formati
- ASF (formato avanzato dei sistemi), numeri e formati di output
- numeri e formati di output, identificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299401"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="6ab54-109">Per identificare i numeri di output</span><span class="sxs-lookup"><span data-stu-id="6ab54-109">To Identify Output Numbers</span></span>

<span data-ttu-id="6ab54-110">Per identificare i numeri di output per un file caricato, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="6ab54-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="6ab54-111">Queste procedure sono identiche sia per il lettore asincrono che per il lettore sincrono.</span><span class="sxs-lookup"><span data-stu-id="6ab54-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="6ab54-112">Laddove i nomi di interfaccia variano, i metodi di lettura sincrona sono elencati tra parentesi dopo i metodi del lettore asincrono.</span><span class="sxs-lookup"><span data-stu-id="6ab54-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="6ab54-113">Creare un oggetto Reader e caricare un file per la lettura.</span><span class="sxs-lookup"><span data-stu-id="6ab54-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="6ab54-114">Per ulteriori informazioni, vedere [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md) (o [per creare un reader sincrono e aprire un file](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="6ab54-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="6ab54-115">Recuperare il numero totale di output per il file chiamando [**IWMReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (o [**IWMSyncReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span><span class="sxs-lookup"><span data-stu-id="6ab54-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="6ab54-116">Scorrere gli output uno alla volta, eseguendo i passaggi seguenti per ognuno di essi:</span><span class="sxs-lookup"><span data-stu-id="6ab54-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="6ab54-117">Recuperare l'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) per l'output corrente con una chiamata a [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) o [**IWMSyncReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops).</span><span class="sxs-lookup"><span data-stu-id="6ab54-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="6ab54-118">Recuperare la struttura del [**\_ \_ tipo di supporto WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) per l'output effettuando due chiamate a [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="6ab54-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="6ab54-119">Eseguire la prima chiamata per ottenere la dimensione della struttura, quindi allocare la memoria per l'oggetto e passare un puntatore alla memoria allocata alla seconda chiamata.</span><span class="sxs-lookup"><span data-stu-id="6ab54-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="6ab54-120">In alternativa, è possibile chiamare [**IWMMediaProps:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), che fornisce il tipo principale senza che sia necessario allocare memoria per la struttura del **\_ \_ tipo di supporto WM** .</span><span class="sxs-lookup"><span data-stu-id="6ab54-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="6ab54-121">È possibile ignorare gli output del tipo principale errato.</span><span class="sxs-lookup"><span data-stu-id="6ab54-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="6ab54-122">Recuperare il tipo di supporto principale e il sottotipo di supporto dalla struttura del **\_ \_ tipo di supporto WM** .</span><span class="sxs-lookup"><span data-stu-id="6ab54-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="6ab54-123">Questi valori vengono archiviati rispettivamente nei membri dati **majortype** e **sottotipo** .</span><span class="sxs-lookup"><span data-stu-id="6ab54-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="6ab54-124">Controllare il valore di **WM \_ media \_ Type. formatType**.</span><span class="sxs-lookup"><span data-stu-id="6ab54-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="6ab54-125">Consente di specificare il tipo di struttura contenuto nel buffer in **WM \_ media \_ Type. pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="6ab54-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="6ab54-126">Per ulteriori informazioni sui tipi di formato, vedere [tipi di supporto](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="6ab54-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="6ab54-127">Allocare memoria per conservare la struttura del tipo identificato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="6ab54-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="6ab54-128">Copiare la struttura nella memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="6ab54-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="6ab54-129">Per audio e video, questa struttura fornisce informazioni essenziali sulla modalità di rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="6ab54-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="6ab54-130">Il lettore sincrono fornisce anche metodi per recuperare le associazioni tra i numeri di output e i numeri di flusso.</span><span class="sxs-lookup"><span data-stu-id="6ab54-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="6ab54-131">Per ulteriori informazioni, vedere [per trovare i numeri di flusso e i numeri di output](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="6ab54-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ab54-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ab54-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ab54-133">**Input, flussi e output**</span><span class="sxs-lookup"><span data-stu-id="6ab54-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="6ab54-134">**Interfaccia IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="6ab54-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="6ab54-135">**Interfaccia IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="6ab54-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="6ab54-136">**Interfaccia IWMReader**</span><span class="sxs-lookup"><span data-stu-id="6ab54-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="6ab54-137">**Interfaccia IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="6ab54-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="6ab54-138">**Uso degli output**</span><span class="sxs-lookup"><span data-stu-id="6ab54-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




