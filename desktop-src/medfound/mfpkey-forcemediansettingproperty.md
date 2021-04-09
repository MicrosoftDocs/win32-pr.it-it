---
description: Specifica se il codec deve usare il filtro mediano durante la codifica.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Proprietà MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886005"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="9e5e2-103">\_Proprietà FORCEMEDIANSETTING di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="9e5e2-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="9e5e2-104">Specifica se il codec deve usare il filtro mediano durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9e5e2-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9e5e2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9e5e2-106">g \_ wszWMVCForceMedianSetting</span><span class="sxs-lookup"><span data-stu-id="9e5e2-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="9e5e2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9e5e2-107">Data Type</span></span>

<span data-ttu-id="9e5e2-108">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="9e5e2-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="9e5e2-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="9e5e2-109">Default Value</span></span>

<span data-ttu-id="9e5e2-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="9e5e2-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5e2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e5e2-111">Remarks</span></span>

<span data-ttu-id="9e5e2-112">Il filtro mediano indica al codec di ignorare il rumore e la granularità durante il calcolo del movimento tra frame.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="9e5e2-113">Questo può migliorare la qualità dei video molto rumorosi, ma può condurre a percorsi di movimento (noti anche come artefatti finali) quando applicati a video di origine puliti.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="9e5e2-114">Per impostazione predefinita, il codec usa la logica interna per determinare se usare il filtro mediano.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="9e5e2-115">Se si imposta questa proprietà, la logica verrà sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="9e5e2-116">Questo filtro non corrisponde ai filtri di sfocatura mediani disponibili in molte applicazioni di modifica e post-elaborazione video.</span><span class="sxs-lookup"><span data-stu-id="9e5e2-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e5e2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e5e2-117">Requirements</span></span>



| <span data-ttu-id="9e5e2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5e2-118">Requirement</span></span> | <span data-ttu-id="9e5e2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9e5e2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5e2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e5e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5e2-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9e5e2-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9e5e2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e5e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5e2-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e5e2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e5e2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e5e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5e2-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5e2-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e5e2-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e5e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5e2-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e5e2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




