---
description: Specifica se il codec utilizzerà il filtro rumore durante la codifica.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: Proprietà MFPKEY_DENOISEOPTION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310636"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="ad742-103">\_Proprietà DENOISEOPTION di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="ad742-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="ad742-104">Specifica se il codec utilizzerà il filtro rumore durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="ad742-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ad742-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ad742-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="ad742-106">g \_ wszWMVCDenoiseOption</span><span class="sxs-lookup"><span data-stu-id="ad742-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="ad742-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad742-107">Data Type</span></span>

<span data-ttu-id="ad742-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="ad742-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="ad742-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="ad742-109">Default Value</span></span>

<span data-ttu-id="ad742-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="ad742-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="ad742-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad742-111">Remarks</span></span>

<span data-ttu-id="ad742-112">Il filtro rumore può migliorare la qualità delle origini video rumorose, ad esempio film che contengono un numero elevato di granularità o video in basso.</span><span class="sxs-lookup"><span data-stu-id="ad742-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="ad742-113">Questo filtro può essere usato negli scenari di codifica live in cui la pre-elaborazione esterna non è un'opzione.</span><span class="sxs-lookup"><span data-stu-id="ad742-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="ad742-114">Questo filtro deve essere disabilitato per le origini video pulite perché può ridurre la qualità dell'immagine quando la qualità è ottima per iniziare.</span><span class="sxs-lookup"><span data-stu-id="ad742-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad742-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad742-115">Requirements</span></span>



| <span data-ttu-id="ad742-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad742-116">Requirement</span></span> | <span data-ttu-id="ad742-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ad742-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad742-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad742-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad742-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ad742-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ad742-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad742-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad742-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ad742-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad742-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad742-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad742-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad742-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad742-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad742-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad742-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad742-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




