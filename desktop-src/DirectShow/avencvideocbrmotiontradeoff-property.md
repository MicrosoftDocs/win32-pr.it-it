---
description: Specifica il compromesso tra movimento e immagini fisse. Questa proprietà si applica solo alla modalità di controllo della velocità in bit costante (CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Proprietà AVEncVideoCBRMotionTradeoff (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965785"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="2bd2c-104">Proprietà AVEncVideoCBRMotionTradeoff</span><span class="sxs-lookup"><span data-stu-id="2bd2c-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="2bd2c-105">Specifica il compromesso tra movimento e immagini fisse.</span><span class="sxs-lookup"><span data-stu-id="2bd2c-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="2bd2c-106">Questa proprietà si applica solo alla modalità di controllo della velocità in bit costante (CBR).</span><span class="sxs-lookup"><span data-stu-id="2bd2c-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="2bd2c-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2bd2c-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2bd2c-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2bd2c-108">Data type</span></span>

<span data-ttu-id="2bd2c-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="2bd2c-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2bd2c-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="2bd2c-110">Property GUID</span></span>

<span data-ttu-id="2bd2c-111">**Codecapis \_ AVEncVideoCBRMotionTradeoff**</span><span class="sxs-lookup"><span data-stu-id="2bd2c-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="2bd2c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2bd2c-112">Property value</span></span>

<span data-ttu-id="2bd2c-113">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="2bd2c-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="2bd2c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2c-114">Value</span></span> | <span data-ttu-id="2bd2c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd2c-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="2bd2c-116">0</span><span class="sxs-lookup"><span data-stu-id="2bd2c-116">0</span></span>     | <span data-ttu-id="2bd2c-117">Ottimizza per immagini ancora</span><span class="sxs-lookup"><span data-stu-id="2bd2c-117">Optimize for still images</span></span> |
| <span data-ttu-id="2bd2c-118">100</span><span class="sxs-lookup"><span data-stu-id="2bd2c-118">100</span></span>   | <span data-ttu-id="2bd2c-119">Ottimizza per il movimento.</span><span class="sxs-lookup"><span data-stu-id="2bd2c-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="2bd2c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bd2c-120">Requirements</span></span>



| <span data-ttu-id="2bd2c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd2c-121">Requirement</span></span> | <span data-ttu-id="2bd2c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2bd2c-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd2c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd2c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd2c-124">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2bd2c-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2bd2c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bd2c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd2c-126">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2bd2c-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2bd2c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2bd2c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bd2c-128"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bd2c-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bd2c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bd2c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bd2c-130">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="2bd2c-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2bd2c-131">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2bd2c-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




