---
description: Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Proprietà AVEncDDProductionInfoExists (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304227"
---
# <a name="avencddproductioninfoexists-property"></a><span data-ttu-id="8b332-104">Proprietà AVEncDDProductionInfoExists</span><span class="sxs-lookup"><span data-stu-id="8b332-104">AVEncDDProductionInfoExists property</span></span>

<span data-ttu-id="8b332-105">Specifica il flag di informazioni di produzione audio in un flusso audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="8b332-105">Specifies the audio production information flag in a Dolby Digital audio stream.</span></span> <span data-ttu-id="8b332-106">Questa proprietà si applica ai codificatori audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="8b332-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="8b332-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8b332-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b332-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8b332-108">Data type</span></span>

<span data-ttu-id="8b332-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="8b332-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8b332-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="8b332-110">Property GUID</span></span>

<span data-ttu-id="8b332-111">**Codecapis \_ AVEncDDProductionInfoExists**</span><span class="sxs-lookup"><span data-stu-id="8b332-111">**CODECAPI\_AVEncDDProductionInfoExists**</span></span>

## <a name="remarks"></a><span data-ttu-id="8b332-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b332-112">Remarks</span></span>

<span data-ttu-id="8b332-113">Se il valore è **Variant \_ true**, le impostazioni del livello di combinazione e del tipo di chat sono valide.</span><span class="sxs-lookup"><span data-stu-id="8b332-113">If the value is **VARIANT\_TRUE**, the mixing level and room type settings are valid.</span></span> <span data-ttu-id="8b332-114">Specificare queste impostazioni con le proprietà [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) e [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) .</span><span class="sxs-lookup"><span data-stu-id="8b332-114">Specify these settings with the [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) and [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b332-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b332-115">Requirements</span></span>



| <span data-ttu-id="8b332-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b332-116">Requirement</span></span> | <span data-ttu-id="8b332-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8b332-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b332-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b332-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b332-119">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="8b332-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8b332-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b332-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b332-121">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b332-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8b332-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b332-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b332-123"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b332-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b332-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b332-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b332-125">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="8b332-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8b332-126">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8b332-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




