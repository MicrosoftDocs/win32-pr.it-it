---
description: Implementazione di IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementazione di IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b31bca377828606fe1beb68d6f1d95d290e01407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050087"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementazione di IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Quando un'applicazione richiede un decodificatore, il primo punto di interazione con il codec è tramite l'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) . Si tratta dell'interfaccia a livello di contenitore che fornisce l'accesso alle proprietà di primo livello del contenitore e, soprattutto, dei frame in esso contenuti. Si tratta dell'interfaccia principale della classe decodificatore a livello di contenitore.

``` syntax
interface IWICBitmapDecoder : IUnknown
{
// Required methods
   HRESULT QueryCapability (IStream *pIStream, 
      DWORD *pdwCapabilities );
   HRESULT Initialize ( IStream *pIStream,
      WICDecodeOptions cacheOptions );
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetDecoderInfo ( IWICBitmapDecoderInfo **pIDecoderInfo );
   HRESULT GetFrameCount ( UINT *pCount );
   HRESULT GetFrame ( UINT index, 
      IWICBitmapFrameDecode **ppIBitmapFrame );

// Optional methods
   HRESULT GetPreview ( IWICBitmapSource **ppIPreview );
   HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
   HRESULT GetColorContexts ( UINT cCount, 
      IWICColorContext **ppIColorContexts, 
      UINT *pcActualCount );
   HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader);
   HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

Alcuni formati di immagine hanno anteprime globali, contesti di colore o metadati, mentre molti formati di immagine li forniscono solo per singolo frame. I metodi per l'accesso a questi elementi sono facoltativi in [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder), ma sono necessari in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode). Analogamente, alcuni codec non utilizzano formati pixel indicizzati e pertanto non è necessario implementare i metodi [CopyPalette](-wic-imp-iwicbitmapframedecode.md) su una delle due interfacce. Per altre informazioni sui metodi facoltativi **IWICBitmapDecoder** , vedere [implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md), dove sono implementate più di frequente.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) è il metodo utilizzato per l'arbitraggio di codec. (Vedere [individuazione e arbitraggio](-wic-howwicworks.md) nell'argomento [come funziona il componente Windows Imaging](-wic-howwicworks.md) ). Se due codec sono in grado di decodificare lo stesso formato di immagine o se si verifica una collisione del modello in cui due codec usano lo stesso modello di identificazione, questo metodo consente di selezionare il codec che può gestire meglio qualsiasi immagine specifica.

Quando si richiama questo metodo, Windows Imaging Component (WIC) passa il flusso effettivo che contiene l'immagine. È necessario verificare se è possibile decodificare ogni fotogramma all'interno dell'immagine ed enumerare i blocchi di metadati per dichiarare accuratamente le funzionalità di questo decodificatore rispetto al flusso di file specifico passato. Questa operazione è importante per tutti i decodificatori, ma è particolarmente importante per i formati di immagine basati sui contenitori Tagged Image File Format (TIFF). Il processo di individuazione funziona mediante la corrispondenza dei modelli associati ai decodificatori nel registro di sistema con i modelli nel file di immagine effettivo. Dichiarare il modello di identificazione nel registro di sistema garantisce che il decodificatore venga sempre rilevato per le immagini nel formato di immagine. Tuttavia, il decodificatore potrebbe essere ancora rilevato per le immagini in altri formati. Ad esempio, tutti i contenitori TIFF includono il modello TIFF, che è un modello di identificazione valido per il formato di immagine TIFF. Ciò significa che, durante l'individuazione, verranno trovati almeno due modelli di identificazione nei file di immagine per qualsiasi formato di immagine basato su un contenitore di tipo TIFF. Uno sarà il modello TIFF e l'altro sarà il modello di formato immagine effettivo. Sebbene sia meno probabile, è possibile che si verifichino conflitti di modelli tra altri formati di immagine non correlati. Questo è il motivo per cui l'individuazione e l'arbitraggio sono un processo in due fasi. Verificare sempre che il flusso di immagini passato a [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) sia in realtà un'istanza valida del proprio formato di immagine. Inoltre, se il codec decodifica un formato di immagine per cui non si è proprietari della specifica, l'implementazione di **QueryCapability** deve verificare la presenza di qualsiasi funzionalità che può essere valida con la specifica del formato di immagine che il codec non implementa. In questo modo gli utenti non possono riscontrare errori di decodifica non necessari o ottenere risultati imprevisti con il codec.

Prima di eseguire qualsiasi operazione sull'immagine, è necessario salvare la posizione corrente del flusso, in modo che sia possibile ripristinarla nella posizione originale prima di restituire il metodo. L'enumerazione [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) che specifica le funzionalità viene definita nel modo seguente:

``` syntax
enum WICBitmapDecoderCapabilities
{   
   WICBitmapDecoderCapabilitySameEncoder,
   WICBitmapDecoderCapabilityCanDecodeAllImages,
   WICBitmapDecoderCapabilityCanDecodeSomeImages,
   WICBitmapDecoderCapabilityCanEnumerateMetadata,
   WICBitmapDecoderCapabilityCanDecodeThumbnail
}
```

È necessario dichiarare **WICBitmapDecoderCapabilitySameEncoder** solo se il codificatore è quello che ha codificato l'immagine. Dopo aver verificato se è possibile decodificare ogni frame nel contenitore, dichiarare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se è possibile decodificare alcuni ma non tutti i frame, **WICBitmapDecoderCapabilityCanDecodeAllImages** se è possibile decodificare tutti i frame o nessuno dei due se non è possibile decodificarli. Queste due enumerazioni si escludono a vicenda. Se si restituisce **WICBitmapDecoderCapabilityCanDecodeAllImages**, **WICBitmapDecoderCapabilityCanDecodeSomeImages** verrà ignorato. Dichiarare **WICBitmapDecoderCapabilityCanEnumerateMetadata** dopo avere verificato che sia possibile enumerare i blocchi di metadati nel contenitore di immagini. Non è necessario cercare un'anteprima in ogni frame. Se è presente un'anteprima globale ed è possibile decodificarla, è possibile dichiarare **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Se non è presente un'anteprima globale, provare a decodificare l'anteprima per il frame 0. Se non è presente alcuna anteprima in nessuna di queste posizioni, non dichiarare questa funzionalità.

Dopo aver determinato le funzionalità del decodificatore rispetto al flusso di immagini passato a questo metodo, eseguire un'operazione OR con il [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) verificato che questo decodificatore possa eseguire su questa immagine e restituire il risultato. Ricordarsi di ripristinare il flusso nella posizione originale prima di restituire.

### <a name="initialize"></a>Inizializzare

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) viene richiamato da un'applicazione dopo che è stato selezionato un decodificatore per decodificare un'immagine specifica. Il flusso di immagini viene passato al decodificatore e un chiamante può specificare facoltativamente l'opzione della cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) per gestire i metadati nel file.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Alcune applicazioni usano metadati più di altre. Per la maggior parte delle applicazioni non è necessario accedere a tutti i metadati in un file di immagine e verranno richiesti metadati specifici in base alle esigenze. In altre applicazioni, invece, i metadati vengono memorizzati nella cache prima che il flusso di file venga aperto ed eseguo l'I/O del disco ogni volta che è necessario accedere ai metadati. Se il chiamante non specifica un'opzione della cache dei metadati, il comportamento predefinito di memorizzazione nella cache deve essere memorizzato nella cache su richiesta. Ciò significa che non è necessario caricare i metadati in memoria fino a quando l'applicazione non esegue una richiesta specifica per i metadati. Se l'applicazione specifica **WICDecodeMetadataCacheOnLoad**, i metadati devono essere caricati in memoria immediatamente e memorizzati nella cache. Quando i metadati vengono memorizzati nella cache durante il caricamento, il flusso di file può essere rilasciato dopo che i metadati sono stati memorizzati nella cache.

### <a name="getcontainerformat"></a>GetContainerFormat

Per implementare [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat), restituire solo il GUID del formato di immagine dell'immagine per cui viene creata un'istanza del decodificatore. Questo metodo viene inoltre implementato in [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) restituisce un oggetto [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) . Per ottenere l'oggetto **IWICBitmapDecoderInfo** , è sufficiente passare il GUID del decodificatore al metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), quindi richiedere l'interfaccia **IWICBitmapDecoderInfo** su di esso, come illustrato nell'esempio seguente.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) restituisce semplicemente il numero di frame nel contenitore. Alcuni formati di contenitore supportano più frame e altri supportano solo un frame per ogni contenitore.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) è un metodo importante sull'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) perché il frame contiene i bit dell'immagine effettivi e l'oggetto del decodificatore di frame restituito da questo metodo è l'oggetto che esegue la decodifica effettiva dell'immagine richiesta. Ovvero l'altro oggetto che è necessario implementare durante la scrittura di un decodificatore. Per ulteriori informazioni sui decodificatori di frame, vedere [implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md).

### <a name="getpreview"></a>Getpreview

[**Getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) restituisce un'anteprima dell'immagine. Per una descrizione dettagliata delle anteprime, vedere Implementazione del metodo [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) sull'implementazione dell'interfaccia [IWICBitmapEncoder](-wic-imp-iwicbitmapencoder.md) .

Se il formato dell'immagine contiene un'anteprima JPEG incorporata, è consigliabile, anziché scrivere un decodificatore JPEG per decodificarlo, delegare al decodificatore JPEG fornito con la piattaforma WIC per la decodifica di anteprime e anteprime. A tale scopo, cercare all'inizio dei dati dell'immagine di anteprima nel flusso e richiamare il metodo [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).


```C++
IWICBitmapDecoder* pPreviewDecoder = NULL;
IWICBitmapFrameDecode* pPreviewFrame = NULL;
IWICBitmapSource* pPreview = NULL;
HRESULT hr;

hr = m_pImagingFactory->CreateDecoderFromStream(
                               m_pStream, NULL, 
                               WICDecodeMetadataCacheOnDemand, &pPreviewDecoder);
hr = pPreviewDecoder->GetFrame(0, pPreviewFrame);
hr = pPreviewFrame->QueryInterface(IID_IWICBitmapSource, (void**)&pPreview);

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfacce del decodificatore](-wic-decoderinterfaces.md)
</dt> <dt>

[Implementazione di IWICBitmapCodecProgressNotification (decodificatore)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



