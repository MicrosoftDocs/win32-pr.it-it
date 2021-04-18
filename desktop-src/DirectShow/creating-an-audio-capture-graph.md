---
description: Creazione di un grafico di acquisizione audio
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creazione di un grafico di acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304322"
---
# <a name="creating-an-audio-capture-graph"></a>Creazione di un grafico di acquisizione audio

Il primo passaggio per un'applicazione di acquisizione audio consiste nel creare un grafico di filtro. La configurazione del grafico dipende dal tipo di file che si desidera creare.

-   File AVI solo audio: filtro di acquisizione audio per il filtro [Mux AVI](avi-mux-filter.md) e Mux AVI al filtro del [writer di file](file-writer-filter.md) .
-   File WAV: filtro di acquisizione audio per l' [esempio di filtro WavDest](wavdest-filter-sample.md) nel filtro del writer di file
-   File Windows Media Audio (WMA): filtro di acquisizione audio per il filtro del [writer ASF WM](wm-asf-writer-filter.md) .

Il filtro WavDest viene fornito come esempio SDK. Per usarlo, è necessario compilare e registrare il filtro.

Per utilizzare il filtro del writer ASF, è necessario installare Windows Media SDK e ottenere una chiave software per sbloccare il filtro. Per ulteriori informazioni, vedere [utilizzo di Windows Media in DirectShow](using-windows-media-in-directshow.md).

È possibile compilare il grafo del filtro usando l'oggetto [Capture Graph Builder](capture-graph-builder.md) oppure è possibile compilare il grafo "Manually"; ovvero, fare in modo che l'applicazione aggiunga e connetta ogni filtro a livello di codice. Questo articolo descrive l'approccio manuale. Per ulteriori informazioni sull'utilizzo del generatore di grafici di acquisizione, vedere [acquisizione video](video-capture.md). Gran parte delle informazioni contenute in questo articolo si applica solo ai grafici di solo audio.

Aggiunta del dispositivo di acquisizione audio

Poiché il filtro di acquisizione audio comunica con un dispositivo hardware specifico, non è possibile chiamare semplicemente **CoCreateInstance** per creare il filtro. Usare invece l' [enumeratore System Device](system-device-enumerator.md) per enumerare tutti i dispositivi nella categoria "origini di acquisizione audio", identificata dall'identificatore di classe CLSID \_ AudioInputDeviceCategory.

L'enumeratore System Device restituisce un elenco di moniker per i dispositivi. il nome descrittivo di ogni moniker corrisponde al nome del dispositivo. Scegliere uno dei moniker restituiti e usarlo per creare un'istanza del filtro di acquisizione audio per quel dispositivo. Aggiungere il filtro al grafico filtro. Il dispositivo di registrazione audio preferito dell'utente viene visualizzato per primo nell'elenco dei moniker. (L'utente seleziona un dispositivo preferito facendo clic su suoni e Multimedia nel pannello di controllo).

Per ulteriori informazioni, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).

Per specificare l'input da cui eseguire l'acquisizione, ottenere l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) dal filtro di acquisizione audio e chiamare il metodo **put \_ Enable** per specificare l'input. Una limitazione di questo metodo, tuttavia, è che diversi dispositivi hardware possono usare stringhe diverse per identificare gli input. Ad esempio, una scheda può usare "Microphone" per identificare l'input del microfono e un'altra scheda può usare "MIC". Per determinare l'identificatore di stringa per un determinato input, usare le funzioni multimediali di Windows [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Per ulteriori informazioni, vedere l'argomento relativo alle [query del dispositivo mixer](/windows/desktop/Multimedia/mixer-device-queries) di MSDN.

Aggiunta del multiplexer e del writer di file

Un grafico di acquisizione audio deve contenere un multiplexer e un writer di file.

Un *multiplexer* è un filtro che combina uno o più flussi in un singolo flusso con un formato specifico. Ad esempio, il filtro Mux AVI combina i flussi audio e video in un flusso AVI con interfoliazione. Per l'acquisizione audio, in genere è presente un solo flusso audio, ma i dati audio devono comunque essere inclusi in un formato che può essere salvato su disco, che richiede un multiplexer. La scelta del multiplexer dipende dal formato di destinazione:

-   AVI: multiplexer AVI
-   WAV: WavDest
-   WMA: ASF Writer

Un *writer di file* è un filtro che scrive i dati in ingresso in un file. Per i file AVI o WAV, usare il [filtro del writer di file](file-writer-filter.md). Per i file WMA, il writer ASF funge sia da multiplexer che da writer di file.

Dopo aver creato i filtri e averli aggiunti al grafico, connettere il pin di output del filtro di acquisizione audio al pin di input del multiplexer e connettere il pin di output del multiplexer al pin di input del writer del filtro (presupponendo che si tratta di filtri distinti). Per specificare il nome del file, eseguire una query sul writer di file per l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chiamare il metodo [**IFileSinkFilter:: myFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) .

### <a name="example-code"></a>Codice di esempio

Nell'esempio seguente viene illustrato come compilare un grafico di acquisizione audio usando il filtro WavDest. Gli stessi principi valgono per gli altri tipi di file.


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



Questo esempio usa la `AddFilterByCLSID` funzione descritta in [aggiungere un filtro in base a CLSID](add-a-filter-by-clsid.md)e la `ConnectFilters` funzione descritta in [connettere due filtri](connect-two-filters.md). Nessuna di queste è un'API DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 
