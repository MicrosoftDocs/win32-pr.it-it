---
description: Specifica il tipo di filtro di deenfasi da usare durante la decodifica. Questa proprietà si applica ai codificatori audio MPEG.
ms.assetid: 1c1f7ac0-48a1-46d6-a131-fe281f2c86ba
title: Proprietà AVEncMPAEmphasisType (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e00b424f8b70176a04385b52c6ca278cfc0a5c53
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304147"
---
# <a name="avencmpaemphasistype-property"></a><span data-ttu-id="2a135-104">Proprietà AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="2a135-104">AVEncMPAEmphasisType property</span></span>

<span data-ttu-id="2a135-105">Specifica il tipo di filtro di deenfasi da usare durante la decodifica.</span><span class="sxs-lookup"><span data-stu-id="2a135-105">Specifies the type of de-emphasis filter that should be used when decoding.</span></span> <span data-ttu-id="2a135-106">Questa proprietà si applica ai codificatori audio MPEG.</span><span class="sxs-lookup"><span data-stu-id="2a135-106">This property applies to MPEG audio encoders.</span></span>

<span data-ttu-id="2a135-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2a135-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a135-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a135-108">Data type</span></span>

<span data-ttu-id="2a135-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2a135-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2a135-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="2a135-110">Property GUID</span></span>

<span data-ttu-id="2a135-111">**Codecapis \_ AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="2a135-111">**CODECAPI\_AVEncMPAEmphasisType**</span></span>

## <a name="property-value"></a><span data-ttu-id="2a135-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2a135-112">Property value</span></span>

<span data-ttu-id="2a135-113">Il valore di questa proprietà è un membro dell'enumerazione [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) .</span><span class="sxs-lookup"><span data-stu-id="2a135-113">The value of this property is a member of the [**eAVEncMPAEmphasisType**](/windows/win32/api/codecapi/ne-codecapi-eavencmpaemphasistype) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a135-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a135-114">Remarks</span></span>

<span data-ttu-id="2a135-115">Questa proprietà imposta i bit di enfasi nell'intestazione del frame.</span><span class="sxs-lookup"><span data-stu-id="2a135-115">This property sets the emphasis bits in the frame header.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a135-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a135-116">Requirements</span></span>



| <span data-ttu-id="2a135-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a135-117">Requirement</span></span> | <span data-ttu-id="2a135-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2a135-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a135-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a135-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a135-120">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2a135-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2a135-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a135-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a135-122">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a135-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2a135-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a135-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a135-124"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a135-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a135-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a135-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a135-126">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="2a135-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2a135-127">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2a135-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

