---
description: Converte un flusso video tra i formati di colore.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertitore di colori DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484108"
---
# <a name="color-converter-dsp"></a><span data-ttu-id="02791-103">Convertitore di colori DSP</span><span class="sxs-lookup"><span data-stu-id="02791-103">Color Converter DSP</span></span>

<span data-ttu-id="02791-104">Converte un flusso video tra i formati di colore.</span><span class="sxs-lookup"><span data-stu-id="02791-104">Converts a video stream between color formats.</span></span>

## <a name="clsid"></a><span data-ttu-id="02791-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="02791-105">CLSID</span></span>

<span data-ttu-id="02791-106">\_CCOLORCONVERTDMO CLSID</span><span class="sxs-lookup"><span data-stu-id="02791-106">CLSID\_CColorConvertDMO</span></span>

## <a name="interfaces"></a><span data-ttu-id="02791-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="02791-107">Interfaces</span></span>

-   [<span data-ttu-id="02791-108">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="02791-108">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="02791-109">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="02791-109">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="02791-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="02791-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="02791-111">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="02791-111">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [<span data-ttu-id="02791-112">IWMColorConvProps</span><span class="sxs-lookup"><span data-stu-id="02791-112">IWMColorConvProps</span></span>](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a><span data-ttu-id="02791-113">Formati di input</span><span class="sxs-lookup"><span data-stu-id="02791-113">Input Formats</span></span>

-   <span data-ttu-id="02791-114">RGB 24</span><span class="sxs-lookup"><span data-stu-id="02791-114">RGB 24</span></span>
-   <span data-ttu-id="02791-115">RGB 32</span><span class="sxs-lookup"><span data-stu-id="02791-115">RGB 32</span></span>
-   <span data-ttu-id="02791-116">RGB 555</span><span class="sxs-lookup"><span data-stu-id="02791-116">RGB 555</span></span>
-   <span data-ttu-id="02791-117">RGB 565</span><span class="sxs-lookup"><span data-stu-id="02791-117">RGB 565</span></span>
-   <span data-ttu-id="02791-118">RGB 8</span><span class="sxs-lookup"><span data-stu-id="02791-118">RGB 8</span></span>
-   <span data-ttu-id="02791-119">AYUV</span><span class="sxs-lookup"><span data-stu-id="02791-119">AYUV</span></span>
-   <span data-ttu-id="02791-120">I420</span><span class="sxs-lookup"><span data-stu-id="02791-120">I420</span></span>
-   <span data-ttu-id="02791-121">IYUV</span><span class="sxs-lookup"><span data-stu-id="02791-121">IYUV</span></span>
-   <span data-ttu-id="02791-122">NV11</span><span class="sxs-lookup"><span data-stu-id="02791-122">NV11</span></span>
-   <span data-ttu-id="02791-123">NV12</span><span class="sxs-lookup"><span data-stu-id="02791-123">NV12</span></span>
-   <span data-ttu-id="02791-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="02791-124">UYVY</span></span>
-   <span data-ttu-id="02791-125">V216</span><span class="sxs-lookup"><span data-stu-id="02791-125">V216</span></span>
-   <span data-ttu-id="02791-126">V410</span><span class="sxs-lookup"><span data-stu-id="02791-126">V410</span></span>
-   <span data-ttu-id="02791-127">Y41P</span><span class="sxs-lookup"><span data-stu-id="02791-127">Y41P</span></span>
-   <span data-ttu-id="02791-128">Y41T</span><span class="sxs-lookup"><span data-stu-id="02791-128">Y41T</span></span>
-   <span data-ttu-id="02791-129">Y42T</span><span class="sxs-lookup"><span data-stu-id="02791-129">Y42T</span></span>
-   <span data-ttu-id="02791-130">YUY2</span><span class="sxs-lookup"><span data-stu-id="02791-130">YUY2</span></span>
-   <span data-ttu-id="02791-131">YV12</span><span class="sxs-lookup"><span data-stu-id="02791-131">YV12</span></span>
-   <span data-ttu-id="02791-132">YVU9</span><span class="sxs-lookup"><span data-stu-id="02791-132">YVU9</span></span>
-   <span data-ttu-id="02791-133">YVYU</span><span class="sxs-lookup"><span data-stu-id="02791-133">YVYU</span></span>

## <a name="output-formats"></a><span data-ttu-id="02791-134">Formati di output</span><span class="sxs-lookup"><span data-stu-id="02791-134">Output Formats</span></span>

-   <span data-ttu-id="02791-135">RGB 24</span><span class="sxs-lookup"><span data-stu-id="02791-135">RGB 24</span></span>
-   <span data-ttu-id="02791-136">RGB 32</span><span class="sxs-lookup"><span data-stu-id="02791-136">RGB 32</span></span>
-   <span data-ttu-id="02791-137">RGB 555</span><span class="sxs-lookup"><span data-stu-id="02791-137">RGB 555</span></span>
-   <span data-ttu-id="02791-138">RGB 565</span><span class="sxs-lookup"><span data-stu-id="02791-138">RGB 565</span></span>
-   <span data-ttu-id="02791-139">RGB 8</span><span class="sxs-lookup"><span data-stu-id="02791-139">RGB 8</span></span>
-   <span data-ttu-id="02791-140">AYUV</span><span class="sxs-lookup"><span data-stu-id="02791-140">AYUV</span></span>
-   <span data-ttu-id="02791-141">I420</span><span class="sxs-lookup"><span data-stu-id="02791-141">I420</span></span>
-   <span data-ttu-id="02791-142">IYUV</span><span class="sxs-lookup"><span data-stu-id="02791-142">IYUV</span></span>
-   <span data-ttu-id="02791-143">NV11</span><span class="sxs-lookup"><span data-stu-id="02791-143">NV11</span></span>
-   <span data-ttu-id="02791-144">NV12</span><span class="sxs-lookup"><span data-stu-id="02791-144">NV12</span></span>
-   <span data-ttu-id="02791-145">UYVY</span><span class="sxs-lookup"><span data-stu-id="02791-145">UYVY</span></span>
-   <span data-ttu-id="02791-146">V216</span><span class="sxs-lookup"><span data-stu-id="02791-146">V216</span></span>
-   <span data-ttu-id="02791-147">V410</span><span class="sxs-lookup"><span data-stu-id="02791-147">V410</span></span>
-   <span data-ttu-id="02791-148">YUY2</span><span class="sxs-lookup"><span data-stu-id="02791-148">YUY2</span></span>
-   <span data-ttu-id="02791-149">YV12</span><span class="sxs-lookup"><span data-stu-id="02791-149">YV12</span></span>
-   <span data-ttu-id="02791-150">YVYU</span><span class="sxs-lookup"><span data-stu-id="02791-150">YVYU</span></span>

## <a name="properties"></a><span data-ttu-id="02791-151">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02791-151">Properties</span></span>

-   [<span data-ttu-id="02791-152">MFPKEY \_ COLORCONV \_ SRCLEFT</span><span class="sxs-lookup"><span data-stu-id="02791-152">MFPKEY\_COLORCONV\_SRCLEFT</span></span>](mfpkey-colorconv-srcleft.md)
-   [<span data-ttu-id="02791-153">MFPKEY \_ COLORCONV \_ SRCTOP</span><span class="sxs-lookup"><span data-stu-id="02791-153">MFPKEY\_COLORCONV\_SRCTOP</span></span>](mfpkey-colorconv-srctop.md)
-   [<span data-ttu-id="02791-154">MFPKEY \_ COLORCONV \_ DSTLEFT</span><span class="sxs-lookup"><span data-stu-id="02791-154">MFPKEY\_COLORCONV\_DSTLEFT</span></span>](mfpkey-colorconv-dstleft.md)
-   [<span data-ttu-id="02791-155">MFPKEY \_ COLORCONV \_ DSTTOP</span><span class="sxs-lookup"><span data-stu-id="02791-155">MFPKEY\_COLORCONV\_DSTTOP</span></span>](mfpkey-colorconv-dsttop.md)
-   [<span data-ttu-id="02791-156">\_larghezza COLORCONV \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="02791-156">MFPKEY\_COLORCONV\_WIDTH</span></span>](mfpkey-colorconv-width.md)
-   [<span data-ttu-id="02791-157">\_altezza COLORCONV \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="02791-157">MFPKEY\_COLORCONV\_HEIGHT</span></span>](mfpkey-colorconv-height.md)
-   [<span data-ttu-id="02791-158">\_modalità COLORCONV \_ MFPKEY</span><span class="sxs-lookup"><span data-stu-id="02791-158">MFPKEY\_COLORCONV\_MODE</span></span>](mfpkey-colorconv-mode.md)

## <a name="remarks"></a><span data-ttu-id="02791-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="02791-159">Remarks</span></span>

<span data-ttu-id="02791-160">Il convertitore di colori DSP viene implementato come un oggetto COM che può fungere da oggetto DirectXMedia (DMO) o da una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="02791-160">The Color Converter DSP is implemented as a COM object that can act as a DirectXMedia Object (DMO) or a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="02791-161">L'oggetto ha un singolo identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT.</span><span class="sxs-lookup"><span data-stu-id="02791-161">The object has a single class identifier (CLSID) regardless of whether it acts as a DMO or an MFT.</span></span> <span data-ttu-id="02791-162">Per informazioni sul momento in cui un DSP funge da DMO o da un MFT, vedere [processori di segnali digitali](windowsmediadigitalsignalprocessors.md).</span><span class="sxs-lookup"><span data-stu-id="02791-162">For information about when a DSP acts as a DMO or an MFT, see [Digital Signal Processors](windowsmediadigitalsignalprocessors.md).</span></span>

<span data-ttu-id="02791-163">Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un DSP funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="02791-163">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="02791-164">I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un DSP funga da DMO o da un MFT.</span><span class="sxs-lookup"><span data-stu-id="02791-164">The GUIDs for non-RGB media subtypes are the same, regardless of whether a DSP is acting as a DMO or an MFT.</span></span> <span data-ttu-id="02791-165">Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="02791-165">For information about the GUIDs that represent media subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="02791-166">Per impostazione predefinita, questo DSP copia l'intera immagine di origine nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="02791-166">By default, this DSP copies the entire source image to the output buffer.</span></span> <span data-ttu-id="02791-167">Facoltativamente, è possibile specificare i rettangoli di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="02791-167">Optionally, you can specify source and destination rectangles.</span></span> <span data-ttu-id="02791-168">Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e la scrive nel rettangolo di destinazione nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="02791-168">The DSP copies the portion of the source image defined by source rectangle, and writes it into the destination rectangle on the output buffer.</span></span> <span data-ttu-id="02791-169">Il DSP non esegue alcun ridimensionamento. i rettangoli di origine e di destinazione devono avere le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="02791-169">The DSP does not perform any scaling; the source and destination rectangles must be the same size.</span></span> <span data-ttu-id="02791-170">I rettangoli di origine e di destinazione non possono superare i limiti del fotogramma video.</span><span class="sxs-lookup"><span data-stu-id="02791-170">The source and destination rectangles cannot exceed the boundaries of the video frame.</span></span>

<span data-ttu-id="02791-171">Tutte le proprietà, ad eccezione della [**\_ \_ modalità COLORCONV di MFPKEY**](mfpkey-colorconv-mode.md) , devono essere impostate in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="02791-171">All of the properties except [**MFPKEY\_COLORCONV\_MODE**](mfpkey-colorconv-mode.md) must be set in a group.</span></span> <span data-ttu-id="02791-172">Se si imposta una di queste proprietà, è necessario impostare tutte le altre.</span><span class="sxs-lookup"><span data-stu-id="02791-172">If you set any of these properties, you must set all of the others.</span></span> <span data-ttu-id="02791-173">In caso contrario, i rettangoli di origine e di destinazione potrebbero non essere validi, nel qual caso entrambi i metodi [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P Rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) restituiranno **e \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="02791-173">Otherwise, the source and destination rectangles might be invalid, in which case both the [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) and [**IMediaObject::ProcessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) methods will return **E\_INVALIDARG**.</span></span>

<span data-ttu-id="02791-174">Il convertitore di colori non supporta tutte le combinazioni di formato di input e di output.</span><span class="sxs-lookup"><span data-stu-id="02791-174">The color converter does not support every combination of input format and output format.</span></span> <span data-ttu-id="02791-175">In genere, è necessario impostare il formato dei supporti noto, ovvero input o output, ed enumerare i formati disponibili sul flusso opposto.</span><span class="sxs-lookup"><span data-stu-id="02791-175">Usually, you should set the media format that you know, either input or output, and then enumerate the available formats on the opposite stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="02791-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02791-176">Requirements</span></span>



| <span data-ttu-id="02791-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="02791-177">Requirement</span></span> | <span data-ttu-id="02791-178">Valore</span><span class="sxs-lookup"><span data-stu-id="02791-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02791-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02791-179">Minimum supported client</span></span><br/> | <span data-ttu-id="02791-180">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02791-180">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="02791-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02791-181">Minimum supported server</span></span><br/> | <span data-ttu-id="02791-182">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02791-182">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="02791-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02791-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="02791-184"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="02791-184"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="02791-185">DLL</span><span class="sxs-lookup"><span data-stu-id="02791-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02791-186"><dt>Colorcnv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02791-186"><dt>Colorcnv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02791-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02791-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02791-188">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="02791-188">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
