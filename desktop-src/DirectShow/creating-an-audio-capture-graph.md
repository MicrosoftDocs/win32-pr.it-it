---
description: Creazione di un'acquisizione audio Graph
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Creazione di un'acquisizione audio Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ff89cff8662bb5da81860053221596b18e89ab2300134cf2ff8826ae99b787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108221"
---
# <a name="creating-an-audio-capture-graph"></a>Creazione di un'acquisizione audio Graph

Il primo passaggio per un'applicazione di acquisizione audio consiste nel creare un grafo di filtro. La configurazione del grafo dipende dal tipo di file che si vuole creare.

-   File AVI solo audio: filtro di acquisizione audio per il filtro [Mux AVI](avi-mux-filter.md) e filtro da Mux AVI a [writer di](file-writer-filter.md) file.
-   File WAV: filtro di acquisizione audio per [il filtro WavDest di esempio](wavdest-filter-sample.md) per il filtro writer di file
-   Windows File audio multimediale (.wma): filtro di acquisizione audio per [il filtro WM ASF Writer.](wm-asf-writer-filter.md)

Il filtro WavDest viene fornito come esempio SDK. Per usarlo, è necessario compilare e registrare il filtro.

Per usare il filtro di ASF Writer, è necessario installare Windows Media SDK e ottenere una chiave software per sbloccare il filtro. Per altre informazioni, vedere [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).

È possibile compilare il grafico dei filtri usando [l'oggetto Capture Graph Builder](capture-graph-builder.md) oppure è possibile compilare il grafo "manualmente". in altri, fare in modo che l'applicazione a livello di codice a ogni filtro sia aggiunto e connesso. Questo articolo descrive l'approccio manuale. Per altre informazioni sull'uso di Capture Graph Builder, vedere [Acquisizione video.](video-capture.md) Gran parte delle informazioni contenute in questo articolo si applica ai grafici solo audio.

Aggiunta del dispositivo di acquisizione audio

Poiché il filtro di acquisizione audio comunica con un dispositivo hardware specifico, non è sufficiente chiamare **CoCreateInstance** per creare il filtro. Usare invece System [Device Enumerator](system-device-enumerator.md) per enumerare tutti i dispositivi nella categoria "Origini di acquisizione audio", identificata dall'identificatore di classe CLSID \_ AudioInputDeviceCategory.

System Device Enumerator restituisce un elenco di moniker per i dispositivi. Il nome descrittivo di ogni moniker corrisponde al nome del dispositivo. Scegliere uno dei moniker restituiti e usarlo per creare un'istanza del filtro di acquisizione audio per il dispositivo. Aggiungere il filtro al grafico dei filtri. Il dispositivo di registrazione audio preferito dell'utente viene visualizzato per primo nell'elenco dei moniker. L'utente seleziona un dispositivo preferito facendo clic su Suoni e funzionalità multimediali Pannello di controllo.

Per altre informazioni, vedere [Using the System Device Enumerator](using-the-system-device-enumerator.md).

Per specificare l'input da cui acquisire, ottenere l'interfaccia [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) dal filtro Acquisizione audio e chiamare il metodo **\_ put Enable** per specificare l'input. Una limitazione di questo metodo, tuttavia, è che dispositivi hardware diversi possono usare stringhe diverse per identificare i relativi input. Ad esempio, una scheda può usare "Microfono" per identificare l'input del microfono e un'altra scheda può usare "Mic". Per determinare l'identificatore di stringa per un determinato input, usare le funzioni Windows Multimedia [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))e [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Per altre informazioni, [vedere l'Mixer MSDN sulle query](/windows/desktop/Multimedia/mixer-device-queries) sui dispositivi.

Aggiunta del multiplexer e del writer di file

Un grafo di acquisizione audio deve contenere un multiplexer e un writer di file.

Un *multiplexer* è un filtro che combina uno o più flussi in un singolo flusso con un formato specifico. Ad esempio, il filtro Mux AVI combina i flussi audio e video in un flusso AVI interleaved. Per l'acquisizione audio, in genere è presente un solo flusso audio, ma i dati audio devono comunque essere in pacchetto in un formato che può essere salvato su disco, che richiede un multiplexer. La scelta del multiplexer dipende dal formato di destinazione:

-   AVI: AVI Multiplexer
-   WAV: WavDest
-   WMA: ASF Writer

Un *writer di file* è un filtro che scrive i dati in ingresso in un file. Per i file AVI o WAV, usare [il filtro writer di file](file-writer-filter.md). Per i file WMA, ASF Writer funge sia da multiplexer che da writer di file.

Dopo aver creato i filtri e averli aggiunti al grafo, connettere il pin di output del filtro di acquisizione audio al pin di input del multiplexer e connettere il pin di output del multiplexer al pin di input del writer di filtri (presupponendo che si tratta di filtri separati). Per specificare il nome del file, eseguire una query sul writer di file per l'interfaccia [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) e chiamare il [**metodo IFileSinkFilter::SetFileName.**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename)

### <a name="example-code"></a>Codice di esempio

L'esempio seguente illustra come creare un grafico di acquisizione audio usando il filtro WavDest. Gli stessi principi si applicano agli altri tipi di file.


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



In questo esempio viene utilizzata la funzione descritta in Aggiungere un filtro in base `AddFilterByCLSID` [al CLSID](add-a-filter-by-clsid.md)e la funzione descritta `ConnectFilters` in Connessione Due [filtri](connect-two-filters.md). Nessuno di questi è un'API DirectShow.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione audio](audio-capture.md)
</dt> </dl>

 

 
