---
description: Il processore video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la conversione dello spazio dei colore, il ridimensionamento video, il deinterlacciamento, la conversione della frequenza dei fotogrammi, la rotazione, il ritaglio, la disimballaggio e il mirroring della visualizzazione a destra e a sinistra.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: Processore video MFT (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332600"
---
# <a name="video-processor-mft"></a><span data-ttu-id="65e9a-103">Processore video MFT</span><span class="sxs-lookup"><span data-stu-id="65e9a-103">Video Processor MFT</span></span>

<span data-ttu-id="65e9a-104">Il processore video MFT è una trasformazione Microsoft Media Foundation (MFT) che esegue la conversione dello spazio dei colore, il ridimensionamento video, il deinterlacciamento, la conversione della frequenza dei fotogrammi, la rotazione, il ritaglio, la disimballaggio e il mirroring della visualizzazione a destra e a sinistra.</span><span class="sxs-lookup"><span data-stu-id="65e9a-104">The video processor MFT is a Microsoft Media Foundation transform (MFT) that performs colorspace conversion, video resizing, deinterlacing, frame rate conversion, rotation, cropping, spatial left and right view unpacking, and mirroring.</span></span>

## <a name="clsid"></a><span data-ttu-id="65e9a-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="65e9a-105">CLSID</span></span>

<span data-ttu-id="65e9a-106">\_VIDEOPROCESSORMFT CLSID</span><span class="sxs-lookup"><span data-stu-id="65e9a-106">CLSID\_VideoProcessorMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="65e9a-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="65e9a-107">Interfaces</span></span>

-   [<span data-ttu-id="65e9a-108">**IMFRealTimeClientEx**</span><span class="sxs-lookup"><span data-stu-id="65e9a-108">**IMFRealTimeClientEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [<span data-ttu-id="65e9a-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="65e9a-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="65e9a-110">**IMFVideoProcessorControl**</span><span class="sxs-lookup"><span data-stu-id="65e9a-110">**IMFVideoProcessorControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a><span data-ttu-id="65e9a-111">Formati di input</span><span class="sxs-lookup"><span data-stu-id="65e9a-111">Input Formats</span></span>

-   <span data-ttu-id="65e9a-112">**\_ARGB32 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-112">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="65e9a-113">**\_AYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-113">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="65e9a-114">**\_I420 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-114">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="65e9a-115">**\_IYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-115">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="65e9a-116">**\_NV11 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-116">**MFVideoFormat\_NV11**</span></span>
-   <span data-ttu-id="65e9a-117">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-117">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="65e9a-118">**\_RGB24 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-118">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="65e9a-119">**\_Rgb32 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-119">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="65e9a-120">**\_RGB555 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-120">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="65e9a-121">**\_RGB565 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-121">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="65e9a-122">**\_RGB8 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-122">**MFVideoFormat\_RGB8**</span></span>
-   <span data-ttu-id="65e9a-123">**\_UYVY MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-123">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="65e9a-124">**\_V410 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-124">**MFVideoFormat\_v410**</span></span>
-   <span data-ttu-id="65e9a-125">**\_Y216 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-125">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="65e9a-126">**\_Y41P MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-126">**MFVideoFormat\_Y41P**</span></span>
-   <span data-ttu-id="65e9a-127">**\_Y41T MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-127">**MFVideoFormat\_Y41T**</span></span>
-   <span data-ttu-id="65e9a-128">**\_Y42T MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-128">**MFVideoFormat\_Y42T**</span></span>
-   <span data-ttu-id="65e9a-129">**\_YUY2 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-129">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="65e9a-130">**\_YV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-130">**MFVideoFormat\_YV12**</span></span>
-   <span data-ttu-id="65e9a-131">**\_YVYU MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-131">**MFVideoFormat\_YVYU**</span></span>

## <a name="output-formats"></a><span data-ttu-id="65e9a-132">Formati di output</span><span class="sxs-lookup"><span data-stu-id="65e9a-132">Output Formats</span></span>

-   <span data-ttu-id="65e9a-133">**\_ARGB32 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-133">**MFVideoFormat\_ARGB32**</span></span>
-   <span data-ttu-id="65e9a-134">**\_AYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-134">**MFVideoFormat\_AYUV**</span></span>
-   <span data-ttu-id="65e9a-135">**\_I420 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-135">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="65e9a-136">**\_IYUV MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-136">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="65e9a-137">**\_NV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-137">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="65e9a-138">**\_RGB24 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-138">**MFVideoFormat\_RGB24**</span></span>
-   <span data-ttu-id="65e9a-139">**\_Rgb32 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-139">**MFVideoFormat\_RGB32**</span></span>
-   <span data-ttu-id="65e9a-140">**\_RGB555 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-140">**MFVideoFormat\_RGB555**</span></span>
-   <span data-ttu-id="65e9a-141">**\_RGB565 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-141">**MFVideoFormat\_RGB565**</span></span>
-   <span data-ttu-id="65e9a-142">**\_UYVY MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-142">**MFVideoFormat\_UYVY**</span></span>
-   <span data-ttu-id="65e9a-143">**\_Y216 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-143">**MFVideoFormat\_Y216**</span></span>
-   <span data-ttu-id="65e9a-144">**\_YUY2 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-144">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="65e9a-145">**\_YV12 MFVideoFormat**</span><span class="sxs-lookup"><span data-stu-id="65e9a-145">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="65e9a-146">Non sono supportate tutte le combinazioni di formati di input e di output.</span><span class="sxs-lookup"><span data-stu-id="65e9a-146">Not every combination of input and output formats is supported.</span></span> <span data-ttu-id="65e9a-147">Per verificare se è supportata una conversione, impostare il tipo di input e quindi chiamare [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="65e9a-147">To test whether a conversion is supported, set the input type and then call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span>

<span data-ttu-id="65e9a-148">Per altre informazioni su questi formati, vedere [GUID del sottotipo video](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="65e9a-148">For more information about these formats, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65e9a-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="65e9a-149">Remarks</span></span>

<span data-ttu-id="65e9a-150">È possibile creare un'istanza del processore video in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="65e9a-150">An instance of the video processor can be created in one of the following ways:</span></span>

-   <span data-ttu-id="65e9a-151">Chiamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="65e9a-151">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="65e9a-152">Il processore video è registrato nella categoria **MFT \_ categoria \_ \_ processore video** .</span><span class="sxs-lookup"><span data-stu-id="65e9a-152">The video processor is registered under the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category.</span></span>
-   <span data-ttu-id="65e9a-153">Chiamando la funzione COM **CoCreateInstance** passando il CLSID CLSID **\_ VideoProcessorMFT**.</span><span class="sxs-lookup"><span data-stu-id="65e9a-153">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_VideoProcessorMFT**.</span></span>

<span data-ttu-id="65e9a-154">Le osservazioni seguenti riguardano l'utilizzo di rettangoli di origine e rettangoli di destinazione nel **processore video MFT**.</span><span class="sxs-lookup"><span data-stu-id="65e9a-154">The following remarks pertain to working with source rectangles and destination rectangles in the **Video Processor MFT**.</span></span> <span data-ttu-id="65e9a-155">I rettangoli di origine e di destinazione vengono impostati con [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) e [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) e alcune volte con [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span><span class="sxs-lookup"><span data-stu-id="65e9a-155">Source and destination rectangles are set with [**IMFVideoProcessorControl::SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) and [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) and some times with [**IMFMediaEngineEx::UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).</span></span>

-   <span data-ttu-id="65e9a-156">Il rettangolo di origine deve essere allineato e arrotondato in modo da corrispondere ai requisiti del formato di colore del frame inserito nel processore video.</span><span class="sxs-lookup"><span data-stu-id="65e9a-156">The source rectangle should be aligned and rounded to match the requirements of the color format of the frame inputted to the video processor.</span></span> <span data-ttu-id="65e9a-157">Questo è importante perché i formati come 420 e 422 presentano requisiti relativi alle dimensioni e agli offset che è possibile creare e a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="65e9a-157">This is important because formats like 420 and 422 have requirements about the dimensions and offsets that can be created and accessed.</span></span> <span data-ttu-id="65e9a-158">Ad esempio, un rettangolo di origine di {1, 0, 319, 240} (a sinistra, in alto, a destra, in basso) verrà arrotondato a {2, 0, 320, 240} quando il formato di input è 420.</span><span class="sxs-lookup"><span data-stu-id="65e9a-158">For example, a source rectangle of {1, 0, 319, 240} (left, top, right, bottom) will be rounded to {2, 0, 320, 240} when the input format is 420.</span></span>
-   <span data-ttu-id="65e9a-159">Sia il rettangolo di destinazione che quello di origine verranno sempre bloccati per adattarsi ai rispettivi frame, ovvero il rettangolo di origine al frame di origine e il rettangolo di destinazione al frame di destinazione.</span><span class="sxs-lookup"><span data-stu-id="65e9a-159">Both the destination and source rectangle will always be clamped to fit inside their respective frames—the source rectangle to the source frame and the destination rectangle to the destination frame.</span></span> <span data-ttu-id="65e9a-160">Ciò significa che i valori negativi non sono significativi, ma verranno sempre bloccati a 0.</span><span class="sxs-lookup"><span data-stu-id="65e9a-160">This means that negative values are not meaningful—they will be always clamped to 0.</span></span>
-   <span data-ttu-id="65e9a-161">Il rettangolo di origine si trova nel sistema di coordinate del frame di destinazione, meno qualsiasi rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="65e9a-161">The source rectangle is in the destination frame's coordinate system, minus any destination rectangle.</span></span> <span data-ttu-id="65e9a-162">Ciò significa che le trasformazioni come la rotazione vengono annullate nel rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="65e9a-162">This means that transformations like rotation are "undone" on the source rectangle.</span></span> <span data-ttu-id="65e9a-163">Pertanto, non è necessario stabilire se il video è stato ruotato o 3D decompresso.</span><span class="sxs-lookup"><span data-stu-id="65e9a-163">Therefore, you do not need to know if the video was rotated or 3D unpacked.</span></span> <span data-ttu-id="65e9a-164">Ad esempio, è possibile tracciare un rettangolo sopra il tag video, prendere le coordinate relative (rispetto al tag video), normalizzarle (intervallo compreso tra 0 e 1) e passarle come rettangolo di origine e dovrebbero funzionare come previsto, anche se è in corso la rotazione del video.</span><span class="sxs-lookup"><span data-stu-id="65e9a-164">For example, you could draw a rectangle on top of the video tag, take the relative coordinates (relative to the video tag), normalize them (range 0 to 1) and pass them down as the source rectangle and they should work as expected, even if the video is being rotated.</span></span>

<span data-ttu-id="65e9a-165">Il processore video supporta l'elaborazione video con accelerazione GPU, con Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="65e9a-165">The video processor supports GPU-accelerated video processing, using Microsoft Direct3D 11.</span></span> <span data-ttu-id="65e9a-166">Per ulteriori informazioni, vedere [MF \_ sa \_ d3d11 \_ Aware](mf-sa-d3d11-aware.md).</span><span class="sxs-lookup"><span data-stu-id="65e9a-166">For more information, see [MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md).</span></span>

### <a name="stereoscopic-video"></a><span data-ttu-id="65e9a-167">Video stereoscopico</span><span class="sxs-lookup"><span data-stu-id="65e9a-167">Stereoscopic Video</span></span>

<span data-ttu-id="65e9a-168">Il processore video supporta la visualizzazione dell'operazione di decompressione nei fotogrammi video 3D:</span><span class="sxs-lookup"><span data-stu-id="65e9a-168">The video processor supports the view unpacking operation on 3D video frames:</span></span>

<span data-ttu-id="65e9a-169">Se il frame di input contiene due visualizzazioni compresse nello stesso frame, il processore video può suddividere le visualizzazioni in buffer distinti oppure estrarre la visualizzazione di base ed eliminare la seconda visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="65e9a-169">If the input frame contains two views packed in the same frame, the video processor can split the views into separate buffers, or extract the base view and discard the second view.</span></span> <span data-ttu-id="65e9a-170">Per abilitare la decompressione della visualizzazione, impostare l'attributo di [ \_ \_ \_ output MF Enable 3DVIDEO](mf-enable-3dvideo-output.md) su **MF3DVideoOutputType \_ stereo** o **MF3DVideoOutputType \_ BaseView**.</span><span class="sxs-lookup"><span data-stu-id="65e9a-170">To enable view unpacking, set the [MF\_ENABLE\_3DVIDEO\_OUTPUT](mf-enable-3dvideo-output.md) attribute to **MF3DVideoOutputType\_Stereo** or **MF3DVideoOutputType\_BaseView**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65e9a-171">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65e9a-171">Requirements</span></span>



| <span data-ttu-id="65e9a-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e9a-172">Requirement</span></span> | <span data-ttu-id="65e9a-173">Valore</span><span class="sxs-lookup"><span data-stu-id="65e9a-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e9a-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65e9a-174">Header</span></span><br/> | <dl> <span data-ttu-id="65e9a-175"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="65e9a-175"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e9a-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65e9a-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e9a-177">Processori di segnale digitale</span><span class="sxs-lookup"><span data-stu-id="65e9a-177">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




