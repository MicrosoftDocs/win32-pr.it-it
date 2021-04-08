---
description: Specifica se il codificatore produce gruppi di immagini aperti (GOPs) o GOPs chiusi. Questa proprietà si applica ai codificatori video MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Proprietà AVEncMPVGOPOpen (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746927"
---
# <a name="avencmpvgopopen-property"></a><span data-ttu-id="86cd7-104">Proprietà AVEncMPVGOPOpen</span><span class="sxs-lookup"><span data-stu-id="86cd7-104">AVEncMPVGOPOpen property</span></span>

<span data-ttu-id="86cd7-105">Specifica se il codificatore produce gruppi di immagini aperti (GOPs) o GOPs chiusi.</span><span class="sxs-lookup"><span data-stu-id="86cd7-105">Specifies whether the encoder produces open groups of pictures (GOPs) or closed GOPs.</span></span> <span data-ttu-id="86cd7-106">Questa proprietà si applica ai codificatori video MPEG.</span><span class="sxs-lookup"><span data-stu-id="86cd7-106">This property applies to MPEG video encoders.</span></span>

<span data-ttu-id="86cd7-107">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="86cd7-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="86cd7-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="86cd7-108">Data type</span></span>

<span data-ttu-id="86cd7-109">**Variante \_ BOOL** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="86cd7-109">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="86cd7-110">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="86cd7-110">Property GUID</span></span>

<span data-ttu-id="86cd7-111">**Codecapis \_ AVEncMPVGOPOpen**</span><span class="sxs-lookup"><span data-stu-id="86cd7-111">**CODECAPI\_AVEncMPVGOPOpen**</span></span>

## <a name="property-value"></a><span data-ttu-id="86cd7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="86cd7-112">Property value</span></span>



| <span data-ttu-id="86cd7-113">Valore</span><span class="sxs-lookup"><span data-stu-id="86cd7-113">Value</span></span>          | <span data-ttu-id="86cd7-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86cd7-114">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="86cd7-115">VARIANTE \_ false</span><span class="sxs-lookup"><span data-stu-id="86cd7-115">VARIANT\_FALSE</span></span> | <span data-ttu-id="86cd7-116">GOPs chiuso</span><span class="sxs-lookup"><span data-stu-id="86cd7-116">Closed GOPs</span></span> |
| <span data-ttu-id="86cd7-117">VARIANT \_ true</span><span class="sxs-lookup"><span data-stu-id="86cd7-117">VARIANT\_TRUE</span></span>  | <span data-ttu-id="86cd7-118">Apri GOPs</span><span class="sxs-lookup"><span data-stu-id="86cd7-118">Open GOPs</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="86cd7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="86cd7-119">Remarks</span></span>

<span data-ttu-id="86cd7-120">Un GOP aperto contiene frame Delta che fanno riferimento a frame del GOP precedente.</span><span class="sxs-lookup"><span data-stu-id="86cd7-120">An open GOP contains delta frames that reference frames from the previous GOP.</span></span> <span data-ttu-id="86cd7-121">Un GOP chiuso non contiene frame Delta che fanno riferimento al GOP precedente.</span><span class="sxs-lookup"><span data-stu-id="86cd7-121">A closed GOP does not contain any delta frames that reference the previous GOP.</span></span>

## <a name="requirements"></a><span data-ttu-id="86cd7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86cd7-122">Requirements</span></span>



| <span data-ttu-id="86cd7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="86cd7-123">Requirement</span></span> | <span data-ttu-id="86cd7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="86cd7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86cd7-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cd7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86cd7-126">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="86cd7-126">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="86cd7-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86cd7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86cd7-128">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="86cd7-128">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="86cd7-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86cd7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86cd7-130"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="86cd7-130"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86cd7-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86cd7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cd7-132">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="86cd7-132">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="86cd7-133">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="86cd7-133">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




