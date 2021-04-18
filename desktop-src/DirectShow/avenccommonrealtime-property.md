---
description: Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.
ms.assetid: 7e98a9f4-113b-45d0-ae55-7dc3f2af099e
title: Proprietà AVEncCommonRealTime (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a03e51da1a088603273da3d083573e5921edf7a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304239"
---
# <a name="avenccommonrealtime-property"></a><span data-ttu-id="a5d1d-103">Proprietà AVEncCommonRealTime</span><span class="sxs-lookup"><span data-stu-id="a5d1d-103">AVEncCommonRealTime property</span></span>

<span data-ttu-id="a5d1d-104">Specifica se l'applicazione richiede prestazioni di codifica in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="a5d1d-104">Specifies whether the application requires real-time encoding performance.</span></span>

<span data-ttu-id="a5d1d-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a5d1d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5d1d-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a5d1d-106">Data type</span></span>

<span data-ttu-id="a5d1d-107">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="a5d1d-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="a5d1d-108">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="a5d1d-108">Property GUID</span></span>

<span data-ttu-id="a5d1d-109">**Codecapis \_ AVEncCommonRealTime**</span><span class="sxs-lookup"><span data-stu-id="a5d1d-109">**CODECAPI\_AVEncCommonRealTime**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5d1d-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5d1d-110">Remarks</span></span>

<span data-ttu-id="a5d1d-111">Per specificare che la codifica deve essere eseguita in tempo reale, impostare questa proprietà su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a5d1d-111">To specify that encoding must be performed in real time, set this property to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="a5d1d-112">I codec possono inoltre restituire questa proprietà come funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a5d1d-112">Codecs can also return this property as a capability.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5d1d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5d1d-113">Requirements</span></span>



| <span data-ttu-id="a5d1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5d1d-114">Requirement</span></span> | <span data-ttu-id="a5d1d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a5d1d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5d1d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5d1d-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="a5d1d-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a5d1d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5d1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5d1d-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a5d1d-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a5d1d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5d1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5d1d-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5d1d-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5d1d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5d1d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5d1d-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="a5d1d-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="a5d1d-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="a5d1d-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




