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
# <a name="sami-cc-parser-filter"></a>Filtro parser SAMI (CC)

Analizza i dati di didascalia da file SAMI (Synchronized Media Interchange).

SAMI è un formato di testo simile a HTML e viene usato per codificare didascalie basate sul tempo. Questo filtro converte i dati SAMI in un flusso di testo. Ogni esempio nel flusso contiene una voce di didascalia, insieme alle informazioni sul formato. Il timestamp degli esempi viene generato dalle informazioni sull'ora nel file SAMI.

Questo filtro è progettato per essere utilizzato con il filtro di [renderer del comando script interno](internal-script-command-renderer-filter.md) . Il renderer interno del comando script riceve gli esempi di testo e li invia all'applicazione sotto forma di notifiche degli eventi. Per altre informazioni, vedere la sezione Osservazioni.



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipi di supporti pin di input                    | \_Flusso MEDIATYPE                                                                                        |
| Interfacce pin di input                     | [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipi di supporti pin di output                   | \_Testo MEDIATYPE, MEDIASUBTYPE \_ null                                                                      |
| Interfacce del PIN di output                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                         |
| File eseguibile                               | quartz.dll                                                                                               |
| [Merito](merit.md)                       | VALORE \_ improbabile                                                                                          |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                            |



 

## <a name="remarks"></a>Commenti

Di seguito è riportato un semplice file SAMI:


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



Il tag di **stile** definisce due impostazioni della lingua, inglese (. ENCC) e francese (. FRCC). Definisce anche due stili, \# Normal e \# GREENTEXT. Ogni tag di **sincronizzazione** definisce l'ora di inizio per una didascalia, in millisecondi. I tag **P** contengono il testo della didascalia, mentre l'attributo **Class** specifica l'impostazione della lingua a cui si applica la didascalia.

Per ogni lingua e stile, il filtro crea un flusso logico. In qualsiasi momento, sono abilitati esattamente un flusso di lingua e un flusso di stile. Quando il filtro genera un campione, viene selezionata la didascalia per la lingua corrente e viene applicato lo stile corrente. Per impostazione predefinita, il primo linguaggio e lo stile dichiarati nel file sono abilitati. Un'applicazione può usare il metodo [**IAMStreamSelect:: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) per abilitare un flusso diverso.

Con le impostazioni predefinite, la prima didascalia del file di esempio produce l'output seguente:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Se l'output passa al renderer interno del comando script, tale filtro Invia una notifica degli eventi dell' [**\_ \_ evento OLE EC**](ec-ole-event.md) . Il secondo parametro dell'evento è un BSTR con il testo della didascalia. L'applicazione può recuperare l'evento e visualizzare la didascalia.

Nell'esempio seguente viene illustrato come eseguire il rendering di un file SAMI, recuperare informazioni sul flusso, abilitare i flussi e visualizzare il testo della didascalia. Nell'esempio si presuppone che il file SAMI precedente venga salvato come file di test C: \\ Sami \_ \_ . Sami.

Per brevità, in questo esempio vengono utilizzati indici di flusso hardcoded quando viene chiamato il metodo **IAMStreamSelect:: Enable** . Esegue anche il controllo minimo degli errori.


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



Questo filtro usa l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) per eseguire il pull degli esempi dal filtro di origine. Pertanto, non supporta l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul relativo pin di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



