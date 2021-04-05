---
description: Specifica il tipo di stanza per un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Proprietà AVEncDDProductionRoomType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125199"
---
# <a name="avencddproductionroomtype-property"></a><span data-ttu-id="54e25-104">Proprietà AVEncDDProductionRoomType</span><span class="sxs-lookup"><span data-stu-id="54e25-104">AVEncDDProductionRoomType property</span></span>

<span data-ttu-id="54e25-105">Specifica il tipo di stanza per un flusso audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="54e25-105">Specifies the room type for a Dolby Digital audio stream.</span></span> <span data-ttu-id="54e25-106">Questa proprietà si applica ai codificatori audio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="54e25-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="54e25-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="54e25-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="54e25-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="54e25-108">Data type</span></span>

<span data-ttu-id="54e25-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="54e25-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="54e25-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="54e25-110">Property GUID</span></span>

<span data-ttu-id="54e25-111">**Codecapis \_ AVEncDDProductionRoomType**</span><span class="sxs-lookup"><span data-stu-id="54e25-111">**CODECAPI\_AVEncDDProductionRoomType**</span></span>

## <a name="property-value"></a><span data-ttu-id="54e25-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="54e25-112">Property value</span></span>

<span data-ttu-id="54e25-113">Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) .</span><span class="sxs-lookup"><span data-stu-id="54e25-113">The value of this property is a member of the [**eAVEncDDProductionRoomType**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e25-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="54e25-114">Remarks</span></span>

<span data-ttu-id="54e25-115">Il *tipo di chat room* si riferisce alle dimensioni della stanza utilizzata durante la produzione.</span><span class="sxs-lookup"><span data-stu-id="54e25-115">*Room type* refers to the size of the room used during production.</span></span> <span data-ttu-id="54e25-116">Se si imposta questa proprietà, impostare la proprietà [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="54e25-116">If you set this property, set the [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) property to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e25-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54e25-117">Requirements</span></span>



| <span data-ttu-id="54e25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e25-118">Requirement</span></span> | <span data-ttu-id="54e25-119">Valore</span><span class="sxs-lookup"><span data-stu-id="54e25-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54e25-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54e25-121">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="54e25-121">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="54e25-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54e25-123">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="54e25-123">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="54e25-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54e25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e25-125"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e25-125"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e25-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54e25-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e25-127">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="54e25-127">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="54e25-128">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="54e25-128">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

