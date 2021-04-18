---
description: Requisiti dei codec RAW per Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisiti dei codec RAW per Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314448"
---
# <a name="raw-codec-requirements-for-windows-7"></a><span data-ttu-id="d0305-103">Requisiti dei codec RAW per Windows 7</span><span class="sxs-lookup"><span data-stu-id="d0305-103">RAW Codec Requirements for Windows 7</span></span>

<span data-ttu-id="d0305-104">Le funzionalità di codec seguenti sono obbligatorie almeno:</span><span class="sxs-lookup"><span data-stu-id="d0305-104">The following codec features are required at a minimum:</span></span>

<span data-ttu-id="d0305-105">Tutte le funzionalità necessarie per il supporto di Shell e raccolta foto di Windows Vista: anteprima, anteprima e rotazione (permanente).</span><span class="sxs-lookup"><span data-stu-id="d0305-105">All functionality that is required for Windows Vista shell and Photo Gallery support: thumbnail, preview, and (persisted) rotation.</span></span> <span data-ttu-id="d0305-106">Per impostazione predefinita, l'elaborazione non ELABORAta deve avere le impostazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="d0305-106">RAW processing should default to appropriate as-shot settings.</span></span>

<span data-ttu-id="d0305-107">Il supporto per i metadati di base (lettura e scrittura), i metadati non EXIF, oltre ai metadati EXIF, deve essere reso permanente all'interno di formati di file non ELABORAti senza usare i file sidecar.</span><span class="sxs-lookup"><span data-stu-id="d0305-107">Support for core metadata (both read and write), Non-EXIF metadata, as well as EXIF metadata, should be persisted inside RAW file formats without use of sidecar files.</span></span>

<span data-ttu-id="d0305-108">Supporto per l'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="d0305-108">Support for the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="d0305-109">Per Windows 7, Windows Imaging Component (WIC) WIC richiede l'implementazione di tutte le interfacce di parametro esposte da [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="d0305-109">For Windows 7, Windows Imaging Component (WIC)WIC requires that all parameter interfaces exposed by [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) be implemented.</span></span>

<span data-ttu-id="d0305-110">Supporto stato orientamento:</span><span class="sxs-lookup"><span data-stu-id="d0305-110">Orientation state support:</span></span>

-   <span data-ttu-id="d0305-111">è necessario applicare le rotazioni delle immagini di livello 90 usando il metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .</span><span class="sxs-lookup"><span data-stu-id="d0305-111">90 degree-step Image rotations should be applied by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) method.</span></span> <span data-ttu-id="d0305-112">Le applicazioni e Windows utilizzano questo metodo per ruotare le immagini (e anteprime e anteprime memorizzate nella cache).</span><span class="sxs-lookup"><span data-stu-id="d0305-112">Applications and Windows use this method to rotate the images (and cached thumbnails and previews).</span></span>
-   <span data-ttu-id="d0305-113">L'applicazione della rotazione tramite questa API deve anche essere resa permanente dal codec (vedere in precedenza in questo articolo).</span><span class="sxs-lookup"><span data-stu-id="d0305-113">Application of rotation by using this API should also be persisted by the codec (see earlier in this paper).</span></span>
-   <span data-ttu-id="d0305-114">Le applicazioni possono usare le funzionalità di rotazione dell'API [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , ma il codec non serializza le impostazioni di rotazione sull'API, quindi le rotazioni eseguite con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) non saranno rese permanente.</span><span class="sxs-lookup"><span data-stu-id="d0305-114">Applications can use the rotation capabilities of the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) API, but the codec will not serialize any rotation settings on this API, so rotations done using [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) will not be persisted.</span></span>

<span data-ttu-id="d0305-115">Supporto per l'estrazione di anteprime e anteprime ad alta velocità.</span><span class="sxs-lookup"><span data-stu-id="d0305-115">High-speed thumbnail and preview extraction support.</span></span> <span data-ttu-id="d0305-116">Se la dimensione massima in pixel dell'anteprima (larghezza o altezza) è inferiore a 1024 pixel, Windows Vista richiederà un rendering per l'anteprima dello schermo:</span><span class="sxs-lookup"><span data-stu-id="d0305-116">If the preview maximum pixel dimension (width or height) is less than 1024 pixels in size, Windows Vista will request a render for screen preview:</span></span>

-   <span data-ttu-id="d0305-117">Il metodo [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) deve supportare almeno le modalità [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) e [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) per consentire il rendering più veloce di anteprime e anteprime rispetto alla modalità di qualità completa.</span><span class="sxs-lookup"><span data-stu-id="d0305-117">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) method should support at least the [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) and [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) modes to allow faster rendering of thumbnails and previews than the full-quality mode.</span></span>
-   <span data-ttu-id="d0305-118">Windows chiamerà [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con le dimensioni di risoluzione dello schermo richieste.</span><span class="sxs-lookup"><span data-stu-id="d0305-118">Windows will call [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) with the requested screen resolution size.</span></span>
-   <span data-ttu-id="d0305-119">Le dimensioni di risoluzione dello schermo devono essere supportate nell'API precedente.</span><span class="sxs-lookup"><span data-stu-id="d0305-119">Screen resolution sizes must be supported in the above API.</span></span>
-   <span data-ttu-id="d0305-120">È richiesta l'elaborazione coerente di immagini di anteprime, anteprime e bit di immagini complete da [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .</span><span class="sxs-lookup"><span data-stu-id="d0305-120">Consistent image processing of thumbnail, preview, and full-image bits from [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) is required.</span></span>

<span data-ttu-id="d0305-121">Formati pixel HDR (High Dynamic Range).</span><span class="sxs-lookup"><span data-stu-id="d0305-121">High dynamic range (HDR) pixel formats.</span></span>

<span data-ttu-id="d0305-122">Stampa XPS (XML Paper Specification).</span><span class="sxs-lookup"><span data-stu-id="d0305-122">XML Paper Specification (XPS) printing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0305-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0305-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d0305-124">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d0305-124">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d0305-125">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="d0305-125">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="d0305-126">Linee guida per WIC per i formati di immagine RAW della fotocamera</span><span class="sxs-lookup"><span data-stu-id="d0305-126">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="d0305-127">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="d0305-127">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



