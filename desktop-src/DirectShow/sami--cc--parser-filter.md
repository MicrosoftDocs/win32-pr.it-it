---
description: Filtro parser SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtro parser SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b77f0aa2d913b7f0295a078c8174ae483bb1cb62
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909679"
---
# <a name="sami-cc-parser-filter"></a><span data-ttu-id="c3148-103">Filtro parser SAMI (CC)</span><span class="sxs-lookup"><span data-stu-id="c3148-103">SAMI (CC) Parser Filter</span></span>

<span data-ttu-id="c3148-104">Analizza i dati dei sottotitoli dai file SAMI (Synchronized Accessible Media Interchange).</span><span class="sxs-lookup"><span data-stu-id="c3148-104">Parses captioning data from Synchronized Accessible Media Interchange (SAMI) files.</span></span>

<span data-ttu-id="c3148-105">SAMI è un formato di testo simile a HTML e viene usato per codificare sottotitoli basati sul tempo.</span><span class="sxs-lookup"><span data-stu-id="c3148-105">SAMI is a text format similar to HTML, and is used for encoding time-based captions.</span></span> <span data-ttu-id="c3148-106">Questo filtro converte i dati SAMI in un flusso di testo.</span><span class="sxs-lookup"><span data-stu-id="c3148-106">This filter converts SAMI data into a text stream.</span></span> <span data-ttu-id="c3148-107">Ogni esempio nel flusso contiene una voce di didascalia, insieme alle informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="c3148-107">Each sample in the stream contains one caption entry, along with format information.</span></span> <span data-ttu-id="c3148-108">I timestamp negli esempi vengono generati dalle informazioni sull'ora nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="c3148-108">The time stamps on the samples are generated from the time information in the SAMI file.</span></span>

<span data-ttu-id="c3148-109">Questo filtro è progettato per essere usato con il [filtro renderer del comando script](internal-script-command-renderer-filter.md) interno.</span><span class="sxs-lookup"><span data-stu-id="c3148-109">This filter is designed to be used with the [Internal Script Command Renderer](internal-script-command-renderer-filter.md) filter.</span></span> <span data-ttu-id="c3148-110">Il renderer del comando script interno riceve gli esempi di testo e li invia all'applicazione sotto forma di notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="c3148-110">The Internal Script Command Renderer receives the text samples and sends them to the application, in the form of event notifications.</span></span> <span data-ttu-id="c3148-111">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="c3148-111">For more information, see the Remarks section.</span></span>



| <span data-ttu-id="c3148-112">Label</span><span class="sxs-lookup"><span data-stu-id="c3148-112">Label</span></span> | <span data-ttu-id="c3148-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c3148-113">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3148-114">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="c3148-114">Filter Interfaces</span></span>                        | <span data-ttu-id="c3148-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="c3148-115">[**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="c3148-116">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="c3148-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="c3148-117">Flusso \_ MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c3148-117">MEDIATYPE\_Stream</span></span>                                                                                        |
| <span data-ttu-id="c3148-118">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="c3148-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="c3148-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c3148-119">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="c3148-120">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="c3148-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="c3148-121">Testo \_ MEDIATYPE, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="c3148-121">MEDIATYPE\_Text, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="c3148-122">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="c3148-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="c3148-123">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c3148-123">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="c3148-124">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="c3148-124">Filter CLSID</span></span>                             | <span data-ttu-id="c3148-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span><span class="sxs-lookup"><span data-stu-id="c3148-125">{33FACFE0-A9BE-11D0-A520-00A0D10129C0}</span></span>                                                                   |
| <span data-ttu-id="c3148-126">CLSID pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c3148-126">Property Page CLSID</span></span>                      | <span data-ttu-id="c3148-127">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="c3148-127">No property page</span></span>                                                                                         |
| <span data-ttu-id="c3148-128">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="c3148-128">Executable</span></span>                               | <span data-ttu-id="c3148-129">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="c3148-129">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="c3148-130">Merito</span><span class="sxs-lookup"><span data-stu-id="c3148-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="c3148-131">PROBABILITÀ \_ IMPROBABILE</span><span class="sxs-lookup"><span data-stu-id="c3148-131">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="c3148-132">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="c3148-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c3148-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c3148-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c3148-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3148-134">Remarks</span></span>

<span data-ttu-id="c3148-135">Di seguito è riportato un semplice file SAMI:</span><span class="sxs-lookup"><span data-stu-id="c3148-135">The following is a simple SAMI file:</span></span>


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



<span data-ttu-id="c3148-136">Il tag **STYLE** definisce due impostazioni della lingua, l'inglese (. ENCC) e francese (. FRCC).</span><span class="sxs-lookup"><span data-stu-id="c3148-136">The **STYLE** tag defines two language settings, English (.ENCC) and French (.FRCC).</span></span> <span data-ttu-id="c3148-137">Definisce anche due stili, \# NORMAL \# e GREENTEXT.</span><span class="sxs-lookup"><span data-stu-id="c3148-137">It also defines two styles, \#NORMAL and \#GREENTEXT.</span></span> <span data-ttu-id="c3148-138">Ogni tag **SYNC** definisce l'ora di inizio per una didascalia, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="c3148-138">Each **SYNC** tag defines the start time for a caption, in milliseconds.</span></span> <span data-ttu-id="c3148-139">I **tag P** contengono il testo della didascalia, mentre **l'attributo CLASS** specifica l'impostazione della lingua a cui si applica la didascalia.</span><span class="sxs-lookup"><span data-stu-id="c3148-139">The **P** tags contain the caption text, while the **CLASS** attribute specifies the language setting to which the caption applies.</span></span>

<span data-ttu-id="c3148-140">Per ogni linguaggio e stile, il filtro crea un flusso logico.</span><span class="sxs-lookup"><span data-stu-id="c3148-140">For each language and style, the filter creates a logical stream.</span></span> <span data-ttu-id="c3148-141">In qualsiasi momento, sono abilitati esattamente un flusso di linguaggio e un flusso di stile.</span><span class="sxs-lookup"><span data-stu-id="c3148-141">At any time, exactly one language stream and one style stream are enabled.</span></span> <span data-ttu-id="c3148-142">Quando il filtro genera un esempio, seleziona la didascalia per la lingua corrente e applica lo stile corrente.</span><span class="sxs-lookup"><span data-stu-id="c3148-142">When the filter generates a sample, it selects the caption for the current language and applies the current style.</span></span> <span data-ttu-id="c3148-143">Per impostazione predefinita, il primo linguaggio e stile dichiarati nel file sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="c3148-143">By default, the first language and style declared in the file are enabled.</span></span> <span data-ttu-id="c3148-144">Un'applicazione può usare [**il metodo IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) per abilitare un flusso diverso.</span><span class="sxs-lookup"><span data-stu-id="c3148-144">An application can use the [**IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) method to enable a different stream.</span></span>

<span data-ttu-id="c3148-145">Con le impostazioni predefinite, la prima didascalia nel file di esempio produce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="c3148-145">With the default settings, the first caption in the example file produces the following output:</span></span>


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



<span data-ttu-id="c3148-146">Se l'output passa al renderer del comando script interno, il filtro invia una [**notifica \_ dell'evento EC OLE \_ EVENT.**](ec-ole-event.md)</span><span class="sxs-lookup"><span data-stu-id="c3148-146">If the output goes to the Internal Script Command Renderer, that filter sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="c3148-147">Il secondo parametro dell'evento è un BSTR con il testo della didascalia.</span><span class="sxs-lookup"><span data-stu-id="c3148-147">The second event parameter is a BSTR with the caption text.</span></span> <span data-ttu-id="c3148-148">L'applicazione può recuperare l'evento e visualizzare la didascalia.</span><span class="sxs-lookup"><span data-stu-id="c3148-148">The application can retrieve the event and display the caption.</span></span>

<span data-ttu-id="c3148-149">L'esempio seguente illustra come eseguire il rendering di un file SAMI, recuperare informazioni sul flusso, abilitare i flussi e visualizzare il testo della didascalia.</span><span class="sxs-lookup"><span data-stu-id="c3148-149">The following example shows how to render a SAMI file, retrieve stream information, enable streams, and display caption text.</span></span> <span data-ttu-id="c3148-150">Nell'esempio si presuppone che il file SAMI precedente sia salvato come C: \\ Sami \_ test \_ file.sami.</span><span class="sxs-lookup"><span data-stu-id="c3148-150">The example assumes that the previous SAMI file is saved as C:\\Sami\_test\_file.sami.</span></span>

<span data-ttu-id="c3148-151">Per brevità, questo esempio usa indici di flusso hard-coded quando chiama il **metodo IAMStreamSelect::Enable.**</span><span class="sxs-lookup"><span data-stu-id="c3148-151">For brevity, this example used hard-coded stream indexes when it calls the **IAMStreamSelect::Enable** method.</span></span> <span data-ttu-id="c3148-152">Esegue anche il controllo degli errori minimo.</span><span class="sxs-lookup"><span data-stu-id="c3148-152">It also performs minimal error checking.</span></span>


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



<span data-ttu-id="c3148-153">Questo filtro usa [**l'interfaccia IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) per eseguire il pull degli esempi dal filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="c3148-153">This filter uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface to pull samples from the source filter.</span></span> <span data-ttu-id="c3148-154">Pertanto, non supporta [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="c3148-154">Therefore, it does not support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on its input pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3148-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3148-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3148-156">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="c3148-156">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



