---
description: Requisiti dei metodi di interfaccia
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Requisiti dei metodi di interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8525f7b04fe82247ecd64a38f5f1acc298be5d3ace56303072268fed6a4a3cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086924"
---
# <a name="interface-method-requirements"></a>Requisiti dei metodi di interfaccia

Non tutti i metodi in ogni interfaccia devono avere un'implementazione. Ad esempio, alcuni codec hanno metadati globali, anteprime o contesti di colore, mentre altri codec forniscono questi solo per fotogramma. Se gli autori di codec li forniscono solo per frame, devono implementare solo [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)SetThumbnail o ColorContexts o implementare i metodi / [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) o [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) anziché in [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) Analogamente, alcuni codec non usano formati indicizzati e pertanto non sono necessari per implementare i [**metodi CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) [**e SetPalette.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) Questi metodi sono quindi facoltativi e sono lasciati alla discrezione dell'autore del codec. La maggior parte degli altri metodi è obbligatoria.

Per Windows [**7**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)Get / [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) e [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) sono obbligatori e devono essere implementati nelle classi a livello di contenuto o nelle classi a livello di frame. Se il formato del file di immagine non supporta le anteprime o le anteprime in uno di questi percorsi, è necessario rivedere il formato del file di immagine per fornire tale supporto.

Quando un metodo non viene implementato, è importante restituire un errore appropriato in modo che il chiamante possa determinare che la funzionalità richiesta non è supportata. Ad esempio, se gli autori di codec non supportano le anteprime a livello di contenitore, devono restituire [WINCODEC \_ ERR \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) quando un'applicazione chiama [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)e, se non hanno un riquadro, devono restituire [WINCODEC \_ ERR \_ PALETTEUNAVAILABLE.](-wic-codec-error-codes.md) Se non esiste [codice WINCODEC \_ ERR](-wic-codec-error-codes.md) appropriato, il codec deve restituire E NOTIMPL per i metodi \_ non implementati.

Nelle tabelle seguenti sono elencati i metodi obbligatori e facoltativi per ogni Windows di componenti di imaging (WIC).

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Necessario

[**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Inizializzare**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Facoltativo

[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**CopiaPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹Richiesta se il formato del file di immagine supporta le anteprime a livello di contenitore. In caso non corretto, è consigliabile rivedere il formato del file di immagine per supportare questa operazione. Se implementato qui, è necessario un [**setPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) corrispondente nella classe di codifica a livello di contenitore.

²Richiesta qui o nella classe di decodifica a livello di frame, a seconda della posizione in cui il formato del file di immagine archivia le anteprime. Se implementato qui, è necessario un [**setThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) corrispondente nella classe di codifica a livello di contenitore.

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Necessario

[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Facoltativo

[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹

[**CopiaPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹Richiesta qui o nella classe di decodifica a livello di contenitore, a seconda della posizione in cui il formato di file di immagine archivia le anteprime. Se implementato qui, è necessario un [**setThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) corrispondente nella classe del codificatore a livello di frame.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Necessario

[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Necessario

[**DoesSupportTransform**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Facoltativo

[**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

Vedere [Supporto per IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md)più avanti in questo documento.

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Necessario

[**Inizializzare**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**GetEncoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Eseguire il commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Facoltativo

[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹Richiesta se il formato del file di immagine supporta le anteprime a livello di frame.

²Richiesta qui o nella classe di codifica a livello di frame, a seconda della posizione in cui il formato del file di immagine archivia le anteprime. Se implementato qui, è necessario un [**getThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) corrispondente nella classe di decodifica a livello di contenitore.

[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Necessario

[**Inizializzare**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Eseguire il commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Facoltativo

[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹

[**CopiaPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

¹Richiesta qui o nella classe di codifica a livello di contenitore, a seconda della posizione in cui il formato del file di immagine archivia le anteprime. Se implementato qui, è necessario un [**getThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) corrispondente nella classe di decodifica a livello di frame.

[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Necessario

[**InitializeFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**AddWriter**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**GetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**SetWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**RemoveWriterByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
