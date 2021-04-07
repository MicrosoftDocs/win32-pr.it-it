---
description: Implementazione di IWICBitmapSource
ms.assetid: d092e9e5-c041-42f5-84c8-0af52bb5c810
title: Implementazione di IWICBitmapSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88e2f7dfd073405f9de8c82b2ce6d9592b241a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758300"
---
# <a name="implementing-iwicbitmapsource"></a><span data-ttu-id="c8d75-103">Implementazione di IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="c8d75-103">Implementing IWICBitmapSource</span></span>

## <a name="iwicbitmapsource"></a><span data-ttu-id="c8d75-104">IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="c8d75-104">IWICBitmapSource</span></span>

<span data-ttu-id="c8d75-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) è importante per l'uso di immagini dal punto di vista dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c8d75-105">[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) is important for working with images from an application perspective.</span></span> <span data-ttu-id="c8d75-106">Rappresenta l'astrazione di livello più alto per un'origine immagine e tutte le interfacce di Windows Imaging Component (WIC) che rappresentano un'immagine, tra cui [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)e tutte le interfacce di trasformazione ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)e [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) derivano da esso.</span><span class="sxs-lookup"><span data-stu-id="c8d75-106">It represents the highest level abstraction for an image source, and all Windows Imaging Component (WIC) interfaces that represent an image, including [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap), and all the transform interfaces ([**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler), [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper), [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator), and [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)) are derived from it.</span></span> <span data-ttu-id="c8d75-107">In un momento specifico, un oggetto **IWICBitmapSource** può essere o meno supportato da una bitmap effettiva in memoria.</span><span class="sxs-lookup"><span data-stu-id="c8d75-107">At any specific time, an **IWICBitmapSource** object may or may not be backed by an actual bitmap in memory.</span></span> <span data-ttu-id="c8d75-108">Ciò consente un'elaborazione molto efficiente da un'applicazione, perché un'immagine può essere gestita come un'astrazione.</span><span class="sxs-lookup"><span data-stu-id="c8d75-108">This enables very efficient processing by an application, because an image can be dealt with as an abstraction.</span></span> <span data-ttu-id="c8d75-109">Le operazioni di trasformazione possono essere concatenate in una pipeline di trasformazione senza usare risorse di memoria fino a quando l'applicazione non è pronta per il rendering o la stampa dell'immagine, a quel punto richiama il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) sulla trasformazione finale per ottenere una bitmap in memoria dell'immagine con le trasformazioni selezionate applicate.</span><span class="sxs-lookup"><span data-stu-id="c8d75-109">Transform operations can be chained in a transform pipeline without consuming memory resources until the application is ready to render or print the image, at which time it invokes the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method on the final transform to get a bitmap in memory of the image with the selected transforms applied.</span></span>

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

<span data-ttu-id="c8d75-110">Dal punto di vista del codec, i metodi [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) vengono implementati nell'oggetto Decoder frame.</span><span class="sxs-lookup"><span data-stu-id="c8d75-110">From a codec perspective, the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) methods are implemented on the frame decoder object.</span></span> <span data-ttu-id="c8d75-111">Questi metodi sono descritti in implementazione di IWICBitmapSource, insieme agli altri metodi in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), derivati da **IWICBitmapSource**.</span><span class="sxs-lookup"><span data-stu-id="c8d75-111">These methods are described in Implementing IWICBitmapSource, along with the other methods on [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), which is derived from **IWICBitmapSource**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8d75-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8d75-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8d75-113">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c8d75-113">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c8d75-114">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="c8d75-114">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="c8d75-115">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="c8d75-115">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="c8d75-116">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="c8d75-116">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="c8d75-117">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c8d75-117">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8d75-118">Implementazione di IWICBitmapCodecProgressNotification (decodificatore)</span><span class="sxs-lookup"><span data-stu-id="c8d75-118">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> <dt>

[<span data-ttu-id="c8d75-119">Implementazione di IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="c8d75-119">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="c8d75-120">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c8d75-120">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c8d75-121">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="c8d75-121">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



