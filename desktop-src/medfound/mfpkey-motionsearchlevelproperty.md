---
description: Specifica il modo in cui le informazioni sui colori vengono usate nelle operazioni di ricerca di movimento.
ms.assetid: a625b103-0a55-4268-a01a-6a464a56fec2
title: Proprietà MFPKEY_MOTIONSEARCHLEVEL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 231c2c0ae70466d41f4bf348ec47ee0a74cb135b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049838"
---
# <a name="mfpkey_motionsearchlevel-property"></a><span data-ttu-id="663bd-103">\_Proprietà MOTIONSEARCHLEVEL di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="663bd-103">MFPKEY\_MOTIONSEARCHLEVEL Property</span></span>

<span data-ttu-id="663bd-104">Specifica il modo in cui le informazioni sui colori vengono usate nelle operazioni di ricerca di movimento.</span><span class="sxs-lookup"><span data-stu-id="663bd-104">Specifies how color information is used in motion search operations.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="663bd-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="663bd-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="663bd-106">g \_ wszWMVCMotionSearchLevel</span><span class="sxs-lookup"><span data-stu-id="663bd-106">g\_wszWMVCMotionSearchLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="663bd-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="663bd-107">Data Type</span></span>

<span data-ttu-id="663bd-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="663bd-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="663bd-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="663bd-109">Default Value</span></span>

<span data-ttu-id="663bd-110">0</span><span class="sxs-lookup"><span data-stu-id="663bd-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="663bd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="663bd-111">Remarks</span></span>

<span data-ttu-id="663bd-112">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="663bd-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="663bd-113">Valore</span><span class="sxs-lookup"><span data-stu-id="663bd-113">Value</span></span> | <span data-ttu-id="663bd-114">Informazioni video utilizzate</span><span class="sxs-lookup"><span data-stu-id="663bd-114">Video information used</span></span>                           |
|-------|--------------------------------------------------|
| <span data-ttu-id="663bd-115">0</span><span class="sxs-lookup"><span data-stu-id="663bd-115">0</span></span>     | <span data-ttu-id="663bd-116">Solo luminanza.</span><span class="sxs-lookup"><span data-stu-id="663bd-116">Luma only.</span></span>                                       |
| <span data-ttu-id="663bd-117">1</span><span class="sxs-lookup"><span data-stu-id="663bd-117">1</span></span>     | <span data-ttu-id="663bd-118">Luma con Chroma integer più vicino.</span><span class="sxs-lookup"><span data-stu-id="663bd-118">Luma with nearest-integer chroma.</span></span>                |
| <span data-ttu-id="663bd-119">2</span><span class="sxs-lookup"><span data-stu-id="663bd-119">2</span></span>     | <span data-ttu-id="663bd-120">Luminanza con crominanza vera.</span><span class="sxs-lookup"><span data-stu-id="663bd-120">Luma with true chroma.</span></span>                           |
| <span data-ttu-id="663bd-121">-1</span><span class="sxs-lookup"><span data-stu-id="663bd-121">-1</span></span>    | <span data-ttu-id="663bd-122">Macroblocco-Adaptive con Chroma true.</span><span class="sxs-lookup"><span data-stu-id="663bd-122">Macroblock-adaptive with true chroma.</span></span>            |
| <span data-ttu-id="663bd-123">-2</span><span class="sxs-lookup"><span data-stu-id="663bd-123">-2</span></span>    | <span data-ttu-id="663bd-124">Macroblocco-Adaptive con Chroma integer più vicino.</span><span class="sxs-lookup"><span data-stu-id="663bd-124">Macroblock-adaptive with nearest-integer chroma.</span></span> |



 

<span data-ttu-id="663bd-125">Per impostazione predefinita, il codec esegue la ricerca di movimento solo nel canale luma.</span><span class="sxs-lookup"><span data-stu-id="663bd-125">By default, the codec performs motion search only in the luma channel.</span></span> <span data-ttu-id="663bd-126">Includere le informazioni sulla crominanza nella stima del movimento può migliorare significativamente la qualità del video codificato.</span><span class="sxs-lookup"><span data-stu-id="663bd-126">Including chroma information in motion estimation can significantly improve the quality of encoded video.</span></span> <span data-ttu-id="663bd-127">La ricerca di movimento con luma e la Croma vera produrrà la migliore qualità del video, ma con il costo massimo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="663bd-127">Motion search with luma and true chroma will yield the best video quality, but at the highest performance cost.</span></span> <span data-ttu-id="663bd-128">Le due modalità dinamiche (-1 e-2) e la Luma con la modalità Chroma con valori integer più vicino forniranno compromessi ragionevoli tra qualità e prestazioni.</span><span class="sxs-lookup"><span data-stu-id="663bd-128">The two dynamic modes (-1 and -2) and the luma with nearest-integer chroma mode will provide reasonable compromises between quality and performance.</span></span>

## <a name="requirements"></a><span data-ttu-id="663bd-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="663bd-129">Requirements</span></span>



| <span data-ttu-id="663bd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="663bd-130">Requirement</span></span> | <span data-ttu-id="663bd-131">Valore</span><span class="sxs-lookup"><span data-stu-id="663bd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="663bd-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="663bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="663bd-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="663bd-133">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="663bd-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="663bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="663bd-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="663bd-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="663bd-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="663bd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="663bd-137"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="663bd-137"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="663bd-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="663bd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="663bd-139">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="663bd-139">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




