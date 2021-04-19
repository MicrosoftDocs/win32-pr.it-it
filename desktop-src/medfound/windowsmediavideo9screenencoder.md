---
description: Il codificatore di schermo Windows Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer.
ms.assetid: 22faebf8-40c0-47f9-b66b-c0a8b5ba7202
title: Codificatore della schermata Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e0729a7b8ef09ad9b86b07e6668a933a307550
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331568"
---
# <a name="windows-media-video-9-screen-encoder"></a><span data-ttu-id="6f8f5-103">Codificatore dello schermo Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6f8f5-103">Windows Media Video 9 Screen Encoder</span></span>

<span data-ttu-id="6f8f5-104">Il codificatore di schermo Windows Media Video 9 è ottimizzato per la codifica di schermate sequenziali dai monitoraggi computer.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-104">The Windows Media Video 9 Screen encoder is optimized for encoding sequential screen shots from computer monitors.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="6f8f5-105">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="6f8f5-105">Class Identifier</span></span>

<span data-ttu-id="6f8f5-106">L'identificatore di classe (CLSID) per il codificatore di schermo Windows Media Video 9 è rappresentato dalla costante **CLSID \_ CMSSCEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-106">The class identifier (CLSID) for the Windows Media Video 9 Screen encoder is represented by the constant **CLSID\_CMSSCEncMediaObject2**.</span></span> <span data-ttu-id="6f8f5-107">È possibile creare un'istanza del codificatore chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-107">You can create an instance of the encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-types"></a><span data-ttu-id="6f8f5-108">Tipi di input</span><span class="sxs-lookup"><span data-stu-id="6f8f5-108">Input Types</span></span>

<span data-ttu-id="6f8f5-109">I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-109">The following input types are supported by the Version 9 Screen encoder when it is being used as a DirectX Media Object (DMO).</span></span>

-   <span data-ttu-id="6f8f5-110">\_RGB24 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-110">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="6f8f5-111">\_Rgb32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-111">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="6f8f5-112">\_ARGB32 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-112">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="6f8f5-113">\_RGB565 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-113">MEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="6f8f5-114">\_RGB555 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-114">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="6f8f5-115">\_RGB8 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-115">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="6f8f5-116">I tipi di input seguenti sono supportati dal codificatore dello schermo versione 9 quando viene usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-116">The following input types are supported by the Version 9 Screen encoder when it is being used as a Media Foundation Transform (MFT).</span></span>

-   <span data-ttu-id="6f8f5-117">\_RGB24 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-117">MFVideoFormat\_RGB24</span></span>
-   <span data-ttu-id="6f8f5-118">\_Rgb32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-118">MFVideoFormat\_RGB32</span></span>
-   <span data-ttu-id="6f8f5-119">\_ARGB32 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-119">MFVideoFormat\_ARGB32</span></span>
-   <span data-ttu-id="6f8f5-120">\_RGB565 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-120">MFVideoFormat\_RGB565</span></span>
-   <span data-ttu-id="6f8f5-121">\_RGB555 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-121">MFVideoFormat\_RGB555</span></span>
-   <span data-ttu-id="6f8f5-122">\_RGB8 MFVideoFormat</span><span class="sxs-lookup"><span data-stu-id="6f8f5-122">MFVideoFormat\_RGB8</span></span>

## <a name="output-types"></a><span data-ttu-id="6f8f5-123">Tipi di output</span><span class="sxs-lookup"><span data-stu-id="6f8f5-123">Output Types</span></span>

<span data-ttu-id="6f8f5-124">Il codice di quattro caratteri (FOURCC) per il contenuto codificato Windows Media Video schermata versione 9 è "MSS2".</span><span class="sxs-lookup"><span data-stu-id="6f8f5-124">The four-character code (FOURCC) for Windows Media Video Screen Version 9 encoded content is "MSS2".</span></span>

<span data-ttu-id="6f8f5-125">I tipi di output seguenti sono supportati dal codificatore dello schermo versione 9.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-125">The following output types are supported by the Version 9 Screen encoder.</span></span>

-   <span data-ttu-id="6f8f5-126">\_Mss2 MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="6f8f5-126">MEDIASUBTYPE\_MSS2</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="6f8f5-127">Proprietà del codificatore</span><span class="sxs-lookup"><span data-stu-id="6f8f5-127">Encoder Properties</span></span>

<span data-ttu-id="6f8f5-128">Il codificatore Windows Media Video 9 dello schermo supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-128">The Windows Media Video 9 Screen encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6f8f5-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6f8f5-129">Property</span></span></th>
<th><span data-ttu-id="6f8f5-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f8f5-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f8f5-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-131"><a href="mfpkey-asfoverheadperframeproperty.md">MFPKEY_ASFOVERHEADPERFRAME</a></span></span></td>
<td><span data-ttu-id="6f8f5-132">Specifica l'overhead, in byte per pacchetto, necessario per il contenitore usato per archiviare il contenuto compresso.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-132">Specifies the overhead, in bytes per packet, required for the container that is used to store the compressed content.</span></span><br/> <dl> <span data-ttu-id="6f8f5-133">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-133">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-134">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-134">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-135"><a href="mfpkey-bavgproperty.md">MFPKEY_BAVG</a></span></span></td>
<td><span data-ttu-id="6f8f5-136">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata in base alla velocità in bit media (specificata da <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-136">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its average bit rate (specified by <a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a>).</span></span><br/> <dl> <span data-ttu-id="6f8f5-137">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-137">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-138">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-138">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-139"><a href="mfpkey-bmaxproperty.md">MFPKEY_BMAX</a></span></span></td>
<td><span data-ttu-id="6f8f5-140">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit (VBR) vincolata alla velocità in bit massima (specificata da <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-140">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate (specified by <a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a>).</span></span><br/> <dl> <span data-ttu-id="6f8f5-141">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-141">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-142">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-142">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-143"><a href="mfpkey-bufferfullnessinfirstbyteproperty.md">MFPKEY_BUFFERFULLNESSINFIRSTBYTE</a></span></span></td>
<td><span data-ttu-id="6f8f5-144">Specifica se il flusso di bit video codificato contiene un valore di completezza del buffer con ogni fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-144">Specifies whether the encoded video bit stream contains a buffer fullness value with every key frame.</span></span><br/> <dl> <span data-ttu-id="6f8f5-145">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-145">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-146">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-146">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-147"><a href="mfpkey-codedframesproperty.md">MFPKEY_CODEDFRAMES</a></span></span></td>
<td><span data-ttu-id="6f8f5-148">Specifica il numero di fotogrammi video codificati dal codec.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-148">Specifies the number of video frames encoded by the codec.</span></span><br/> <dl> <span data-ttu-id="6f8f5-149">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-149">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-150">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-150">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-151"><a href="mfpkey-codednonzeroframesproperty.md">MFPKEY_CODEDNONZEROFRAMES</a></span></span></td>
<td><span data-ttu-id="6f8f5-152">Specifica il numero di fotogrammi video codificati dal codec che contengono effettivamente i dati.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-152">Specifies the number of video frames encoded by the codec that actually contain data.</span></span><br/> <dl> <span data-ttu-id="6f8f5-153">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-153">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-154">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-154">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-155"><a href="mfpkey-complexityproperty.md">MFPKEY_COMPLEXITY</a></span></span></td>
<td><span data-ttu-id="6f8f5-156">Questa proprietà viene sostituita da <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-156">This property is superseded by <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-157"><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a></span></span></td>
<td><span data-ttu-id="6f8f5-158">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-158">Specifies the complexity of the encoder algorithm.</span></span><br/> <dl> <span data-ttu-id="6f8f5-159">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="6f8f5-160">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-160">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-161"><a href="mfpkey-crispproperty.md">MFPKEY_CRISP</a></span></span></td>
<td><span data-ttu-id="6f8f5-162">Specifica una rappresentazione numerica del compromesso tra smoothing del movimento e qualità dell'immagine nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-162">Specifies a numeric representation of the tradeoff between motion smoothness and image quality in codec output.</span></span><br/> <dl> <span data-ttu-id="6f8f5-163">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-163">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-164">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-164">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-165"><a href="mfpkey-droppedframesproperty.md">MFPKEY_DROPPEDFRAMES</a></span></span></td>
<td><span data-ttu-id="6f8f5-166">Specifica il numero di fotogrammi video eliminati durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-166">Specifies the number of video frames dropped during encoding.</span></span><br/> <dl> <span data-ttu-id="6f8f5-167">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-167">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-168">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-168">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-169"><a href="mfpkey-endofpassproperty.md">MFPKEY_ENDOFPASS</a></span></span></td>
<td><span data-ttu-id="6f8f5-170">Specifica la fine di un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-170">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="6f8f5-171">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-171">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-172">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-172">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-173"><a href="mfpkey-fourccproperty.md">MFPKEY_FOURCC</a></span></span></td>
<td><span data-ttu-id="6f8f5-174">Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-174">Specifies the FOURCC that identifies the encoder you want to use.</span></span><br/> <dl> <span data-ttu-id="6f8f5-175">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-175">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-176">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-177"><a href="mfpkey-keydistproperty.md">MFPKEY_KEYDIST</a></span></span></td>
<td><span data-ttu-id="6f8f5-178">Specifica il tempo massimo, in millisecondi, tra i fotogrammi chiave nell'output del codec.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-178">Specifies the maximum time, in milliseconds, between key frames in the codec output.</span></span><br/> <dl> <span data-ttu-id="6f8f5-179">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-179">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-180">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-180">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-181"><a href="mfpkey-liveencodeproperty.md">MFPKEY_LIVEENCODE</a></span></span></td>
<td><span data-ttu-id="6f8f5-182">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-182">Obsolete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-183"><a href="mfpkey-passesrecommendedproperty.md">MFPKEY_PASSESRECOMMENDED</a></span></span></td>
<td><span data-ttu-id="6f8f5-184">Specifica il numero massimo di passaggi supportati dal codec.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-184">Specifies the maximum number of passes supported by the codec.</span></span><br/> <dl> <span data-ttu-id="6f8f5-185">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-185">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-186">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-186">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-187"><a href="mfpkey-passesusedproperty.md">MFPKEY_PASSESUSED</a></span></span></td>
<td><span data-ttu-id="6f8f5-188">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-188">Windows XP and later.</span></span> <span data-ttu-id="6f8f5-189">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-189">Read/write.</span></span><br/> <span data-ttu-id="6f8f5-190">Specifica il numero di passaggi che il codec utilizzerà per codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-190">Specifies the number of passes that the codec will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="6f8f5-191">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-191">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-192">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-192">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-193"><a href="mfpkey-qpperframeproperty.md">MFPKEY_QPPERFRAME</a></span></span></td>
<td><span data-ttu-id="6f8f5-194">Specifica QP.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-194">Specifies QP.</span></span> <span data-ttu-id="6f8f5-195">I valori possibili sono compresi tra 1,0 e 31,0.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-195">Possible values are 1.0 through 31.0.</span></span><br/> <dl> <span data-ttu-id="6f8f5-196">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-196">Windows Vista and later.</span></span><br />
<span data-ttu-id="6f8f5-197">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-197">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-198"><a href="mfpkey-ravgproperty.md">MFPKEY_RAVG</a></span></span></td>
<td><span data-ttu-id="6f8f5-199">Specifica la velocità in bit media, in bit al secondo, usata per la codifica con velocità in bit variabile (VBR) a 2 passaggi.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-199">Specifies the average bit rate, in bits per second, used for 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="6f8f5-200">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-200">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-201">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-202"><a href="mfpkey-rmaxproperty.md">MFPKEY_RMAX</a></span></span></td>
<td><span data-ttu-id="6f8f5-203">Specifica la velocità in bit del picco, in bit al secondo, usata per la codifica con velocità in bit (VBR) a 2 passaggi vincolata.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-203">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="6f8f5-204">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-204">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-205">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-205">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-206"><a href="mfpkey-totalframesproperty.md">MFPKEY_TOTALFRAMES</a></span></span></td>
<td><span data-ttu-id="6f8f5-207">Specifica il numero di fotogrammi video passati al codificatore durante il processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-207">Specifies the number of video frames passed to the encoder during the encoding process.</span></span><br/> <dl> <span data-ttu-id="6f8f5-208">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-208">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-209">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-209">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-210"><a href="mfpkey-vbrenabledproperty.md">MFPKEY_VBRENABLED</a></span></span></td>
<td><span data-ttu-id="6f8f5-211">Specifica se il codec utilizzerà la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-211">Specifies whether the codec will use variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="6f8f5-212">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-212">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-213">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-213">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-214"><a href="mfpkey-vbrqualityproperty.md">MFPKEY_VBRQUALITY</a></span></span></td>
<td><span data-ttu-id="6f8f5-215">Specifica il livello di qualità effettivo per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-215">Specifies the actual quality level for quality based (1-pass) variable-bit-rate (VBR) encoding.</span></span><br/> <dl> <span data-ttu-id="6f8f5-216">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-216">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-217">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-217">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f8f5-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-218"><a href="mfpkey-videowindowproperty.md">MFPKEY_VIDEOWINDOW</a></span></span></td>
<td><span data-ttu-id="6f8f5-219">Quantità di contenuto, in millisecondi, che può rientrare nel buffer del modello.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-219">The amount of content, in milliseconds, that can fit into the model buffer.</span></span><br/> <dl> <span data-ttu-id="6f8f5-220">Windows XP e versioni successive,</span><span class="sxs-lookup"><span data-stu-id="6f8f5-220">Windows XP and later,</span></span><br />
<span data-ttu-id="6f8f5-221">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-221">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f8f5-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span><span class="sxs-lookup"><span data-stu-id="6f8f5-222"><a href="mfpkey-zerobyteframesproperty.md">MFPKEY_ZEROBYTEFRAMES</a></span></span></td>
<td><span data-ttu-id="6f8f5-223">Specifica il numero di fotogrammi video ignorati perché erano duplicati dei frame precedenti.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-223">Specifies the number of video frames that were skipped because they were duplicates of previous frames.</span></span><br/> <dl> <span data-ttu-id="6f8f5-224">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-224">Windows XP and later.</span></span><br />
<span data-ttu-id="6f8f5-225">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-225">Read-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6f8f5-226">Commenti</span><span class="sxs-lookup"><span data-stu-id="6f8f5-226">Remarks</span></span>

<span data-ttu-id="6f8f5-227">Un oggetto del codificatore di schermata espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="6f8f5-227">A screen encoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="6f8f5-228">Un codificatore dello schermo si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-228">A screen encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="6f8f5-229">Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore dello schermo si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-229">The following table shows the conditions under which a screen encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="6f8f5-230">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="6f8f5-230">Operating system</span></span>            | <span data-ttu-id="6f8f5-231">Comportamento del codificatore</span><span class="sxs-lookup"><span data-stu-id="6f8f5-231">Encoder behavior</span></span>                                                                                                                                    |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8f5-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6f8f5-232">Windows XP</span></span>                  | <span data-ttu-id="6f8f5-233">Un codificatore Windows Media Screen si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-233">A Windows Media Screen encoder always behaves as a DMO.</span></span>                                                                                             |
| <span data-ttu-id="6f8f5-234">Windows Vista e Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f8f5-234">Windows Vista and Windows 7</span></span> | <span data-ttu-id="6f8f5-235">Per impostazione predefinita, un codificatore Windows Media Screen si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-235">By default, a Windows Media Screen encoder behaves as a DMO.</span></span> <span data-ttu-id="6f8f5-236">Se si ottiene un'interfaccia **IMFTransform** su un codificatore di schermo, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="6f8f5-236">If you obtain an **IMFTransform** interface on a screen encoder, it behaves as an MFT.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6f8f5-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f8f5-237">Requirements</span></span>



| <span data-ttu-id="6f8f5-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f8f5-238">Requirement</span></span> | <span data-ttu-id="6f8f5-239">Valore</span><span class="sxs-lookup"><span data-stu-id="6f8f5-239">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f8f5-240">Client</span><span class="sxs-lookup"><span data-stu-id="6f8f5-240">Client</span></span><br/> | <span data-ttu-id="6f8f5-241">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="6f8f5-241">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="6f8f5-242">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f8f5-242">Header</span></span><br/> | <dl> <span data-ttu-id="6f8f5-243"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f8f5-243"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="6f8f5-244">DLL</span><span class="sxs-lookup"><span data-stu-id="6f8f5-244">DLL</span></span><br/>    | <dl> <span data-ttu-id="6f8f5-245"><dt>Wmvsencd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f8f5-245"><dt>Wmvsencd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f8f5-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f8f5-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f8f5-247">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="6f8f5-247">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="6f8f5-248">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="6f8f5-248">Codec Implementation</span></span>](codecimplementation.md)
</dt> <dt>

[<span data-ttu-id="6f8f5-249">Uso del codec della schermata Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6f8f5-249">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[<span data-ttu-id="6f8f5-250">Decodificatore dello schermo Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="6f8f5-250">Windows Media Video 9 Screen Decoder</span></span>](windowsmediavideo9screendecoder.md)
</dt> </dl>

 

 




