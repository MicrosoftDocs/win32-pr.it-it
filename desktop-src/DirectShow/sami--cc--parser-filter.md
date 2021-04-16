---
description: Filtro parser SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro parser SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0449bccd41a09fca952b5d84552ef919055526
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522041"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="f0b63-103">Filtro parser SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="f0b63-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="f0b63-104">Analizza i dati di didascalia da file SAMI (Synchronized Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="f0b63-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="f0b63-105">SAMI è un formato di testo simile a HTML e viene usato per codificare didascalie basate sul tempo.</span><span class="sxs-lookup"><span data-stu-id="f0b63-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="f0b63-106">Questo filtro converte i dati SAMI in un flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="f0b63-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="f0b63-107">Ogni esempio nel flusso contiene una voce di didascalia, insieme alle informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="f0b63-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="f0b63-108">Il timestamp degli esempi viene generato dalle informazioni sull'ora nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="f0b63-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="f0b63-109">Questo filtro è progettato per essere utilizzato con il filtro di [renderer del comando script interno](internal-script-command-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f0b63-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="f0b63-110">Il renderer interno del comando script riceve gli esempi di testo e li invia all'applicazione sotto forma di notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f0b63-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="f0b63-111">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="f0b63-111">For more information, see the Remarks section.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b63-112">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="f0b63-112">Filter Interfaces</span></span>                        | <span data-ttu-id="f0b63-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="f0b63-113">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="f0b63-114">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="f0b63-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="f0b63-115">\_Flusso MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="f0b63-115">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="f0b63-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="f0b63-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f0b63-117">[**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f0b63-117">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="f0b63-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="f0b63-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="f0b63-119">\_Testo MEDIATYPE, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="f0b63-119">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="f0b63-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="f0b63-120">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f0b63-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f0b63-121">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="f0b63-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="f0b63-122">Filter CLSID</span></span>                             | <span data-ttu-id="f0b63-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="f0b63-123">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="f0b63-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f0b63-124">Property Page CLSID</span></span>                      | <span data-ttu-id="f0b63-125">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f0b63-125">No property page</span></span>                                                                                         |
| <span data-ttu-id="f0b63-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="f0b63-126">Executable</span></span>                               | <span data-ttu-id="f0b63-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f0b63-127">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="f0b63-128">Merito</span><span class="sxs-lookup"><span data-stu-id="f0b63-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="f0b63-129">VALORE \_ improbabile</span><span class="sxs-lookup"><span data-stu-id="f0b63-129">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="f0b63-130">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="f0b63-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f0b63-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="f0b63-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="f0b63-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0b63-132">Remarks</span></span>

<span data-ttu-id="f0b63-133">Di seguito è riportato un semplice file SAMI:</span><span class="sxs-lookup"><span data-stu-id="f0b63-133">The following is a simple SAMI file:</span></span>


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



<span data-ttu-id="f0b63-134">Il tag di **stile** definisce due impostazioni della lingua, inglese (. ENCC) e francese (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="f0b63-134">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="f0b63-135">Definisce anche due stili, \# Normal e \# GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="f0b63-135">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="f0b63-136">Ogni tag di **sincronizzazione** definisce l'ora di inizio per una didascalia, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="f0b63-136">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="f0b63-137">I tag **P** contengono il testo della didascalia, mentre l'attributo **Class** specifica l'impostazione della lingua a cui si applica la didascalia.</span><span class="sxs-lookup"><span data-stu-id="f0b63-137">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="f0b63-138">Per ogni lingua e stile, il filtro crea un flusso logico.</span><span class="sxs-lookup"><span data-stu-id="f0b63-138">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="f0b63-139">In qualsiasi momento, sono abilitati esattamente un flusso di lingua e un flusso di stile.</span><span class="sxs-lookup"><span data-stu-id="f0b63-139">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="f0b63-140">Quando il filtro genera un campione, viene selezionata la didascalia per la lingua corrente e viene applicato lo stile corrente.</span><span class="sxs-lookup"><span data-stu-id="f0b63-140">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="f0b63-141">Per impostazione predefinita, il primo linguaggio e lo stile dichiarati nel file sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="f0b63-141">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="f0b63-142">Un'applicazione può usare il metodo [**IAMStreamSelect:: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) per abilitare un flusso diverso.</span><span class="sxs-lookup"><span data-stu-id="f0b63-142">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="f0b63-143">Con le impostazioni predefinite, la prima didascalia del file di esempio produce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="f0b63-143">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="f0b63-144">Se l'output passa al renderer interno del comando script, tale filtro Invia una notifica degli eventi dell' [**\_ \_ evento OLE EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="f0b63-144">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="f0b63-145">Il secondo parametro dell'evento è un BSTR con il testo della didascalia.</span><span class="sxs-lookup"><span data-stu-id="f0b63-145">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="f0b63-146">L'applicazione può recuperare l'evento e visualizzare la didascalia.</span><span class="sxs-lookup"><span data-stu-id="f0b63-146">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="f0b63-147">Nell'esempio seguente viene illustrato come eseguire il rendering di un file SAMI, recuperare informazioni sul flusso, abilitare i flussi e visualizzare il testo della didascalia.</span><span class="sxs-lookup"><span data-stu-id="f0b63-147">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="f0b63-148">Nell'esempio si presuppone che il file SAMI precedente venga salvato come file di test C: \\ Sami \_ \_ . Sami.</span><span class="sxs-lookup"><span data-stu-id="f0b63-148">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="f0b63-149">Per brevità, in questo esempio vengono utilizzati indici di flusso hardcoded quando viene chiamato il metodo **IAMStreamSelect:: Enable** .</span><span class="sxs-lookup"><span data-stu-id="f0b63-149">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="f0b63-150">Esegue anche il controllo minimo degli errori.</span><span class="sxs-lookup"><span data-stu-id="f0b63-150">It also performs minimal error checking.</span></span>


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



<span data-ttu-id="f0b63-151">Questo filtro usa l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) per eseguire il pull degli esempi dal filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="f0b63-151">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="f0b63-152">Pertanto, non supporta l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul relativo pin di input.</span><span class="sxs-lookup"><span data-stu-id="f0b63-152">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0b63-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0b63-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b63-154">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="f0b63-154">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



