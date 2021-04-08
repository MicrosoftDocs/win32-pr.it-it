---
description: Specifica il numero di fotogrammi video ignorati perché sono duplicati dei frame precedenti.
ms.assetid: ef4aa5a0-3788-493e-b541-c3a24509d939
title: Proprietà MFPKEY_ZEROBYTEFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffcf29d099b3a3fb27a307e970af7af1a5c3d58b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880077"
---
# <a name="mfpkey_zerobyteframes-property"></a><span data-ttu-id="7ce2b-103">\_Proprietà ZEROBYTEFRAMES di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="7ce2b-103">MFPKEY\_ZEROBYTEFRAMES Property</span></span>

<span data-ttu-id="7ce2b-104">Specifica il numero di fotogrammi video ignorati perché sono duplicati dei frame precedenti.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-104">Specifies the number of video frames that are skipped because they were duplicates of previous frames.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7ce2b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="7ce2b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7ce2b-106">g \_ wszWMVCZeroByteFrames</span><span class="sxs-lookup"><span data-stu-id="7ce2b-106">g\_wszWMVCZeroByteFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="7ce2b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7ce2b-107">Data Type</span></span>

<span data-ttu-id="7ce2b-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7ce2b-108">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="7ce2b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ce2b-109">Remarks</span></span>

<span data-ttu-id="7ce2b-110">Questo valore non viene sottratto dal numero totale di frame passati ([MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md)) durante il calcolo del numero di frame codificati ([MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="7ce2b-110">This value is not subtracted from the total number of frames passed ([MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md)) when calculating the number of encoded frames ([MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md)).</span></span>

<span data-ttu-id="7ce2b-111">È possibile arrestare il codec ignorando i frame duplicati impostando [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-111">You can stop the codec from skipping duplicate frames by setting [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE.</span></span>

<span data-ttu-id="7ce2b-112">È possibile ottenere questo valore al termine del passaggio degli esempi.</span><span class="sxs-lookup"><span data-stu-id="7ce2b-112">You can get this value after you are finished passing samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ce2b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ce2b-113">Requirements</span></span>



| <span data-ttu-id="7ce2b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce2b-114">Requirement</span></span> | <span data-ttu-id="7ce2b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7ce2b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce2b-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce2b-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7ce2b-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7ce2b-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce2b-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7ce2b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7ce2b-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ce2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ce2b-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ce2b-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ce2b-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ce2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce2b-123">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7ce2b-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




