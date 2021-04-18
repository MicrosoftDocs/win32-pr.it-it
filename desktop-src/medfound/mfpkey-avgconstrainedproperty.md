---
description: Specifica se il codificatore usa la codifica VBR media controllabile.
ms.assetid: 2c150eb1-4ffe-4f77-8ef8-e3bf29b17b10
title: Proprietà MFPKEY_AVGCONSTRAINED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0623fb4a73e3721f9079f2a1e5e330ecb466a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306753"
---
# <a name="mfpkey_avgconstrained-property"></a><span data-ttu-id="54c5c-103">\_Proprietà AVGCONSTRAINED di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="54c5c-103">MFPKEY\_AVGCONSTRAINED Property</span></span>

<span data-ttu-id="54c5c-104">Specifica se il codificatore usa la codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="54c5c-104">Specifies whether the encoder uses average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="54c5c-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="54c5c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="54c5c-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="54c5c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="54c5c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="54c5c-107">Data Type</span></span>

<span data-ttu-id="54c5c-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="54c5c-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="54c5c-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="54c5c-109">Default Value</span></span>

<span data-ttu-id="54c5c-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="54c5c-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="54c5c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="54c5c-111">Remarks</span></span>

<span data-ttu-id="54c5c-112">Se questa proprietà e la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **Variant \_ true**, il codificatore usa la codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="54c5c-112">If this property and the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="54c5c-113">In tal caso, il codificatore viene configurato in base ai valori di [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) e [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span><span class="sxs-lookup"><span data-stu-id="54c5c-113">In that case, the encoder configures itself according to the values of [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) and [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="54c5c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54c5c-114">Requirements</span></span>



| <span data-ttu-id="54c5c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="54c5c-115">Requirement</span></span> | <span data-ttu-id="54c5c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="54c5c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54c5c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54c5c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54c5c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54c5c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54c5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54c5c-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54c5c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54c5c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54c5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="54c5c-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="54c5c-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54c5c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54c5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54c5c-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54c5c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
