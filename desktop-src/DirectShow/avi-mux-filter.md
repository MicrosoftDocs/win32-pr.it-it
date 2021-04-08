---
description: Filtro Mux AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro Mux AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876965"
---
# <a name="avi-mux-filter"></a>Filtro Mux AVI

Il filtro Mux AVI accetta più flussi di input e li invia in formato AVI. Il filtro usa i pin di input separati per ogni flusso di input e un pin di output per il flusso AVI.

Le applicazioni di creazione/acquisizione video possono usare questo filtro per salvare i file su disco in formato AVI. Il filtro è in genere connesso al filtro del [writer di file](file-writer-filter.md) , ma può connettersi a qualsiasi filtro il cui pin di input supporta le interfacce IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Qualsiasi tipo principale che corrisponde a un FOURCC di tipo obsoleto o MEDIATYPE_AUXLine21Data. Per ulteriori informazioni, vedere la <a href="fourccmap.md"><strong>classe FOURCCMap</strong></a>.
<ul>
<li>Se il tipo principale è MEDIATYPE_Audio, il formato deve essere FORMAT_WaveFormatEx.</li>
<li>Se il tipo principale è MEDIATYPE_Video, il formato deve essere FORMAT_VideoInfo o FORMAT_DvInfo.</li>
<li>Se il tipo principale è MEDIATYPE_Interleaved, il formato deve essere FORMAT_DvInfo.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_Avi</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_AviDest</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>qcap.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Commenti

Le osservazioni seguenti descrivono i vari aspetti della funzionalità del filtro Mux di AVI.

Segnaposto

Quando viene creato il filtro Mux AVI, è presente un pin di input. Quando ogni pin di input è connesso, il filtro crea un nuovo PIN di input.

Proprietà del flusso

I pin di input supportano l'interfaccia IPropertyBag per l'impostazione delle proprietà nei singoli flussi. Attualmente, viene definita la proprietà seguente:



| Proprietà | Descrizione                                                           |
|----------|-----------------------------------------------------------------------|
| name     | Nome del flusso. Questa proprietà viene scritta come `'strn'` blocco. |



 

Se il filtro è in esecuzione o in pausa, il metodo IPropertyBag:: Write restituisce \_ \_ lo stato VFW E non valido \_ .

Frequenza fotogrammi

Se il filtro upstream non specifica una frequenza dei fotogrammi nel membro **AvgTimePerFrame** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , il mux AVI usa i timestamp sul primo fotogramma video. Il formato di file AVI non supporta le frequenze dei fotogrammi variabili.

Frame eliminati

Il filtro Mux AVI calcola i frame eliminati in base ai tempi di supporto di ogni campione, se disponibili, oppure ai timestamp del campione. Scrive una voce di indice di lunghezza zero per ogni frame eliminato.

IMediaSeeking

Il filtro Mux AVI implementa l'interfaccia [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) come indicato di seguito:

-   Il metodo [**getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) restituisce lo stato di avanzamento corrente del multiplexing. Se si esegue la transcodifica di un file (più lento rispetto al tempo reale), questo valore è più preciso del valore restituito da Filter Graph Manager. Per ulteriori informazioni, vedere la sezione Osservazioni della pagina di riferimento di GetCurrentPosition.
-   Il metodo [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) esegue una query su ogni filtro upstream e restituisce la durata del flusso più lungo. Se uno di questi filtri ha esito negativo sulla chiamata GetDuration (o non supporta IMediaSeeking), il mux AVI restituisce un codice di errore e compila il parametro *pDuration* con la durata più lunga trovata. Tuttavia, il valore di *pDuration* in questo caso non è necessariamente la lunghezza del flusso di input più lungo.
-   AVI Mux non implementa i metodi GetStopPosition, GetPositions, GetAvailable, getrate o GetPreroll; né implementa alcun \* metodo set per la ricerca.

Estensioni del formato di file AVI 2,0

DirectShow supporta attualmente le estensioni del formato di file AVI 2,0 seguenti:

-   Aumento delle dimensioni del file AVI (maggiore di 1 GB)
-   Indicizzazione gerarchica

Per ulteriori informazioni, vedere la versione 1,02 delle "estensioni di formato file AVI OpenDML" pubblicate dal sottocomitato formato file OpenDML AVI M-JPEG.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



