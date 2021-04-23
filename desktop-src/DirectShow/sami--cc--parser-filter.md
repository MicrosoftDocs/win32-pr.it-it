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
# <a name="sami-cc-parser-filter"></a>Filtro parser SAMI (CC)

Analizza i dati dei sottotitoli dai file SAMI (Synchronized Accessible Media Interchange).

SAMI è un formato di testo simile a HTML e viene usato per codificare sottotitoli basati sul tempo. Questo filtro converte i dati SAMI in un flusso di testo. Ogni esempio nel flusso contiene una voce di didascalia, insieme alle informazioni sul formato. I timestamp negli esempi vengono generati dalle informazioni sull'ora nel file SAMI.

Questo filtro è progettato per essere usato con il [filtro renderer del comando script](internal-script-command-renderer-filter.md) interno. Il renderer del comando script interno riceve gli esempi di testo e li invia all'applicazione sotto forma di notifiche degli eventi. Per altre informazioni, vedere la sezione Osservazioni.



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Tipi di supporti pin di input                    | Flusso \_ MEDIATYPE                                                                                        |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Tipi di supporti pin di output                   | Testo \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                      |
| Interfacce pin di output                    | [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID del filtro                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                         |
| File eseguibile                               | quartz.dll                                                                                               |
| [Merito](merit.md)                       | PROBABILITÀ \_ IMPROBABILE                                                                                          |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

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



Il tag **STYLE** definisce due impostazioni della lingua, l'inglese (. ENCC) e francese (. FRCC). Definisce anche due stili, \# NORMAL \# e GREENTEXT. Ogni tag **SYNC** definisce l'ora di inizio per una didascalia, in millisecondi. I **tag P** contengono il testo della didascalia, mentre **l'attributo CLASS** specifica l'impostazione della lingua a cui si applica la didascalia.

Per ogni linguaggio e stile, il filtro crea un flusso logico. In qualsiasi momento, sono abilitati esattamente un flusso di linguaggio e un flusso di stile. Quando il filtro genera un esempio, seleziona la didascalia per la lingua corrente e applica lo stile corrente. Per impostazione predefinita, il primo linguaggio e stile dichiarati nel file sono abilitati. Un'applicazione può usare [**il metodo IAMStreamSelect::Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) per abilitare un flusso diverso.

Con le impostazioni predefinite, la prima didascalia nel file di esempio produce l'output seguente:


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Se l'output passa al renderer del comando script interno, il filtro invia una [**notifica \_ dell'evento EC OLE \_ EVENT.**](ec-ole-event.md) Il secondo parametro dell'evento è un BSTR con il testo della didascalia. L'applicazione può recuperare l'evento e visualizzare la didascalia.

L'esempio seguente illustra come eseguire il rendering di un file SAMI, recuperare informazioni sul flusso, abilitare i flussi e visualizzare il testo della didascalia. Nell'esempio si presuppone che il file SAMI precedente sia salvato come C: \\ Sami \_ test \_ file.sami.

Per brevità, questo esempio usa indici di flusso hard-coded quando chiama il **metodo IAMStreamSelect::Enable.** Esegue anche il controllo degli errori minimo.


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



Questo filtro usa [**l'interfaccia IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) per eseguire il pull degli esempi dal filtro di origine. Pertanto, non supporta [**l'interfaccia IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



