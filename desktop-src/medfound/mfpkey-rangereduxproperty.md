---
description: Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Proprietà MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec326e5d21a72792aab38f08d8c8c9207ab867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310619"
---
# <a name="mfpkey_rangeredux-property"></a><span data-ttu-id="b65ff-103">\_Proprietà RANGEREDUX di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="b65ff-103">MFPKEY\_RANGEREDUX Property</span></span>

<span data-ttu-id="b65ff-104">Specifica il livello in cui il codec deve ridurre l'intervallo di colori effettivo del video.</span><span class="sxs-lookup"><span data-stu-id="b65ff-104">Specifies the degree to which the codec should reduce the effective color range of the video.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b65ff-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b65ff-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b65ff-106">g \_ wszWMVCRangeRedux</span><span class="sxs-lookup"><span data-stu-id="b65ff-106">g\_wszWMVCRangeRedux</span></span>

## <a name="data-type"></a><span data-ttu-id="b65ff-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b65ff-107">Data Type</span></span>

<span data-ttu-id="b65ff-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="b65ff-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="b65ff-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="b65ff-109">Default Value</span></span>

<span data-ttu-id="b65ff-110">0</span><span class="sxs-lookup"><span data-stu-id="b65ff-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="b65ff-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b65ff-111">Remarks</span></span>

<span data-ttu-id="b65ff-112">Riduzione intervallo specifica il grado di riduzione del video da parte del codec.</span><span class="sxs-lookup"><span data-stu-id="b65ff-112">Range reduction specifies the degree to which the codec should reduce luma and chroma range of the video.</span></span> <span data-ttu-id="b65ff-113">Riducendo l'intervallo si riducono le dimensioni dei fotogrammi video codificati, ma si riducono anche i dettagli di colore del video.</span><span class="sxs-lookup"><span data-stu-id="b65ff-113">Reducing range reduces the size of encoded video frames but also reduces the color detail of the video.</span></span>

<span data-ttu-id="b65ff-114">La riduzione dell'intervallo è costituita dalla riduzione durante la codifica e dall'espansione durante la decodifica.</span><span class="sxs-lookup"><span data-stu-id="b65ff-114">Range reduction consists of reduction during encoding and expansion during decoding.</span></span> <span data-ttu-id="b65ff-115">È possibile rendere i fattori di espansione diversi dai fattori di riduzione, ma ciò non è consigliabile nella maggior parte degli scenari in cui è utile il rimapping degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="b65ff-115">It is possible to make the expansion factors different than the reduction factors, but this is not recommended in most scenarios where range remapping is useful.</span></span>

<span data-ttu-id="b65ff-116">La riduzione e l'espansione dell'intervallo vengono eseguite separatamente sui canali luma e Chroma.</span><span class="sxs-lookup"><span data-stu-id="b65ff-116">Range reduction and expansion is performed separately on luma and chroma channels.</span></span> <span data-ttu-id="b65ff-117">La riduzione dell'intervallo può essere un modo efficiente per ridurre la complessità del video a bassa velocità senza sacrificare i dettagli dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b65ff-117">Reducing range can be an efficient way to reduce the complexity of low bit-rate video without sacrificing image detail.</span></span> <span data-ttu-id="b65ff-118">Impostando tutti e quattro i valori su 8 si riduce la quantità di dati luma e Chroma per metà, lasciando più bit da indirizzare per mantenere i dettagli dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="b65ff-118">Setting all four values to 8 reduces the amount of luma and chroma information by half, leaving more bits to be directed to preserving image detail.</span></span>

<span data-ttu-id="b65ff-119">Il codec può scegliere di utilizzare automaticamente la riduzione intervallo quando si codifica il video con velocità in bit molto bassa.</span><span class="sxs-lookup"><span data-stu-id="b65ff-119">The codec can choose to automatically use range reduction when encoding video at very low bit-rates.</span></span> <span data-ttu-id="b65ff-120">L'impostazione di tutti e quattro i valori su 0 Disabilita completamente la riduzione dell'intervallo anche negli scenari a bassa velocità.</span><span class="sxs-lookup"><span data-stu-id="b65ff-120">Setting all four values to 0 completely disables range reduction even in low bit-rate scenarios.</span></span>

<span data-ttu-id="b65ff-121">Riducendo l'intervallo di colori si riducono le dimensioni codificate dei fotogrammi video, ma è possibile introdurre sfocatura nei frame decodificati.</span><span class="sxs-lookup"><span data-stu-id="b65ff-121">Reducing the color range reduces the encoded size of video frames but can introduce blurriness in the decoded frames.</span></span>

<span data-ttu-id="b65ff-122">Se questa proprietà non è impostata, il codec determina se utilizzare la riduzione intervallo al momento della codifica.</span><span class="sxs-lookup"><span data-stu-id="b65ff-122">If this property is not set, the codec determines whether to use range reduction at encoding time.</span></span> <span data-ttu-id="b65ff-123">Questa opzione è in genere selezionata dal codec solo a velocità in bit ridotte.</span><span class="sxs-lookup"><span data-stu-id="b65ff-123">Typically this option is selected by the codec only at low bit rates.</span></span>

<span data-ttu-id="b65ff-124">Il valore di questa proprietà è costituito da una combinazione di quattro componenti, separati da zeri, formattati come 0x0M0m0N0n, in cui:</span><span class="sxs-lookup"><span data-stu-id="b65ff-124">The value of this property is a combination of four components, separated by zeros, formatted as 0x0M0m0N0n, where:</span></span>

-   <span data-ttu-id="b65ff-125">M è il fattore di riduzione dell'intervallo di codifica per il componente Y.</span><span class="sxs-lookup"><span data-stu-id="b65ff-125">M is the encoding range reduction factor for the Y component.</span></span>
-   <span data-ttu-id="b65ff-126">m è il fattore di espansione dell'intervallo di decodifica per il componente Y, in genere uguale a M.</span><span class="sxs-lookup"><span data-stu-id="b65ff-126">m is the decoding range expansion factor for the Y component (usually the same as M).</span></span>
-   <span data-ttu-id="b65ff-127">N è il fattore di riduzione dell'intervallo di codifica per il componente UV.</span><span class="sxs-lookup"><span data-stu-id="b65ff-127">N is the encoding range reduction factor for the UV component.</span></span>
-   <span data-ttu-id="b65ff-128">n è il fattore di espansione dell'intervallo di decodifica per il componente UV (in genere uguale a N).</span><span class="sxs-lookup"><span data-stu-id="b65ff-128">n is the decoding range expansion factor for the UV component (usually the same as N).</span></span>

<span data-ttu-id="b65ff-129">Ogni fattore è una cifra da 0 a 8, dove 0 non è alcuna riduzione o espansione e 8 è la riduzione o l'espansione massima.</span><span class="sxs-lookup"><span data-stu-id="b65ff-129">Each factor is a digit from 0 to 8, where 0 is no reduction or expansion and 8 is the maximum reduction or expansion.</span></span>

<span data-ttu-id="b65ff-130">Se si imposta il valore su 0x00000000, la riduzione dell'intervallo è completamente disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b65ff-130">If you set the value to 0x00000000, range reduction is completely disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65ff-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65ff-131">Requirements</span></span>



| <span data-ttu-id="b65ff-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65ff-132">Requirement</span></span> | <span data-ttu-id="b65ff-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b65ff-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b65ff-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65ff-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b65ff-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b65ff-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b65ff-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b65ff-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b65ff-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b65ff-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b65ff-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b65ff-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b65ff-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b65ff-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65ff-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b65ff-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65ff-141">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b65ff-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




