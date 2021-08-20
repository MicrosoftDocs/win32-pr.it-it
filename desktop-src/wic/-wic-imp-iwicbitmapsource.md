---
description: Implementazione di IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementazione di IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b7ffd73271e8e159eea825ed40c24347ec2af98f0edbfa9ecc0d5ac584df23b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965020"
---
# <a name="implementing-iwicbitmapsource"></a>Implementazione di IWICBitmapSource

## <a name="iwicbitmapsource"></a>IWICBitmapSource

[**IWICBitmapSource è**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) importante per l'uso di immagini dal punto di vista dell'applicazione. Rappresenta l'astrazione di livello più alto per un'origine immagine e tutte le interfacce Windows del componente di creazione dell'immagine (WIC) che rappresentano un'immagine, tra cui [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)e tutte le interfacce di trasformazione ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) derivano da essa. In qualsiasi momento specifico, un **oggetto IWICBitmapSource** può essere supportato o meno da una bitmap effettiva in memoria. Ciò consente un'elaborazione molto efficiente da parte di un'applicazione, perché un'immagine può essere trattata come un'astrazione. Le operazioni di trasformazione possono essere concatenate in una pipeline di trasformazione senza utilizzare risorse di memoria fino a quando l'applicazione non è pronta per il rendering o la stampa dell'immagine. A questo punto richiama il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sulla trasformazione finale per ottenere una bitmap in memoria dell'immagine con le trasformazioni selezionate applicate.

``` syntax
interface IWICBitmapSource : IUnknown
{
   // Required methods
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

Dal punto di vista del codec, [**i metodi IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vengono implementati nell'oggetto decodificatore di fotogrammi. Questi metodi sono descritti in Implementazione di IWICBitmapSource, insieme agli altri metodi in [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)derivato da **IWICBitmapSource.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapCodecProgressNotification (decodificatore)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[Implementazione di IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Cenni preliminari sul componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



