---
description: Specifica la fine di un passaggio di codifica.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Proprietà MFPKEY_ENDOFPASS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880806"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="72b37-103">\_Proprietà ENDOFPASS di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="72b37-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="72b37-104">Specifica la fine di un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="72b37-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="72b37-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="72b37-105">Data Type</span></span>

<span data-ttu-id="72b37-106">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="72b37-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="72b37-107">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="72b37-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="72b37-108">g \_ wszWMVCEndOfPass</span><span class="sxs-lookup"><span data-stu-id="72b37-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="72b37-109">Tipo di dati per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="72b37-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="72b37-110">Nessun tipo di dati richiesto.</span><span class="sxs-lookup"><span data-stu-id="72b37-110">No data type is required.</span></span> <span data-ttu-id="72b37-111">Per impostare questa proprietà, passare una **variante** non inizializzata.</span><span class="sxs-lookup"><span data-stu-id="72b37-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b37-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="72b37-112">Remarks</span></span>

<span data-ttu-id="72b37-113">Questa proprietà non è una proprietà normale perché ha lo stesso effetto indipendentemente dal fatto che il valore sia VARIANT \_ true o Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="72b37-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="72b37-114">È necessario impostare questa proprietà dopo l'elaborazione degli ultimi esempi di input per un passaggio di pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="72b37-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="72b37-115">Se si eseguono più sessioni, è necessario impostare questa proprietà alla fine di ogni passaggio di pre-elaborazione (al momento nessuno dei codec supporta più di uno).</span><span class="sxs-lookup"><span data-stu-id="72b37-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="72b37-116">Se non si imposta questa proprietà, il codec presuppone che si stiano ancora passando esempi per la pre-elaborazione.</span><span class="sxs-lookup"><span data-stu-id="72b37-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b37-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72b37-117">Requirements</span></span>



| <span data-ttu-id="72b37-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b37-118">Requirement</span></span> | <span data-ttu-id="72b37-119">Valore</span><span class="sxs-lookup"><span data-stu-id="72b37-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72b37-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72b37-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72b37-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72b37-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="72b37-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72b37-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72b37-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72b37-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72b37-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72b37-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b37-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b37-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b37-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72b37-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b37-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72b37-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




