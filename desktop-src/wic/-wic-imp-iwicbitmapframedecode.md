---
description: Implementazione di IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementazione di IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 394b5858ec5eee37ef1c7f52b766806c4a0c1a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758303"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementazione di IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) è l'interfaccia a livello di frame che consente di accedere ai bit dell'immagine effettivi. Questa interfaccia viene implementata nella classe di decodifica a livello di frame. Poiché è derivato da [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), l'implementazione di **IWICBitmapFrameDecode** includerà un'implementazione dei metodi **IWICBitmapSource** . I metodi aggiuntivi di **IWICBitmapFrameDecode** forniscono l'accesso all'anteprima a livello di frame, a tutti i contesti di colore per l'immagine e al lettore di query dei metadati per il frame.

``` syntax
interface IWICBitmapFrameDecode : IWICBitmapSource
{
// Required methods
HRESULT GetThumbnail ( IWICBitmapSource **ppIThumbnail );
HRESULT GetColorContexts ( UINT cCount, 
IWICColorContext **ppIColorContexts, UINT *pcActualCount );
HRESULT GetMetadataQueryReader ( IWICMetadataQueryReader **ppIMetadataQueryReader );

// Methods inherited from IWICBitmapSource
HRESULT GetSize ( UINT *puiWidth, UINT *puiHeight );
HRESULT GetPixelFormat ( WICPixelFormatGUID *pPixelFormat );
HRESULT GetResolution ( double *pDpiX, double *pDpiY );
HRESULT CopyPixels ( const WICRect *prc, 
   UINT cbStride,
   UINT cbBufferSize, 
   BYTE *pbBuffer );
// Optional method
HRESULT CopyPalette ( IWICPalette *pIPalette );
}
```

-   [GetThumbnail](#getthumbnail)
-   [GetColorContexts](#getcolorcontexts)
-   [GetMetadataQueryReader](#getmetadataqueryreader)
-   [GetSize, GetPixelFormat e getsolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) restituisce l'anteprima per il frame corrente. Per motivi di prestazioni, le anteprime vengono in genere codificate in formato JPEG. Come per l'anteprima nel decodificatore, non è necessario o consigliabile fornire il proprio decodificatore JPEG per le anteprime. Al contrario, è necessario delegare al decodificatore JPEG fornito da Windows Imaging Component (WIC).

Per ulteriori informazioni sulle anteprime, vedere il metodo [sethumbnail](-wic-imp-iwicbitmapframeencode.md) sull' [implementazione di IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) restituisce i contesti di colore validi (noti anche come profili colori) associati all'immagine in questo frame. Nella maggior parte dei casi, questo sarà uno solo, ma in alcuni casi possono verificarsi due o, raramente più. Il chiamante passerà uno o più oggetti [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , impostando il parametro *ccount* per indicare il numero di passaggi. Questo metodo popola gli oggetti **IWICColorContext** con i dati del contesto di colore effettivi per i profili colori associati all'immagine. Impostare il parametro *pcActualCount* sul numero effettivo di contesti di colore associati all'immagine, anche se è maggiore del numero che è possibile restituire. (Nel caso in cui siano disponibili più contesti di colore rispetto al numero di oggetti **IWICColorContext** passati dal chiamante, questo indica al chiamante che sono disponibili uno o più altri elementi).

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) restituisce un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) che può essere utilizzato da un'applicazione per recuperare i metadati dal frame immagine. Questa interfaccia viene implementata da un gestore di metadati e consente a un'applicazione di eseguire query per proprietà di metadati specifiche appartenenti a un determinato formato di metadati. Per ulteriori informazioni, vedere [implementazione di IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).

Per creare un'istanza di un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), chiamare [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) in [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat e getsolution

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**getsolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sono di chiara interpretazione e restituiscono le proprietà richieste dell'immagine.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) è il metodo chiamato da un'applicazione quando vuole creare una bitmap in memoria di cui è possibile eseguire il rendering sullo schermo o sulla stampante. Si tratta del metodo che esegue la decodifica effettiva dei bit dell'immagine. I parametri sono un rettangolo, che rappresenta l'area di interesse nell'immagine di origine da copiare in memoria; Stride, che specifica il numero di byte in una sola riga di analisi. dimensione del buffer in memoria allocata dall'applicazione. e un puntatore al buffer in cui devono essere copiati i bit dell'immagine richiesta. Per evitare potenziali sovraccarichi del buffer dall'introduzione di vulnerabilità della sicurezza, assicurarsi di copiare solo i dati di immagine nel buffer come specificato dal parametro *cbBufferSize* .

### <a name="copypalette"></a>CopyPalette

Solo i codec con formati pixel indicizzati devono implementare il metodo [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) . Se un'immagine usa un formato indicizzato, usare questo metodo per restituire la tavolozza dei colori usati nell'immagine. Se il codec non ha un formato indicizzato, restituire WINCODEC \_ Err \_ PALETTEUNAVAILABLE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Implementazione di IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



