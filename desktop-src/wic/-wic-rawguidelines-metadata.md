---
description: Supporto dei metadati
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Supporto dei metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315944"
---
# <a name="metadata-support"></a><span data-ttu-id="29365-103">Supporto dei metadati</span><span class="sxs-lookup"><span data-stu-id="29365-103">Metadata Support</span></span>

<span data-ttu-id="29365-104">I formati RAW devono supportare anche gli scenari di lettura e scrittura dei metadati comuni per le immagini di Windows.</span><span class="sxs-lookup"><span data-stu-id="29365-104">RAW formats should also support the common metadata read and write scenarios for images in Windows.</span></span> <span data-ttu-id="29365-105">Microsoft ha sviluppato un set di provider di metadati nativi per i metadati di file di immagine scambiabili (EXIF), International Press Telecommunications Council (IPTC) ed Extensible Metadata Platform (XMP) attualmente richiamati solo per i contenitori TIFF e JPEG.</span><span class="sxs-lookup"><span data-stu-id="29365-105">Microsoft has developed a set of native metadata providers for exchangeable image file (EXIF), International Press Telecommunications Council (IPTC), and Extensible Metadata Platform (XMP) metadata that are currently invoked only for TIFF and JPEG containers.</span></span> <span data-ttu-id="29365-106">Se l'immagine non ELABORAta è archiviata in uno di questi formati di contenitore, è consigliabile usare i provider di metadati predefiniti di Windows.</span><span class="sxs-lookup"><span data-stu-id="29365-106">If the RAW image is stored in one of these container formats, it is recommended to use the Windows built-in metadata providers.</span></span> <span data-ttu-id="29365-107">Tuttavia, l'autore del codec è responsabile della configurazione corretta.</span><span class="sxs-lookup"><span data-stu-id="29365-107">However, the codec author is responsible for configuring this properly.</span></span> <span data-ttu-id="29365-108">Per i file non ELABORAti non basati su un contenitore TIFF, potrebbe essere necessario implementare i writer EXIF, IPTC o XMP perché i reader e i writer incorporati si aspettano che i dati siano conformi alle specifiche del layout su disco EXIF, IPTC e XMP.</span><span class="sxs-lookup"><span data-stu-id="29365-108">For RAW files that are not based on a TIFF container, it might be necessary to implement EXIF, IPTC, or XMP writers because the built-in readers and writers expect the data to conform to EXIF, IPTC, and XMP on-disk layout specifications.</span></span> <span data-ttu-id="29365-109">Gli autori di codec possono inoltre implementare i propri provider per eventuali metadati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="29365-109">Codec authors can also implement their own providers for any custom metadata.</span></span>

<span data-ttu-id="29365-110">A causa dell'architettura di Windows Imaging Component (WIC), i writer dei metadati possono essere richiamati solo tramite un'istanza di un codificatore di immagini.</span><span class="sxs-lookup"><span data-stu-id="29365-110">Because of the architecture of Windows Imaging Component (WIC), metadata writers can be invoked only through an instance of an image encoder.</span></span> <span data-ttu-id="29365-111">Pertanto, i proprietari del formato RAW devono creare almeno un codificatore "Stub" [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) , anche se la codifica effettiva di pixel in un formato non elaborato non è implementata.</span><span class="sxs-lookup"><span data-stu-id="29365-111">Therefore, RAW format owners should create at least a "stub" [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) encoder, even if the actual encoding of pixels into a RAW format is not implemented.</span></span> <span data-ttu-id="29365-112">L'autore del codec deve richiamare i gestori di metadati appropriati:</span><span class="sxs-lookup"><span data-stu-id="29365-112">The codec author must invoke the proper metadata handlers:</span></span>

-   <span data-ttu-id="29365-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) sia nel decodificatore che nel decodificatore di frame, nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="29365-113">[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) on both the decoder and frame decoder as appropriate.</span></span>
-   <span data-ttu-id="29365-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) sia nel codificatore che nel codificatore di frame, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="29365-114">[**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on both the encoder and frame encoder as appropriate.</span></span>

<span data-ttu-id="29365-115">Per supportare tutti gli scenari previsti nelle applicazioni di creazione di immagini in Windows Vista, è consigliabile che i fornitori di codec supportino almeno quanto segue:</span><span class="sxs-lookup"><span data-stu-id="29365-115">To support all of the anticipated scenarios in imaging applications in Windows Vista, it is recommended that codec vendors support the following at a minimum:</span></span>

-   <span data-ttu-id="29365-116">Lettura EXIF</span><span class="sxs-lookup"><span data-stu-id="29365-116">EXIF read</span></span>
-   <span data-ttu-id="29365-117">Scrittura EXIF parziale (per consentire agli aggiornamenti di acquisire data e ora)</span><span class="sxs-lookup"><span data-stu-id="29365-117">Partial EXIF write (to permit updates to capture date and time)</span></span>
-   <span data-ttu-id="29365-118">Lettura e scrittura XMP (inclusa l'opzione IPTC Core per XMP)</span><span class="sxs-lookup"><span data-stu-id="29365-118">XMP read and write (including optionally IPTC Core for XMP)</span></span>
-   <span data-ttu-id="29365-119">Lettura e scrittura di IPTC IIMv4</span><span class="sxs-lookup"><span data-stu-id="29365-119">IPTC IIMv4 read and write</span></span>

<span data-ttu-id="29365-120">La maggior parte degli accessi ai metadati (sia di lettura che di scrittura) in Windows Vista viene eseguita tramite l'interfaccia [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) o [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="29365-120">Most of the metadata access (both read and write) in Windows Vista occurs through the [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) or [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) interface.</span></span> <span data-ttu-id="29365-121">Pertanto, per partecipare all'esperienza dei metadati di Windows Vista, gli autori di codec non ELABORAti devono implementare i metodi [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) e [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="29365-121">Therefore, to participate in the Windows Vista metadata experiences, RAW codec authors must implement the [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29365-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="29365-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="29365-123">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="29365-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29365-124">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="29365-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="29365-125">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="29365-125">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="29365-126">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="29365-126">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



