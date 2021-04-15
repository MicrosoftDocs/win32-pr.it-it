---
description: Acquisizione di video in un file AVI
ms.assetid: 0f5f4a82-4a2e-4c48-b201-bda641cb8619
title: Acquisizione di video in un file AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86504e9ce149f495e1ea31664f56382340d33887
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104569451"
---
# <a name="capturing-video-to-an-avi-file"></a><span data-ttu-id="bd889-103">Acquisizione di video in un file AVI</span><span class="sxs-lookup"><span data-stu-id="bd889-103">Capturing Video to an AVI File</span></span>

<span data-ttu-id="bd889-104">La figura seguente mostra il grafico più semplice possibile per l'acquisizione di video in un file AVI.</span><span class="sxs-lookup"><span data-stu-id="bd889-104">The following illustration shows the simplest possible graph for capturing video to an AVI file.</span></span>

![grafico di acquisizione video AVI](images/vidcap02.png)

<span data-ttu-id="bd889-106">Il filtro [Mux AVI](avi-mux-filter.md) accetta il flusso video dal pin di acquisizione e lo inserisce in un flusso AVI.</span><span class="sxs-lookup"><span data-stu-id="bd889-106">The [AVI Mux](avi-mux-filter.md) filter takes the video stream from the capture pin and packages it into an AVI stream.</span></span> <span data-ttu-id="bd889-107">Un flusso audio potrebbe anche essere connesso al filtro Mux AVI, nel qual caso il mux eseguirà l'interleave dei due flussi.</span><span class="sxs-lookup"><span data-stu-id="bd889-107">An audio stream could also be connected to the AVI Mux filter, in which case the mux would interleave the two streams.</span></span> <span data-ttu-id="bd889-108">Il filtro del [writer di file](file-writer-filter.md) scrive il flusso AVI su disco.</span><span class="sxs-lookup"><span data-stu-id="bd889-108">The [File Writer](file-writer-filter.md) filter writes the AVI stream to disk.</span></span>

<span data-ttu-id="bd889-109">Per compilare il grafo, iniziare chiamando il metodo [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bd889-109">To build the graph, start by calling the [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) method, as follows:</span></span>


```C++
IBaseFilter *pMux;
hr = pBuild->SetOutputFileName(
    &MEDIASUBTYPE_Avi,  // Specifies AVI for the target file.
    L"C:\\Example.avi", // File name.
    &pMux,              // Receives a pointer to the mux.
    NULL);              // (Optional) Receives a pointer to the file sink.
```



<span data-ttu-id="bd889-110">Il primo parametro specifica il tipo di file, in questo caso AVI.</span><span class="sxs-lookup"><span data-stu-id="bd889-110">The first parameter specifies the file type — in this case, AVI.</span></span> <span data-ttu-id="bd889-111">Il secondo parametro assegna il nome del file.</span><span class="sxs-lookup"><span data-stu-id="bd889-111">The second parameter gives the file name.</span></span> <span data-ttu-id="bd889-112">Per AVI, il metodo SetOutputFileName crea il filtro MUX per AVI e il filtro del writer di file e li aggiunge al grafico.</span><span class="sxs-lookup"><span data-stu-id="bd889-112">For AVI, the SetOutputFileName method cocreates the AVI Mux filter and the File Writer filter and adds them to the graph.</span></span> <span data-ttu-id="bd889-113">Imposta anche il nome del file nel filtro del writer di file, chiamando il metodo [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) e connette i due filtri.</span><span class="sxs-lookup"><span data-stu-id="bd889-113">It also sets the file name on the File Writer filter, by calling the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method, and connects the two filters.</span></span> <span data-ttu-id="bd889-114">Il metodo restituisce un puntatore al Mux AVI nel terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="bd889-114">The method returns a pointer to the AVI Mux in the third parameter.</span></span> <span data-ttu-id="bd889-115">Facoltativamente, restituisce un puntatore all'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) nel quarto parametro.</span><span class="sxs-lookup"><span data-stu-id="bd889-115">Optionally, it returns a pointer to the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface in the fourth parameter.</span></span> <span data-ttu-id="bd889-116">Se questa interfaccia non è necessaria, è possibile impostare questo parametro su **null**, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="bd889-116">If you don't need this interface, you can set this parameter to **NULL**, as shown in the previous example.</span></span>

<span data-ttu-id="bd889-117">Chiamare quindi il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) per connettere il filtro di acquisizione al Mux AVI, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="bd889-117">Next, call the [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method to connect the capture filter to the AVI Mux, as follows:</span></span>


```C++
hr = pBuild->RenderStream(
    &PIN_CATEGORY_CAPTURE, // Pin category.
    &MEDIATYPE_Video,      // Media type.
    pCap,                  // Capture filter.
    NULL,                  // Intermediate filter (optional).
    pMux);                 // Mux or file sink filter.

// Release the mux filter.
pMux->Release();
```



<span data-ttu-id="bd889-118">Il primo parametro assegna la categoria pin, che è l' \_ acquisizione della categoria pin \_ per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bd889-118">The first parameter gives the pin category, which is PIN\_CATEGORY\_CAPTURE for capture.</span></span> <span data-ttu-id="bd889-119">Il secondo parametro fornisce il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="bd889-119">The second parameter gives the media type.</span></span> <span data-ttu-id="bd889-120">Il terzo parametro è un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bd889-120">The third parameter is a pointer to the capture filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="bd889-121">Il quarto parametro è facoltativo. consente di instradare il flusso video tramite un filtro intermedio, ad esempio un codificatore, prima di passarlo al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="bd889-121">The fourth parameter is optional; it lets you route the video stream through an intermediate filter, such as an encoder, before passing it to the mux filter.</span></span> <span data-ttu-id="bd889-122">In caso contrario, impostare questo parametro su **null**, come illustrato nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="bd889-122">Otherwise, set this parameter to **NULL**, as shown in the previous example.</span></span> <span data-ttu-id="bd889-123">Il quinto parametro è il puntatore al filtro MUX.</span><span class="sxs-lookup"><span data-stu-id="bd889-123">The fifth parameter is the pointer to the mux filter.</span></span> <span data-ttu-id="bd889-124">Questo puntatore viene ottenuto chiamando il metodo SetOutputFileName.</span><span class="sxs-lookup"><span data-stu-id="bd889-124">This pointer is obtained by calling the SetOutputFileName method.</span></span>

<span data-ttu-id="bd889-125">Per acquisire audio, chiamare RenderStream con il tipo di supporto MEDIATYPE \_ audio.</span><span class="sxs-lookup"><span data-stu-id="bd889-125">To capture audio, call RenderStream with the media type MEDIATYPE\_Audio.</span></span> <span data-ttu-id="bd889-126">Se si acquisisce audio e video da due dispositivi distinti, è consigliabile fare in modo che il flusso audio sia il flusso master.</span><span class="sxs-lookup"><span data-stu-id="bd889-126">If you are capturing audio and video from two separate devices, it is a good idea to make the audio stream the master stream.</span></span> <span data-ttu-id="bd889-127">In questo modo è possibile evitare la deriva tra i due flussi, perché il filtro Mux AVI regola la velocità di riproduzione nel flusso video in modo che corrisponda al flusso audio.</span><span class="sxs-lookup"><span data-stu-id="bd889-127">This helps to prevent drift between the two streams, because the AVI Mux filter adjust the playback rate on the video stream to match the audio stream.</span></span> <span data-ttu-id="bd889-128">Per impostare il flusso Master, chiamare il metodo [**IConfigAviMux:: SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) sul filtro Mux AVI:</span><span class="sxs-lookup"><span data-stu-id="bd889-128">To set the master stream, call the [**IConfigAviMux::SetMasterStream**](/windows/desktop/api/Strmif/nf-strmif-iconfigavimux-setmasterstream) method on the AVI Mux filter:</span></span>


```C++
IConfigAviMux *pConfigMux = NULL;
hr = pMux->QueryInterface(IID_IConfigAviMux, (void**)&pConfigMux);
if (SUCCEEDED(hr))
{
    pConfigMux->SetMasterStream(1);
    pConfigMux->Release();
}
```



<span data-ttu-id="bd889-129">Il parametro per SetMasterStream è il numero del flusso, determinato dall'ordine in cui viene chiamato RenderStream.</span><span class="sxs-lookup"><span data-stu-id="bd889-129">The parameter to SetMasterStream is the stream number, which is determined by the order in which you call RenderStream.</span></span> <span data-ttu-id="bd889-130">Ad esempio, se si chiama prima RenderStream per il video e quindi per l'audio, il video è Stream 0 e l'audio è Stream 1.</span><span class="sxs-lookup"><span data-stu-id="bd889-130">For example, if you call RenderStream first for video and then for audio, the video is stream 0 and the audio is stream 1.</span></span>

<span data-ttu-id="bd889-131">È anche possibile impostare il modo in cui il filtro Mux AVI interleaves i flussi audio e video chiamando il metodo [**IConfigInterleaving::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="bd889-131">You may also want to set how the AVI Mux filter interleaves the audio and video streams, by calling the [**IConfigInterleaving::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iconfiginterleaving-put_mode) method.</span></span>


```C++
IConfigInterleaving *pInterleave = NULL;
hr = pMux->QueryInterface(IID_IConfigInterleaving, (void**)&pInterleave);
if (SUCCEEDED(hr))
{
    pInterleave->put_Mode(INTERLEAVE_CAPTURE);
    pInterleave->Release();
}
```



<span data-ttu-id="bd889-132">Con il flag di acquisizione interleave \_ , il mux di AVI esegue l'interfoliazione a una velocità adatta per l'acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="bd889-132">With the INTERLEAVE\_CAPTURE flag, the AVI Mux performs interleaving at a rate that is suitable for video capture.</span></span> <span data-ttu-id="bd889-133">È anche possibile usare l'interleave \_ None, che significa nessuna interfoliazione: il mux di AVI scriverà semplicemente i dati nell'ordine in cui arrivano.</span><span class="sxs-lookup"><span data-stu-id="bd889-133">You can also use INTERLEAVE\_NONE, which means no interleaving — the AVI Mux will simply write the data in the order that it arrives.</span></span> <span data-ttu-id="bd889-134">Il \_ flag di interfoliazione completo significa che il mux di AVI esegue l'interfoliazione completo. Tuttavia, questa modalità è meno adatta per l'acquisizione video perché richiede il più overheard.</span><span class="sxs-lookup"><span data-stu-id="bd889-134">The INTERLEAVE\_FULL flag means the AVI Mux performs full interleaving; however, this mode is less suitable for video capture because it requires the most overheard.</span></span>

<span data-ttu-id="bd889-135">Codifica del flusso video</span><span class="sxs-lookup"><span data-stu-id="bd889-135">Encoding the Video Stream</span></span>

<span data-ttu-id="bd889-136">È possibile codificare il flusso video inserendo un filtro del codificatore tra il filtro di acquisizione e il filtro Mux AVI.</span><span class="sxs-lookup"><span data-stu-id="bd889-136">You can encode the video stream by inserting an encoder filter between the capture filter and the AVI Mux filter.</span></span> <span data-ttu-id="bd889-137">Usare l' [enumeratore del dispositivo di sistema](system-device-enumerator.md) o il [mapper del filtro](filter-mapper.md) per selezionare un filtro del codificatore.</span><span class="sxs-lookup"><span data-stu-id="bd889-137">Use the [System Device Enumerator](system-device-enumerator.md) or the [Filter Mapper](filter-mapper.md) to select an encoder filter.</span></span> <span data-ttu-id="bd889-138">Per ulteriori informazioni, vedere [enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bd889-138">(For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).)</span></span>

<span data-ttu-id="bd889-139">Specificare il filtro del codificatore come quarto parametro per RenderStream, illustrato in grassetto nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="bd889-139">Specify the encoder filter as the fourth parameter to RenderStream, shown in bold in the following example:</span></span>


```C++
IBaseFilter *pEncoder;
/* Create the encoder filter (not shown). */
// Add it to the filter graph.
pGraph->AddFilter(pEncoder, L"Encoder");

/* Call SetOutputFileName as shown previously. */

// Render the stream.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, 
    pCap, 
pEncoder, pMux);
pEncoder->Release();
```



<span data-ttu-id="bd889-140">Il filtro del codificatore potrebbe supportare [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) o altre interfacce per l'impostazione dei parametri di codifica.</span><span class="sxs-lookup"><span data-stu-id="bd889-140">The encoder filter might support [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) or other interfaces for setting the encoding parameters.</span></span> <span data-ttu-id="bd889-141">Per un elenco delle interfacce possibili, vedere [codifica e decodifica di file](file-encoding-and-decoding-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="bd889-141">For a list of possible interfaces, see [File Encoding and Decoding Interfaces](file-encoding-and-decoding-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd889-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd889-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd889-143">Acquisizione di video in un file</span><span class="sxs-lookup"><span data-stu-id="bd889-143">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



