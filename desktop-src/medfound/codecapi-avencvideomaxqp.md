---
description: Specifica il numero massimo di QP supportato dal codificatore.
ms.assetid: 2C02F82B-E645-4C5B-9526-5E130A6E2F67
title: Proprietà CODECAPI_AVEncVideoMaxQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bcf23866da5530d2edc1203be359071e5e33e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305488"
---
# <a name="codecapi_avencvideomaxqp-property"></a><span data-ttu-id="c7ce6-103">Proprietà AVEncVideoMaxQP di codecapi \_</span><span class="sxs-lookup"><span data-stu-id="c7ce6-103">CODECAPI\_AVEncVideoMaxQP property</span></span>

<span data-ttu-id="c7ce6-104">Specifica il numero massimo di QP supportato dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="c7ce6-104">Specifies the maximum QP supported by the encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7ce6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c7ce6-105">Data type</span></span>

<span data-ttu-id="c7ce6-106">**ULONG** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="c7ce6-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c7ce6-107">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="c7ce6-107">Property GUID</span></span>

<span data-ttu-id="c7ce6-108">**Codecapis \_ AVEncVideoMaxQP**</span><span class="sxs-lookup"><span data-stu-id="c7ce6-108">**CODECAPI\_AVEncVideoMaxQP**</span></span>

## <a name="remarks"></a><span data-ttu-id="c7ce6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7ce6-109">Remarks</span></span>

<span data-ttu-id="c7ce6-110">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="c7ce6-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="c7ce6-111">Il codificatore deve supportare [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)e [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="c7ce6-111">The encoder shall support [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="c7ce6-112">Si tratta di una proprietà statica che significa che può essere impostata solo prima dell'avvio della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="c7ce6-112">This is a static property meaning that it can only be set before the encoding session starts.</span></span>

<span data-ttu-id="c7ce6-113">Il valore predefinito deve essere il numero massimo di QP consentito dallo standard di codifica corrispondente.</span><span class="sxs-lookup"><span data-stu-id="c7ce6-113">Default value shall be the max QP allowed by the corresponding coding standard.</span></span> <span data-ttu-id="c7ce6-114">Ad esempio, i codificatori H. 264 avranno un valore predefinito di 51.</span><span class="sxs-lookup"><span data-stu-id="c7ce6-114">For example, H.264 encoders shall have a default value of 51.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7ce6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7ce6-115">Requirements</span></span>



| <span data-ttu-id="c7ce6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7ce6-116">Requirement</span></span> | <span data-ttu-id="c7ce6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c7ce6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ce6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7ce6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7ce6-119">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7ce6-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="c7ce6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7ce6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7ce6-121">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7ce6-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c7ce6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7ce6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7ce6-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7ce6-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7ce6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7ce6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ce6-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7ce6-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="c7ce6-126">Codecapis \_ AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="c7ce6-126">CODECAPI\_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
</dt> </dl>

 

