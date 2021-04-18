---
title: Estensioni di file
description: Estensioni di file
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Metafile di Windows Media, estensioni
- Metafile di Windows Media, estensioni di file
- Metafile, estensioni
- Metafile, estensioni di file
- Windows Media, metafile
- estensioni dei nomi di file per i file multimediali di Windows
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298725"
---
# <a name="file-name-extensions"></a><span data-ttu-id="5b788-109">Estensioni di file</span><span class="sxs-lookup"><span data-stu-id="5b788-109">File Name Extensions</span></span>

<span data-ttu-id="5b788-110">Sono disponibili linee guida specifiche per l'utilizzo delle estensioni di file per i file multimediali di Windows.</span><span class="sxs-lookup"><span data-stu-id="5b788-110">There are specific guidelines for the use of file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="5b788-111">Le estensioni del nome Metafile di Windows Media vengono utilizzate per identificare i diversi tipi di file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5b788-111">Windows Media metafile name extensions are used to identify the different types of Windows Media files.</span></span> <span data-ttu-id="5b788-112">Un'estensione di file fornisce un fornitore di software indipendente (ISV) con informazioni sui requisiti di rendering di un'applicazione che utilizza un'estensione specifica e consente agli autori di contenuti di specificare come destinazione tipi generali di lettori multimediali.</span><span class="sxs-lookup"><span data-stu-id="5b788-112">A file name extension provides an Independent Software Vendor (ISV) with information about the rendering requirements of an application that uses a particular extension, and enables content authors to target general types of media players.</span></span>

<span data-ttu-id="5b788-113">Nella tabella seguente sono elencate le linee guida relative all'estensione del nome file.</span><span class="sxs-lookup"><span data-stu-id="5b788-113">The file name extension guidelines are listed in the following table.</span></span> <span data-ttu-id="5b788-114">È consigliabile usare il tipo MIME di un file, che si trova nell'intestazione del file, per l'identificazione del tipo di file.</span><span class="sxs-lookup"><span data-stu-id="5b788-114">It is recommended that a file's MIME type, located in the file header, be used for file-type identification.</span></span>



| <span data-ttu-id="5b788-115">Estensione del file</span><span class="sxs-lookup"><span data-stu-id="5b788-115">File name extension</span></span> | <span data-ttu-id="5b788-116">tipo MIME</span><span class="sxs-lookup"><span data-stu-id="5b788-116">MIME type</span></span>      | <span data-ttu-id="5b788-117">Contenuto del file</span><span class="sxs-lookup"><span data-stu-id="5b788-117">File content</span></span>                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b788-118">wma</span><span class="sxs-lookup"><span data-stu-id="5b788-118">.wma</span></span>                | <span data-ttu-id="5b788-119">audio/x-ms-WMA</span><span class="sxs-lookup"><span data-stu-id="5b788-119">audio/x-ms-wma</span></span> | <span data-ttu-id="5b788-120">File Windows Media con solo contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="5b788-120">Windows Media file with audio content only.</span></span> <span data-ttu-id="5b788-121">Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5b788-121">Typically used to download and play files or to stream content.</span></span>                                                                             |
| <span data-ttu-id="5b788-122">wmv</span><span class="sxs-lookup"><span data-stu-id="5b788-122">.wmv</span></span>                | <span data-ttu-id="5b788-123">video/x-MS-WMV</span><span class="sxs-lookup"><span data-stu-id="5b788-123">video/x-ms-wmv</span></span> | <span data-ttu-id="5b788-124">File Windows Media con contenuto audio e/o video.</span><span class="sxs-lookup"><span data-stu-id="5b788-124">Windows Media file with audio and/or video content.</span></span> <span data-ttu-id="5b788-125">Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5b788-125">Typically used to download and play files or to stream content.</span></span>                                                                     |
| <span data-ttu-id="5b788-126">.asf</span><span class="sxs-lookup"><span data-stu-id="5b788-126">.asf</span></span>                | <span data-ttu-id="5b788-127">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="5b788-127">video/x-ms-asf</span></span> | <span data-ttu-id="5b788-128">Contenuto legacy.</span><span class="sxs-lookup"><span data-stu-id="5b788-128">Legacy content.</span></span> <span data-ttu-id="5b788-129">Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5b788-129">Typically used to download and play files or to stream content.</span></span> <span data-ttu-id="5b788-130">Può contenere contenuto audio e/o video.</span><span class="sxs-lookup"><span data-stu-id="5b788-130">May contain audio and/or video content.</span></span> <span data-ttu-id="5b788-131">Usato in genere per scaricare e riprodurre file o per trasmettere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5b788-131">Typically used to download and play files or to stream content.</span></span> |
| <span data-ttu-id="5b788-132">. WM</span><span class="sxs-lookup"><span data-stu-id="5b788-132">.wm</span></span>                 | <span data-ttu-id="5b788-133">video/x-ms-WM</span><span class="sxs-lookup"><span data-stu-id="5b788-133">video/x-ms-wm</span></span>  | <span data-ttu-id="5b788-134">Riservato</span><span class="sxs-lookup"><span data-stu-id="5b788-134">Reserved</span></span>                                                                                                                                                                                |
| <span data-ttu-id="5b788-135">. Wax</span><span class="sxs-lookup"><span data-stu-id="5b788-135">.wax</span></span>                | <span data-ttu-id="5b788-136">audio/x-ms-Wax</span><span class="sxs-lookup"><span data-stu-id="5b788-136">audio/x-ms-wax</span></span> | <span data-ttu-id="5b788-137">Metafile che fanno riferimento a file di Windows Media con estensioni di file. ASF,. WMA o. Wax.</span><span class="sxs-lookup"><span data-stu-id="5b788-137">Metafiles that reference Windows Media files with .asf, .wma, or .wax file name extensions.</span></span>                                                                                             |
| <span data-ttu-id="5b788-138">. wvx</span><span class="sxs-lookup"><span data-stu-id="5b788-138">.wvx</span></span>                | <span data-ttu-id="5b788-139">video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="5b788-139">video/x-ms-wvx</span></span> | <span data-ttu-id="5b788-140">Metafile che fanno riferimento a file Windows Media con file con estensione WMA, WMV, wvx o Wax.</span><span class="sxs-lookup"><span data-stu-id="5b788-140">Metafiles that reference Windows Media files with .wma, .wmv, .wvx, or .wax file name extensions.</span></span>                                                                                       |
| <span data-ttu-id="5b788-141">.asx</span><span class="sxs-lookup"><span data-stu-id="5b788-141">.asx</span></span>                | <span data-ttu-id="5b788-142">video/x-ms-asf</span><span class="sxs-lookup"><span data-stu-id="5b788-142">video/x-ms-asf</span></span> | <span data-ttu-id="5b788-143">Metafile che fanno riferimento a file Windows Media con file con estensione WMA, Wax, WMV, WVX, ASF o ASX.</span><span class="sxs-lookup"><span data-stu-id="5b788-143">Metafiles that reference Windows Media files with .wma, .wax, .wmv, .wvx, .asf, or .asx file name extensions.</span></span>                                                                           |
| <span data-ttu-id="5b788-144">. WMX</span><span class="sxs-lookup"><span data-stu-id="5b788-144">.wmx</span></span>                | <span data-ttu-id="5b788-145">video/x-ms-wvx</span><span class="sxs-lookup"><span data-stu-id="5b788-145">video/x-ms-wvx</span></span> | <span data-ttu-id="5b788-146">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5b788-146">Reserved.</span></span>                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="5b788-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b788-147">Remarks</span></span>

<span data-ttu-id="5b788-148">Gli script e i Digital Rights Management (DRM) devono essere supportati da qualsiasi applicazione che esegua il rendering dei file di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5b788-148">Scripting and digital rights management (DRM) must be supported by any application that renders Windows Media files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b788-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b788-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b788-150">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5b788-150">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="5b788-151">**Guida ai metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5b788-151">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="5b788-152">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5b788-152">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 




