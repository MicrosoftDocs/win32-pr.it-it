---
description: Ridimensiona un flusso video.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: Video Resizer DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7826f21cadc6d30bc2b8b04bbcc741c2bf31bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308967"
---
# <a name="video-resizer-dsp"></a><span data-ttu-id="28c5c-103">Ridimensionamento video DSP</span><span class="sxs-lookup"><span data-stu-id="28c5c-103">Video Resizer DSP</span></span>

<span data-ttu-id="28c5c-104">Ridimensiona un flusso video.</span><span class="sxs-lookup"><span data-stu-id="28c5c-104">Resizes a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="28c5c-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="28c5c-105">CLSID</span></span>

<span data-ttu-id="28c5c-106">\_CRESIZERDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="28c5c-106">CLSID\_CResizerDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="28c5c-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="28c5c-107">Interfaces</span></span>

-   [<span data-ttu-id="28c5c-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="28c5c-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="28c5c-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="28c5c-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="28c5c-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="28c5c-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="28c5c-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="28c5c-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="28c5c-112">**IWMResizerProps**</span><span class="sxs-lookup"><span data-stu-id="28c5c-112">**IWMResizerProps**</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a><span data-ttu-id="28c5c-113">Formati</span><span class="sxs-lookup"><span data-stu-id="28c5c-113">Formats</span></span>

<span data-ttu-id="28c5c-114">Il video Resizer di ridimensionamento video supporta i sottotipi di supporti di input/output seguenti quando funge da oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="28c5c-114">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="28c5c-115">\_IYUV MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-115">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="28c5c-116">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-116">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="28c5c-117">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-117">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="28c5c-118">\_I420 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-118">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="28c5c-119">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-119">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="28c5c-120">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-120">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="28c5c-121">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-121">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="28c5c-122">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-122">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="28c5c-123">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-123">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="28c5c-124">\_AYUV MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-124">MEDIASUBTYPE\_AYUV</span></span>
-   <span data-ttu-id="28c5c-125">\_V216 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-125">MEDIASUBTYPE\_V216</span></span>
-   <span data-ttu-id="28c5c-126">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="28c5c-126">MEDIASUBTYPE\_YV12</span></span>

<span data-ttu-id="28c5c-127">Il video Resizer di ridimensionamento video supporta i sottotipi di supporti di input/output seguenti quando funge da trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="28c5c-127">The Video Resizer DSP supports the following input/output media subtypes when it is acting as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="28c5c-128">\_IYUV MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-128">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="28c5c-129">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-129">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="28c5c-130">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-130">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="28c5c-131">\_I420 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-131">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="28c5c-132">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-132">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="28c5c-133">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-133">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="28c5c-134">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-134">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="28c5c-135">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-135">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="28c5c-136">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-136">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="28c5c-137">\_AYUV MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-137">MFVideoFormat\_AYUV</span></span>
-   <span data-ttu-id="28c5c-138">\_V216 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-138">MFVideoFormat\_V216</span></span>
-   <span data-ttu-id="28c5c-139">\_YV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="28c5c-139">MFVideoFormat\_YV12</span></span>

## <a name="properties"></a><span data-ttu-id="28c5c-140">Proprietà</span><span class="sxs-lookup"><span data-stu-id="28c5c-140">Properties</span></span>

-   [<span data-ttu-id="28c5c-141">MFPKEY \_ ridimensionare \_ src a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="28c5c-141">MFPKEY\_RESIZE\_SRC\_LEFT</span></span>](mfpkey-resize-src-left.md)
-   [<span data-ttu-id="28c5c-142">MFPKEY \_ ridimensionare \_ src in \_ alto</span><span class="sxs-lookup"><span data-stu-id="28c5c-142">MFPKEY\_RESIZE\_SRC\_TOP</span></span>](mfpkey-resize-src-top.md)
-   [<span data-ttu-id="28c5c-143">MFPKEY \_ ridimensionare la \_ \_ larghezza src</span><span class="sxs-lookup"><span data-stu-id="28c5c-143">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span>](mfpkey-resize-src-width.md)
-   [<span data-ttu-id="28c5c-144">\_altezza src di ridimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-144">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span>](mfpkey-resize-src-height.md)
-   [<span data-ttu-id="28c5c-145">\_ridimensionamento MFPKEY \_ DST a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="28c5c-145">MFPKEY\_RESIZE\_DST\_LEFT</span></span>](mfpkey-resize-dst-left.md)
-   [<span data-ttu-id="28c5c-146">MFPKEY \_ ridimensionare l' \_ inizio dell'ora legale \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-146">MFPKEY\_RESIZE\_DST\_TOP</span></span>](mfpkey-resize-dst-top.md)
-   [<span data-ttu-id="28c5c-147">\_larghezza DST MFPKEY ridimensionamento \_ \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-147">MFPKEY\_RESIZE\_DST\_WIDTH</span></span>](mfpkey-resize-dst-width.md)
-   [<span data-ttu-id="28c5c-148">MFPKEY \_ ridimensionare l' \_ \_ altezza DST</span><span class="sxs-lookup"><span data-stu-id="28c5c-148">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span>](mfpkey-resize-dst-height.md)
-   [<span data-ttu-id="28c5c-149">MFPKEY \_ ridimensionare la \_ qualità</span><span class="sxs-lookup"><span data-stu-id="28c5c-149">MFPKEY\_RESIZE\_QUALITY</span></span>](mfpkey-resize-quality.md)
-   [<span data-ttu-id="28c5c-150">MFPKEY \_ ridimensionamento \_ interlacciato</span><span class="sxs-lookup"><span data-stu-id="28c5c-150">MFPKEY\_RESIZE\_INTERLACE</span></span>](mfpkey-resize-interlace.md)
-   [<span data-ttu-id="28c5c-151">\_ridimensionamento MFPKEY \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-151">MFPKEY\_RESIZE\_GEOMAPX</span></span>](mfpkey-resize-geomapx.md)
-   [<span data-ttu-id="28c5c-152">\_ridimensionamento MFPKEY \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-152">MFPKEY\_RESIZE\_GEOMAPY</span></span>](mfpkey-resize-geomapy.md)
-   [<span data-ttu-id="28c5c-153">\_ridimensionamento MFPKEY \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-153">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span>](mfpkey-resize-geomapwidth.md)
-   [<span data-ttu-id="28c5c-154">\_ridimensionamento MFPKEY \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-154">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span>](mfpkey-resize-geomapheight.md)
-   [<span data-ttu-id="28c5c-155">\_ridimensionamento MFPKEY \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-155">MFPKEY\_RESIZE\_MINAPX</span></span>](mfpkey-resize-minapx.md)
-   [<span data-ttu-id="28c5c-156">\_ridimensionamento MFPKEY \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-156">MFPKEY\_RESIZE\_MINAPY</span></span>](mfpkey-resize-minapy.md)
-   [<span data-ttu-id="28c5c-157">\_ridimensionamento MFPKEY \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-157">MFPKEY\_RESIZE\_MINAPWIDTH</span></span>](mfpkey-resize-minapwidth.md)
-   [<span data-ttu-id="28c5c-158">\_ridimensionamento MFPKEY \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-158">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span>](mfpkey-resize-minapheight.md)
-   [<span data-ttu-id="28c5c-159">\_ridimensionamento MFPKEY \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-159">MFPKEY\_RESIZE\_PANSCANAPX</span></span>](mfpkey-resize-panscanapx.md)
-   [<span data-ttu-id="28c5c-160">\_ridimensionamento MFPKEY \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-160">MFPKEY\_RESIZE\_PANSCANAPY</span></span>](mfpkey-resize-panscanapy.md)
-   [<span data-ttu-id="28c5c-161">\_ridimensionamento MFPKEY \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-161">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span>](mfpkey-resize-panscanapwidth.md)
-   [<span data-ttu-id="28c5c-162">\_ridimensionamento MFPKEY \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-162">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span>](mfpkey-resize-panscanapheight.md)
-   [<span data-ttu-id="28c5c-163">\_PIXELASPECTRATIO MFPKEY</span><span class="sxs-lookup"><span data-stu-id="28c5c-163">MFPKEY\_PIXELASPECTRATIO</span></span>](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a><span data-ttu-id="28c5c-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="28c5c-164">Remarks</span></span>

<span data-ttu-id="28c5c-165">Il video Resizer viene implementato come un oggetto COM che può fungere da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="28c5c-165">The Video Resizer DSP is implemented as a COM object that can act as a DMO or an MFT.</span></span> <span data-ttu-id="28c5c-166">L'oggetto ha un singolo identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.</span><span class="sxs-lookup"><span data-stu-id="28c5c-166">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="28c5c-167">Per informazioni sul momento in cui un DSP funge da DMO o da un MFT, vedere [processori di segnali digitali](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="28c5c-167">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="28c5c-168">Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un DSP funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="28c5c-168">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="28c5c-169">I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un DSP funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="28c5c-169">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="28c5c-170">Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="28c5c-170">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="28c5c-171">Questo DSP può eseguire sia il ritaglio che la scalabilità nell'immagine video.</span><span class="sxs-lookup"><span data-stu-id="28c5c-171">This DSP can perform both cropping and scaling on the video image.</span></span> <span data-ttu-id="28c5c-172">Il formato del tipo di output deve corrispondere al formato del tipo di input.</span><span class="sxs-lookup"><span data-stu-id="28c5c-172">The format of the output type must match the format of the input type.</span></span> <span data-ttu-id="28c5c-173">Il DSP non esegue le conversioni dello spazio dei colori.</span><span class="sxs-lookup"><span data-stu-id="28c5c-173">The DSP does not perform color-space conversions.</span></span>

<span data-ttu-id="28c5c-174">Prima di impostare il tipo di output, è possibile definire una delle aree seguenti utilizzando le proprietà elencate in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="28c5c-174">Before setting the output type, you can define any of the following regions by using the properties listed in this table.</span></span>



| <span data-ttu-id="28c5c-175">Region</span><span class="sxs-lookup"><span data-stu-id="28c5c-175">Region</span></span>                   | <span data-ttu-id="28c5c-176">Proprietà</span><span class="sxs-lookup"><span data-stu-id="28c5c-176">Properties</span></span>                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c5c-177">Rettangolo di origine</span><span class="sxs-lookup"><span data-stu-id="28c5c-177">Source rectangle</span></span>         | <span data-ttu-id="28c5c-178">MFPKEY \_ ridimensionare \_ src a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="28c5c-178">MFPKEY\_RESIZE\_SRC\_LEFT</span></span><br/> <span data-ttu-id="28c5c-179">MFPKEY \_ ridimensionare \_ src in \_ alto</span><span class="sxs-lookup"><span data-stu-id="28c5c-179">MFPKEY\_RESIZE\_SRC\_TOP</span></span><br/> <span data-ttu-id="28c5c-180">MFPKEY \_ ridimensionare la \_ \_ larghezza src</span><span class="sxs-lookup"><span data-stu-id="28c5c-180">MFPKEY\_RESIZE\_SRC\_WIDTH</span></span><br/> <span data-ttu-id="28c5c-181">\_altezza src di ridimensionamento MFPKEY \_ \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-181">MFPKEY\_RESIZE\_SRC\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="28c5c-182">Rettangolo di destinazione</span><span class="sxs-lookup"><span data-stu-id="28c5c-182">Destination rectangle</span></span>    | <span data-ttu-id="28c5c-183">\_ridimensionamento MFPKEY \_ DST a \_ sinistra</span><span class="sxs-lookup"><span data-stu-id="28c5c-183">MFPKEY\_RESIZE\_DST\_LEFT</span></span><br/> <span data-ttu-id="28c5c-184">MFPKEY \_ ridimensionare l' \_ inizio dell'ora legale \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-184">MFPKEY\_RESIZE\_DST\_TOP</span></span><br/> <span data-ttu-id="28c5c-185">\_larghezza DST MFPKEY ridimensionamento \_ \_</span><span class="sxs-lookup"><span data-stu-id="28c5c-185">MFPKEY\_RESIZE\_DST\_WIDTH</span></span><br/> <span data-ttu-id="28c5c-186">MFPKEY \_ ridimensionare l' \_ \_ altezza DST</span><span class="sxs-lookup"><span data-stu-id="28c5c-186">MFPKEY\_RESIZE\_DST\_HEIGHT</span></span><br/>            |
| <span data-ttu-id="28c5c-187">Apertura geometrica</span><span class="sxs-lookup"><span data-stu-id="28c5c-187">Geometric aperture</span></span>       | <span data-ttu-id="28c5c-188">\_ridimensionamento MFPKEY \_ GEOMAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-188">MFPKEY\_RESIZE\_GEOMAPX</span></span><br/> <span data-ttu-id="28c5c-189">\_ridimensionamento MFPKEY \_ GEOMAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-189">MFPKEY\_RESIZE\_GEOMAPY</span></span><br/> <span data-ttu-id="28c5c-190">\_ridimensionamento MFPKEY \_ GEOMAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-190">MFPKEY\_RESIZE\_GEOMAPWIDTH</span></span><br/> <span data-ttu-id="28c5c-191">\_ridimensionamento MFPKEY \_ GEOMAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-191">MFPKEY\_RESIZE\_GEOMAPHEIGHT</span></span><br/>             |
| <span data-ttu-id="28c5c-192">Apertura minima visualizzazione</span><span class="sxs-lookup"><span data-stu-id="28c5c-192">Minimum display aperture</span></span> | <span data-ttu-id="28c5c-193">\_ridimensionamento MFPKEY \_ MINAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-193">MFPKEY\_RESIZE\_MINAPX</span></span><br/> <span data-ttu-id="28c5c-194">\_ridimensionamento MFPKEY \_ MINAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-194">MFPKEY\_RESIZE\_MINAPY</span></span><br/> <span data-ttu-id="28c5c-195">\_ridimensionamento MFPKEY \_ MINAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-195">MFPKEY\_RESIZE\_MINAPWIDTH</span></span><br/> <span data-ttu-id="28c5c-196">\_ridimensionamento MFPKEY \_ MINAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-196">MFPKEY\_RESIZE\_MINAPHEIGHT</span></span><br/>                 |
| <span data-ttu-id="28c5c-197">Area Pan/Scan</span><span class="sxs-lookup"><span data-stu-id="28c5c-197">Pan/scan region</span></span>          | <span data-ttu-id="28c5c-198">\_ridimensionamento MFPKEY \_ PANSCANAPX</span><span class="sxs-lookup"><span data-stu-id="28c5c-198">MFPKEY\_RESIZE\_PANSCANAPX</span></span><br/> <span data-ttu-id="28c5c-199">\_ridimensionamento MFPKEY \_ PANSCANAPY</span><span class="sxs-lookup"><span data-stu-id="28c5c-199">MFPKEY\_RESIZE\_PANSCANAPY</span></span><br/> <span data-ttu-id="28c5c-200">\_ridimensionamento MFPKEY \_ PANSCANAPWIDTH</span><span class="sxs-lookup"><span data-stu-id="28c5c-200">MFPKEY\_RESIZE\_PANSCANAPWIDTH</span></span><br/> <span data-ttu-id="28c5c-201">\_ridimensionamento MFPKEY \_ PANSCANAPHEIGHT</span><span class="sxs-lookup"><span data-stu-id="28c5c-201">MFPKEY\_RESIZE\_PANSCANAPHEIGHT</span></span><br/> |



 

<span data-ttu-id="28c5c-202">In ogni caso, è necessario impostare tutte le proprietà associate affinché l'impostazione abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="28c5c-202">In each case, you must set all of the associated properties for the setting to take effect.</span></span>

<span data-ttu-id="28c5c-203">Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e lo estende o comprime nel rettangolo di destinazione nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="28c5c-203">The DSP copies the portion of the source image defined by source rectangle, and stretches or compresses it onto the destination rectangle on the output buffer.</span></span> <span data-ttu-id="28c5c-204">I rettangoli di origine e di destinazione non devono necessariamente avere le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="28c5c-204">The source and destination rectangles do not need to be the same size.</span></span> <span data-ttu-id="28c5c-205">La dimensione del fotogramma nel tipo di supporto di output deve essere sufficientemente grande da contenere il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="28c5c-205">The frame size in the output media type must be large enough to hold the destination rectangle.</span></span>

<span data-ttu-id="28c5c-206">L'apertura geometrica, l'apertura minima dello schermo e l'area di Pan/Scan non influiscono sul modo in cui il DSP ridimensiona il video.</span><span class="sxs-lookup"><span data-stu-id="28c5c-206">The geometric aperture, minimum display aperture, and pan/scan region do not affect how the DSP resizes the video.</span></span> <span data-ttu-id="28c5c-207">Tuttavia, potrebbero influire sul modo in cui il componente downstream interpreta il frame del video.</span><span class="sxs-lookup"><span data-stu-id="28c5c-207">However, they might affect how the downstream component interprets the video frame.</span></span> <span data-ttu-id="28c5c-208">In particolare, il renderer video avanzato (EVR) usa questi valori quando calcola le proporzioni dell'immagine e l'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="28c5c-208">In particular, the enhanced video renderer (EVR) uses these values when it calculates the picture aspect ratio and the display area.</span></span>

<span data-ttu-id="28c5c-209">Se si usano Media Foundation tipi di supporto, è possibile impostare l'apertura geometrica, l'apertura minima dello schermo e le aree di Pan/Scan direttamente nel tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="28c5c-209">If you are using Media Foundation media types, you can set the geometric aperture, minimum display aperture, and pan/scan regions directly in the output media type.</span></span> <span data-ttu-id="28c5c-210">In caso contrario, se si usano i tipi di supporto DMO, impostarli usando le proprietà.</span><span class="sxs-lookup"><span data-stu-id="28c5c-210">Otherwise, if you are using DMO media types, set them using the properties.</span></span>

<span data-ttu-id="28c5c-211">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="28c5c-211">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="28c5c-212">**\_ \_ apertura geometrica MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="28c5c-212">**MF\_MT\_GEOMETRIC\_APERTURE**</span></span>](mf-mt-geometric-aperture-attribute.md)
-   [<span data-ttu-id="28c5c-213">**\_ \_ \_ apertura minima schermo \_ MF mt**</span><span class="sxs-lookup"><span data-stu-id="28c5c-213">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="28c5c-214">**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**</span><span class="sxs-lookup"><span data-stu-id="28c5c-214">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a><span data-ttu-id="28c5c-215">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28c5c-215">Requirements</span></span>



| <span data-ttu-id="28c5c-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c5c-216">Requirement</span></span> | <span data-ttu-id="28c5c-217">Valore</span><span class="sxs-lookup"><span data-stu-id="28c5c-217">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28c5c-218">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28c5c-218">Minimum supported client</span></span><br/> | <span data-ttu-id="28c5c-219">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28c5c-219">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="28c5c-220">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28c5c-220">Minimum supported server</span></span><br/> | <span data-ttu-id="28c5c-221">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28c5c-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28c5c-222">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28c5c-222">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c5c-223"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="28c5c-223"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="28c5c-224">DLL</span><span class="sxs-lookup"><span data-stu-id="28c5c-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c5c-225"><dt>Vidreszr.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28c5c-225"><dt>Vidreszr.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28c5c-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28c5c-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c5c-227">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="28c5c-227">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
