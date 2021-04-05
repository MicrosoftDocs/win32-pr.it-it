---
title: Oggetto writer
description: Oggetto writer
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- Windows Media Format SDK, oggetti writer
- ASF (Advanced Systems Format), oggetti writer
- ASF (Advanced Systems Format), oggetti writer
- oggetti, oggetti writer
- oggetti writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724124"
---
# <a name="writer-object"></a><span data-ttu-id="e3ba1-108">Oggetto writer</span><span class="sxs-lookup"><span data-stu-id="e3ba1-108">Writer Object</span></span>

<span data-ttu-id="e3ba1-109">L'oggetto writer viene utilizzato per scrivere file multimediali digitali utilizzando la struttura di file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e3ba1-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="e3ba1-110">Il processo di scrittura di un file multimediale digitale comporta molti passaggi interni al writer, che coordina la compressione, la creazione di pacchetti e il multiplexing.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="e3ba1-111">L'oggetto writer include interfacce per l'output su file o una rete, supporta un'interfaccia di callback e può creare uno o più oggetti proprietà supporti di input.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="e3ba1-112">L'oggetto writer viene creato dalla funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), che imposta un puntatore a un'interfaccia **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="e3ba1-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="e3ba1-113">Le altre interfacce dell'oggetto writer possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e3ba1-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="e3ba1-114">Le interfacce seguenti sono supportate dall'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="e3ba1-115">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e3ba1-115">Interface</span></span>                                          | <span data-ttu-id="e3ba1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3ba1-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3ba1-117">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="e3ba1-118">Fornisce metodi per generare chiavi [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="e3ba1-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="e3ba1-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="e3ba1-120">Configura l'oggetto writer per la scrittura di un file contenente un flusso pre-crittografato conforme al protocollo Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="e3ba1-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="e3ba1-122">Gestisce la specifica e il recupero delle informazioni di intestazione, ad esempio metadati, [*marcatori*](wmformat-glossary.md)e così via.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="e3ba1-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="e3ba1-124">Gestisce l'enumerazione tramite le informazioni sui codec disponibili.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="e3ba1-125">Eredita tutti i metodi di **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="e3ba1-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="e3ba1-127">Gestisce l'enumerazione tramite le informazioni sui codec disponibili.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="e3ba1-128">Eredita tutti i metodi di **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="e3ba1-129">**IWMWatermarkInfo**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="e3ba1-130">Consente di accedere alle informazioni sui sistemi di filigrana presenti nel sistema.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="e3ba1-131">**IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="e3ba1-132">Avvia e arresta la scrittura dei file ASF; sono inclusi i metodi per l'allocazione di buffer, l'impostazione e il recupero di proprietà di input, l'impostazione di profili e i nomi dei file di output e lo sblocco del writer.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="e3ba1-133">**IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="e3ba1-134">Aggiunge, ottiene e rimuove gli oggetti sink specificati; Recupera le statistiche, il numero di sink e l'ora di clock a cui il writer sta lavorando; ed esegue altre funzioni avanzate.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="e3ba1-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="e3ba1-136">Fornisce alcune funzionalità avanzate, in particolare per la gestione di video deinterlacciati.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="e3ba1-137">Eredita tutti i metodi di **IWMWriterAdvanced**.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="e3ba1-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="e3ba1-139">Fornisce funzionalità aggiuntive del writer, inclusa la possibilità di ottenere statistiche dettagliate del writer.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="e3ba1-140">Eredita tutti i metodi di **IWMWriterAdvanced** e **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="e3ba1-141">**IWMWriterPostView**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="e3ba1-142">Gestisce alcune funzionalità di scrittura avanzate relative agli esempi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="e3ba1-143">Per verificare che il processo di codifica/decodifica funzioni correttamente, è possibile visualizzare l'output, in genere da un codificatore.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="e3ba1-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="e3ba1-145">Gestisce i passaggi di pre-elaborazione effettuati dal writer.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="e3ba1-146">I passaggi di pre-elaborazione vengono usati per migliorare la qualità dell'output codificato.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="e3ba1-147">L'interfaccia di callback seguente deve essere implementata dall'applicazione per tenere traccia dello stato di avanzamento della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="e3ba1-148">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e3ba1-148">Interface</span></span>                                                      | <span data-ttu-id="e3ba1-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3ba1-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3ba1-150">**IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="e3ba1-151">Consente di gestire il modo in cui vengono ricevuti gli esempi non compressi dall'oggetto writer per visualizzare in anteprima le attività del codec.</span><span class="sxs-lookup"><span data-stu-id="e3ba1-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3ba1-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3ba1-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ba1-153">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="e3ba1-154">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="e3ba1-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




