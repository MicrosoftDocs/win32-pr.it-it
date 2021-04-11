---
description: Implementazione di IWICBitmapFrameEncode
ms.assetid: 509fa49c-c90d-4270-a338-6ce638ccd89a
title: Implementazione di IWICBitmapFrameEncode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d2a5ea0412ea4a45ea329618d00443c1755391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232888"
---
# <a name="implementing-iwicbitmapframeencode"></a>Implementazione di IWICBitmapFrameEncode

## <a name="iwicbitmapframeencode"></a>IWICBitmapFrameEncode

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) è la controparte del codificatore dell'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) . È possibile implementare questa interfaccia nella classe di codifica a livello di frame, ovvero la classe che esegue la codifica effettiva dei bit dell'immagine per ogni frame.


```C++
interface IWICBitmapFrameEncode : public IUnknown
{
   // Required methods
   HRESULT Initialize ( IPropertyBag2 *pIEncoderOptions );
   HRESULT SetSize ( UINT width,
               UINT height );
   HRESULT SetResolution ( double dpiX,
               double dpiY );
   HRESULT SetPixelFormat (WICPixelFormatGUID *pPixelFormat);
   HRESULT SetColorContexts ( UINT cCount,
               IWICColorContext **ppIColorContext );
   HRESULT GetMetadataQueryWriter ( IWICMetadataQueryWriter 
               **ppIMetadataQueryWriter );
   HRESULT SetThumbnail ( IWICBitmapSource *pIThumbnail );
   HRESULT WritePixels ( UINT lineCount,
               UINT cbStride,
               UINT cbBufferSize,
               BYTE *pbPixels );
   HRESULT WriteSource ( IWICBitmapSource *pIWICBitmapSource,
               WICRect *prc );
   HRESULT Commit ( void );

// Optional method
   HRESULT SetPalette ( IWICPalette *pIPalette );
};
```



-   [Inizializzare](#initialize)
-   [Ridimensionamento e risoluzione](#setsize-and-setresolution)
-   [SetPixelFormat](#setpixelformat)
-   [SetColorContexts](#setcolorcontexts)
-   [GetMetadataQueryWriter](#getmetadataquerywriter)
-   [Anteprima](#setthumbnail)
-   [WritePixels](#writepixels)
-   [WriteSource](#writesource)
-   [Eseguire il commit](#commit)
-   [SetPalette](#setpalette)

### <a name="initialize"></a>Inizializzare

[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) è il primo metodo richiamato su un oggetto [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) dopo che ne è stata creata un'istanza. Questo metodo ha un parametro, che può essere impostato su **null**. Questo parametro rappresenta le opzioni del codificatore ed è la stessa istanza di [IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) creata nel metodo [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) sul decodificatore a livello di contenitore e passata di nuovo al chiamante nel parametro pIEncoderOptions di tale metodo. In quel momento è stato popolato lo struct IPropertyBag2 con proprietà che rappresentano le opzioni di codifica supportate dal codificatore a livello di frame. Il chiamante ha ora fornito i valori per tali proprietà per indicare determinati parametri dell'opzione di codifica e passa di nuovo lo stesso oggetto per inizializzare l'oggetto **IWICBitmapFrameEncode** . Quando si codificano i bit dell'immagine, è necessario applicare le opzioni specificate.

### <a name="setsize-and-setresolution"></a>Ridimensionamento e risoluzione

Le [**dimensioni**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) e la [**risoluzione**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) dei problemi sono di chiara interpretazione. Il chiamante utilizza questi metodi per specificare le dimensioni e la risoluzione per l'immagine codificata.

### <a name="setpixelformat"></a>SetPixelFormat

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) viene usato per richiedere un formato pixel in cui codificare l'immagine. Se il formato pixel richiesto non è supportato, è necessario restituire il GUID del formato pixel più vicino supportato in *pPixelFormat*, che è un parametro in/out.

### <a name="setcolorcontexts"></a>SetColorContexts

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts) viene usato per specificare uno o più contesti di colore validi (noti anche come profili colori) per questa immagine. È importante specificare i contesti di colore, in modo che un'applicazione che decodifica l'immagine in un secondo momento possa eseguire la conversione dal profilo dei colori di origine al profilo di destinazione del dispositivo usato per visualizzare o stampare l'immagine. Senza un profilo colori, non è possibile ottenere colori coerenti tra dispositivi diversi. Questo può essere frustrante per gli utenti finali quando le foto hanno un aspetto diverso su monitoraggi diversi e non possono ottenere le stampe corrispondenti a quanto visualizzato sullo schermo.

### <a name="getmetadataquerywriter"></a>GetMetadataQueryWriter

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) restituisce un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) che un'applicazione può usare per inserire o modificare proprietà di metadati specifiche in un blocco di metadati nel frame dell'immagine.

È possibile creare un'istanza di un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) da [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) in diversi modi. È possibile crearlo dalla [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter), nello stesso modo in cui [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) è stato creato da un [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) nel metodo [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) sull'interfaccia [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .


```C++
IWICMetadataQueryWriter* piMetadataQueryWriter = NULL;
HRESULT hr;

hr = m_piComponentFactory->CreateQueryWriterFromBlockWriter( 
      static_cast<IWICMetadataBlockWriter*>(this), 
      &piMetadataQueryWriter);

```



È anche possibile crearlo da un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)esistente, ad esempio quello ottenuto usando il metodo precedente.


```C++
hr = m_piComponentFactory->CreateQueryWriterFromReader( 
      piMetadataQueryReader, pguidVendor, &piMetadataQueryWriter);
```



Il parametro *pguidVendor* consente di specificare un particolare fornitore per il writer di query da utilizzare quando si crea un'istanza di un writer di metadati. Se, ad esempio, si forniscono i propri writer di metadati, è consigliabile specificare il proprio GUID fornitore. È possibile passare **null** a questo parametro se non si ha una preferenza.

### <a name="setthumbnail"></a>Anteprima

L' [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) viene utilizzata per fornire un'anteprima. Tutte le immagini devono fornire un'anteprima a livello globale, in ogni frame o in entrambi i casi. I metodi **GetThumbnail** e **sethumbnail** sono facoltativi a livello di contenitore, ma se un codec restituisce WINCODEC \_ Err \_ CODECNOTHUMBNAIL dal metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) , Windows Imaging Component (WIC) richiamerà il metodo [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) per il frame 0. Se non viene trovata alcuna anteprima in nessuna delle due località, WIC deve decodificare l'immagine completa e ridimensionarla in base alle dimensioni di anteprima, il che potrebbe comportare un notevole calo delle prestazioni per le immagini più grandi.

L'anteprima deve avere una dimensione e una risoluzione che consentono di decodificare e visualizzare rapidamente. Per questo motivo, le anteprime sono più comunemente immagini JPEG. Si noti che, se si usa il formato JPEG per le anteprime, non è necessario scrivere un codificatore JPEG per codificarli o un decodificatore JPEG per decodificarli. È sempre necessario delegare il codec JPEG fornito con la piattaforma WIC per la codifica e la decodifica delle anteprime.

### <a name="writepixels"></a>WritePixels

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) è il metodo utilizzato per passare le righe di analisi da una bitmap in memoria per la codifica. Il metodo verrà chiamato ripetutamente fino a quando tutte le righe di analisi non sono state passate. Il parametro *LineCount* indica il numero di righe di analisi da scrivere in questa chiamata. Il parametro *cbStride* indica il numero di byte per riga di analisi. *cbBufferSize* indica le dimensioni del buffer passato nel parametro pbPixels, che contiene i bit di immagine effettivi da codificare. Se l'altezza combinata delle righe di analisi dalle chiamate cumulative è maggiore dell'altezza specificata nel metodo [**sesize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) , restituire WINCODEC \_ Err \_ TOOMANYSCANLINES.

Quando [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) è **WICBitmapEncoderCacheInMemory**, le righe di analisi devono essere memorizzate nella cache fino a quando non sono state passate tutte le righe di analisi. Se l'opzione cache del codificatore è **WICBitmapEncoderCacheTempFile**, le righe di analisi devono essere memorizzate nella cache in un file temporaneo, creato durante l'inizializzazione dell'oggetto. In entrambi i casi, l'immagine non deve essere codificata finché il chiamante chiama [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit). Nel caso in cui l'opzione cache sia **WICBitmapEncoderNoCache**, il codificatore deve codificare le righe di analisi man mano che vengono ricevute, se possibile. (In alcuni formati, questo non è possibile e le righe di analisi devono essere memorizzate nella cache fino a quando non viene chiamato il commit).

La maggior parte dei codec non elaborati non implementerà [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels), perché non supportano la modifica dei bit dell'immagine nel file non elaborato. I codec non elaborati devono comunque implementare **WritePixels**, tuttavia, poiché quando vengono aggiunti metadati, può aumentare la dimensione del file, richiedendo la riscrittura del file sul disco. In tal caso, è necessario essere in grado di copiare i bit dell'immagine esistente, che è il metodo **WritePixels** .

### <a name="writesource"></a>WriteSource

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) viene usato per codificare un oggetto [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) . Il primo parametro è un puntatore a un oggetto **IWICBitmapSource** . Il secondo parametro è un WICRect che specifica l'area di interesse da codificare. Questo metodo può essere chiamato più volte in successione, a condizione che la larghezza di ogni rettangolo corrisponda alla larghezza dell'immagine finale da codificare. Se la larghezza del rettangolo passato nel parametro PRC è diversa dalla larghezza specificata nel metodo sesize, restituire WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS. Se l'altezza combinata delle righe di analisi dalle chiamate cumulative è maggiore dell'altezza specificata nel metodo sesize, restituire WINCODEC \_ Err \_ TOOMANYSCANLINES.

Le opzioni della cache funzionano allo stesso modo con questo metodo, come per il metodo [**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels) descritto in precedenza.

### <a name="commit"></a>Commit

[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) è il metodo che serializza i bit dell'immagine codificata nel flusso di file e scorre tutti i writer di metadati per il frame richiedendo loro di serializzare i metadati nel flusso. Nel caso in cui l'opzione cache del codificatore sia WICBitmapEncoderCacheInMemory o WICBitmapEncoderCacheTempFile, questo metodo è anche responsabile della codifica dell'immagine e quando l'opzione cache è WICBitmapEncoderCacheTempFile, il metodo **commit** deve eliminare anche il file temporaneo usato per memorizzare nella cache i dati dell'immagine prima della codifica.

Questo metodo viene sempre richiamato dopo che tutte le righe o i rettangoli di analisi che costituiscono l'immagine sono stati passati utilizzando il metodo [**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-commit) o [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) . Le dimensioni del rettangolo finale composto tramite le chiamate accumulate a WritePixels o WriteSource devono essere uguali a quelle specificate nel metodo sesize. Se la dimensione non corrisponde alla dimensione prevista, questo metodo deve restituire WINCODECERROR \_ UNEXPECTEDSIZE.

Per scorrere i writer dei metadati e indicare a ogni writer di metadati di serializzare i metadati, passare al flusso, richiamare GetWriterByIndex per scorrere i writer per ogni blocco e richiamare IWICPersistStream. Save su ogni writer di metadati.


```C++
IWICMetadataWriter* piMetadataWRiter = NULL;
IWICPersistStream* piPersistStream = NULL;
HRESULT hr;

for (UINT x=0; x < m_blockCount; x++) 
{
    hr = GetWriterByIndex(x, & piMetadataWriter);
hr = piMetadataWriter->QueryInterface(
IID_IWICPersistStream,(void**)&piPersistStream);

hr = piPersistStream->Save(m_piStream, 
WICPersistOptions.WicPersistOptionDefault, 
true);
...
}
```



### <a name="setpalette"></a>SetPalette

Solo i codec con formati indicizzati devono implementare il metodo [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpalette) . Se un'immagine usa un formato indicizzato, usare questo metodo per specificare la tavolozza dei colori usati nell'immagine. Se il codec non ha un formato indicizzato, restituire WINCODEC \_ Err \_ PALETTEUNAVAILABLE da questo metodo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapCodecProgressNotification (encoder)](-wic-imp-iwicbitmapcodecprogressnotification-encoder.md)
</dt> <dt>

[Implementazione di IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
