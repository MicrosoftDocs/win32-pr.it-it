---
description: Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.
ms.assetid: ce330ce0-4bda-4340-b21c-63a8b9168cf4
title: Proprietà MFPKEY_DYN_VBR_BAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e117c2852f660b015bcdd95224178730d2e2a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310632"
---
# <a name="mfpkey_dyn_vbr_bavg-property"></a><span data-ttu-id="c5050-103">MFPKEY \_ dyn \_ - \_ Proprietà BAVG VBR</span><span class="sxs-lookup"><span data-stu-id="c5050-103">MFPKEY\_DYN\_VBR\_BAVG Property</span></span>

<span data-ttu-id="c5050-104">Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="c5050-104">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c5050-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c5050-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c5050-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="c5050-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="c5050-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c5050-107">Data Type</span></span>

<span data-ttu-id="c5050-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="c5050-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="c5050-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5050-109">Remarks</span></span>

<span data-ttu-id="c5050-110">Se le proprietà [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **Variant \_ true**, il codificatore usa la codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="c5050-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="c5050-111">In tal caso, il codificatore viene configurato in base al valore di questa proprietà e alla proprietà [**MFPKEY \_ dyn \_ VBR \_ RAVG**](mfpkey-dyn-vbr-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="c5050-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_RAVG**](mfpkey-dyn-vbr-ravgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5050-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5050-112">Requirements</span></span>



| <span data-ttu-id="c5050-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5050-113">Requirement</span></span> | <span data-ttu-id="c5050-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c5050-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5050-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5050-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5050-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5050-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c5050-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5050-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5050-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5050-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5050-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5050-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5050-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5050-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5050-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5050-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5050-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5050-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
