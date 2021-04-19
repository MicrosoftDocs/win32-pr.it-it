---
description: Il codificatore Windows Media Video 7/8 implementa le versioni precedenti del codificatore Windows Media Video.
ms.assetid: c4165614-b9ec-4216-b36c-f57bc05e3a8e
title: Codificatore Windows Media Video 7/8 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5467d02681ef319a508f6f6581e1f3c0191950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332806"
---
# <a name="windows-media-video-78-encoder"></a><span data-ttu-id="c6f2e-103">Codificatore Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="c6f2e-103">Windows Media Video 7/8 Encoder</span></span>

<span data-ttu-id="c6f2e-104">Il codificatore Windows Media Video 7/8 implementa le versioni precedenti del codificatore Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-104">The Windows Media Video 7/8 encoder implements previous versions of the Windows Media Video encoder.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="c6f2e-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="c6f2e-105">Class Identifier</span></span>

<span data-ttu-id="c6f2e-106">L'identificatore di classe (CLSID) per il codificatore Windows Media Video 7/8 è **CLSID \_ CWMVXEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-106">The class identifier (CLSID) for the Windows Media Video 7/8 encoder is **CLSID\_CWMVXEncMediaObject**.</span></span> <span data-ttu-id="c6f2e-107">È possibile creare un'istanza del codificatore chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="c6f2e-108">Interfacce</span><span class="sxs-lookup"><span data-stu-id="c6f2e-108">Interfaces</span></span>

<span data-ttu-id="c6f2e-109">Un oggetto del codificatore video espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="c6f2e-109">A video encoder object exposes the [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="c6f2e-110">Un codificatore video si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-110">A video encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="c6f2e-111">Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore video si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-111">The following table shows the conditions under which a video encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="c6f2e-112">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="c6f2e-112">Operating system</span></span>            | <span data-ttu-id="c6f2e-113">Comportamento del codificatore</span><span class="sxs-lookup"><span data-stu-id="c6f2e-113">Encoder behavior</span></span>                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f2e-114">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6f2e-114">Windows XP</span></span>                  | <span data-ttu-id="c6f2e-115">Un codificatore Windows Media video si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-115">A Windows Media video encoder always behaves as a DMO.</span></span>                                                                                                                |
| <span data-ttu-id="c6f2e-116">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6f2e-116">Windows Vista and Windows 7</span></span> | <span data-ttu-id="c6f2e-117">Per impostazione predefinita, un codificatore video Windows Media si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-117">By default, a Windows Media video encoder behaves as a DMO.</span></span> <span data-ttu-id="c6f2e-118">Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un codificatore video, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-118">If you obtain an [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface on a video encoder, it behaves as an MFT.</span></span> |



 

## <a name="input-formats"></a><span data-ttu-id="c6f2e-119">Formati di input</span><span class="sxs-lookup"><span data-stu-id="c6f2e-119">Input Formats</span></span>

<span data-ttu-id="c6f2e-120">Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da DMO.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-120">The Windows Media Video encoder supports the following input media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="c6f2e-121">\_IYUV MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-121">MEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="c6f2e-122">\_I420 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-122">MEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="c6f2e-123">\_YV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-123">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="c6f2e-124">\_NV11 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-124">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="c6f2e-125">\_NV12 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-125">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="c6f2e-126">\_YUY2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-126">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="c6f2e-127">\_UYVY MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-127">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="c6f2e-128">\_YVYU MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-128">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="c6f2e-129">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-129">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="c6f2e-130">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-130">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="c6f2e-131">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-131">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="c6f2e-132">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-132">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="c6f2e-133">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6f2e-133">MEDIASUBTYPE\_RGB8</span></span>
-   <span data-ttu-id="c6f2e-134">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="c6f2e-134">MEDIASUBTYPE\_PHOTOMOTION</span></span>

<span data-ttu-id="c6f2e-135">Il codificatore Windows Media Video supporta i sottotipi di supporti di input seguenti quando funge da MFT.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-135">The Windows Media Video encoder supports the following input media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="c6f2e-136">\_IYUV MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-136">MFVideoFormat\_IYUV</span></span>
-   <span data-ttu-id="c6f2e-137">\_I420 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-137">MFVideoFormat\_I420</span></span>
-   <span data-ttu-id="c6f2e-138">\_YV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-138">MFVideoFormat\_YV12</span></span>
-   <span data-ttu-id="c6f2e-139">\_NV11 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-139">MFVideoFormat\_NV11</span></span>
-   <span data-ttu-id="c6f2e-140">\_NV12 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-140">MFVideoFormat\_NV12</span></span>
-   <span data-ttu-id="c6f2e-141">\_YUY2 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-141">MFVideoFormat\_YUY2</span></span>
-   <span data-ttu-id="c6f2e-142">\_UYVY MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-142">MFVideoFormat\_UYVY</span></span>
-   <span data-ttu-id="c6f2e-143">\_YVYU MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-143">MFVideoFormat\_YVYU</span></span>
-   <span data-ttu-id="c6f2e-144">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-144">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="c6f2e-145">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-145">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="c6f2e-146">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-146">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="c6f2e-147">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-147">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="c6f2e-148">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="c6f2e-148">MFVideoFormat\_RGB8</span></span>
-   <span data-ttu-id="c6f2e-149">MEDIASUBTYPE \_ FOTOmotion</span><span class="sxs-lookup"><span data-stu-id="c6f2e-149">MEDIASUBTYPE\_PHOTOMOTION</span></span>

## <a name="output-formats"></a><span data-ttu-id="c6f2e-150">Formati di output</span><span class="sxs-lookup"><span data-stu-id="c6f2e-150">Output Formats</span></span>

<span data-ttu-id="c6f2e-151">La tabella seguente illustra i codici a quattro caratteri (fourcc) per i tipi di output supportati dal codificatore Windows Media Video 7/8.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-151">The following table shows the four-character codes (FOURCCs) for the output types supported by the Windows Media Video 7/8 encoder.</span></span>



| <span data-ttu-id="c6f2e-152">Category</span><span class="sxs-lookup"><span data-stu-id="c6f2e-152">Category</span></span>              | <span data-ttu-id="c6f2e-153">FOURCC</span><span class="sxs-lookup"><span data-stu-id="c6f2e-153">FOURCC</span></span> |
|-----------------------|--------|
| <span data-ttu-id="c6f2e-154">Windows Media Video 7</span><span class="sxs-lookup"><span data-stu-id="c6f2e-154">Windows Media Video 7</span></span> | <span data-ttu-id="c6f2e-155">WMV1</span><span class="sxs-lookup"><span data-stu-id="c6f2e-155">"WMV1"</span></span> |
| <span data-ttu-id="c6f2e-156">Windows Media Video 8</span><span class="sxs-lookup"><span data-stu-id="c6f2e-156">Windows Media Video 8</span></span> | <span data-ttu-id="c6f2e-157">WMV2</span><span class="sxs-lookup"><span data-stu-id="c6f2e-157">"WMV2"</span></span> |



 

## <a name="properties"></a><span data-ttu-id="c6f2e-158">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6f2e-158">Properties</span></span>

<span data-ttu-id="c6f2e-159">Il codificatore Windows Media Video 7/8 supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-159">The Windows Media Video 7/8 encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c6f2e-160">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c6f2e-160">Property</span></span></th>
<th><span data-ttu-id="c6f2e-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6f2e-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6f2e-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-162"><a href="mfpkey-asfoverheadperframeproperty.md"><strong>MFPKEY_ASFOVERHEADPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-163">Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-163">Specifies the overhead, in bytes per packet, required for the container used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="c6f2e-164">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-164">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-165">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-165">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-166"><a href="mfpkey-avgframerateproperty.md"><strong>MFPKEY_AVGFRAMERATE</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-167">Specifica la frequenza media dei fotogrammi del contenuto video, in frame al secondo.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-167">Specifies the average frame rate of video content, in frames per second.</span></span><br/> <dl> <span data-ttu-id="c6f2e-168">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-168">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-169">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-169">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-170"><a href="mfpkey-bavgproperty.md"><strong>MFPKEY_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-171">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="c6f2e-171">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a>).</span></span><br/> <dl> <span data-ttu-id="c6f2e-172">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-172">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-173">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-173">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-174"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-175">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="c6f2e-175">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a>).</span></span><br/> <dl> <span data-ttu-id="c6f2e-176">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-176">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-177">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-177">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-178"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md"><strong>MFPKEY_BUFFERFULLNESSINFIRSTBYTE</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-179">Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-179">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="c6f2e-180">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-180">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-181">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-181">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-182"><a href="mfpkey-codedframesproperty.md"><strong>MFPKEY_CODEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-183">Specifica il numero di fotogrammi video codificati dal codec.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-183">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="c6f2e-184">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-184">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-185">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-185">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-186"><a href="mfpkey-codednonzeroframesproperty.md"><strong>MFPKEY_CODEDNONZEROFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-187">Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-187">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="c6f2e-188">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-188">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-189">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-189">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-190"><a href="mfpkey-complexityproperty.md"><strong>MFPKEY_COMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-191">Questa proprietà viene sostituita da <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-191">This property is superseded by <a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-192"><a href="mfpkey-complexityexproperty.md"><strong>MFPKEY_COMPLEXITYEX</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-193">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-193">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="c6f2e-194">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-194">Windows Vista and later.</span></span><br />
<span data-ttu-id="c6f2e-195">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-195">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-196"><a href="mfpkey-crispproperty.md"><strong>MFPKEY_CRISP</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-197">Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-197">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="c6f2e-198">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-198">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-199">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-199">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-200"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-201">Specifica il modello di conformità del dispositivo in cui è conforme il contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-201">Specifies the device conformance template to which the encoded content conforms.</span></span><br/> <dl> <span data-ttu-id="c6f2e-202">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-202">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-203">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-203">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-204"><a href="mfpkey-decodercomplexityrequestedproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYREQUESTED</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-205">Specifica il modello di conformità del dispositivo che si vuole usare per la codifica video.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-205">Specifies the device conformance template that you want to use for video encoding.</span></span><br/> <dl> <span data-ttu-id="c6f2e-206">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-206">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-207">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-207">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-208"><a href="mfpkey-droppedframesproperty.md"><strong>MFPKEY_DROPPEDFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-209">Specifica il numero di fotogrammi video eliminati durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-209">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="c6f2e-210">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-210">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-211">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-211">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-212"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-213">Specifica la fine di un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-213">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="c6f2e-214">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-214">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-215">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-215">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-216"><a href="mfpkey-fourccproperty.md"><strong>MFPKEY_FOURCC</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-217">Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-217">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="c6f2e-218">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-218">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-219">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-219">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-220"><a href="mfpkey-interlacedcodingenabledproperty.md"><strong>MFPKEY_INTERLACEDCODINGENABLED</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-221">Specifica se l'output del codec sarà interlacciato.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-221">Specifies whether the codec output will be interlaced.</span></span><br/> <dl> <span data-ttu-id="c6f2e-222">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-222">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-223">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-223">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-224"><a href="mfpkey-keydistproperty.md"><strong>MFPKEY_KEYDIST</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-225">Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-225">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="c6f2e-226">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-226">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-227">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-227">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-228"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-229">Specifica il numero massimo di passaggi supportati dal codec.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-229">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="c6f2e-230">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-230">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-231">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-231">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-232"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-233">Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-233">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="c6f2e-234">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-234">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-235">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-235">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-236"><a href="mfpkey-producedummyframesproperty.md"><strong>MFPKEY_PRODUCEDUMMYFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-237">Specifica se il codificatore produce voci di frame fittizie nel flusso di bit per i frame duplicati.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-237">Specifies whether the encoder produces dummy frame entries in the bit stream for duplicate frames.</span></span><br/> <dl> <span data-ttu-id="c6f2e-238">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-238">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-239">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-239">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-240"><a href="mfpkey-qpperframeproperty.md"><strong>MFPKEY_QPPERFRAME</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-241">Specifica QP.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-241">Specifies QP.</span></span><br/> <dl> <span data-ttu-id="c6f2e-242">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-242">Windows Vista and later.</span></span><br />
<span data-ttu-id="c6f2e-243">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-243">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-244"><a href="mfpkey-ravgproperty.md"><strong>MFPKEY_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-245">Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-245">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c6f2e-246">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-246">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-247">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-247">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-248"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-249">Specifica la velocità in bit del picco, in bit al secondo, usata per la velocità in bit (VBR) a due passaggi vincolati.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-249">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR).</span></span><br/> <dl> <span data-ttu-id="c6f2e-250">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-250">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-251">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-252"><a href="mfpkey-totalframesproperty.md"><strong>MFPKEY_TOTALFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-253">Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-253">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="c6f2e-254">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-254">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-255">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-255">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-256"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-257">Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="c6f2e-257">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c6f2e-258">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-258">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-259">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-259">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-260"><a href="mfpkey-vbrqualityproperty.md"><strong>MFPKEY_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-261">Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).</span><span class="sxs-lookup"><span data-stu-id="c6f2e-261">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="c6f2e-262">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-262">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-263">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-263">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c6f2e-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-264"><a href="mfpkey-videowindowproperty.md"><strong>MFPKEY_VIDEOWINDOW</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-265">Specifica la quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-265">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="c6f2e-266">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-266">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-267">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-267">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6f2e-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span><span class="sxs-lookup"><span data-stu-id="c6f2e-268"><a href="mfpkey-zerobyteframesproperty.md"><strong>MFPKEY_ZEROBYTEFRAMES</strong></a></span></span></td>
<td><span data-ttu-id="c6f2e-269">Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-269">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="c6f2e-270">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c6f2e-270">Windows XP and later.</span></span><br />
<span data-ttu-id="c6f2e-271">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="c6f2e-271">Read-only</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c6f2e-272">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6f2e-272">Requirements</span></span>



| <span data-ttu-id="c6f2e-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f2e-273">Requirement</span></span> | <span data-ttu-id="c6f2e-274">Valore</span><span class="sxs-lookup"><span data-stu-id="c6f2e-274">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f2e-275">Client</span><span class="sxs-lookup"><span data-stu-id="c6f2e-275">Client</span></span><br/> | <span data-ttu-id="c6f2e-276">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6f2e-276">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="c6f2e-277">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6f2e-277">Header</span></span><br/> | <dl> <span data-ttu-id="c6f2e-278"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f2e-278"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="c6f2e-279">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f2e-279">DLL</span></span><br/>    | <dl> <span data-ttu-id="c6f2e-280"><dt>Wmvxencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f2e-280"><dt>Wmvxencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f2e-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6f2e-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f2e-282">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="c6f2e-282">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="c6f2e-283">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="c6f2e-283">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="c6f2e-284">GUID del sottotipo video</span><span class="sxs-lookup"><span data-stu-id="c6f2e-284">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> </dl>

 

 
