---
description: Specifica il numero massimo di passaggi supportati dal codificatore.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: Proprietà MFPKEY_PASSESRECOMMENDED (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226999"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="ab7bd-103">\_Proprietà PASSESRECOMMENDED di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ab7bd-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="ab7bd-104">Specifica il numero massimo di passaggi supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="ab7bd-105">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="ab7bd-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ab7bd-106">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ab7bd-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="ab7bd-107">g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses</span><span class="sxs-lookup"><span data-stu-id="ab7bd-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="ab7bd-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ab7bd-108">Data Type</span></span>

<span data-ttu-id="ab7bd-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ab7bd-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="ab7bd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab7bd-110">Remarks</span></span>

<span data-ttu-id="ab7bd-111">È possibile ottenere il valore di questa proprietà chiamando [IWMCodecProps:: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="ab7bd-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="ab7bd-112">Se si usa **IPropertyBag**, è innanzitutto necessario impostare il valore fourcc del formato compresso desiderato usando la proprietà [MFPKEY \_ fourcc](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="ab7bd-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab7bd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab7bd-113">Requirements</span></span>



| <span data-ttu-id="ab7bd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab7bd-114">Requirement</span></span> | <span data-ttu-id="ab7bd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ab7bd-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab7bd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab7bd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab7bd-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ab7bd-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab7bd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab7bd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab7bd-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ab7bd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab7bd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab7bd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab7bd-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab7bd-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab7bd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab7bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab7bd-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab7bd-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




