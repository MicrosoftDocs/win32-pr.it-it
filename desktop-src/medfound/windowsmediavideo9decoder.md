---
description: Il decodificatore Windows Media Video 9 decodifica i flussi video codificati dal codificatore Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Decodificatore Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329985"
---
# <a name="windows-media-video-9-decoder"></a><span data-ttu-id="2cd79-103">Decodificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-103">Windows Media Video 9 Decoder</span></span>

<span data-ttu-id="2cd79-104">Il decodificatore Windows Media Video 9 decodifica i flussi video codificati dal [**codificatore Windows Media video**](windowsmediavideo9encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2cd79-104">The Windows Media Video 9 decoder decodes video streams that were encoded by the [**Windows Media Video Encoder**](windowsmediavideo9encoder.md).</span></span> <span data-ttu-id="2cd79-105">Il codificatore e il decodificatore supportano le quattro categorie di video codificate seguenti.</span><span class="sxs-lookup"><span data-stu-id="2cd79-105">The encoder and decoder support the following four categories of encoded video.</span></span>

-   <span data-ttu-id="2cd79-106">Profilo semplice Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="2cd79-107">Profilo principale Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="2cd79-108">Profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="2cd79-109">Immagine di Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="2cd79-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="2cd79-110">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="2cd79-110">Class Identifier</span></span>

<span data-ttu-id="2cd79-111">L'identificatore di classe (CLSID) per il decodificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMVDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="2cd79-111">The class identifier (CLSID) for the Windows Media Video decoder is represented by the constant **CLSID\_CWMVDecMediaObject**.</span></span> <span data-ttu-id="2cd79-112">È possibile creare un'istanza del decodificatore video chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="2cd79-112">You can create an instance of the video decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="2cd79-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="2cd79-113">Interfaces</span></span>

<span data-ttu-id="2cd79-114">Un oggetto decodificatore video espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="2cd79-114">A video decoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="2cd79-115">Un decodificatore video si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2cd79-115">A video decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="2cd79-116">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore video si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="2cd79-116">The following table shows the conditions under which a video decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="2cd79-117">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2cd79-117">Operating system</span></span>            | <span data-ttu-id="2cd79-118">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="2cd79-118">Decoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd79-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2cd79-119">Windows XP</span></span>                  | <span data-ttu-id="2cd79-120">Un decodificatore Windows Media video si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="2cd79-120">A Windows Media video decoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="2cd79-121">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cd79-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="2cd79-122">Per impostazione predefinita, un decodificatore Windows Media video si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="2cd79-122">By default, a Windows Media video decoder behaves as a DMO.</span></span> <span data-ttu-id="2cd79-123">Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un decodificatore video, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="2cd79-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video decoder, it behaves as an MFT.</span></span> |



 

<span data-ttu-id="2cd79-124">A partire da Windows 7, il decodificatore Windows Media Video implementa l'interfaccia [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .</span><span class="sxs-lookup"><span data-stu-id="2cd79-124">Beginning with Windows 7, the Windows Media Video decoder implements the [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) interface.</span></span>

## <a name="input-formats"></a><span data-ttu-id="2cd79-125">Formati di input</span><span class="sxs-lookup"><span data-stu-id="2cd79-125">Input Formats</span></span>

<span data-ttu-id="2cd79-126">La tabella seguente illustra i codici a quattro caratteri (fourcc) che corrispondono alle categorie di input codificati supportati dal decodificatore Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="2cd79-126">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded input that are supported by the Windows Media Video decoder.</span></span>



| <span data-ttu-id="2cd79-127">Category</span><span class="sxs-lookup"><span data-stu-id="2cd79-127">Category</span></span>                               | <span data-ttu-id="2cd79-128">FOURCC</span><span class="sxs-lookup"><span data-stu-id="2cd79-128">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="2cd79-129">Profilo semplice Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-129">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="2cd79-130">WMV3</span><span class="sxs-lookup"><span data-stu-id="2cd79-130">"WMV3"</span></span>                                   |
| <span data-ttu-id="2cd79-131">Profilo principale Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-131">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="2cd79-132">WMV3</span><span class="sxs-lookup"><span data-stu-id="2cd79-132">"WMV3"</span></span>                                   |
| <span data-ttu-id="2cd79-133">Profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="2cd79-133">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="2cd79-134">WVC1</span><span class="sxs-lookup"><span data-stu-id="2cd79-134">"WVC1"</span></span>                                   |
| <span data-ttu-id="2cd79-135">Immagine di Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="2cd79-135">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="2cd79-136">"WMVP" per 9,1, "WVP2" per 9,1 versione 2</span><span class="sxs-lookup"><span data-stu-id="2cd79-136">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="2cd79-137">Formati di output</span><span class="sxs-lookup"><span data-stu-id="2cd79-137">Output Formats</span></span>

<span data-ttu-id="2cd79-138">Il decodificatore Windows Media Video supporta i sottotipi di supporti di output seguenti quando funge da DMO.</span><span class="sxs-lookup"><span data-stu-id="2cd79-138">The Windows Media Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="2cd79-139">\_NV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-139">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="2cd79-140">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-140">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="2cd79-141">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-141">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="2cd79-142">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-142">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="2cd79-143">\_YVYU MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-143">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="2cd79-144">\_NV11 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-144">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="2cd79-145">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-145">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="2cd79-146">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-146">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="2cd79-147">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-147">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="2cd79-148">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-148">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="2cd79-149">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="2cd79-149">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="2cd79-150">Il decodificatore Windows Media Video supporta i sottotipi di supporti di output seguenti quando funge da MFT.</span><span class="sxs-lookup"><span data-stu-id="2cd79-150">The Windows Media Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="2cd79-151">\_NV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-151">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="2cd79-152">\_YV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-152">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="2cd79-153">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-153">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="2cd79-154">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-154">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="2cd79-155">\_YVYU MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-155">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="2cd79-156">\_NV11 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-156">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="2cd79-157">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-157">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="2cd79-158">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-158">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="2cd79-159">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-159">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="2cd79-160">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-160">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="2cd79-161">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="2cd79-161">MFVideoFormat\_RGB8</span></span>

## <a name="properties"></a><span data-ttu-id="2cd79-162">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cd79-162">Properties</span></span>

<span data-ttu-id="2cd79-163">Il decodificatore Windows Media Video supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="2cd79-163">The Windows Media Video decoder supports the following properties.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2cd79-164">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2cd79-164">Property</span></span></th>
<th><span data-ttu-id="2cd79-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cd79-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2cd79-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-166"><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></span></span></td>
<td><span data-ttu-id="2cd79-167">Specifica se il codec decodifica i fotogrammi video interlacciati dal flusso compresso come frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="2cd79-167">Specifies whether the codec decodes interlaced video frames from the compressed stream as progressive frames.</span></span><br/> <dl> <span data-ttu-id="2cd79-168">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-168">Windows XP and later.</span></span><br />
<span data-ttu-id="2cd79-169">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="2cd79-169">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="2cd79-170">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-170">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cd79-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-171"><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></span></span></td>
<td><span data-ttu-id="2cd79-172">Specifica se il decodificatore userà l'hardware di accelerazione video DirectX, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="2cd79-172">Specifies whether the decoder will use DirectX video acceleration hardware, if available.</span></span><br/> <dl> <span data-ttu-id="2cd79-173">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-173">Windows XP and later.</span></span><br />
<span data-ttu-id="2cd79-174">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="2cd79-174">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="2cd79-175">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-175">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cd79-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-176"><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></span></span></td>
<td><span data-ttu-id="2cd79-177">Specifica il livello di alimentazione per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2cd79-177">Specifies the power level for the decoder.</span></span><br/> <dl> <span data-ttu-id="2cd79-178">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2cd79-178">Windows 7.</span></span><br />
<span data-ttu-id="2cd79-179">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="2cd79-179">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="2cd79-180">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-180">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cd79-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-181"><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></span></span></td>
<td><span data-ttu-id="2cd79-182">Specifica se il decodificatore deve usare l'interpolazione dei frame.</span><span class="sxs-lookup"><span data-stu-id="2cd79-182">Specifies whether the decoder should use frame interpolation.</span></span><br/> <dl> <span data-ttu-id="2cd79-183">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-183">Windows XP and later.</span></span><br />
<span data-ttu-id="2cd79-184">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="2cd79-184">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="2cd79-185">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-185">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cd79-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-186"><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></span></span></td>
<td><span data-ttu-id="2cd79-187">Specifica se il decodificatore supporta l'interpolazione dei frame.</span><span class="sxs-lookup"><span data-stu-id="2cd79-187">Specifies whether the decoder supports frame interpolation.</span></span><br/> <dl> <span data-ttu-id="2cd79-188">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-188">Windows XP and later.</span></span><br />
<span data-ttu-id="2cd79-189">Profilo semplice, profilo principale, profilo avanzato, immagine</span><span class="sxs-lookup"><span data-stu-id="2cd79-189">Simple Profile, Main Profile, Advanced Profile, Image</span></span><br />
<span data-ttu-id="2cd79-190">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-190">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cd79-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-191"><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></span></span></td>
<td><span data-ttu-id="2cd79-192">Specifica il numero di thread che saranno utilizzati dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2cd79-192">Specifies the number of threads that the decoder will use.</span></span><br/> <dl> <span data-ttu-id="2cd79-193">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-193">Windows Vista and later.</span></span><br />
<span data-ttu-id="2cd79-194">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="2cd79-194">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="2cd79-195">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-195">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2cd79-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span><span class="sxs-lookup"><span data-stu-id="2cd79-196"><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></span></span></td>
<td><span data-ttu-id="2cd79-197">Specifica la modalità di post-elaborazione per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2cd79-197">Specifies the post processing mode for the decoder.</span></span><br/> <dl> <span data-ttu-id="2cd79-198">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cd79-198">Windows Vista and later.</span></span><br />
<span data-ttu-id="2cd79-199">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="2cd79-199">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="2cd79-200">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-200">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2cd79-201"><strong>g_wszWMVCNeedsDrain</strong></span><span class="sxs-lookup"><span data-stu-id="2cd79-201"><strong>g_wszWMVCNeedsDrain</strong></span></span></td>
<td><span data-ttu-id="2cd79-202">Specifica se il decodificatore deve essere svuotato.</span><span class="sxs-lookup"><span data-stu-id="2cd79-202">Specifies whether the decoder should be drained.</span></span><br/> <dl> <span data-ttu-id="2cd79-203">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2cd79-203">Windows 8</span></span><br />
<span data-ttu-id="2cd79-204">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2cd79-204">Read-only.</span></span><br />
</dl> <span data-ttu-id="2cd79-205">Questa proprietà viene utilizzata dal runtime del formato Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2cd79-205">This property is used by the Windows Media Format runtime.</span></span> <span data-ttu-id="2cd79-206">Il tipo di proprietà è <strong>VARIANT_BOOL</strong>.</span><span class="sxs-lookup"><span data-stu-id="2cd79-206">The property type is <strong>VARIANT_BOOL</strong>.</span></span> <span data-ttu-id="2cd79-207">Se il valore è <strong>VARIANT_TRUE</strong>, il decodificatore deve essere svuotato dopo una discontinuità.</span><span class="sxs-lookup"><span data-stu-id="2cd79-207">If the value is <strong>VARIANT_TRUE</strong>, the decoder should be drained after a discontinuity.</span></span> <span data-ttu-id="2cd79-208">Per altre informazioni sullo svuotamento di un MFT, vedere <a href="basic-mft-processing-model.md">modello di elaborazione MFT di base</a>.</span><span class="sxs-lookup"><span data-stu-id="2cd79-208">For more information about draining an MFT, see <a href="basic-mft-processing-model.md">Basic MFT Processing Model</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2cd79-209">Per eseguire una query su questa proprietà, usare l'interfaccia <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2cd79-209">To query this property, use the <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> interface.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="2cd79-210">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cd79-210">Remarks</span></span>

<span data-ttu-id="2cd79-211">La risoluzione massima consentita dal decodificatore Windows Media Video 9 è 4096x4096.</span><span class="sxs-lookup"><span data-stu-id="2cd79-211">The maximum resolution allowed by the Windows Media Video 9 decoder is 4096x4096.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cd79-212">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cd79-212">Requirements</span></span>



| <span data-ttu-id="2cd79-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd79-213">Requirement</span></span> | <span data-ttu-id="2cd79-214">Valore</span><span class="sxs-lookup"><span data-stu-id="2cd79-214">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd79-215">Client</span><span class="sxs-lookup"><span data-stu-id="2cd79-215">Client</span></span><br/> | <span data-ttu-id="2cd79-216">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="2cd79-216">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="2cd79-217">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cd79-217">Header</span></span><br/> | <dl> <span data-ttu-id="2cd79-218"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd79-218"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="2cd79-219">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd79-219">DLL</span></span><br/>    | <dl> <span data-ttu-id="2cd79-220"><dt>Wmvdecod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd79-220"><dt>Wmvdecod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd79-221">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cd79-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd79-222">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="2cd79-222">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="2cd79-223">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="2cd79-223">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
