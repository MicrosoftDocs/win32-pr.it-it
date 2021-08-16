---
description: Implementazione di IWICBitmapEncoder
ms.assetid: b671e941-ded6-4bde-bc4d-461f13feade0
title: Implementazione di IWICBitmapEncoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69d02105470f837dba0689b665473c01c42f6cd6497a85424ea6eea3371696f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088013"
---
# <a name="implementing-iwicbitmapencoder"></a>Implementazione di IWICBitmapEncoder

-   [IWICBitmapEncoder](#implementing-iwicbitmapencoder)
    -   [Inizializzare](#initialize)
    -   [GetContainerFormat](#getcontainerformat)
    -   [GetEncoderInfo](#getencoderinfo)
    -   [CreateNewFrame](#createnewframe)
    -   [Eseguire il commit](#commit)
    -   [SetPreview](#setpreview)
-   [Argomenti correlati](#related-topics)

## <a name="iwicbitmapencoder"></a>IWICBitmapEncoder

-   [Inizializzare](#initialize)
-   [GetContainerFormat](#getcontainerformat)
-   [GetEncoderInfo](#getencoderinfo)
-   [CreateNewFrame](#createnewframe)
-   [Eseguire il commit](#commit)
-   [SetPreview](#setpreview)

Questa interfaccia è la controparte [**dell'interfaccia IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) ed è il punto di partenza per la codifica di un file di immagine. Proprio come **IWICBitmapDecoder** viene usato per recuperare le proprietà a livello di contenitore e i singoli fotogrammi dal contenitore di immagini, [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) viene usato per impostare le proprietà a livello di contenitore e serializzare singoli fotogrammi di immagine nel contenitore. Questa interfaccia viene implementata nella classe del codificatore a livello di contenitore.

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

Come illustrato in [Implementazione di IWICBitmapDecoder,](-wic-imp-iwicbitmapdecoder.md)alcuni formati di immagine hanno anteprime globali, contesti di colore o metadati, mentre molti formati di immagine li forniscono solo per ogni fotogramma. I metodi per l'impostazione sono pertanto facoltativi in [**IWICBitmapEncoder,**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)ma sono necessari in [**IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) Verranno illustrati i metodi facoltativi in **IWICBitmapEncoder** nella sezione su **IWICBitmapFrameEncode,** dove vengono implementati più comunemente.

Se non si supportano anteprime globali, restituire WINCODEC \_ ERR \_ CODECNOTHUMBNAIL dal metodo SetThumbnail in [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Se non si supporta un riquadro a livello di contenitore o se l'immagine da codificare non ha un formato indicizzato, restituire WINCODEC \_ ERR \_ PALETTEUNAVAILABLE dal metodo SetPalette. Per qualsiasi altro metodo non supportato, restituire WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION.

### <a name="initialize"></a>Inizializzare

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) è il primo metodo richiamato su [**un oggetto IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) dopo la creazione di un'istanza. Un flusso di immagini viene passato al codificatore e un chiamante può specificare facoltativamente un'opzione di cache. Nel caso del decodificatore, il flusso è di sola lettura, ma il flusso passato a un codificatore è un flusso scrivibile in cui il codificatore serializza tutti i metadati e i dati dell'immagine. Anche le opzioni della cache nel codificatore sono diverse.

``` syntax
enum WICBitmapEncoderCacheOption
{
   WICBitmapEncoderCacheInMemory,
   WICBitmapEncoderCacheTempFile,
   WICBitmapEncoderNoCache
}
```

L'applicazione può scegliere di richiedere al codificatore di memorizzare nella cache i dati dell'immagine in memoria, memorizzarla nella cache in un file temporaneo o scriverla direttamente nel file su disco senza memorizzazione nella cache. Quando viene richiesto di memorizzare nella cache i dati in un file temporaneo, il codificatore deve creare un file temporaneo su disco e scrivere direttamente in tale file senza memorizzare nella cache in memoria. Quando il chiamante seleziona l'opzione nessuna cache, è necessario eseguire il commit di ogni frame in ordine prima di poter creare il frame successivo.

### <a name="getcontainerformat"></a>GetContainerFormat

[**GetContainerFormat viene**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat) implementato come il [metodo GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) in [Implementazione di IWICBitmapDecoder.](-wic-imp-iwicbitmapdecoder.md)

### <a name="getencoderinfo"></a>GetEncoderInfo

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo) restituisce un [**oggetto IWICBitmapEncoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo) Per ottenere **l'oggetto IWICBitmapEncoderInfo,** è sufficiente passare il GUID del codificatore al metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e quindi richiedere l'interfaccia **IWICBitmapEncoderInfo.**

Vedere l'esempio in [Implementazione di IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) in [GetDecoderInfo](-wic-imp-iwicbitmapdecoder.md).

### <a name="createnewframe"></a>CreateNewFrame

[**CreateNewFrame è**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) la controparte del codificatore [**di GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) in [**IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Questo metodo restituisce un [**oggetto IWICBitmapFrameEncode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) ovvero l'oggetto che serializza effettivamente i dati dell'immagine per un frame specifico all'interno del contenitore.

Uno dei vantaggi di Windows Imaging Component (WIC) è che offre un livello di astrazione per le applicazioni che consente loro di usare tutti i formati di immagine nello stesso modo. Tuttavia, non tutti i formati di immagine sono esattamente gli stessi. Alcuni formati di immagine hanno funzionalità che altri non hanno. Per consentire alle applicazioni di sfruttare queste funzionalità univoche, è necessario fornire al codec un modo per esporle. Questo è lo scopo delle opzioni del codificatore. Se il codec supporta le opzioni del codificatore, è necessario creare un oggetto [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) che espone le opzioni del codificatore supportate e restituirlo nel parametro *ppIEncoderOptions* di questo metodo. Il chiamante può quindi usare questo oggetto IPropertyBag2 per determinare le opzioni del codificatore supportate dal codec. Se il chiamante vuole specificare valori per una delle opzioni del codificatore supportate, assegna il valore alla proprietà pertinente nell'oggetto IPropertyBag2 e lo passa all'oggetto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) appena creato nel metodo Initialize.

Per creare un'istanza di un oggetto [IPropertyBag2,](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) è prima necessario creare uno struct PROPBAG2 per specificare ogni opzione del codificatore supportato dal codificatore e il relativo tipo di dati per ogni proprietà. È quindi necessario implementare un oggetto IPropertyBag2 che applica gli intervalli di valori per ogni proprietà in scrittura e riconcilia eventuali valori in conflitto o sovrapposti. Per set semplici di opzioni del codificatore non in conflitto, è possibile richiamare il metodo [**CreateEncoderPropertyBag,**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createencoderpropertybag) che creerà un semplice oggetto IPropertyBag2 usando le proprietà specificate nello struct PROPBAG2. È comunque necessario applicare gli intervalli di valori. Per opzioni del codificatore più avanzate o se è necessario riconciliare i valori in conflitto, è necessario scrivere un'implementazione IPropertyBag2 personalizzata.


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



WIC offre un piccolo set di opzioni del codificatore canonico usate da alcuni dei formati di immagine comuni. Tutte le opzioni del codificatore canonico sono facoltative e i codec non sono necessari per supportarle. Il motivo per cui vengono fornite come opzioni canoniche è che molte applicazioni espongono l'interfaccia utente per consentire agli utenti di specificare queste opzioni quando salvano un file di immagine in un formato che le supporta. Fornire un modo canonico per specificare queste opzioni rende più semplice per le applicazioni comunicarle ai codificatori in modo coerente. Le opzioni del codificatore canonico sono elencate nella tabella seguente.



| Opzione del codificatore     | VARTYPE  | Gamma valori               |
|--------------------|----------|---------------------------|
| Lossless           | VT \_ BOOL | Vero/Falso                |
| ImageQuality       | VT \_ R4   | 0.0-1.0                   |
| CompressionQuality | VT \_ R4   | 0.0-1.0                   |
| BitmapTransform    | VT \_ UI1  | WICBitmapTransformOptions |



 

Se il codec supporta la codifica senza perdita di dati, è consigliabile esporre l'opzione Codificatore senza perdita come modo per le applicazioni per richiedere che un'immagine venga codificata senza perdita di dati. Se un chiamante imposta questa proprietà su True, è necessario ignorare l'opzione ImageQuality e codificare l'immagine senza perdita di dati.

L'opzione ImageQuality consente a un'applicazione di specificare il grado di fedeltà con cui codificare l'immagine. Questa opzione consente a un utente di effettuare un compromesso tra qualità dell'immagine e velocità e/o dimensioni del file. JPEG è un esempio di formato immagine che supporta questo compromesso. Il valore 0,0 indica che la fedeltà è di scarsa importanza e che il codificatore deve usare l'algoritmo più rischioso. Il valore 1.0 indica che la fedeltà è la più importante e che il codificatore deve mantenere la massima fedeltà possibile. A seconda del codec, questo può essere sinonimo dell'opzione Lossless. Tuttavia, se il codec supporta la codifica senza perdita e se l'opzione Lossless è impostata su True, l'opzione ImageQuality deve essere ignorata.

L'opzione CompressionQuality consente a un'applicazione di specificare l'efficienza della compressione da usare per la codifica dell'immagine. Un algoritmo molto efficiente può produrre un file di immagine più piccolo con la stessa qualità di un algoritmo di compressione meno efficiente, ma potrebbe richiedere più tempo per la codifica. Questa opzione consente a un utente di specificare un compromesso tra le dimensioni del file e la velocità di codifica, mantenendo lo stesso livello di qualità. TIFF è un esempio di formato immagine che supporta questo compromesso. Si noti che un formato come JPEG supporta diversi livelli di compressione, ma una frequenza di compressione più elevata determina una qualità dell'immagine inferiore. Pertanto, un formato di immagine JPEG esporrebbe l'opzione ImageQuality anziché l'opzione CompressionQuality. Il valore 0,0 per questa opzione indica che è necessario comprimere l'immagine il più rapidamente possibile, senza ridurre la fedeltà, a scapito di dimensioni maggiori del file. Il valore 1.0 indica che è necessario creare le dimensioni di file più piccole possibili (allo stesso livello di qualità), indipendentemente dal tempo necessario per codificarlo. Un codec può supportare sia l'opzione ImageQuality che l'opzione CompressionQuality, in cui l'opzione ImageQuality specifica il grado accettabile di perdita e l'opzione CompressionQuality offre un compromesso tra dimensioni e velocità al livello di qualità specificato.

L'opzione BitmapTransform consente al chiamante di specificare un angolo di rotazione o un orientamento verticale o orizzontale durante la codifica. L'enumerazione WICBitmapTransformOptions usata per specificare la trasformazione richiesta è la stessa enum usata quando si richiede una trasformazione durante la decodifica tramite l'interfaccia IWICBitmapSourceTransform.

Si noti che i codificatori non sono limitati alle opzioni del codificatore canonico. Lo scopo delle opzioni del codificatore è consentire ai codificatori di esporre le relative funzionalità e non esiste alcun limite ai tipi di funzionalità che è possibile esporre. Assicurarsi che le opzioni del codificatore siano ben documentate. Anche se un'applicazione può usare il contenitore di proprietà restituito da questo metodo per individuare i nomi, i tipi e gli intervalli di valori per le opzioni supportate, l'unico modo per scoprirne i significati o come esporli nell'interfaccia utente è dalla documentazione.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit) è il metodo chiamato dopo che tutti i dati e i metadati dell'immagine sono stati serializzati nel flusso. È consigliabile usare questo metodo per serializzare i dati dell'immagine di anteprima nel flusso e, se applicabile, eventuali anteprime globali, metadati, tavolozza o altri elementi. Questo metodo non deve chiudere il flusso di file, perché è previsto che l'applicazione che ha aperto il flusso lo chiuda.

La sezione sul metodo IWICBitmapFrameEncode:Commit contiene informazioni dettagliate su come IWICBitmapEncoderCacheOptions influisce sul comportamento di questo metodo.

### <a name="setpreview"></a>SetPreview

[**SetPreview viene**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) usato per creare un'anteprima dell'immagine. Anche se non è strettamente necessario che ogni immagine abbia un'anteprima, è consigliabile. Le moderne fotocamere digitali e gli scanner generano immagini ad alta risoluzione, che tendono a essere molto grandi e, di conseguenza, richiedere tempi di elaborazione significativi per la decodifica. Le immagini della prossima generazione di fotocamere saranno ancora più grandi. È buona norma fornire una versione con risoluzione inferiore di un'immagine, in genere in formato JPEG, che può essere decodificata e visualizzata "immediatamente" quando un utente la richiede. Un'applicazione può richiedere un'anteprima prima di richiedere la decodifica dell'immagine effettiva per offrire un'esperienza migliore agli utenti e mostrare loro una rappresentazione dell'immagine con dimensioni dello schermo mentre sono in attesa di decodificare l'immagine effettiva. Anche se i codec devono fornire anteprime, i codec che non supportano [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) dovrebbero sicuramente farlo.

Se si fornisce un'anteprima JPEG, non è necessario scrivere un codificatore JPEG per codificarlo. È consigliabile delegare al codificatore JPEG fornito con la piattaforma WIC per la codifica di anteprime e anteprime.

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

[Implementazione di IWICBitmapCodecProgressNotification (codificatore)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
