---
description: 'Completezza delle funzionalità: interfacce consigliate'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Completezza delle funzionalità: interfacce consigliate'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315953"
---
# <a name="feature-completeness-recommended-interfaces"></a><span data-ttu-id="e0a7a-103">Completezza delle funzionalità: interfacce consigliate</span><span class="sxs-lookup"><span data-stu-id="e0a7a-103">Feature Completeness: Recommended Interfaces</span></span>

<span data-ttu-id="e0a7a-104">Nella tabella seguente sono elencati i codec non ELABORAti delle interfacce di Windows Imaging Component (WIC) che devono essere implementati.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-104">The following table lists the Windows Imaging Component (WIC) interfaces RAW codecs should implement.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0a7a-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e0a7a-105">Interface</span></span></th>
<th><span data-ttu-id="e0a7a-106">Necessario per</span><span class="sxs-lookup"><span data-stu-id="e0a7a-106">Required for</span></span></th>
<th><span data-ttu-id="e0a7a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0a7a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0a7a-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-108"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-109">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-109">Decoders</span></span></td>
<td><span data-ttu-id="e0a7a-110">Rappresenta il punto di partenza per la decodifica di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-110">Represents the starting point for decoding an image file.</span></span> <span data-ttu-id="e0a7a-111">Fornisce l'accesso alle proprietà a livello di contenitore come anteprime, frame e tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-111">Provides access to container-level properties like thumbnails, frames, and palette.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a7a-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-112"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-113">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-113">Decoders</span></span></td>
<td><span data-ttu-id="e0a7a-114">Rappresenta un frame di immagine specifico all'interno del contenitore che fornisce l'accesso alle proprietà a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-114">Represents a specific image frame within the container that provides access to frame-level properties.</span></span> <span data-ttu-id="e0a7a-115">Si tratta dell'interfaccia che decodifica i bit dell'immagine effettivi.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-115">This is the interface that decodes the actual image bits.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0a7a-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-116"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-117">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-117">Decoders</span></span></td>
<td><span data-ttu-id="e0a7a-118">Obbligatorio per l'enumerazione e l'iterazione nei blocchi di metadati e per richiamare i reader di metadati appropriati durante la lettura da un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-118">Required for enumerating and iterating through metadata blocks and invoking the appropriate metadata readers when reading from an image file.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0a7a-119">Se il formato del contenitore non elaborato è compatibile con TIFF oppure utilizza IFDs o IRBs standard per archiviare i metadati EXIF o XMP, gli autori di codec possono scegliere di richiamare i lettori di metadati predefiniti anziché scriverne di propri.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-119">If the RAW container format is TIFF compatible or uses standard IFDs or IRBs to store EXIF or XMP metadata, codec authors can choose to invoke the built-in metadata readers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a7a-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-120"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-121">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-121">Decoders</span></span></td>
<td><span data-ttu-id="e0a7a-122">Consente al chiamante di specificare il formato di ridimensionamento, ritaglio, rotazione o pixel desiderato per l'immagine decodificata, che può migliorare significativamente le prestazioni del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-122">Allows the caller to specify desired scaling, cropping, rotation, or pixel format for the decoded image, which can significantly improve decoder performance.</span></span> <span data-ttu-id="e0a7a-123">Ad esempio, i decodificatori JPEG e wireless datagramma (WDP) di Microsoft utilizzano uno schema di ottimizzazione a piramide per ottenere una decodifica più veloce quando la bitmap di destinazione è inferiore alla bitmap di origine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-123">For example, Microsoft's JPEG and Wireless Datagram Protocol (WDP) decoders use a pyramid optimization scheme to achieve faster decoding when the target bitmap is smaller than the source bitmap.</span></span> <span data-ttu-id="e0a7a-124">Windows Vista (e versioni successive) tenterà di utilizzare questa interfaccia per estrarre un' &quot; &quot; Anteprima veloce da un'immagine non elaborata ogni volta che l'anteprima incorporata è mancante o inferiore a 1.024 pixel nella dimensione massima.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-124">Windows Vista (and later) will attempt to use this interface to extract a &quot;fast&quot; preview from a RAW image whenever the embedded preview is missing or less than 1,024 pixels in its largest dimension.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0a7a-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-125"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-126">Decodificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-126">Decoders</span></span></td>
<td><span data-ttu-id="e0a7a-127">Obbligatorio per i formati non ELABORAti.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-127">Required for RAW formats.</span></span> <span data-ttu-id="e0a7a-128">Espone parametri specifici dell'elaborazione di immagini non ELABORAte.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-128">Exposes parameters that are specific to RAW image processing.</span></span> <span data-ttu-id="e0a7a-129">I codec RAW dovrebbero supportare tutti questi parametri applicabili al codec.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-129">RAW codecs should support as many of these parameters as apply to the codec.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a7a-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-130"><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-131">Codificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-131">Encoders</span></span></td>
<td><span data-ttu-id="e0a7a-132">Rappresenta il punto di partenza per la codifica di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-132">Represents the starting point for encoding an image file.</span></span> <span data-ttu-id="e0a7a-133">Questa interfaccia viene utilizzata per impostare le proprietà a livello di contenitore, ad esempio le anteprime, i frame e la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-133">This interface is used for setting container-level properties, such as thumbnails, frames, and palette.</span></span> <span data-ttu-id="e0a7a-134">È inoltre necessario richiamare un writer di metadati per abilitare la persistenza dei metadati nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-134">It is also required to invoke a metadata writer to enable metadata persistence to the image file.</span></span> <span data-ttu-id="e0a7a-135">Per questi motivi, questa interfaccia è necessaria anche se la codifica della bitmap primaria nel formato non elaborato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-135">For these reasons, this interface is necessary even if encoding the primary bitmap to the RAW format is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0a7a-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-136"><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-137">Codificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-137">Encoders</span></span></td>
<td><span data-ttu-id="e0a7a-138">Rappresenta un frame di immagine specifico all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-138">Represents a specific image frame within the container.</span></span> <span data-ttu-id="e0a7a-139">Questa interfaccia viene usata per codificare i bit dell'immagine effettivi e per impostare i metadati e le proprietà per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-139">This interface is used to encode the actual image bits and to set per-frame metadata and properties.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0a7a-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span><span class="sxs-lookup"><span data-stu-id="e0a7a-140"><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></span></span></td>
<td><span data-ttu-id="e0a7a-141">Codificatori</span><span class="sxs-lookup"><span data-stu-id="e0a7a-141">Encoders</span></span></td>
<td><span data-ttu-id="e0a7a-142">Obbligatorio per scorrere i blocchi di metadati e richiamare i writer di metadati appropriati durante la serializzazione di un file di immagine.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-142">Required for iterating through metadata blocks and invoking the appropriate metadata writers when serializing an image file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0a7a-143">Se il formato del contenitore non elaborato è compatibile con TIFF, gli autori di codec possono scegliere di richiamare i writer di metadati predefiniti anziché scriverne di propri.</span><span class="sxs-lookup"><span data-stu-id="e0a7a-143">If the RAW container format is TIFF-compatible, codec authors can choose to invoke the built-in metadata writers rather than writing their own.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e0a7a-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0a7a-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e0a7a-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="e0a7a-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0a7a-146">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="e0a7a-146">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="e0a7a-147">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="e0a7a-147">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="e0a7a-148">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="e0a7a-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




