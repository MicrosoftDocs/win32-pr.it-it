---
description: Requisiti del metodo di interfaccia
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Requisiti del metodo di interfaccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9cabe02900fa789773f4104cf282ab326bd4930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315952"
---
# <a name="interface-method-requirements"></a><span data-ttu-id="146ee-103">Requisiti del metodo di interfaccia</span><span class="sxs-lookup"><span data-stu-id="146ee-103">Interface Method Requirements</span></span>

<span data-ttu-id="146ee-104">Non tutti i metodi di ogni interfaccia devono avere un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="146ee-104">Not every method on every interface must have an implementation.</span></span> <span data-ttu-id="146ee-105">Ad esempio, alcuni codec hanno metadati globali, anteprime o contesti di colore, mentre altri codec li forniscono solo per ogni singolo fotogramma.</span><span class="sxs-lookup"><span data-stu-id="146ee-105">For example, some codecs have global metadata, thumbnails, or color contexts, whereas other codecs provide these only on a per-frame basis.</span></span> <span data-ttu-id="146ee-106">Se gli autori di codec li forniscono solo per singolo frame, devono implementare solo [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**sethumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) o ColorContext oppure implementare i metodi [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) o [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) in [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) anziché in [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span><span class="sxs-lookup"><span data-stu-id="146ee-106">If codec authors provide these only on a per-frame basis, they need only implement the [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) or ColorContexts, or implement the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) or [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods on the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) rather than on the [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) and [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder).</span></span> <span data-ttu-id="146ee-107">Analogamente, alcuni codec non usano i formati indicizzati e pertanto non sono necessari per implementare i metodi [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) e [**sepalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) .</span><span class="sxs-lookup"><span data-stu-id="146ee-107">Likewise, some codecs do not use indexed formats and so are not required to implement the [**CopyPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) and [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) methods.</span></span> <span data-ttu-id="146ee-108">Questi metodi sono pertanto facoltativi e rimangono a discrezione dell'autore del codec.</span><span class="sxs-lookup"><span data-stu-id="146ee-108">These methods are therefore optional and are left to the discretion of the codec creator.</span></span> <span data-ttu-id="146ee-109">La maggior parte degli altri metodi sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="146ee-109">Most other methods are required.</span></span>

<span data-ttu-id="146ee-110">Per Windows 7 [](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / , è necessario ottenere la versione di [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) e [**ottenere**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / l'[**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) e deve essere implementata nelle classi a livello di contenitore o nelle classi a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="146ee-110">For Windows 7 [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)/[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) and [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)/[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) are required and must be implemented on either the contain-level classes or on the frame-level classes.</span></span> <span data-ttu-id="146ee-111">Se il formato del file di immagine non supporta anteprime o anteprime in uno di questi percorsi, è necessario rivedere il formato del file di immagine per fornire tale supporto.</span><span class="sxs-lookup"><span data-stu-id="146ee-111">If your image file format doesn't support previews or thumbnails in either of these locations, then you should revise your image file format to provide such support.</span></span>

<span data-ttu-id="146ee-112">Quando un metodo non è implementato, è importante restituire un errore appropriato, in modo che il chiamante possa determinare che la funzionalità richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="146ee-112">When a method is not implemented, it is important to return an appropriate error so the caller can determine that the requested feature is not supported.</span></span> <span data-ttu-id="146ee-113">Ad esempio, se gli autori di codec non supportano le anteprime a livello di contenitore, devono restituire [WINCODEC \_ Err \_ CODECNOTHUMBNAIL](-wic-codec-error-codes.md) quando un'applicazione chiama [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md)e, se non hanno una tavolozza, devono restituire [WINCODEC \_ Err \_ PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="146ee-113">For example, if codec authors do not support container-level thumbnails, they should return [WINCODEC\_ERR\_CODECNOTHUMBNAIL](-wic-codec-error-codes.md) when an application calls [**GetThumbnail**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), and if they don't have a palette, they should return [WINCODEC\_ERR\_PALETTEUNAVAILABLE](-wic-codec-error-codes.md).</span></span> <span data-ttu-id="146ee-114">Se non esiste alcun codice [WINCODEC \_ Err](-wic-codec-error-codes.md) appropriato, il codec deve restituire E \_ NOTIMPL per i metodi non implementati.</span><span class="sxs-lookup"><span data-stu-id="146ee-114">If no suitable [WINCODEC\_ERR](-wic-codec-error-codes.md) code exists, then the codec should return E\_NOTIMPL for unimplemented methods.</span></span>

<span data-ttu-id="146ee-115">Nelle tabelle seguenti sono elencati i metodi obbligatori e facoltativi per ogni interfaccia di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="146ee-115">The following tables list the required and optional methods for each Windows Imaging Component (WIC) interfaces.</span></span>

[<span data-ttu-id="146ee-116">**IWICBitmapDecoder**</span><span class="sxs-lookup"><span data-stu-id="146ee-116">**IWICBitmapDecoder**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



<span data-ttu-id="146ee-117">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-117">Required</span></span>

[<span data-ttu-id="146ee-118">**QueryCapability**</span><span class="sxs-lookup"><span data-stu-id="146ee-118">**QueryCapability**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[<span data-ttu-id="146ee-119">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="146ee-119">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[<span data-ttu-id="146ee-120">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-120">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[<span data-ttu-id="146ee-121">**GetDecoderInfo**</span><span class="sxs-lookup"><span data-stu-id="146ee-121">**GetDecoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[<span data-ttu-id="146ee-122">**GetFrameCount**</span><span class="sxs-lookup"><span data-stu-id="146ee-122">**GetFrameCount**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[<span data-ttu-id="146ee-123">**GetFrame**</span><span class="sxs-lookup"><span data-stu-id="146ee-123">**GetFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

<span data-ttu-id="146ee-124">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="146ee-124">Optional</span></span>

<span data-ttu-id="146ee-125">[**Getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span><span class="sxs-lookup"><span data-stu-id="146ee-125">[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹</span></span>

<span data-ttu-id="146ee-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="146ee-126">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²</span></span>

[<span data-ttu-id="146ee-127">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="146ee-127">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[<span data-ttu-id="146ee-128">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="146ee-128">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[<span data-ttu-id="146ee-129">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="146ee-129">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="146ee-130">¹ obbligatorio se il formato del file di immagine supporta le anteprime a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="146ee-130">¹Required if your image file format supports container-level previews.</span></span> <span data-ttu-id="146ee-131">In caso contrario, si consiglia vivamente di rivedere il formato del file di immagine per supportare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="146ee-131">If this is not the case you are strongly encouraged to revise your image file format to support this.</span></span> <span data-ttu-id="146ee-132">Se implementato in questo punto, è necessaria una versione di [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) corrispondente nella classe Encode a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="146ee-132">If implemented here, then a corresponding [**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) is required on the container-level encode class.</span></span>

<span data-ttu-id="146ee-133">² è obbligatorio qui o nella classe Decode a livello di frame, a seconda della posizione in cui il formato del file di immagine archivia le anteprime.</span><span class="sxs-lookup"><span data-stu-id="146ee-133">²Required either here, or on the frame-level decode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="146ee-134">Se implementato in questo punto, è necessario specificare un' [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) corrispondente nella classe Encode a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="146ee-134">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) is required on the container-level encode class.</span></span>

[<span data-ttu-id="146ee-135">**IWICBitmapFrameDecode**</span><span class="sxs-lookup"><span data-stu-id="146ee-135">**IWICBitmapFrameDecode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



<span data-ttu-id="146ee-136">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-136">Required</span></span>

[<span data-ttu-id="146ee-137">**GetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="146ee-137">**GetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[<span data-ttu-id="146ee-138">**GetMetadataQueryReader**</span><span class="sxs-lookup"><span data-stu-id="146ee-138">**GetMetadataQueryReader**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[<span data-ttu-id="146ee-139">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="146ee-139">**GetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[<span data-ttu-id="146ee-140">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-140">**GetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[<span data-ttu-id="146ee-141">**Getsolution**</span><span class="sxs-lookup"><span data-stu-id="146ee-141">**GetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[<span data-ttu-id="146ee-142">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="146ee-142">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

<span data-ttu-id="146ee-143">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="146ee-143">Optional</span></span>

<span data-ttu-id="146ee-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="146ee-144">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹</span></span>

[<span data-ttu-id="146ee-145">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="146ee-145">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

<span data-ttu-id="146ee-146">¹ obbligatorio qui o nella classe Decode a livello di contenitore, a seconda della posizione in cui vengono archiviate le anteprime in formato file di immagine.</span><span class="sxs-lookup"><span data-stu-id="146ee-146">¹Required either here, or on the container-level decode class, depending on where you image file format stores thumbnails.</span></span> <span data-ttu-id="146ee-147">Se implementato in questo punto, è necessario specificare un' [**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) corrispondente nella classe del codificatore a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="146ee-147">If implemented here, then a corresponding [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) is required on the frame-level encoder class.</span></span>

[<span data-ttu-id="146ee-148">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="146ee-148">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="146ee-149">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-149">Required</span></span>

[<span data-ttu-id="146ee-150">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-150">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[<span data-ttu-id="146ee-151">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="146ee-151">**GetCount**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[<span data-ttu-id="146ee-152">**GetReaderByIndex**</span><span class="sxs-lookup"><span data-stu-id="146ee-152">**GetReaderByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[<span data-ttu-id="146ee-153">**GetEnumerator**</span><span class="sxs-lookup"><span data-stu-id="146ee-153">**GetEnumerator**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[<span data-ttu-id="146ee-154">**IWICBitmapSourceTransform**</span><span class="sxs-lookup"><span data-stu-id="146ee-154">**IWICBitmapSourceTransform**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



<span data-ttu-id="146ee-155">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-155">Required</span></span>

[<span data-ttu-id="146ee-156">**DoesSupportTransform**</span><span class="sxs-lookup"><span data-stu-id="146ee-156">**DoesSupportTransform**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[<span data-ttu-id="146ee-157">**CopyPixels**</span><span class="sxs-lookup"><span data-stu-id="146ee-157">**CopyPixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

<span data-ttu-id="146ee-158">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="146ee-158">Optional</span></span>

[<span data-ttu-id="146ee-159">**GetClosestSize**</span><span class="sxs-lookup"><span data-stu-id="146ee-159">**GetClosestSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[<span data-ttu-id="146ee-160">**GetClosestPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-160">**GetClosestPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[<span data-ttu-id="146ee-161">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="146ee-161">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

<span data-ttu-id="146ee-162">Vedere [supporto per IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), più avanti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="146ee-162">See [Support for IWICDevelopRaw](./-wic-rawguidelines-iwicdevelopraw.md), later in this document.</span></span>

[<span data-ttu-id="146ee-163">**IWICBitmapEncoder**</span><span class="sxs-lookup"><span data-stu-id="146ee-163">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



<span data-ttu-id="146ee-164">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-164">Required</span></span>

[<span data-ttu-id="146ee-165">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="146ee-165">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="146ee-166">**GetContainerFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-166">**GetContainerFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[<span data-ttu-id="146ee-167">**GetEncoderInfo**</span><span class="sxs-lookup"><span data-stu-id="146ee-167">**GetEncoderInfo**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[<span data-ttu-id="146ee-168">**CreateNewFrame**</span><span class="sxs-lookup"><span data-stu-id="146ee-168">**CreateNewFrame**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[<span data-ttu-id="146ee-169">**Commit**</span><span class="sxs-lookup"><span data-stu-id="146ee-169">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="146ee-170">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="146ee-170">Optional</span></span>

<span data-ttu-id="146ee-171">[**Anteprima**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span><span class="sxs-lookup"><span data-stu-id="146ee-171">[**SetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹</span></span>

<span data-ttu-id="146ee-172">[**Sethumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span><span class="sxs-lookup"><span data-stu-id="146ee-172">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²</span></span>

[<span data-ttu-id="146ee-173">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="146ee-173">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[<span data-ttu-id="146ee-174">**GetMetadataQueryWriter**</span><span class="sxs-lookup"><span data-stu-id="146ee-174">**GetMetadataQueryWriter**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[<span data-ttu-id="146ee-175">**SetPalette**</span><span class="sxs-lookup"><span data-stu-id="146ee-175">**SetPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

<span data-ttu-id="146ee-176">¹ obbligatorio se il formato del file di immagine supporta le anteprime a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="146ee-176">¹Required if your image file format supports frame-level previews.</span></span>

<span data-ttu-id="146ee-177">² è obbligatorio qui o nella classe di codifica a livello di frame, a seconda della posizione in cui il formato del file di immagine archivia le anteprime.</span><span class="sxs-lookup"><span data-stu-id="146ee-177">²Required either here, or on the frame-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="146ee-178">Se implementato in questo punto, è necessario un [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) corrispondente nella classe Decode a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="146ee-178">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) is required on the container-level decode class.</span></span>

[<span data-ttu-id="146ee-179">**IWICBitmapFrameEncode**</span><span class="sxs-lookup"><span data-stu-id="146ee-179">**IWICBitmapFrameEncode**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



<span data-ttu-id="146ee-180">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-180">Required</span></span>

[<span data-ttu-id="146ee-181">**Inizializzare**</span><span class="sxs-lookup"><span data-stu-id="146ee-181">**Initialize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[<span data-ttu-id="146ee-182">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="146ee-182">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="146ee-183">**SetColorContexts**</span><span class="sxs-lookup"><span data-stu-id="146ee-183">**SetColorContexts**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[<span data-ttu-id="146ee-184">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="146ee-184">**SetSize**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[<span data-ttu-id="146ee-185">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="146ee-185">**SetPixelFormat**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[<span data-ttu-id="146ee-186">**Risoluzione dei problemi**</span><span class="sxs-lookup"><span data-stu-id="146ee-186">**SetResolution**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[<span data-ttu-id="146ee-187">**WritePixels**</span><span class="sxs-lookup"><span data-stu-id="146ee-187">**WritePixels**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[<span data-ttu-id="146ee-188">**WriteSource**</span><span class="sxs-lookup"><span data-stu-id="146ee-188">**WriteSource**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[<span data-ttu-id="146ee-189">**Commit**</span><span class="sxs-lookup"><span data-stu-id="146ee-189">**Commit**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

<span data-ttu-id="146ee-190">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="146ee-190">Optional</span></span>

<span data-ttu-id="146ee-191">[**Sethumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span><span class="sxs-lookup"><span data-stu-id="146ee-191">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹</span></span>

[<span data-ttu-id="146ee-192">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="146ee-192">**CopyPalette**</span></span>](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

<span data-ttu-id="146ee-193">¹ obbligatorio qui o nella classe di codifica a livello di contenitore, a seconda della posizione in cui il formato del file di immagine archivia le anteprime.</span><span class="sxs-lookup"><span data-stu-id="146ee-193">¹Required either here, or on the container-level encode class, depending on where your image file format stores thumbnails.</span></span> <span data-ttu-id="146ee-194">Se implementato in questo punto, è necessario un [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) corrispondente nella classe Decode a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="146ee-194">If implemented here, then a corresponding [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) is required on the frame-level decode class.</span></span>

[<span data-ttu-id="146ee-195">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="146ee-195">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



<span data-ttu-id="146ee-196">Necessario</span><span class="sxs-lookup"><span data-stu-id="146ee-196">Required</span></span>

[<span data-ttu-id="146ee-197">**InitializeFromBlockReader**</span><span class="sxs-lookup"><span data-stu-id="146ee-197">**InitializeFromBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[<span data-ttu-id="146ee-198">**AddWriter**</span><span class="sxs-lookup"><span data-stu-id="146ee-198">**AddWriter**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[<span data-ttu-id="146ee-199">**GetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="146ee-199">**GetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[<span data-ttu-id="146ee-200">**SetWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="146ee-200">**SetWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[<span data-ttu-id="146ee-201">**RemoveWriterByIndex**</span><span class="sxs-lookup"><span data-stu-id="146ee-201">**RemoveWriterByIndex**</span></span>](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

## <a name="related-topics"></a><span data-ttu-id="146ee-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="146ee-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="146ee-203">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="146ee-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="146ee-204">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="146ee-204">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="146ee-205">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="146ee-205">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="146ee-206">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="146ee-206">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 
