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
# <a name="implementing-iwicbitmapframedecode"></a><span data-ttu-id="7187f-103">Implementazione di IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="7187f-103">Implementing IWICBitmapFrameDecode</span></span>

## <a name="iwicbitmapframedecode"></a><span data-ttu-id="7187f-104">IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="7187f-104">IWICBitmapFrameDecode</span></span>

<span data-ttu-id="7187f-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) è l'interfaccia a livello di frame che consente di accedere ai bit dell'immagine effettivi.</span><span class="sxs-lookup"><span data-stu-id="7187f-105">[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) is the frame-level interface that provides access to the actual image bits.</span></span> <span data-ttu-id="7187f-106">Questa interfaccia viene implementata nella classe di decodifica a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="7187f-106">You implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="7187f-107">Poiché è derivato da [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), l'implementazione di **IWICBitmapFrameDecode** includerà un'implementazione dei metodi **IWICBitmapSource** .</span><span class="sxs-lookup"><span data-stu-id="7187f-107">Because it’s derived from [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource), your implementation of **IWICBitmapFrameDecode** will include an implementation of the **IWICBitmapSource** methods.</span></span> <span data-ttu-id="7187f-108">I metodi aggiuntivi di **IWICBitmapFrameDecode** forniscono l'accesso all'anteprima a livello di frame, a tutti i contesti di colore per l'immagine e al lettore di query dei metadati per il frame.</span><span class="sxs-lookup"><span data-stu-id="7187f-108">The additional methods on **IWICBitmapFrameDecode** provide access to the frame-level thumbnail, any color contexts for the image, and the metadata query reader for the frame.</span></span>

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

-   [<span data-ttu-id="7187f-109">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="7187f-109">GetThumbnail</span></span>](#getthumbnail)
-   [<span data-ttu-id="7187f-110">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="7187f-110">GetColorContexts</span></span>](#getcolorcontexts)
-   [<span data-ttu-id="7187f-111">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="7187f-111">GetMetadataQueryReader</span></span>](#getmetadataqueryreader)
-   [<span data-ttu-id="7187f-112">GetSize, GetPixelFormat e getsolution</span><span class="sxs-lookup"><span data-stu-id="7187f-112">GetSize, GetPixelFormat, and GetResolution</span></span>](#getsize-getpixelformat-and-getresolution)
-   [<span data-ttu-id="7187f-113">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="7187f-113">CopyPixels</span></span>](#copypixels)
-   [<span data-ttu-id="7187f-114">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="7187f-114">CopyPalette</span></span>](#copypalette)

### <a name="getthumbnail"></a><span data-ttu-id="7187f-115">GetThumbnail</span><span class="sxs-lookup"><span data-stu-id="7187f-115">GetThumbnail</span></span>

<span data-ttu-id="7187f-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) restituisce l'anteprima per il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="7187f-116">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) returns the thumbnail for the current frame.</span></span> <span data-ttu-id="7187f-117">Per motivi di prestazioni, le anteprime vengono in genere codificate in formato JPEG.</span><span class="sxs-lookup"><span data-stu-id="7187f-117">For performance reasons, thumbnails are most commonly encoded in a JPEG format.</span></span> <span data-ttu-id="7187f-118">Come per l'anteprima nel decodificatore, non è necessario o consigliabile fornire il proprio decodificatore JPEG per le anteprime.</span><span class="sxs-lookup"><span data-stu-id="7187f-118">Just as with the Preview on the decoder, it is not necessary or recommended to provide your own JPEG decoder for thumbnails.</span></span> <span data-ttu-id="7187f-119">Al contrario, è necessario delegare al decodificatore JPEG fornito da Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="7187f-119">Instead, you should delegate to the JPEG decoder provided by Windows Imaging Component (WIC).</span></span>

<span data-ttu-id="7187f-120">Per ulteriori informazioni sulle anteprime, vedere il metodo [sethumbnail](-wic-imp-iwicbitmapframeencode.md) sull' [implementazione di IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span><span class="sxs-lookup"><span data-stu-id="7187f-120">For more information on thumbnails, see the [SetThumbnail](-wic-imp-iwicbitmapframeencode.md) method on [Implementing IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md).</span></span>

### <a name="getcolorcontexts"></a><span data-ttu-id="7187f-121">GetColorContexts</span><span class="sxs-lookup"><span data-stu-id="7187f-121">GetColorContexts</span></span>

<span data-ttu-id="7187f-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) restituisce i contesti di colore validi (noti anche come profili colori) associati all'immagine in questo frame.</span><span class="sxs-lookup"><span data-stu-id="7187f-122">[**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) returns the valid color contexts (also known as color profiles) associated with the image in this frame.</span></span> <span data-ttu-id="7187f-123">Nella maggior parte dei casi, questo sarà uno solo, ma in alcuni casi possono verificarsi due o, raramente più.</span><span class="sxs-lookup"><span data-stu-id="7187f-123">In most cases, this will only be one, but there could be cases where there are two or, rarely, more.</span></span> <span data-ttu-id="7187f-124">Il chiamante passerà uno o più oggetti [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) , impostando il parametro *ccount* per indicare il numero di passaggi.</span><span class="sxs-lookup"><span data-stu-id="7187f-124">The caller will pass in one or more [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects, setting the *cCount* parameter to indicate how many they are passing in.</span></span> <span data-ttu-id="7187f-125">Questo metodo popola gli oggetti **IWICColorContext** con i dati del contesto di colore effettivi per i profili colori associati all'immagine.</span><span class="sxs-lookup"><span data-stu-id="7187f-125">This method populates the **IWICColorContext** objects with the actual color context data for the color profiles associated with the image.</span></span> <span data-ttu-id="7187f-126">Impostare il parametro *pcActualCount* sul numero effettivo di contesti di colore associati all'immagine, anche se è maggiore del numero che è possibile restituire.</span><span class="sxs-lookup"><span data-stu-id="7187f-126">Set the *pcActualCount* parameter to the actual number of color contexts associated with the image, even if this is greater than the number you can return.</span></span> <span data-ttu-id="7187f-127">(Nel caso in cui siano disponibili più contesti di colore rispetto al numero di oggetti **IWICColorContext** passati dal chiamante, questo indica al chiamante che sono disponibili uno o più altri elementi).</span><span class="sxs-lookup"><span data-stu-id="7187f-127">(In the case where more color contexts are available than the number of **IWICColorContext** objects passed in by the caller, this tells the caller there are one or more others available.)</span></span>

### <a name="getmetadataqueryreader"></a><span data-ttu-id="7187f-128">GetMetadataQueryReader</span><span class="sxs-lookup"><span data-stu-id="7187f-128">GetMetadataQueryReader</span></span>

<span data-ttu-id="7187f-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) restituisce un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) che può essere utilizzato da un'applicazione per recuperare i metadati dal frame immagine.</span><span class="sxs-lookup"><span data-stu-id="7187f-129">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) returns an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) that an application can use to retrieve metadata from the image frame.</span></span> <span data-ttu-id="7187f-130">Questa interfaccia viene implementata da un gestore di metadati e consente a un'applicazione di eseguire query per proprietà di metadati specifiche appartenenti a un determinato formato di metadati.</span><span class="sxs-lookup"><span data-stu-id="7187f-130">This interface is implemented by a metadata handler, and allows an application to query for specific metadata properties belonging to a particular metadata format.</span></span> <span data-ttu-id="7187f-131">Per ulteriori informazioni, vedere [implementazione di IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span><span class="sxs-lookup"><span data-stu-id="7187f-131">For more information, see [Implementing IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md).</span></span>

<span data-ttu-id="7187f-132">Per creare un'istanza di un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), chiamare [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) in [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span><span class="sxs-lookup"><span data-stu-id="7187f-132">To instantiate an [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader), call [**CreateQueryReaderFromBlockReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createqueryreaderfromblockreader) on the [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory).</span></span>


```C++
IWICMetadataQueryReader* pQueryReader = NULL;
HRESULT hr;

hr = m_pComponentFactory->CreateQueryReaderFromBlockReader( 
  static_cast<IWICMetadataBlockWriter*>(this),
  &pQueryReader);
```



### <a name="getsize-getpixelformat-and-getresolution"></a><span data-ttu-id="7187f-133">GetSize, GetPixelFormat e getsolution</span><span class="sxs-lookup"><span data-stu-id="7187f-133">GetSize, GetPixelFormat, and GetResolution</span></span>

<span data-ttu-id="7187f-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)e [**getsolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) sono di chiara interpretazione e restituiscono le proprietà richieste dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7187f-134">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize), [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat), and [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) are self-explanatory, and return the requested properties of the image.</span></span>

### <a name="copypixels"></a><span data-ttu-id="7187f-135">CopyPixels</span><span class="sxs-lookup"><span data-stu-id="7187f-135">CopyPixels</span></span>

<span data-ttu-id="7187f-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) è il metodo chiamato da un'applicazione quando vuole creare una bitmap in memoria di cui è possibile eseguire il rendering sullo schermo o sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="7187f-136">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) is the method an application calls when it wants to create a bitmap in memory that can be rendered to the display or printer.</span></span> <span data-ttu-id="7187f-137">Si tratta del metodo che esegue la decodifica effettiva dei bit dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7187f-137">This is the method that does the actual decoding of the image bits.</span></span> <span data-ttu-id="7187f-138">I parametri sono un rettangolo, che rappresenta l'area di interesse nell'immagine di origine da copiare in memoria; Stride, che specifica il numero di byte in una sola riga di analisi. dimensione del buffer in memoria allocata dall'applicazione. e un puntatore al buffer in cui devono essere copiati i bit dell'immagine richiesta.</span><span class="sxs-lookup"><span data-stu-id="7187f-138">The parameters are a rectangle, which represents the region of interest in the source image to copy into memory; the stride, which specifies the number of bytes in one scan line; the size of the buffer in memory that has been allocated by the application; and a pointer to the buffer into which the requested image bits should be copied.</span></span> <span data-ttu-id="7187f-139">Per evitare potenziali sovraccarichi del buffer dall'introduzione di vulnerabilità della sicurezza, assicurarsi di copiare solo i dati di immagine nel buffer come specificato dal parametro *cbBufferSize* .</span><span class="sxs-lookup"><span data-stu-id="7187f-139">(To prevent potential buffer overruns from introducing security vulnerabilities, be sure to copy only as much image data into the buffer as the *cbBufferSize* parameter specifies.)</span></span>

### <a name="copypalette"></a><span data-ttu-id="7187f-140">CopyPalette</span><span class="sxs-lookup"><span data-stu-id="7187f-140">CopyPalette</span></span>

<span data-ttu-id="7187f-141">Solo i codec con formati pixel indicizzati devono implementare il metodo [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) .</span><span class="sxs-lookup"><span data-stu-id="7187f-141">Only codecs that have indexed pixel formats must implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette) method.</span></span> <span data-ttu-id="7187f-142">Se un'immagine usa un formato indicizzato, usare questo metodo per restituire la tavolozza dei colori usati nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7187f-142">If an image uses an indexed format, use this method to return the palette of colors used in the image.</span></span> <span data-ttu-id="7187f-143">Se il codec non ha un formato indicizzato, restituire WINCODEC \_ Err \_ PALETTEUNAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="7187f-143">If your codec doesn’t have an indexed format, return WINCODEC\_ERR\_PALETTEUNAVAILABLE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7187f-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7187f-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7187f-145">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7187f-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7187f-146">**IWICBitmapSource**</span><span class="sxs-lookup"><span data-stu-id="7187f-146">**IWICBitmapSource**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)
</dt> <dt>

[<span data-ttu-id="7187f-147">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="7187f-147">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)
</dt> <dt>

[<span data-ttu-id="7187f-148">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="7187f-148">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
</dt> <dt>

<span data-ttu-id="7187f-149">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7187f-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7187f-150">Implementazione di IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="7187f-150">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="7187f-151">Implementazione di IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="7187f-151">Implementing IWICMetadataBlockReader</span></span>](-wic-imp-iwicmetadatablockreader.md)
</dt> <dt>

[<span data-ttu-id="7187f-152">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="7187f-152">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="7187f-153">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="7187f-153">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



