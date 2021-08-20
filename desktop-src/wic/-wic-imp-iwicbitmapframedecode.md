---
description: Implementazione di IWICBitmapFrameDecode
ms.assetid: 7dc626ad-1158-4b67-8ca7-47b4cf88e278
title: Implementazione di IWICBitmapFrameDecode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b49e3636f5d81202b1060d868ecb40bb99d095dd9f26b6afd0d40c5f5fd0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205765"
---
# <a name="implementing-iwicbitmapframedecode"></a>Implementazione di IWICBitmapFrameDecode

## <a name="iwicbitmapframedecode"></a>IWICBitmapFrameDecode

[**IWICBitmapFrameDecode è**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) l'interfaccia a livello di frame che fornisce l'accesso ai bit di immagine effettivi. Questa interfaccia viene implementata nella classe di decodifica a livello di frame. Poiché deriva da [**IWICBitmapSource,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)l'implementazione di **IWICBitmapFrameDecode** includerà un'implementazione **dei metodi IWICBitmapSource.** I metodi aggiuntivi in **IWICBitmapFrameDecode** forniscono l'accesso all'anteprima a livello di frame, a tutti i contesti di colore per l'immagine e al lettore di query dei metadati per il frame.

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
-   [GetSize, GetPixelFormat e GetResolution](#getsize-getpixelformat-and-getresolution)
-   [CopyPixels](#copypixels)
-   [CopyPalette](#copypalette)

### <a name="getthumbnail"></a>GetThumbnail

[**GetThumbnail restituisce**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) l'anteprima per il frame corrente. Per motivi di prestazioni, le anteprime vengono in genere codificate in formato JPEG. Come per l'anteprima nel decodificatore, non è necessario o consigliato fornire il proprio decodificatore JPEG per le anteprime. È invece necessario delegare al decodificatore JPEG fornito da Windows Imaging Component (WIC).

Per altre informazioni sulle anteprime, vedere il [metodo SetThumbnail](-wic-imp-iwicbitmapframeencode.md) sull'implementazione [di IWICBitmapFrameEncode.](-wic-imp-iwicbitmapframeencode.md)

### <a name="getcolorcontexts"></a>GetColorContexts

[**GetColorContexts restituisce**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) i contesti di colore validi (noti anche come profili colori) associati all'immagine in questo frame. Nella maggior parte dei casi, sarà solo uno, ma in alcuni casi potrebbero essere presenti due o, raramente, più. Il chiamante passerà uno o più [**oggetti IWICColorContext,**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) impostando il parametro *cCount* per indicare il numero di oggetti passati. Questo metodo popola gli oggetti **IWICColorContext** con i dati del contesto di colore effettivi per i profili colori associati all'immagine. Impostare il *parametro pcActualCount* sul numero effettivo di contesti di colore associati all'immagine, anche se è maggiore del numero che è possibile restituire. Nel caso in cui siano disponibili più contesti di colore rispetto al numero di oggetti **IWICColorContext** passati dal chiamante, ciò indica al chiamante che sono disponibili uno o più altri.

### <a name="getmetadataqueryreader"></a>GetMetadataQueryReader

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) restituisce un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) che un'applicazione può usare per recuperare i metadati dal frame dell'immagine. Questa interfaccia viene implementata da un gestore di metadati e consente a un'applicazione di eseguire una query per proprietà di metadati specifiche appartenenti a un particolare formato di metadati. Per altre informazioni, vedere [Implementazione di IWICMetadataBlockReader.](-wic-imp-iwicmetadatablockreader.md)

Per creare [**un'istanza di IWICMetadataQueryReader,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)chiamare [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) su [**IWICComponentFactory.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a>GetSize, GetPixelFormat e GetResolution

[**GetSize,**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sono auto-esplicativi e restituiscono le proprietà richieste dell'immagine.

### <a name="copypixels"></a>CopyPixels

[**CopyPixels è**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) il metodo chiamato da un'applicazione quando desidera creare una bitmap in memoria di cui è possibile eseguire il rendering sulla periferica di visualizzazione o sulla stampante. Si tratta del metodo che esegue la decodifica effettiva dei bit dell'immagine. I parametri sono un rettangolo che rappresenta l'area di interesse nell'immagine di origine da copiare in memoria. stride, che specifica il numero di byte in una riga di analisi; la dimensione del buffer in memoria allocata dall'applicazione; e un puntatore al buffer in cui copiare i bit dell'immagine richiesti. Per evitare potenziali sovraccarichi del buffer che introducono vulnerabilità di sicurezza, assicurarsi di copiare nel buffer solo la quantità di dati immagine specificata dal parametro *cbBufferSize.*

### <a name="copypalette"></a>CopyPalette

Solo i codec con formati pixel indicizzati devono implementare il [**metodo CopyPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) Se un'immagine usa un formato indicizzato, usare questo metodo per restituire la tavolozza dei colori usati nell'immagine. Se il codec non ha un formato indicizzato, restituire WINCODEC \_ ERR \_ PALETTEUNAVAILABLE.

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

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



