---
description: Il codificatore Windows Media Video 9 codifica i flussi video.
ms.assetid: 1d0a41bc-7f7c-4e25-860c-1108ab292951
title: Codificatore Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36ee5823c585d60ee74e75f99e8ec9b4d91f5cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331569"
---
# <a name="windows-media-video-9-encoder"></a><span data-ttu-id="efafb-103">Codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-103">Windows Media Video 9 Encoder</span></span>

<span data-ttu-id="efafb-104">Il codificatore Windows Media Video 9 codifica i flussi video.</span><span class="sxs-lookup"><span data-stu-id="efafb-104">The Windows Media Video 9 encoder encodes video streams.</span></span> <span data-ttu-id="efafb-105">Il codificatore supporta le quattro categorie di output codificate seguenti.</span><span class="sxs-lookup"><span data-stu-id="efafb-105">The encoder supports the following four categories of encoded output.</span></span>

-   <span data-ttu-id="efafb-106">Profilo semplice Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-106">Windows Media Video 9 Simple Profile</span></span>
-   <span data-ttu-id="efafb-107">Profilo principale Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-107">Windows Media Video 9 Main Profile</span></span>
-   <span data-ttu-id="efafb-108">Profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-108">Windows Media Video 9 Advanced Profile</span></span>
-   <span data-ttu-id="efafb-109">Immagine di Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="efafb-109">Windows Media Video 9.1 Image</span></span>

## <a name="class-identifier"></a><span data-ttu-id="efafb-110">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="efafb-110">Class Identifier</span></span>

<span data-ttu-id="efafb-111">L'identificatore di classe (CLSID) per il codificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMV9EncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="efafb-111">The class identifier (CLSID) for the Windows Media Video encoder is represented by the constant **CLSID\_CWMV9EncMediaObject**.</span></span> <span data-ttu-id="efafb-112">È possibile creare un'istanza del codificatore video chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="efafb-112">You can create an instance of the video encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="efafb-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="efafb-113">Interfaces</span></span>

<span data-ttu-id="efafb-114">Un oggetto del codificatore video espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="efafb-114">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="efafb-115">Un codificatore video si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="efafb-115">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="efafb-116">Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore video si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="efafb-116">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="efafb-117">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="efafb-117">Operating system</span></span>            | <span data-ttu-id="efafb-118">Comportamento del codificatore</span><span class="sxs-lookup"><span data-stu-id="efafb-118">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efafb-119">Windows XP</span><span class="sxs-lookup"><span data-stu-id="efafb-119">Windows XP</span></span>                  | <span data-ttu-id="efafb-120">Un codificatore Windows Media video si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="efafb-120">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="efafb-121">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="efafb-121">Windows Vista and Windows 7</span></span> | <span data-ttu-id="efafb-122">Per impostazione predefinita, un codificatore video Windows Media si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="efafb-122">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="efafb-123">Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un codificatore video, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="efafb-123">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="efafb-124">Formati di input</span><span class="sxs-lookup"><span data-stu-id="efafb-124">Input Formats</span></span>

<span data-ttu-id="efafb-125">Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da DMO.</span><span class="sxs-lookup"><span data-stu-id="efafb-125">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="efafb-126">\_IYUV MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-126">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="efafb-127">\_I420 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-127">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="efafb-128">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-128">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="efafb-129">\_NV11 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-129">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="efafb-130">\_NV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="efafb-131">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-131">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="efafb-132">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-132">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="efafb-133">\_YVYU MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-133">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="efafb-134">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-134">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="efafb-135">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-135">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="efafb-136">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-136">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="efafb-137">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-137">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="efafb-138">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="efafb-138">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="efafb-139">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="efafb-139">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="efafb-140">Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da MFT.</span><span class="sxs-lookup"><span data-stu-id="efafb-140">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="efafb-141">\_IYUV MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-141">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="efafb-142">\_I420 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-142">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="efafb-143">\_YV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-143">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="efafb-144">\_NV11 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-144">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="efafb-145">\_NV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-145">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="efafb-146">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-146">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="efafb-147">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-147">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="efafb-148">\_YVYU MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-148">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="efafb-149">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-149">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="efafb-150">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-150">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="efafb-151">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-151">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="efafb-152">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-152">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="efafb-153">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="efafb-153">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="efafb-154">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="efafb-154">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="efafb-155">Formati di output</span><span class="sxs-lookup"><span data-stu-id="efafb-155">Output Formats</span></span>

<span data-ttu-id="efafb-156">La tabella seguente illustra i codici a quattro caratteri (fourcc) che corrispondono alle categorie di output codificato.</span><span class="sxs-lookup"><span data-stu-id="efafb-156">The following table shows the four-character codes (FOURCCs) that correspond to the categories of encoded output.</span></span>



| <span data-ttu-id="efafb-157">Category</span><span class="sxs-lookup"><span data-stu-id="efafb-157">Category</span></span>                               | <span data-ttu-id="efafb-158">FOURCC</span><span class="sxs-lookup"><span data-stu-id="efafb-158">FOURCC</span></span>                                   |
|----------------------------------------|------------------------------------------|
| <span data-ttu-id="efafb-159">Profilo semplice Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-159">Windows Media Video 9 Simple Profile</span></span>   | <span data-ttu-id="efafb-160">WMV3</span><span class="sxs-lookup"><span data-stu-id="efafb-160">"WMV3"</span></span>                                   |
| <span data-ttu-id="efafb-161">Profilo principale Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-161">Windows Media Video 9 Main Profile</span></span>     | <span data-ttu-id="efafb-162">WMV3</span><span class="sxs-lookup"><span data-stu-id="efafb-162">"WMV3"</span></span>                                   |
| <span data-ttu-id="efafb-163">Profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="efafb-163">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="efafb-164">WVC1</span><span class="sxs-lookup"><span data-stu-id="efafb-164">"WVC1"</span></span>                                   |
| <span data-ttu-id="efafb-165">Immagine di Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="efafb-165">Windows Media Video 9.1 Image</span></span>          | <span data-ttu-id="efafb-166">"WMVP" per 9,1, "WVP2" per 9,1 versione 2</span><span class="sxs-lookup"><span data-stu-id="efafb-166">"WMVP" for 9.1, "WVP2" for 9.1 version 2</span></span> |



 

<span data-ttu-id="efafb-167">Per distinguere tra profilo semplice e profilo principale, impostare la proprietà [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="efafb-167">To distinguish between Simple Profile and Main Profile, set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property.</span></span>

## <a name="properties"></a><span data-ttu-id="efafb-168">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efafb-168">Properties</span></span>

<span data-ttu-id="efafb-169">Il codificatore Windows Media Video 9 supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="efafb-169">The Windows Media Video 9 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="efafb-170">Proprietà</span><span class="sxs-lookup"><span data-stu-id="efafb-170">Property</span></span></th>
<th><span data-ttu-id="efafb-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efafb-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efafb-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-172"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="efafb-173">Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.</span><span class="sxs-lookup"><span data-stu-id="efafb-173">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="efafb-174">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-174">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-175">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-175">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-176">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-177"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-178">Specifica la frequenza media dei fotogrammi del contenuto video, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="efafb-178">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="efafb-179">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-179">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-180">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-180">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-181">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-182"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="efafb-183">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="efafb-183">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="efafb-184">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-184">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-185">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-185">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-186">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-187"><a href="mfpkey-bdeltaqpproperty.md"><strong>MFPKEY_BDELTAQP</strong></a></span></span></td>
<td><span data-ttu-id="efafb-188">Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.</span><span class="sxs-lookup"><span data-stu-id="efafb-188">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span><br/> <dl> <span data-ttu-id="efafb-189">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-189">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-190">Profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-190">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-191">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-191">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-192"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="efafb-193">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="efafb-193">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="efafb-194">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-194">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-195">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-195">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-196">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-196">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-197"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-198">Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="efafb-198">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="efafb-199">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-199">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-200">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-200">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-201">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-201">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-202"><a href="mfpkey-closedentrypointproperty.md"><strong>MFPKEY_CLOSEDENTRYPOINT</strong></a></span></span></td>
<td><span data-ttu-id="efafb-203">Specifica il modello di codifica da usare all'inizio di un Group of Pictures.</span><span class="sxs-lookup"><span data-stu-id="efafb-203">Specifies the encoding pattern to use at the beginning of a group of pictures.</span></span><br/> <dl> <span data-ttu-id="efafb-204">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-205">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-205">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-206">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-206">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-207"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-208">Specifica il numero di fotogrammi video codificati dal codec.</span><span class="sxs-lookup"><span data-stu-id="efafb-208">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="efafb-209">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-209">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-210">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-210">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-211">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-212"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-213">Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.</span><span class="sxs-lookup"><span data-stu-id="efafb-213">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="efafb-214">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-214">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-215">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-215">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-216">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-216">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-217"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="efafb-218">Questa proprietà viene sostituita da <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="efafb-218">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-219"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="efafb-220">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="efafb-220">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="efafb-221">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-221">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-222">Profilo semplice, profilo principale.</span><span class="sxs-lookup"><span data-stu-id="efafb-222">Simple Profile, Main Profile.</span></span> <span data-ttu-id="efafb-223">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-223">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-224">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-224">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-225"><a href="mfpkey-compressionoptimizationtypeproperty.md"><strong>MFPKEY_COMPRESSIONOPTIMIZATIONTYPE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-226">Specifica il tipo di ottimizzazione da utilizzare per il codec del profilo avanzato Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="efafb-226">Specifies the type of optimization to use for the Windows Media Video 9 Advanced Profile codec.</span></span><br/> <dl> <span data-ttu-id="efafb-227">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-227">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-228">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-228">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-229">Scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-229">Write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-230"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="efafb-231">Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="efafb-231">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="efafb-232">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-232">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-233">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-233">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-234">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-234">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-235"><a href="mfpkey-datarateproperty.md"><strong>MFPKEY_DATARATE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-236">Non usato.</span><span class="sxs-lookup"><span data-stu-id="efafb-236">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-237"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-238">Specifica il modello di conformità del dispositivo in cui è conforme il contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="efafb-238">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="efafb-239">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-239">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-240">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-240">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-241">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-241">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-242"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="efafb-243">Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.</span><span class="sxs-lookup"><span data-stu-id="efafb-243">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-244">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-244">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-245">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-245">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-246">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-246">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-247"><a href="mfpkey-deltamvrangeindexproperty.md"><strong>MFPKEY_DELTAMVRANGEINDEX</strong></a></span></span></td>
<td><span data-ttu-id="efafb-248">Specifica il metodo usato per codificare le informazioni sul vettore di movimento.</span><span class="sxs-lookup"><span data-stu-id="efafb-248">Specifies the method used to encode the motion vector information.</span></span><br/> <dl> <span data-ttu-id="efafb-249">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-249">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-250">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-250">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-251">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-251">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-252"><a href="mfpkey-denoiseoptionproperty.md"><strong>MFPKEY_DENOISEOPTION</strong></a></span></span></td>
<td><span data-ttu-id="efafb-253">Specifica se il codec utilizzerà il filtro rumore durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-253">Specifies whether the codec will use the noise filter when encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-254">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-254">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-255">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-255">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-256">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-256">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-257"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="efafb-258">Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).</span><span class="sxs-lookup"><span data-stu-id="efafb-258">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-259">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-260">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-260">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-261">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-261">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-262"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-263">Specifica il numero di fotogrammi video eliminati durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-263">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-264">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-264">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-265">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-265">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-266">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-266">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-267"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="efafb-268">Specifica la fine di un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-268">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="efafb-269">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-269">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-270">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-270">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-271">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-271">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-272"><a href="mfpkey-forceframeheightproperty.md"><strong>MFPKEY_FORCEFRAMEHEIGHT</strong></a></span></span></td>
<td><span data-ttu-id="efafb-273">Specifica un'altezza del frame intermedia per il video codificato.</span><span class="sxs-lookup"><span data-stu-id="efafb-273">Specifies an intermediate frame height for encoded video.</span></span><br/> <dl> <span data-ttu-id="efafb-274">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-274">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-275">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-275">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-276">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-277"><a href="mfpkey-forceframewidthproperty.md"><strong>MFPKEY_FORCEFRAMEWIDTH</strong></a></span></span></td>
<td><span data-ttu-id="efafb-278">Specifica una larghezza del frame intermedia per il video codificato.</span><span class="sxs-lookup"><span data-stu-id="efafb-278">Specifies an intermediate frame width for encoded video.</span></span><br/> <dl> <span data-ttu-id="efafb-279">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-279">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-280">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-280">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-281">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-282"><a href="mfpkey-forcemediansettingproperty.md"><strong>MFPKEY_FORCEMEDIANSETTING</strong></a></span></span></td>
<td><span data-ttu-id="efafb-283">Specifica se il codec deve usare il filtro mediano durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-283">Specifies whether the codec should use median filtering during encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-284">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-284">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-285">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-285">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-286">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-286">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-287"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="efafb-288">Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="efafb-288">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="efafb-289">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-289">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-290">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-290">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-291">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-291">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-292"><a href="mfpkey-framecountproperty.md"><strong>MFPKEY_FRAMECOUNT</strong></a></span></span></td>
<td><span data-ttu-id="efafb-293">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="efafb-293">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-294"><a href="mfpkey-fullframerateproperty.md"><strong>MFPKEY_FULLFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-295">Specifica se il codificatore può rilasciare frame.</span><span class="sxs-lookup"><span data-stu-id="efafb-295">Specifies whether the encoder is allowed to drop frames.</span></span><br/> <dl> <span data-ttu-id="efafb-296">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-296">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-297">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-297">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-298">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-298">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-299"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="efafb-300">Specifica se l'output del codec sarà interlacciato.</span><span class="sxs-lookup"><span data-stu-id="efafb-300">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="efafb-301">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-301">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-302">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-302">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-303">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-303">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-304"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="efafb-305">Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="efafb-305">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="efafb-306">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-306">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-307">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-307">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-308">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-308">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-309"><a href="mfpkey-liveencodeproperty.md"><strong>MFPKEY_LIVEENCODE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-310">Non usato.</span><span class="sxs-lookup"><span data-stu-id="efafb-310">Not used.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-311"><a href="mfpkey-lookaheadproperty.md"><strong>MFPKEY_LOOKAHEAD</strong></a></span></span></td>
<td><span data-ttu-id="efafb-312">Specifica il numero di fotogrammi dopo il frame corrente che il codec valuterà prima di codificare il frame corrente.</span><span class="sxs-lookup"><span data-stu-id="efafb-312">Specifies the number of frames after the current frame that the codec will evaluate before encoding the current frame.</span></span><br/> <dl> <span data-ttu-id="efafb-313">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-313">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-314">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-314">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-315">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-315">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-316"><a href="mfpkey-loopfilterproperty.md"><strong>MFPKEY_LOOPFILTER</strong></a></span></span></td>
<td><span data-ttu-id="efafb-317">Specifica se il codec deve usare il filtro di deblocco in ciclo durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-317">Specifies whether the codec should use the in-loop deblocking filter during encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-318">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-318">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-319">Profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-319">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-320">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-320">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-321"><a href="mfpkey-macroblockmodecostmethodproperty.md"><strong>MFPKEY_MACROBLOCKMODECOSTMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="efafb-322">Specifica il metodo di costo utilizzato dal codec per determinare la modalità di macroblocco da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="efafb-322">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span><br/> <dl> <span data-ttu-id="efafb-323">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-323">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-324">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-324">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-325">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-325">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-326"><a href="mfpkey-motionmatchmethodproperty.md"><strong>MFPKEY_MOTIONMATCHMETHOD</strong></a></span></span></td>
<td><span data-ttu-id="efafb-327">Specifica il metodo da usare per la corrispondenza di movimento.</span><span class="sxs-lookup"><span data-stu-id="efafb-327">Specifies the method to use for motion matching.</span></span><br/> <dl> <span data-ttu-id="efafb-328">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-328">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-329">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-329">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-330">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-330">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-331"><a href="mfpkey-motionsearchlevelproperty.md"><strong>MFPKEY_MOTIONSEARCHLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="efafb-332">Specifica i tipi di informazioni video utilizzate nelle operazioni di ricerca di movimento.</span><span class="sxs-lookup"><span data-stu-id="efafb-332">Specifies the types of video information that are used in motion search operations.</span></span><br/> <dl> <span data-ttu-id="efafb-333">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-333">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-334">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-334">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-335">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-335">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-336"><a href="mfpkey-motionsearchrangeproperty.md"><strong>MFPKEY_MOTIONSEARCHRANGE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-337">Specifica l'intervallo usato nelle ricerche di movimento.</span><span class="sxs-lookup"><span data-stu-id="efafb-337">Specifies the range used in motion searches.</span></span><br/> <dl> <span data-ttu-id="efafb-338">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-338">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-339">Profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-339">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-340">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-340">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-341"><a href="mfpkey-noiseedgeremovalproperty.md"><strong>MFPKEY_NOISEEDGEREMOVAL</strong></a></span></span></td>
<td><span data-ttu-id="efafb-342">Specifica se il codec deve tentare di rilevare i bordi del frame disturbati e di rimuoverli.</span><span class="sxs-lookup"><span data-stu-id="efafb-342">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span><br/> <dl> <span data-ttu-id="efafb-343">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-343">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-344">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-344">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-345">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-345">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-346"><a href="mfpkey-numbframesproperty.md"><strong>MFPKEY_NUMBFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-347">Specifica il numero di frame predittivi bidirezionali (fotogrammi B).</span><span class="sxs-lookup"><span data-stu-id="efafb-347">Specifies the number of bidirectional predictive frames (B-frames).</span></span><br/> <dl> <span data-ttu-id="efafb-348">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-348">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-349">Profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-349">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-350">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-350">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-351"><a href="mfpkey-numthreadsproperty.md"><strong>MFPKEY_NUMTHREADS</strong></a></span></span></td>
<td><span data-ttu-id="efafb-352">Specifica il numero di thread che il codec utilizzerà per la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-352">Specifies the number of threads that the codec will use for encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-353">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-353">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-354">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-354">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-355">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-355">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-356"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="efafb-357">Specifica il numero massimo di passaggi supportati dal codec.</span><span class="sxs-lookup"><span data-stu-id="efafb-357">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="efafb-358">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-358">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-359">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-359">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-360">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-360">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-361"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="efafb-362">Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="efafb-362">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="efafb-363">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-363">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-364">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-364">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-365">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-365">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-366"><a href="mfpkey-perceptualoptlevelproperty.md"><strong>MFPKEY_PERCEPTUALOPTLEVEL</strong></a></span></span></td>
<td><span data-ttu-id="efafb-367">Specifica se il codec deve usare l'ottimizzazione percettiva conservativa durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-367">Specifies whether the codec should use conservative perceptual optimization when encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-368">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-368">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-369">Profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-369">Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-370">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-370">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-371"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-372">Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.</span><span class="sxs-lookup"><span data-stu-id="efafb-372">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="efafb-373">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-373">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-374">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-374">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-375">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-375">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-376"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="efafb-377">Specifica QP.</span><span class="sxs-lookup"><span data-stu-id="efafb-377">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="efafb-378">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-378">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-379">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-379">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-380">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-380">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-381"><a href="mfpkey-rangereduxproperty.md"><strong>MFPKEY_RANGEREDUX</strong></a></span></span></td>
<td><span data-ttu-id="efafb-382">Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.</span><span class="sxs-lookup"><span data-stu-id="efafb-382">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span><br/> <dl> <span data-ttu-id="efafb-383">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-383">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-384">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-384">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-385">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-385">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-386"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="efafb-387">Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.</span><span class="sxs-lookup"><span data-stu-id="efafb-387">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-388">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-388">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-389">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-389">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-390">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-390">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-391"><a href="mfpkey-rdsubpixelsearchproperty.md"><strong>MFPKEY_RDSUBPIXELSEARCH</strong></a></span></span></td>
<td><span data-ttu-id="efafb-392">Specifica se il codificatore usa la ricerca MV dei sottopixel basata su desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="efafb-392">Specifies whether the encoder uses RD-based sub-pixel MV search.</span></span> <br/> <dl> <span data-ttu-id="efafb-393">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-393">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-394">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-394">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-395">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-395">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-396"><a href="mfpkey-reencendbuffersizeproperty.md"><strong>MFPKEY_REENCENDBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-397">Per la ricodifica del segmento, specifica le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="efafb-397">For segment re-encoding, specifies the buffer size.</span></span><br/> <dl> <span data-ttu-id="efafb-398">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-398">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-399">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-399">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-400">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-400">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-401"><a href="mfpkey-reencdurationproperty.md"><strong>MFPKEY_REENCDURATION</strong></a></span></span></td>
<td><span data-ttu-id="efafb-402">Per la ricodifica del segmento, specifica la durata del segmento da codificare di nuovo.</span><span class="sxs-lookup"><span data-stu-id="efafb-402">For segment re-encoding, specifies the duration of the segment to be re-encoded.</span></span><br/> <dl> <span data-ttu-id="efafb-403">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-403">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-404">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-404">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-405">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-405">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-406"><a href="mfpkey-reencqprefproperty.md"><strong>MFPKEY_REENCQPREF</strong></a></span></span></td>
<td><span data-ttu-id="efafb-407">Per la ricodifica del segmento, specifica il quantizzatore del frame prima del segmento iniziale.</span><span class="sxs-lookup"><span data-stu-id="efafb-407">For segment re-encoding, specifies the quantizer of the frame prior to the starting segment.</span></span><br/> <dl> <span data-ttu-id="efafb-408">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-408">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-409">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-409">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-410">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-410">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-411"><a href="mfpkey-reencstartbuffersizeproperty.md"><strong>MFPKEY_REENCSTARTBUFFERSIZE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-412">Per la ricodifica del segmento, specifica la completezza del buffer iniziale.</span><span class="sxs-lookup"><span data-stu-id="efafb-412">For segment re-encoding, specifies the starting buffer fullness.</span></span><br/> <dl> <span data-ttu-id="efafb-413">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-413">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-414">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-414">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-415">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-415">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-416"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="efafb-417">Specifica la velocità in bit del picco, in bit al secondo, usata per la velocità in bit (VBR) a due passaggi vincolati.</span><span class="sxs-lookup"><span data-stu-id="efafb-417">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="efafb-418">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-418">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-419">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-419">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-420">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-420">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-421"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-422">Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="efafb-422">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="efafb-423">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-423">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-424">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-424">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-425">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="efafb-425">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-426"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="efafb-427">Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="efafb-427">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-428">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-428">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-429">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-429">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-430">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-430">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-431"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="efafb-432">Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).</span><span class="sxs-lookup"><span data-stu-id="efafb-432">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="efafb-433">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-433">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-434">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-434">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-435">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-435">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-436"><a href="mfpkey-videoscalingproperty.md"><strong>MFPKEY_VIDEOSCALING</strong></a></span></span></td>
<td><span data-ttu-id="efafb-437">Specifica se il codec utilizzerà l'ottimizzazione del ridimensionamento del video.</span><span class="sxs-lookup"><span data-stu-id="efafb-437">Specifies whether the codec will use video scaling optimization.</span></span><br/> <dl> <span data-ttu-id="efafb-438">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-438">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-439">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-439">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-440">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-440">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-441"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="efafb-442">Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.</span><span class="sxs-lookup"><span data-stu-id="efafb-442">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="efafb-443">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-443">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-444">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-444">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-445">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-445">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-446"><a href="mfpkey-volheaderforreencodeproperty.md"><strong>MFPKEY_VOLHEADERFORREENCODE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-447">Per la ricodifica del segmento, specifica i dati privati dei codec del file da codificare di nuovo.</span><span class="sxs-lookup"><span data-stu-id="efafb-447">For segment re-encoding, specifies the codec private data of the file that is being re-encoded.</span></span><br/> <dl> <span data-ttu-id="efafb-448">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-448">Windows Vista and later.</span></span><br />
<span data-ttu-id="efafb-449">Profilo semplice, profilo principale, profilo avanzato, immagine.</span><span class="sxs-lookup"><span data-stu-id="efafb-449">Simple Profile, Main Profile, Advanced Profile, Image.</span></span><br />
<span data-ttu-id="efafb-450">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-450">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efafb-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-451"><a href="mfpkey-vtypeproperty.md"><strong>MFPKEY_VTYPE</strong></a></span></span></td>
<td><span data-ttu-id="efafb-452">Specifica il tipo di logica che il codec userà per rilevare il video di origine interlacciato.</span><span class="sxs-lookup"><span data-stu-id="efafb-452">Specifies the type of logic that the codec will use to detect interlaced source video.</span></span><br/> <dl> <span data-ttu-id="efafb-453">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-453">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-454">Profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-454">Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-455">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="efafb-455">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efafb-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="efafb-456"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="efafb-457">Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.</span><span class="sxs-lookup"><span data-stu-id="efafb-457">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="efafb-458">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="efafb-458">Windows XP and later.</span></span><br />
<span data-ttu-id="efafb-459">Profilo semplice, profilo principale, profilo avanzato.</span><span class="sxs-lookup"><span data-stu-id="efafb-459">Simple Profile, Main Profile, Advanced Profile.</span></span><br />
<span data-ttu-id="efafb-460">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="efafb-460">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="efafb-461">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efafb-461">Requirements</span></span>



| <span data-ttu-id="efafb-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="efafb-462">Requirement</span></span> | <span data-ttu-id="efafb-463">Valore</span><span class="sxs-lookup"><span data-stu-id="efafb-463">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efafb-464">Client</span><span class="sxs-lookup"><span data-stu-id="efafb-464">Client</span></span><br/> | <span data-ttu-id="efafb-465">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="efafb-465">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="efafb-466">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efafb-466">Header</span></span><br/> | <dl> <span data-ttu-id="efafb-467"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="efafb-467"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="efafb-468">DLL</span><span class="sxs-lookup"><span data-stu-id="efafb-468">DLL</span></span><br/>    | <dl> <span data-ttu-id="efafb-469"><dt>Wmvencod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efafb-469"><dt>Wmvencod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efafb-470">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efafb-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efafb-471">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="efafb-471">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="efafb-472">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="efafb-472">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 
