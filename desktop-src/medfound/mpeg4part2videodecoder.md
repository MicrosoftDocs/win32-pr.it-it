---
description: Il decodificatore MPEG4 Part 2 video decodifica i flussi video codificati in base allo standard MPEG4 Part 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: MPEG-4 Part 2 video decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226525"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="b83c7-103">MPEG-4 Part 2 video decoder</span><span class="sxs-lookup"><span data-stu-id="b83c7-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="b83c7-104">Il decodificatore MPEG4 Part 2 video decodifica i flussi video codificati in base allo standard MPEG4 Part 2.</span><span class="sxs-lookup"><span data-stu-id="b83c7-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="b83c7-105">È possibile creare un'istanza del decodificatore MPEG4 Part 2 video chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b83c7-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="b83c7-106">Per creare un'istanza del decodificatore che si comporta come un oggetto DMO (DirectX Media Object), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="b83c7-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="b83c7-107">Per creare un istanza del decodificatore che si comporta come una trasformazione Media Foundation (MFT), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMFT**.</span><span class="sxs-lookup"><span data-stu-id="b83c7-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="b83c7-108">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="b83c7-108">Input Types</span></span>

<span data-ttu-id="b83c7-109">Il decodificatore MPEG4 Part 2 video supporta i tipi di supporti di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="b83c7-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="b83c7-110">\_M4S2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="b83c7-111">\_M4S2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="b83c7-112">\_MP4V MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="b83c7-113">\_MP4V MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="b83c7-114">MEDIASUBTYPE \_ mp4s (deprecato)</span><span class="sxs-lookup"><span data-stu-id="b83c7-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="b83c7-115">MEDIASUBTYPE \_ mp4s (deprecato)</span><span class="sxs-lookup"><span data-stu-id="b83c7-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="b83c7-116">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="b83c7-116">Output Types</span></span>

<span data-ttu-id="b83c7-117">Il decodificatore MPEG4 Part 2 video supporta i sottotipi di supporti di output seguenti quando funge da DMO.</span><span class="sxs-lookup"><span data-stu-id="b83c7-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="b83c7-118">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="b83c7-119">\_NV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="b83c7-120">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="b83c7-121">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="b83c7-122">\_YVYU MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="b83c7-123">\_NV11 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="b83c7-124">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="b83c7-125">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="b83c7-126">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="b83c7-127">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="b83c7-128">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="b83c7-129">Il decodificatore MPEG4 Part 2 video supporta i sottotipi di supporti di output seguenti quando funge da MFT.</span><span class="sxs-lookup"><span data-stu-id="b83c7-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="b83c7-130">\_NV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="b83c7-131">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b83c7-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="b83c7-132">Formati</span><span class="sxs-lookup"><span data-stu-id="b83c7-132">Formats</span></span>

<span data-ttu-id="b83c7-133">Il decodificatore MPEG4 Part 2 video accetta i formati seguenti.</span><span class="sxs-lookup"><span data-stu-id="b83c7-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="b83c7-134">**VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="b83c7-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="b83c7-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="b83c7-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="b83c7-136">**MFVideoInfo**</span><span class="sxs-lookup"><span data-stu-id="b83c7-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="b83c7-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (viene utilizzata solo la parte VIH2 dell'intestazione).</span><span class="sxs-lookup"><span data-stu-id="b83c7-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="b83c7-138">Interfacce per DMO</span><span class="sxs-lookup"><span data-stu-id="b83c7-138">Interfaces for the DMO</span></span>

<span data-ttu-id="b83c7-139">Se si crea un'istanza del decodificatore MPEG4 Part 2 video come DMO, il decodificatore espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="b83c7-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="b83c7-140">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="b83c7-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="b83c7-141">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="b83c7-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="b83c7-142">È possibile ottenere un'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) chiamando **CoCreateInstance** ed è possibile ottenere un'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) chiamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b83c7-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="b83c7-143">Interfacce per MFT</span><span class="sxs-lookup"><span data-stu-id="b83c7-143">Interfaces for the MFT</span></span>

<span data-ttu-id="b83c7-144">Se si crea un'istanza del decodificatore MPEG2 Part 2 video come MFT, il decodificatore espone le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="b83c7-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="b83c7-145">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="b83c7-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="b83c7-146">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="b83c7-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="b83c7-147">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="b83c7-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="b83c7-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="b83c7-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="b83c7-149">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="b83c7-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="b83c7-150">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="b83c7-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="b83c7-151">È possibile ottenere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) chiamando **CoCreateInstance** ed è possibile ottenere un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) chiamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span><span class="sxs-lookup"><span data-stu-id="b83c7-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="b83c7-152">È possibile ottenere un puntatore all'interfaccia [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) chiamando **QueryInterface** in MFT.</span><span class="sxs-lookup"><span data-stu-id="b83c7-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="b83c7-153">È possibile ottenere un puntatore all'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e passando l'identificatore del servizio **MF \_ rate \_ Control \_ Service**.</span><span class="sxs-lookup"><span data-stu-id="b83c7-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="b83c7-154">Profili e livelli</span><span class="sxs-lookup"><span data-stu-id="b83c7-154">Profiles and Levels</span></span>

<span data-ttu-id="b83c7-155">La specifica MPEG4 definisce diversi profili, ognuno dei quali specifica gli strumenti che un codificatore può usare per generare un flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="b83c7-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="b83c7-156">Il decodificatore del video MPEG4 part2 supporta due di questi profili: profilo visivo semplice e profilo semplice avanzato.</span><span class="sxs-lookup"><span data-stu-id="b83c7-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="b83c7-157">In altre parole, il decodificatore MPEG4 Part 2 video può decodificare i flussi codificati in base al profilo visivo semplice o al profilo semplice avanzato.</span><span class="sxs-lookup"><span data-stu-id="b83c7-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="b83c7-158">Il profilo visivo semplice supporta la trasmissione di base di video a bassa velocità in modalità progressiva.</span><span class="sxs-lookup"><span data-stu-id="b83c7-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="b83c7-159">Supporta solo le immagini intra e Prediction.</span><span class="sxs-lookup"><span data-stu-id="b83c7-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="b83c7-160">Supporta anche la modalità di intestazione breve, che è compatibile con le versioni precedenti del profilo di base H. 263.</span><span class="sxs-lookup"><span data-stu-id="b83c7-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="b83c7-161">A partire da Windows 10, il decoder MPEG-4 Part 2 video supporta anche H. 263v2 (H. 263 +) che supporta le dimensioni delle immagini personalizzate.</span><span class="sxs-lookup"><span data-stu-id="b83c7-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="b83c7-162">Il profilo semplice avanzato supporta tutti gli strumenti del profilo visivo semplice e supporta inoltre i video interlacciati, i frame B, la compensazione del movimento trimestrale, le tabelle di quantizzazione aggiuntive e la compensazione di movimento globale.</span><span class="sxs-lookup"><span data-stu-id="b83c7-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="b83c7-163">La specifica MPEG4 definisce anche diversi livelli, ognuno dei quali specifica i vincoli sul flusso di output generato da un codificatore.</span><span class="sxs-lookup"><span data-stu-id="b83c7-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="b83c7-164">La tabella seguente illustra i profili e i livelli, insieme alle risoluzioni tipiche, supportate dal decodificatore MPEG4 Part 2 video.</span><span class="sxs-lookup"><span data-stu-id="b83c7-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="b83c7-165">Profilo</span><span class="sxs-lookup"><span data-stu-id="b83c7-165">Profile</span></span>         | <span data-ttu-id="b83c7-166">Level</span><span class="sxs-lookup"><span data-stu-id="b83c7-166">Level</span></span> | <span data-ttu-id="b83c7-167">Risoluzione tipica</span><span class="sxs-lookup"><span data-stu-id="b83c7-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="b83c7-168">Visualizzazione semplice</span><span class="sxs-lookup"><span data-stu-id="b83c7-168">Simple Visual</span></span>   | <span data-ttu-id="b83c7-169">0</span><span class="sxs-lookup"><span data-stu-id="b83c7-169">0</span></span>     | <span data-ttu-id="b83c7-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="b83c7-170">176 x 144</span></span>          |
| <span data-ttu-id="b83c7-171">Visualizzazione semplice</span><span class="sxs-lookup"><span data-stu-id="b83c7-171">Simple Visual</span></span>   | <span data-ttu-id="b83c7-172">1</span><span class="sxs-lookup"><span data-stu-id="b83c7-172">1</span></span>     | <span data-ttu-id="b83c7-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="b83c7-173">176 x 144</span></span>          |
| <span data-ttu-id="b83c7-174">Visualizzazione semplice</span><span class="sxs-lookup"><span data-stu-id="b83c7-174">Simple Visual</span></span>   | <span data-ttu-id="b83c7-175">2</span><span class="sxs-lookup"><span data-stu-id="b83c7-175">2</span></span>     | <span data-ttu-id="b83c7-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="b83c7-176">352 x 288</span></span>          |
| <span data-ttu-id="b83c7-177">Visualizzazione semplice</span><span class="sxs-lookup"><span data-stu-id="b83c7-177">Simple Visual</span></span>   | <span data-ttu-id="b83c7-178">3</span><span class="sxs-lookup"><span data-stu-id="b83c7-178">3</span></span>     | <span data-ttu-id="b83c7-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="b83c7-179">352 x 288</span></span>          |
| <span data-ttu-id="b83c7-180">SimpleVisual</span><span class="sxs-lookup"><span data-stu-id="b83c7-180">SimpleVisual</span></span>    | <span data-ttu-id="b83c7-181">4a</span><span class="sxs-lookup"><span data-stu-id="b83c7-181">4a</span></span>    | <span data-ttu-id="b83c7-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="b83c7-182">640 x 480</span></span>          |
| <span data-ttu-id="b83c7-183">Visualizzazione semplice</span><span class="sxs-lookup"><span data-stu-id="b83c7-183">Simple Visual</span></span>   | <span data-ttu-id="b83c7-184">5</span><span class="sxs-lookup"><span data-stu-id="b83c7-184">5</span></span>     | <span data-ttu-id="b83c7-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="b83c7-185">720 x 576</span></span>          |
| <span data-ttu-id="b83c7-186">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-186">Advanced Simple</span></span> | <span data-ttu-id="b83c7-187">0</span><span class="sxs-lookup"><span data-stu-id="b83c7-187">0</span></span>     | <span data-ttu-id="b83c7-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="b83c7-188">176 x 144</span></span>          |
| <span data-ttu-id="b83c7-189">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-189">Advanced Simple</span></span> | <span data-ttu-id="b83c7-190">1</span><span class="sxs-lookup"><span data-stu-id="b83c7-190">1</span></span>     | <span data-ttu-id="b83c7-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="b83c7-191">176 x 144</span></span>          |
| <span data-ttu-id="b83c7-192">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-192">Advanced Simple</span></span> | <span data-ttu-id="b83c7-193">2</span><span class="sxs-lookup"><span data-stu-id="b83c7-193">2</span></span>     | <span data-ttu-id="b83c7-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="b83c7-194">352 x 288</span></span>          |
| <span data-ttu-id="b83c7-195">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-195">Advanced Simple</span></span> | <span data-ttu-id="b83c7-196">3</span><span class="sxs-lookup"><span data-stu-id="b83c7-196">3</span></span>     | <span data-ttu-id="b83c7-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="b83c7-197">352 x 288</span></span>          |
| <span data-ttu-id="b83c7-198">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-198">Advanced Simple</span></span> | <span data-ttu-id="b83c7-199">3b</span><span class="sxs-lookup"><span data-stu-id="b83c7-199">3b</span></span>    | <span data-ttu-id="b83c7-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="b83c7-200">352 x 288</span></span>          |
| <span data-ttu-id="b83c7-201">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-201">Advanced Simple</span></span> | <span data-ttu-id="b83c7-202">4</span><span class="sxs-lookup"><span data-stu-id="b83c7-202">4</span></span>     | <span data-ttu-id="b83c7-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="b83c7-203">352 x 756</span></span>          |
| <span data-ttu-id="b83c7-204">Semplice avanzata</span><span class="sxs-lookup"><span data-stu-id="b83c7-204">Advanced Simple</span></span> | <span data-ttu-id="b83c7-205">5</span><span class="sxs-lookup"><span data-stu-id="b83c7-205">5</span></span>     | <span data-ttu-id="b83c7-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="b83c7-206">720 x 576</span></span>          |



 

<span data-ttu-id="b83c7-207">Per ulteriori informazioni sui profili e sui livelli, vedere la specifica MPEG4 Part 2 (ISO/IEC 14496-2): Information technology--Coding of audio-visual objects--Part 2: Visual.</span><span class="sxs-lookup"><span data-stu-id="b83c7-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="b83c7-208">Proprietà decodificatore</span><span class="sxs-lookup"><span data-stu-id="b83c7-208">Decoder Properties</span></span>

<span data-ttu-id="b83c7-209">Per impostare le proprietà nel decodificatore MPEG4 Part 2 video, usare l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="b83c7-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="b83c7-210">Il decodificatore MPEG4 Part 2 video supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="b83c7-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b83c7-211">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b83c7-211">Property</span></span></th>
<th><span data-ttu-id="b83c7-212">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b83c7-212">Description</span></span></th>
<th><span data-ttu-id="b83c7-213">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b83c7-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b83c7-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="b83c7-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="b83c7-215">Specifica il livello di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="b83c7-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="b83c7-216">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b83c7-216">Windows 7.</span></span><br />
<span data-ttu-id="b83c7-217">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="b83c7-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="b83c7-218">100</span><span class="sxs-lookup"><span data-stu-id="b83c7-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b83c7-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="b83c7-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="b83c7-220">Specifica la modalità di generazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="b83c7-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="b83c7-221">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b83c7-221">Windows 7.</span></span><br />
<span data-ttu-id="b83c7-222">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="b83c7-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="b83c7-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="b83c7-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b83c7-224">Commenti</span><span class="sxs-lookup"><span data-stu-id="b83c7-224">Remarks</span></span>

<span data-ttu-id="b83c7-225">Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="b83c7-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="b83c7-226">I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="b83c7-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="b83c7-227">Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere tipi di [supporti](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="b83c7-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b83c7-228">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b83c7-228">Requirements</span></span>



| <span data-ttu-id="b83c7-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="b83c7-229">Requirement</span></span> | <span data-ttu-id="b83c7-230">Valore</span><span class="sxs-lookup"><span data-stu-id="b83c7-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b83c7-231">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b83c7-231">Minimum supported client</span></span><br/> | <span data-ttu-id="b83c7-232">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b83c7-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b83c7-233">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b83c7-233">Minimum supported server</span></span><br/> | <span data-ttu-id="b83c7-234">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b83c7-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b83c7-235">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b83c7-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="b83c7-236"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b83c7-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="b83c7-237">DLL</span><span class="sxs-lookup"><span data-stu-id="b83c7-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b83c7-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b83c7-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b83c7-239">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b83c7-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83c7-240">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="b83c7-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
