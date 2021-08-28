---
description: Filtro Mux AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro Mux AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3250746a65aaaf075c28700c3531bf97b1faf23
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986264"
---
# <a name="avi-mux-filter"></a>Filtro Mux AVI

Il filtro Mux AVI accetta più flussi di input e li interfolia in formato AVI. Il filtro usa pin di input separati per ogni flusso di input e un pin di output per il flusso AVI.

Le applicazioni di acquisizione o creazione di video possono usare questo filtro per salvare i file su disco in formato AVI. Il filtro è in genere connesso al filtro [Writer](file-writer-filter.md) file, ma può connettersi a qualsiasi filtro il cui pin di input supporta le interfacce IStream e [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages | 
| Tipi di supporti pin di input | Qualsiasi tipo principale che corrisponde a un tipo FOURCC o MEDIATYPE_AUXLine21Data. Per altre informazioni, vedere <a href="fourccmap.md"><strong>Classe FOURCCMap.</strong></a><ul><li>Se il tipo principale è MEDIATYPE_Audio, il formato deve essere FORMAT_WaveFormatEx.</li><li>Se il tipo principale è MEDIATYPE_Video, il formato deve essere FORMAT_VideoInfo o FORMAT_DvInfo.</li><li>Se il tipo principale è MEDIATYPE_Interleaved, il formato deve essere FORMAT_DvInfo.</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | MEDIATYPE_Stream, MEDIASUBTYPE_Avi | 
| Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| CLSID del filtro | CLSID_AviDest | 
| CLSID pagina delle proprietà | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | 
| File eseguibile | qcap.dll | 
| <a href="merit.md">Merito</a> | MERIT_DO_NOT_USE | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Commenti

Le osservazioni seguenti descrivono vari aspetti della funzionalità del filtro Mux AVI.

Segnaposto

Quando viene creato, il filtro Mux AVI ha un pin di input. Quando ogni pin di input è connesso, il filtro crea un nuovo pin di input.

Proprietà del flusso

I pin di input supportano l'interfaccia IPropertyBag per l'impostazione delle proprietà nei singoli flussi. Attualmente è definita la proprietà seguente:



| Proprietà | Descrizione                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Nome del flusso. Questa proprietà viene scritta come `'strn'` blocco. |



 

Se il filtro è in esecuzione o sospeso, il metodo IPropertyBag::Write restituisce VFW \_ E \_ WRONG \_ STATE.

Frequenza dei fotogrammi

Se il filtro upstream non specifica una frequenza dei fotogrammi nel membro **AvgTimePerFrame** della struttura [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) il mux AVI usa i timestamp nel primo fotogramma video. Il formato di file AVI non supporta frequenze di fotogrammi variabili.

Frame eliminati

Il filtro Mux AVI calcola i fotogrammi rilasciati in base ai tempi multimediali di ogni campione, se disponibili, oppure ai timestamp del campione. Scrive una voce di indice di lunghezza zero per ogni frame eliminato.

IMediaSeeking

Il filtro Mux AVI implementa [**l'interfaccia IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) come indicato di seguito:

-   Il [**metodo GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisce lo stato di avanzamento corrente del multiplexing. Se si sta transcodendo un file (più lento rispetto al tempo reale), questo valore è più accurato del valore restituito da Filter Graph Manager. Per altre informazioni, vedere la sezione Osservazioni della pagina di riferimento getCurrentPosition.
-   Il [**metodo GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) esegue una query su ogni filtro upstream e restituisce la durata del flusso più lungo. Se uno di questi filtri non riesce a chiamare GetDuration (o non supporta IMediaSeeking), il mux AVI restituisce un codice di errore e inserisce nel parametro *pDuration* la durata più lunga trovata. Tuttavia, il valore di *pDuration* in questo caso non corrisponde necessariamente alla lunghezza del flusso di input più lungo.
-   Il mux AVI non implementa i metodi GetStopPosition, GetPositions, GetAvailable, GetRate o GetPreroll. né implementa metodi Set \* per la ricerca.

Estensioni di formato di file AVI 2.0

DirectShow attualmente supporta le estensioni di formato di file AVI 2.0 seguenti:

-   Aumento delle dimensioni del file AVI (superiore a 1 GB)
-   Indicizzazione gerarchica

Per altre informazioni, vedere la versione 1.02 di "OpenDML AVI File Format Extensions" pubblicata dal sottocommit OpenDML M-JPEG File Format Subcommittee.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



