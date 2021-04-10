---
description: Specifica il numero massimo di frame di riferimento supportati dal codificatore.
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: Proprietà CODECAPI_AVEncVideoMaxNumRefFrame (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132162"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a><span data-ttu-id="516f6-103">Proprietà AVEncVideoMaxNumRefFrame di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="516f6-103">CODECAPI\_AVEncVideoMaxNumRefFrame property</span></span>

<span data-ttu-id="516f6-104">Specifica il numero massimo di frame di riferimento supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="516f6-104">Specifies the maximum reference frames supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="516f6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="516f6-105">Data type</span></span>

<span data-ttu-id="516f6-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="516f6-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="516f6-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="516f6-107">Property GUID</span></span>

<span data-ttu-id="516f6-108">**Codecapis \_ AVEncVideoMaxNumRefFrame**</span><span class="sxs-lookup"><span data-stu-id="516f6-108">**CODECAPI\_AVEncVideoMaxNumRefFrame**</span></span>

## <a name="remarks"></a><span data-ttu-id="516f6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="516f6-109">Remarks</span></span>

<span data-ttu-id="516f6-110">Per H. 264, viene eseguito il mapping alla variabile del set di parametri Sequence **Max \_ num \_ \_ frame Ref** come definito nella specifica H. 264.</span><span class="sxs-lookup"><span data-stu-id="516f6-110">For H.264, this maps to the Sequence Parameter Set variable **max\_num\_ref\_frames** as defined in H.264 specification.</span></span>

<span data-ttu-id="516f6-111">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="516f6-111">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="516f6-112">I codificatori possono usare un minor numero di frame di riferimento per rispettare il livello specificato nel bitstream.</span><span class="sxs-lookup"><span data-stu-id="516f6-112">Encoders may use fewer reference frames in order to obey the level specified in the bitstream.</span></span>

<span data-ttu-id="516f6-113">I codificatori devono supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="516f6-113">Encoders shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="516f6-114">Si tratta di una proprietà statica che significa che può essere impostata solo prima dell'avvio della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="516f6-114">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="516f6-115">Il valore predefinito consigliato è 2.</span><span class="sxs-lookup"><span data-stu-id="516f6-115">Recommended default value is 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="516f6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="516f6-116">Requirements</span></span>



| <span data-ttu-id="516f6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="516f6-117">Requirement</span></span> | <span data-ttu-id="516f6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="516f6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="516f6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="516f6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="516f6-120">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="516f6-120">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="516f6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="516f6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="516f6-122">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="516f6-122">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="516f6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="516f6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="516f6-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="516f6-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516f6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="516f6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516f6-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="516f6-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

