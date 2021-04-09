---
description: Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: Proprietà MFPKEY_FOURCC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967170"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="030f1-103">\_Proprietà FourCC di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="030f1-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="030f1-104">Specifica il FOURCC che identifica il codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="030f1-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="030f1-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="030f1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="030f1-106">g \_ wszWMVCFOURCC</span><span class="sxs-lookup"><span data-stu-id="030f1-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="030f1-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="030f1-107">Data Type</span></span>

<span data-ttu-id="030f1-108">VT \_ I4 (valore fourcc)</span><span class="sxs-lookup"><span data-stu-id="030f1-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="030f1-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="030f1-109">Remarks</span></span>

<span data-ttu-id="030f1-110">È necessario impostare questo valore prima di recuperare i valori per le proprietà seguenti utilizzando **IPropertyBag** o **IPropertyStore**:</span><span class="sxs-lookup"><span data-stu-id="030f1-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="030f1-111">\_BUFFERFULLNESSINFIRSTBYTE MFPKEY</span><span class="sxs-lookup"><span data-stu-id="030f1-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="030f1-112">\_PASSESRECOMMENDED MFPKEY</span><span class="sxs-lookup"><span data-stu-id="030f1-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="030f1-113">Usare [**IWMCodecProps:: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) per recuperare i valori delle proprietà dipendenti da FourCC elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="030f1-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="030f1-114">Quando si usa **GetCodecProp**, non è necessario impostare **MFPKEY \_ fourcc**.</span><span class="sxs-lookup"><span data-stu-id="030f1-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="030f1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="030f1-115">Requirements</span></span>



| <span data-ttu-id="030f1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="030f1-116">Requirement</span></span> | <span data-ttu-id="030f1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="030f1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="030f1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="030f1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="030f1-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="030f1-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="030f1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="030f1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="030f1-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="030f1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="030f1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="030f1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="030f1-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="030f1-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="030f1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="030f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="030f1-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="030f1-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




