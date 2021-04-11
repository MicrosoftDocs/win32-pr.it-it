---
description: Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.
ms.assetid: d689a34c-97f7-4b1c-82b6-863ce3b8403f
title: Proprietà MFPKEY_DYN_VBR_RAVG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8103d36db5a9e946449231943e076c26258eec19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967172"
---
# <a name="mfpkey_dyn_vbr_ravg-property"></a><span data-ttu-id="b2233-103">MFPKEY \_ dyn \_ - \_ Proprietà RAVG VBR</span><span class="sxs-lookup"><span data-stu-id="b2233-103">MFPKEY\_DYN\_VBR\_RAVG Property</span></span>

<span data-ttu-id="b2233-104">Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="b2233-104">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="b2233-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="b2233-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="b2233-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="b2233-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="b2233-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b2233-107">Data Type</span></span>

<span data-ttu-id="b2233-108">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b2233-108">**VT\_I4**</span></span>

## <a name="remarks"></a><span data-ttu-id="b2233-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2233-109">Remarks</span></span>

<span data-ttu-id="b2233-110">Se le proprietà [**MFPKEY \_ AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) e [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) sono entrambe impostate su **Variant \_ true**, il codificatore usa la codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="b2233-110">If the [**MFPKEY\_AVGCONSTRAINED**](mfpkey-avgconstrainedproperty.md) and [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) properties are both set to **VARIANT\_TRUE**, the encoder uses average-controllable VBR encoding.</span></span> <span data-ttu-id="b2233-111">In tal caso, il codificatore viene configurato in base al valore di questa proprietà e alla proprietà [**MFPKEY \_ dyn \_ VBR \_ BAVG**](mfpkey-dyn-vbr-bavgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="b2233-111">In that case, the encoder configures itself according to the value of this property and the [**MFPKEY\_DYN\_VBR\_BAVG**](mfpkey-dyn-vbr-bavgproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2233-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2233-112">Requirements</span></span>



| <span data-ttu-id="b2233-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2233-113">Requirement</span></span> | <span data-ttu-id="b2233-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b2233-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2233-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2233-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b2233-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2233-116">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2233-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2233-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b2233-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2233-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2233-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2233-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2233-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2233-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2233-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2233-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2233-122">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2233-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
