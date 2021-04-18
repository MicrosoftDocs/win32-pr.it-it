---
description: Anteprime e anteprime
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Anteprime e anteprime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315940"
---
# <a name="thumbnails-and-previews"></a><span data-ttu-id="594a9-103">Anteprime e anteprime</span><span class="sxs-lookup"><span data-stu-id="594a9-103">Thumbnails and Previews</span></span>

<span data-ttu-id="594a9-104">Windows Vista e la raccolta foto di Windows si basano su Windows Imaging Component (WIC) per eseguire il rendering di anteprime e anteprime veloci delle immagini.</span><span class="sxs-lookup"><span data-stu-id="594a9-104">Windows Vista and the Windows Photo Gallery rely on Windows Imaging Component (WIC) to render fast thumbnails and previews of images.</span></span> <span data-ttu-id="594a9-105">Per supportare il rendering rapido di anteprime e anteprime, i codec non ELABORAti devono implementare le interfacce WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) e [**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) .</span><span class="sxs-lookup"><span data-stu-id="594a9-105">To support fast thumbnail and preview rendering, RAW codecs must implement the WIC [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) and [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) interfaces.</span></span> <span data-ttu-id="594a9-106">Per supportare un'esperienza utente reattiva, è consigliabile che queste interfacce restituiscano un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) al chiamante in 200 millisecondi o meno.</span><span class="sxs-lookup"><span data-stu-id="594a9-106">To support a responsive user experience, it is highly desirable that these interfaces return an [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to the caller in 200 milliseconds or less.</span></span>

<span data-ttu-id="594a9-107">Microsoft consiglia vivamente ai proprietari del formato di file non elaborato di generare un'anteprima prerenderizzata e di memorizzarla nella cache del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="594a9-107">Microsoft strongly recommends that RAW file format owners generate a prerendered preview and cache this in the image file.</span></span> <span data-ttu-id="594a9-108">Per un formato nel dispositivo, questa operazione viene in genere eseguita in fase di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="594a9-108">For an in-device format, this is usually done at capture time.</span></span> <span data-ttu-id="594a9-109">Tuttavia, le anteprime possono anche essere rigenerate e archiviate nel file di immagine ogni volta che vengono modificate le proprietà dell'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="594a9-109">However, previews could also be regenerated and stored in the image file whenever [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface properties are changed-if it does not take too much work to do so.</span></span>

## <a name="related-topics"></a><span data-ttu-id="594a9-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="594a9-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="594a9-111">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="594a9-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="594a9-112">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="594a9-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="594a9-113">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="594a9-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="594a9-114">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="594a9-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



