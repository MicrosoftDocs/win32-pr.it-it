---
description: Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: Proprietà MFPKEY_BDELTAQP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba1ca7d30e17841badeda0312f77471116a8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311584"
---
# <a name="mfpkey_bdeltaqp-property"></a><span data-ttu-id="c33fa-103">\_Proprietà BDELTAQP di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c33fa-103">MFPKEY\_BDELTAQP Property</span></span>

<span data-ttu-id="c33fa-104">Specifica l'incremento Delta tra il quantizzatore immagine del frame di ancoraggio e il quantizzatore dell'immagine del fotogramma B.</span><span class="sxs-lookup"><span data-stu-id="c33fa-104">Specifies the delta increase between the picture quantizer of the anchor frame and the picture quantizer of the B-frame.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c33fa-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c33fa-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c33fa-106">g \_ wszWMVCBDeltaQP</span><span class="sxs-lookup"><span data-stu-id="c33fa-106">g\_wszWMVCBDeltaQP</span></span>

## <a name="data-type"></a><span data-ttu-id="c33fa-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c33fa-107">Data Type</span></span>

<span data-ttu-id="c33fa-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c33fa-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c33fa-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c33fa-109">Default Value</span></span>

<span data-ttu-id="c33fa-110">0</span><span class="sxs-lookup"><span data-stu-id="c33fa-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="c33fa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c33fa-111">Remarks</span></span>

<span data-ttu-id="c33fa-112">Il quantizzatore immagini (QP) è una misurazione della modalità di compressione di un frame.</span><span class="sxs-lookup"><span data-stu-id="c33fa-112">Picture quantizer (QP) is a measurement of how compressed a frame is.</span></span> <span data-ttu-id="c33fa-113">I valori più alti rappresentano rapporti di compressione più elevati.</span><span class="sxs-lookup"><span data-stu-id="c33fa-113">Higher values represent higher compression ratios.</span></span> <span data-ttu-id="c33fa-114">Il QP può essere impostato con incrementi di due punti.</span><span class="sxs-lookup"><span data-stu-id="c33fa-114">The QP can be set in half-point increments.</span></span> <span data-ttu-id="c33fa-115">Un frame B viene in genere compresso in un QP uguale a o 0,5 superiore rispetto al QP del frame di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="c33fa-115">A B-frame is typically compressed at a QP the same as or 0.5 higher than the anchor frame's QP.</span></span> <span data-ttu-id="c33fa-116">Specificando un Delta QP con frame B maggiore di 0, è possibile comprimere i fotogrammi B a un rapporto di compressione ancora superiore.</span><span class="sxs-lookup"><span data-stu-id="c33fa-116">By specifying a B-frame QP delta higher than 0, it is possible to compress B-frames at an even higher compression ratio.</span></span>

<span data-ttu-id="c33fa-117">È possibile impostare la QP Delta del frame B solo in incrementi completi.</span><span class="sxs-lookup"><span data-stu-id="c33fa-117">The B-frame delta QP can be set only in whole-point increments.</span></span> <span data-ttu-id="c33fa-118">Questa proprietà deve essere impostata su un valore intero compreso tra 0 e 31.</span><span class="sxs-lookup"><span data-stu-id="c33fa-118">This property must be set to an integer value from 0 to 31.</span></span> <span data-ttu-id="c33fa-119">Il valore consigliato è 1.</span><span class="sxs-lookup"><span data-stu-id="c33fa-119">The recommended value is 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c33fa-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c33fa-120">Requirements</span></span>



| <span data-ttu-id="c33fa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c33fa-121">Requirement</span></span> | <span data-ttu-id="c33fa-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c33fa-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c33fa-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c33fa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c33fa-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c33fa-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c33fa-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c33fa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c33fa-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c33fa-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c33fa-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c33fa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c33fa-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c33fa-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c33fa-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c33fa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c33fa-130">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c33fa-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




