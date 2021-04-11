---
title: Guida di riferimento a Gestione compressione video
description: Guida di riferimento a Gestione compressione video
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video per Windows (VFW), Video Compression Manager (VCM)
- VFW (video per Windows), Gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221122"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="1393e-105">Guida di riferimento a Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="1393e-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="1393e-106">Questa sezione descrive le funzioni, le strutture, i messaggi e le macro associate a VCM.</span><span class="sxs-lookup"><span data-stu-id="1393e-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="1393e-107">Questi elementi vengono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="1393e-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="1393e-108">Installazione e rimozione del compressore</span><span class="sxs-lookup"><span data-stu-id="1393e-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="1393e-109">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="1393e-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="1393e-110">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="1393e-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="1393e-111">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="1393e-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="1393e-112">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="1393e-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="1393e-113">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="1393e-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="1393e-114">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="1393e-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="1393e-115">Individuazione e apertura di un compressore</span><span class="sxs-lookup"><span data-stu-id="1393e-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="1393e-116">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="1393e-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="1393e-117">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="1393e-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="1393e-118">**ICDecompressOpen**</span><span class="sxs-lookup"><span data-stu-id="1393e-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="1393e-119">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="1393e-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="1393e-120">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="1393e-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="1393e-121">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="1393e-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="1393e-122">Selezione di comprimeri</span><span class="sxs-lookup"><span data-stu-id="1393e-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="1393e-123">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="1393e-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="1393e-124">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="1393e-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="1393e-125">**COMPVARS**</span><span class="sxs-lookup"><span data-stu-id="1393e-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="1393e-126">Configurazione di compressatori</span><span class="sxs-lookup"><span data-stu-id="1393e-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="1393e-127">**configurazione di ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="1393e-128">**STATO di ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="1393e-129">**\_stato MCI**</span><span class="sxs-lookup"><span data-stu-id="1393e-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="1393e-130">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="1393e-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="1393e-131">Informazioni sul compressore</span><span class="sxs-lookup"><span data-stu-id="1393e-131">Compressor Information</span></span>

-   [<span data-ttu-id="1393e-132">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1393e-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="1393e-133">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="1393e-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="1393e-134">**\_GETDEFAULTKEYFRAMERATE ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="1393e-135">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="1393e-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="1393e-136">**\_GETDEFAULTQUALITY ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="1393e-137">**ICM \_ su**</span><span class="sxs-lookup"><span data-stu-id="1393e-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="1393e-138">Compressione di immagini singole</span><span class="sxs-lookup"><span data-stu-id="1393e-138">Single Image Compression</span></span>

-   [<span data-ttu-id="1393e-139">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="1393e-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="1393e-140">Compressione sequenza</span><span class="sxs-lookup"><span data-stu-id="1393e-140">Sequence Compression</span></span>

-   [<span data-ttu-id="1393e-141">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="1393e-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="1393e-142">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="1393e-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="1393e-143">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="1393e-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="1393e-144">COMPVARS</span><span class="sxs-lookup"><span data-stu-id="1393e-144">COMPVARS</span></span>

-   [<span data-ttu-id="1393e-145">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="1393e-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="1393e-146">Compressione dati immagine</span><span class="sxs-lookup"><span data-stu-id="1393e-146">Image Data Compression</span></span>

-   [<span data-ttu-id="1393e-147">**ICCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="1393e-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="1393e-148">**\_formato MCI compress \_ get \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="1393e-149">**\_query di compressione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="1393e-150">**\_ \_ dimensioni Get della compressione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="1393e-151">**\_inizio compressione \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="1393e-152">**\_fine compressione \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="1393e-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="1393e-153">Monitoraggio compressore</span><span class="sxs-lookup"><span data-stu-id="1393e-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="1393e-154">**ICSETSTATUSPROC**</span><span class="sxs-lookup"><span data-stu-id="1393e-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="1393e-155">Decompressione di immagini singole</span><span class="sxs-lookup"><span data-stu-id="1393e-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="1393e-156">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="1393e-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="1393e-157">Decompressione dei dati dell'immagine</span><span class="sxs-lookup"><span data-stu-id="1393e-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="1393e-158">**ICDECOMPRESSEX**</span><span class="sxs-lookup"><span data-stu-id="1393e-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="1393e-159">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="1393e-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="1393e-160">**\_fine DECOMPRESSEX \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="1393e-161">**\_formato di \_ ottenimento di MCI decompresso \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="1393e-162">**\_tavolozza Decomprimi MCI \_ get \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="1393e-163">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="1393e-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="1393e-164">**ICDECOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="1393e-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="1393e-165">**\_inizio decompressione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="1393e-166">**\_fine Decomprimi MCI \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="1393e-167">**\_query di decompressione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="1393e-168">Uso delle funzionalità di Hardware-Drawing</span><span class="sxs-lookup"><span data-stu-id="1393e-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="1393e-169">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="1393e-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="1393e-170">**ICDRAWBEGIN**</span><span class="sxs-lookup"><span data-stu-id="1393e-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="1393e-171">**\_fine di disegnato ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="1393e-172">**\_ \_ SCARICAmento ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="1393e-173">**\_query di estrazione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="1393e-174">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="1393e-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="1393e-175">**\_inizio estrazione \_ ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="1393e-176">**\_arresto di disegnato ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="1393e-177">**\_GETBUFFERSWANTED ICM**</span><span class="sxs-lookup"><span data-stu-id="1393e-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="1393e-178">**\_progetto ICM \_ realizzato**</span><span class="sxs-lookup"><span data-stu-id="1393e-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="1393e-179">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="1393e-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="1393e-180">**ICDRAW**</span><span class="sxs-lookup"><span data-stu-id="1393e-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="1393e-181">**\_tempo di elaborazione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="1393e-182">**\_tempo di elaborazione ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="1393e-183">**\_finestra di disegni ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="1393e-184">**\_progetto ICM \_ realizzato**</span><span class="sxs-lookup"><span data-stu-id="1393e-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="1393e-185">**\_CHANGEPALETTE di disegni ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="1393e-186">**\_RENDERBUFFER di disegni ICM \_**</span><span class="sxs-lookup"><span data-stu-id="1393e-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="1393e-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1393e-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1393e-188">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="1393e-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




