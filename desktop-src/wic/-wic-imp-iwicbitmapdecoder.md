---
description: Implementazione di IWICBitmapDecoder
ms.assetid: 9e316bdd-803a-47af-b004-7675478eb829
title: Implementazione di IWICBitmapDecoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0088b756a7a30134224e32fa67ee891f2c48339f9af70447cb760915ad420619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711148"
---
# <a name="implementing-iwicbitmapdecoder"></a>Implementazione di IWICBitmapDecoder

## <a name="iwicbitmapdecoder"></a>IWICBitmapDecoder

Quando un'applicazione richiede un decodificatore, il primo punto di interazione con il codec è tramite [**l'interfaccia IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) Si tratta dell'interfaccia a livello di contenitore che consente di accedere alle proprietà di primo livello del contenitore e, soprattutto, ai frame in esso contenuti. Si tratta dell'interfaccia principale nella classe del decodificatore a livello di contenitore.

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

Alcuni formati di immagine hanno anteprime globali, contesti di colore o metadati, mentre molti formati di immagine forniscono queste informazioni solo per fotogramma. I metodi per accedere a questi elementi sono facoltativi in [**IWICBitmapDecoder,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)ma sono necessari in [**IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) Analogamente, alcuni codec non usano formati di pixel indicizzati e pertanto non è necessario implementare i metodi [CopyPalette](-wic-imp-iwicbitmapframedecode.md) in entrambe le interfacce. Per altre informazioni sui metodi **IWICBitmapDecoder** facoltativi, vedere [Implementazione di IWICBitmapFrameDecode,](-wic-imp-iwicbitmapframedecode.md)dove vengono implementati più comunemente.

### <a name="querycapability"></a>QueryCapability

[**QueryCapability è il**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) metodo usato per l'arbitraggio dei codec. Vedere Discovery [and Arbitration (Individuazione e arbitraggio)](-wic-howwicworks.md) [nell'argomento How the Windows Imaging Component Works](-wic-howwicworks.md) (Funzionamento del Windows imaging). Se due codec sono in grado di decodificare lo stesso formato di immagine o se si verifica una collisione di modelli in cui due codec usano lo stesso modello di identificazione, questo metodo consente di selezionare il codec che può gestire al meglio qualsiasi immagine specifica.

Quando si richiama questo metodo, Windows Imaging Component (WIC) passa il flusso effettivo contenente l'immagine. È necessario verificare se è possibile decodificare ogni frame all'interno dell'immagine ed enumerarlo tramite i blocchi di metadati, per dichiarare in modo accurato le funzionalità di questo decodificatore rispetto al flusso di file specifico passato. Questo è importante per tutti i decodificatori, ma è particolarmente importante per i formati di immagine basati su Tagged Image File Format (TIFF). Il processo di individuazione funziona abbinando i modelli associati ai decodificatori nel Registro di sistema ai criteri nel file di immagine effettivo. La dichiarazione del modello di identificazione nel registro garantisce che il decodificatore verrà sempre rilevato per le immagini nel formato immagine. Tuttavia, il decodificatore potrebbe comunque essere rilevato per le immagini in altri formati. Ad esempio, tutti i contenitori TIFF includono il modello TIFF, che è un modello di identificazione valido per il formato di immagine TIFF. Ciò significa che, durante l'individuazione, nei file di immagine di qualsiasi formato di immagine basato su un contenitore di tipo TIFF saranno presenti almeno due modelli di identificazione. Uno sarà il modello TIFF e l'altro sarà il modello di formato immagine effettivo. Sebbene sia meno probabile, potrebbero verificarsi conflitti di modelli anche tra altri formati di immagine non correlati. Ecco perché l'individuazione e l'arbitraggio sono processi in due fasi. Verificare sempre che il flusso dell'immagine passato [**a QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) sia effettivamente un'istanza valida del proprio formato di immagine. Inoltre, se il codec decodifica un formato di immagine di cui non si è proprietari della specifica, l'implementazione di **QueryCapability** deve verificare la presenza di qualsiasi funzionalità che potrebbe essere valida in base alla specifica del formato dell'immagine non implementata dal codec. In questo modo si garantisce che gli utenti non si verifichino errori di decodifica non necessari o non si verifichino risultati imprevisti con il codec.

Prima di eseguire qualsiasi operazione sull'immagine, è necessario salvare la posizione corrente del flusso, in modo che sia possibile ripristinarne la posizione originale prima di tornare dal metodo . [**L'enumerazione WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) che specifica le funzionalità è definita come segue:

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

È necessario dichiarare **WICBitmapDecoderCapabilitySameEncoder** solo se il codificatore è quello che ha codificato l'immagine. Dopo aver verificato se è possibile decodificare ogni frame nel contenitore, dichiarare **WICBitmapDecoderCapabilityCanDecodeSomeImages** se è possibile decodificare alcuni ma non tutti i frame, **WICBitmapDecoderCapabilityCanDecodeAllImages** se è possibile decodificare tutti i frame o nessuno dei due se non è possibile decodificarli. Queste due enumerazioni si escludono a vicenda. Se si restituisce **WICBitmapDecoderCapabilityCanDecodeAllImages,** **WICBitmapDecoderCapabilityCanDecodeSomeImages** verrà ignorato. Dichiarare **WICBitmapDecoderCapabilityCanEnumerateMetadata** dopo aver verificato che è possibile enumerare i blocchi di metadati nel contenitore di immagini. Non è necessario cercare un'anteprima in ogni fotogramma. Se è presente un'anteprima globale ed è possibile decodificarla, è possibile dichiarare **WICBitmapDecoderCapabilityCanDecodeThumbnail**. Se non è presente alcuna anteprima globale, provare a decodificare l'anteprima per il frame 0. Se non è presente alcuna anteprima in una di queste posizioni, non dichiarare questa funzionalità.

Dopo aver determinato le funzionalità del decodificatore rispetto al flusso dell'immagine passato a questo metodo, eseguire un'operazione OR con [**WICBitmapDecoderCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdecodercapabilities) dopo aver verificato che il decodificatore può eseguire su questa immagine e restituire il risultato. Ricordarsi di ripristinare la posizione originale del flusso prima della restituzione.

### <a name="initialize"></a>Inizializzare

[**L'inizializzazione**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize) viene richiamata da un'applicazione dopo che è stato selezionato un decodificatore per decodificare un'immagine specifica. Il flusso dell'immagine viene passato al decodificatore e un chiamante può facoltativamente specificare l'opzione di cache [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) per gestire i metadati nel file.

``` syntax
enum WICDecodeOptions
{
   WICDecodeMetadataCacheOnDemand,
   WICDecodeMetadataCacheOnLoad
}
```

Alcune applicazioni usano i metadati più di altre. La maggior parte delle applicazioni non deve accedere a tutti i metadati in un file di immagine e richiederà metadati specifici in base alle esigenze. Altre applicazioni preferirebbe memorizzare nella cache tutti i metadati in anticipo anziché mantenere aperto il flusso di file ed eseguire operazioni di I/O su disco ogni volta che devono accedere ai metadati. Se il chiamante non specifica un'opzione di cache dei metadati, il comportamento di memorizzazione nella cache predefinito deve essere cache su richiesta. Ciò significa che nessun metadati deve essere caricato in memoria fino a quando l'applicazione non effettua una richiesta specifica per tali metadati. Se l'applicazione specifica **WICDecodeMetadataCacheOnLoad,** i metadati devono essere caricati immediatamente in memoria e memorizzati nella cache. Quando i metadati vengono memorizzati nella cache al caricamento, il flusso di file può essere rilasciato dopo che i metadati sono stati memorizzati nella cache.

### <a name="getcontainerformat"></a>GetContainerFormat

Per [**implementare GetContainerFormat,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)è sufficiente restituire il GUID del formato immagine dell'immagine per cui viene creata un'istanza del decodificatore. Questo metodo viene implementato anche in [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) e [**IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

### <a name="getdecoderinfo"></a>GetDecoderInfo

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) restituisce un [**oggetto IWICBitmapDecoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo) Per ottenere **l'oggetto IWICBitmapDecoderInfo,** è sufficiente passare il GUID del decodificatore al metodo [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) in [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)e quindi richiedere l'interfaccia **IWICBitmapDecoderInfo,** come illustrato nell'esempio seguente.


```C++
IWICComponentInfo* pComponentInfo = NULL;
HRESULT hr;
 
hr = m_pImagingFactory->CreateComponentInfo(CLSID_This, &pComponentInfo);

hr = pComponentInfo->QueryInterface(IID_IWICBitmapDecoderInfo, (void**)ppIDecoderInfo);

```



### <a name="getframecount"></a>GetFrameCount

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) restituisce solo il numero di fotogrammi nel contenitore. Alcuni formati di contenitore supportano più frame, mentre altri supportano un solo frame per ogni contenitore.

### <a name="getframe"></a>GetFrame

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) è un metodo importante nell'interfaccia [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) perché il frame contiene i bit di immagine effettivi e l'oggetto decodificatore di frame restituito da questo metodo è l'oggetto che esegue la decodifica effettiva dell'immagine richiesta. Si tratta dell'altro oggetto che è necessario implementare quando si scrive un decodificatore. Per altre informazioni sui decodificatori di frame, vedere [Implementazione di IWICBitmapFrameDecode.](-wic-imp-iwicbitmapframedecode.md)

### <a name="getpreview"></a>GetPreview

[**GetPreview restituisce**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) un'anteprima dell'immagine. Per una descrizione dettagliata delle anteprime, vedere il metodo [Implementing IWICBitmapEncoder (Implementazione di IWICBitmapEncoder)](-wic-imp-iwicbitmapencoder.md) nell'interfaccia [Implementing IWICBitmapEncoder ( Implementazione di IWICBitmapEncoder).](-wic-imp-iwicbitmapencoder.md)

Se il formato dell'immagine contiene un'anteprima JPEG incorporata, è consigliabile delegare al decodificatore JPEG fornito con la piattaforma WIC per la decodifica di anteprime e anteprime, anziché scrivere un decodificatore JPEG. A tale scopo, cercare all'inizio dei dati dell'immagine di anteprima nel flusso e richiamare il [**metodo CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) su [**IWICImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)


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

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



