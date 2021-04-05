---
description: Implementazione di IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementazione di IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590dffcf762d22155a89a8143994d9a4d8bcab02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883978"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementazione di IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Inizializzare](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Eseguire il commit](#commit)
    -   [Anteprima](#setpreview)
-   [Argomenti correlati](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Inizializzare](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Eseguire il commit](#commit)
-   [Anteprima](#setpreview)

Questa interfaccia è la controparte dell'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) ed è il punto di partenza per la codifica di un file di immagine. Proprio come **IWICBitmapDecoder** viene usato per recuperare le proprietà a livello di contenitore e i singoli frame dal contenitore di immagini, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) viene usato per impostare le proprietà a livello di contenitore e serializzare i singoli frame di immagine nel contenitore. Questa interfaccia viene implementata nella classe del codificatore a livello di contenitore.

``` syntax
interface IWICBitmapEncoder : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IStream *pIStream,
              WICBitmapEncoderCacheOption cacheOption );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetEncoderInfo ( IWICBitmapEncoderInfo **pIEncoderInfo );
   HRESULT CreateNewFrame ( IWICBitmapFrameEncode **ppIFrameEncode,
              IPropertyBag2 **ppIEncoderOptions );
   HRESULT Commit ( void );

   // Optional methods
   HRESULT SetPreview ( IWICBitmapSource *pIPreview );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT SetColorContexts ( UINT cCount,
              IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
              **ppIMetadataQueryWriter );
   HRESULT SetPalette ( IWICPalette *pIPalette);
};
```

Come illustrato nell'argomento relativo all' [implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md), alcuni formati di immagine hanno anteprime globali, contesti di colore o metadati, mentre molti formati di immagine li forniscono solo in base ai singoli frame. I metodi per l'impostazione di questi metodi sono pertanto facoltativi in [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder), ma sono necessari in [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode). Verranno illustrati i metodi facoltativi in **IWICBitmapEncoder** nella sezione di **IWICBitmapFrameEncode**, in cui sono implementati più di frequente.

Se non sono supportate le anteprime globali, restituire WINCODEC \_ Err \_ CODECNOTHUMBNAIL dal metodo sethumbnail su [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Se non si supporta una tavolozza a livello di contenitore o se l'immagine che si sta codificando non ha un formato indicizzato, restituire WINCODEC \_ Err \_ PALETTEUNAVAILABLE dal metodo sepalette. Per tutti gli altri metodi non supportati, restituire WINCODEC \_ Err \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inizializzare

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) è il primo metodo richiamato su un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) dopo che ne è stata creata un'istanza. Un flusso di immagini viene passato al codificatore e un chiamante può facoltativamente specificare un'opzione cache. Nel caso del decodificatore, il flusso è di sola lettura, ma il flusso passato a un codificatore è un flusso scrivibile, in cui il codificatore eseguirà la serializzazione di tutti i dati e i metadati dell'immagine. Anche le opzioni della cache nel codificatore sono diverse.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

L'applicazione può scegliere di richiedere al codificatore di memorizzare nella cache i dati dell'immagine in memoria, memorizzarli nella cache in un file temporaneo o scriverli direttamente nel file su disco senza Caching. Quando viene richiesto di memorizzare nella cache i dati in un file temporaneo, il codificatore deve creare un file temporaneo su disco e scrivere direttamente in tale file senza caching in memoria. Quando il chiamante seleziona l'opzione no cache, è necessario eseguire il commit di ogni frame in ordine prima che sia possibile creare il frame successivo.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) viene implementato in modo analogo al metodo [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) nell' [implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) restituisce un oggetto [**IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) . Per ottenere l'oggetto **IWICBitmapEncoderInfo** , è sufficiente passare il GUID del codificatore al metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), quindi richiedere l'interfaccia **IWICBitmapEncoderInfo** .

Vedere l'esempio in [implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) in [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) è la controparte del codificatore di [**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) in [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder). Questo metodo restituisce un oggetto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , ovvero l'oggetto che serializza effettivamente i dati dell'immagine per un frame specifico all'interno del contenitore.

Uno dei vantaggi di Windows Imaging Component (WIC) è che fornisce un livello di astrazione per le applicazioni che consente loro di utilizzare tutti i formati di immagine nello stesso modo. Tuttavia, non tutti i formati di immagine sono esattamente uguali. Alcuni formati di immagine hanno funzionalità non disponibili in altri. Affinché le applicazioni possano sfruttare i vantaggi di queste funzionalità esclusive, è necessario fornire un modo per il codec per esporle. Questo è lo scopo delle opzioni del codificatore. Se il codec supporta le opzioni del codificatore, è necessario creare un oggetto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che espone le opzioni del codificatore supportate e restituirlo nel parametro *ppIEncoderOptions* di questo metodo. Il chiamante può quindi usare questo oggetto IPropertyBag2 per determinare quali opzioni del codificatore supporta il codec. Se il chiamante desidera specificare i valori per una qualsiasi delle opzioni del codificatore supportate, assegnerà il valore alla proprietà pertinente nell'oggetto IPropertyBag2 e lo passerà all'oggetto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) appena creato nel relativo metodo Initialize.

Per creare un'istanza di un oggetto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , è prima di tutto necessario creare uno struct Campo PROPBAG2 per specificare ogni opzione del codificatore supportata dal codificatore e il tipo di dati per ogni proprietà. Quindi, è necessario implementare un oggetto IPropertyBag2 che impone gli intervalli di valori per ogni proprietà in scrittura e riconcilia tutti i valori in conflitto o sovrapposti. Per i set semplici di opzioni del codificatore non in conflitto, è possibile richiamare il metodo [**CreateEncoderPropertyBag**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) , che creerà un semplice oggetto IPropertyBag2 usando le proprietà specificate nello struct Campo PROPBAG2. È comunque necessario applicare gli intervalli di valori. Per le opzioni del codificatore più avanzate o per risolvere i conflitti, è necessario scrivere un'implementazione IPropertyBag2 personalizzata.


```C++
UINT cuiPropertyCount = 0;
IPropertyBag2* pPropertyBag = NULL;
PROPBAG2* pPropBagOptions;
HRESULT hr;

// Insert code here to initialize piPropertyBag with the 
// supported options for your encoder, and to initialize 
// cuiPropertyCount to the number of encoder option properties
// you are exposing.
...

hr = pComponentFactory->CreateEncoderPropertyBag( 
   pPropBagOptions, cuiPropertyCount, &pPropertyBag);
```



WIC fornisce un piccolo set di opzioni del codificatore canonico utilizzate da alcuni formati di immagine comuni. Tutte le opzioni del codificatore canonico sono facoltative e i codec non sono necessari per supportarli. Il motivo per cui vengono fornite come opzioni canoniche è che molte applicazioni espongono l'interfaccia utente per consentire agli utenti di specificare queste opzioni quando si salva un file di immagine in un formato che li supporta. Fornire un metodo canonico per specificare queste opzioni consente alle applicazioni di comunicare con facilità ai codificatori in modo coerente. Le opzioni del codificatore canonico sono elencate nella tabella seguente.



| Opzione del codificatore     | VARTYPE  | Gamma valori               |
|--------------------|----------|---------------------------|
| Lossless           | \_bool VT | Vero/Falso                |
| ImageQuality       | \_R4 VT   | 0.0-1,0                   |
| CompressionQuality | \_R4 VT   | 0.0-1,0                   |
| BitmapTransform    | \_Ui1 VT  | WICBitmapTransformOptions |



 

Se il codec supporta la codifica senza perdita di codice, è necessario esporre l'opzione del codificatore lossless come metodo per le applicazioni per richiedere che un'immagine venga codificata senza perdita di codice. Se un chiamante imposta questa proprietà su true, è necessario ignorare l'opzione ImageQuality e codificare l'immagine senza perdita di pagina.

L'opzione ImageQuality consente a un'applicazione di specificare il grado di fedeltà con cui codificare l'immagine. Questa opzione consente a un utente di raggiungere un compromesso tra la qualità dell'immagine e la velocità e/o le dimensioni del file. JPEG è un esempio di formato di immagine che supporta questo compromesso. Il valore 0,0 indica che la fedeltà è di importanza bassa e che il codificatore deve utilizzare l'algoritmo con la massima perdita. Il valore 1,0 indica che la fedeltà è la più importante e che il codificatore deve mantenere la massima fedeltà possibile. (A seconda del codec, questo potrebbe essere sinonimo di opzione Lossless). Tuttavia, se il codec supporta la codifica lossless e se l'opzione lossless è impostata su true, l'opzione ImageQuality deve essere ignorata.

L'opzione CompressionQuality consente a un'applicazione di specificare l'efficienza della compressione da usare durante la codifica dell'immagine. Un algoritmo molto efficiente può produrre un file di immagine più piccolo con la stessa qualità di un algoritmo di compressione meno efficiente, ma potrebbe richiedere più tempo per la codifica. Questa opzione consente a un utente di specificare un compromesso tra le dimensioni del file e la velocità di codifica, conservando allo stesso tempo lo stesso livello di qualità. TIFF è un esempio di formato di immagine che supporta questo compromesso. Si noti che un formato, ad esempio JPEG, supporta diversi livelli di compressione, ma una maggiore velocità di compressione comporta una riduzione della qualità dell'immagine. Pertanto, un formato di immagine JPEG esporrà l'opzione ImageQuality anziché l'opzione CompressionQuality. Il valore 0,0 per questa opzione indica che è necessario comprimere l'immagine il più rapidamente possibile, senza ridurre la fedeltà, a scapito di una dimensione di file più grande. Il valore 1,0 indica che è necessario creare le dimensioni più piccole possibile del file (allo stesso livello di qualità), indipendentemente dal tempo necessario per la codifica. Un codec può supportare sia l'opzione ImageQuality che l'opzione CompressionQuality, dove l'opzione ImageQuality specifica il grado accettabile di lossiness e l'opzione CompressionQuality offre un compromesso di dimensioni/velocità al livello di qualità specificato.

L'opzione BitmapTransform consente al chiamante di specificare un angolo di rotazione o un orientamento verticale o orizzontale per il capovolgimento durante la codifica. L'enumerazione WICBitmapTransformOptions utilizzata per specificare la trasformazione richiesta è la stessa enum utilizzata per la richiesta di una trasformazione durante la decodifica tramite l'interfaccia IWICBitmapSourceTransform.

Si noti che i codificatori non sono limitati alle opzioni del codificatore canonico. Lo scopo delle opzioni del codificatore è consentire ai codificatori di esporre le proprie funzionalità e non esiste alcun limite ai tipi di funzionalità che è possibile esporre. Verificare che le opzioni del codificatore siano ben documentate. Anche se un'applicazione può usare il contenitore delle proprietà restituito da questo metodo per individuare i nomi, i tipi e gli intervalli di valori per le opzioni supportate, l'unico modo per individuare i significati o come esporli nell'interfaccia utente è dalla documentazione.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) è il metodo chiamato dopo che tutti i dati e i metadati dell'immagine sono stati serializzati nel flusso. È consigliabile usare questo metodo per serializzare i dati dell'immagine di anteprima nel flusso e qualsiasi anteprima globale, metadati, tavolozza o altri elementi, se applicabile. Questo metodo non deve chiudere il flusso di file, perché l'applicazione che ha aperto il flusso è prevista per chiuderla.

La sezione nel metodo IWICBitmapFrameEncode: commit contiene informazioni dettagliate sul modo in cui IWICBitmapEncoderCacheOptions influisce sul comportamento di questo metodo.

### <a name="setpreview"></a>Anteprima

L' [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) viene utilizzata per creare un'anteprima dell'immagine. Sebbene non sia strettamente necessario che ogni immagine disponga di un'anteprima, si consiglia vivamente di usarla. Le fotocamere digitali e gli scanner moderni generano immagini con risoluzione molto elevata, che tendono a essere molto grandi e, di conseguenza, importano un tempo di elaborazione significativo per la decodifica. Le immagini della prossima generazione di fotocamere saranno ancora più grandi. È consigliabile fornire una versione più piccola, più bassa della risoluzione, di un'immagine, in genere in formato JPEG, che può essere rapidamente decodificata e visualizzata "immediatamente" quando un utente la richiede. Un'applicazione può richiedere un'anteprima prima di richiedere la decodifica dell'immagine effettiva per offrire un'esperienza migliore per gli utenti e mostrare loro una rappresentazione delle dimensioni dello schermo dell'immagine mentre sono in attesa di decodificare l'immagine effettiva. Sebbene i codec forniscano anteprime, i codec che non supportano [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) devono assolutamente farlo.

Se si fornisce un'anteprima JPEG, non è necessario scrivere un codificatore JPEG per codificarlo. È necessario delegare il codificatore JPEG fornito con la piattaforma WIC per la codifica di anteprime e anteprime.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfacce del codificatore](-wic-encoderinterfaces.md)
</dt> <dt>

[Implementazione di IWICBitmapCodecProgressNotification (encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
