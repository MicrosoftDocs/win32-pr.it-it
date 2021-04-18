---
description: Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo oppure usa un downmix non standard.
ms.assetid: a384d24e-07e2-45e7-84b8-e791feb64a83
title: Proprietà AVDecAACDownmixMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 388d1437dfe396d5072ef09082c4ad17ddb75953
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304208"
---
# <a name="avdecaacdownmixmode-property"></a><span data-ttu-id="2b47a-103">Proprietà AVDecAACDownmixMode</span><span class="sxs-lookup"><span data-stu-id="2b47a-103">AVDecAACDownmixMode property</span></span>

<span data-ttu-id="2b47a-104">Specifica se un decodificatore AAC USA equazioni downmix standard MPEG-2/MPEG-4 stereo oppure usa un downmix non standard.</span><span class="sxs-lookup"><span data-stu-id="2b47a-104">Specifies whether an AAC decoder uses standard MPEG-2/MPEG-4 stereo downmix equations, or uses a non-standard downmix.</span></span>

<span data-ttu-id="2b47a-105">Un esempio di downmix non standard è quello definito dal documento ARIB STD-B21 versione 4,4.</span><span class="sxs-lookup"><span data-stu-id="2b47a-105">An example of a non-standard downmix is the one defined by ARIB document STD-B21 version 4.4.</span></span>

<span data-ttu-id="2b47a-106">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2b47a-106">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b47a-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2b47a-107">Data type</span></span>

<span data-ttu-id="2b47a-108">**UInt32** (**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="2b47a-108">**UINT32** (**VT\_UI4**</span></span>

## <a name="property-guid"></a><span data-ttu-id="2b47a-109">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="2b47a-109">Property GUID</span></span>

<span data-ttu-id="2b47a-110">**Codecapis \_ AVDecAACDownmixMode**</span><span class="sxs-lookup"><span data-stu-id="2b47a-110">**CODECAPI\_AVDecAACDownmixMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="2b47a-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2b47a-111">Property value</span></span>

<span data-ttu-id="2b47a-112">Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) .</span><span class="sxs-lookup"><span data-stu-id="2b47a-112">The value of this property is a member of the [**eAVDecAACDownmixMode**](/windows/win32/api/codecapi/ne-codecapi-eavdecaacdownmixmode) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b47a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b47a-113">Requirements</span></span>



| <span data-ttu-id="2b47a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b47a-114">Requirement</span></span> | <span data-ttu-id="2b47a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2b47a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b47a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b47a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2b47a-117">App UWP di Windows 2000 Professional \[ desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="2b47a-117">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="2b47a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b47a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2b47a-119">App desktop di Windows 2000 Server \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b47a-119">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2b47a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b47a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b47a-121"><dt>Codecapis. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b47a-121"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b47a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b47a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b47a-123">Proprietà dell'API codec</span><span class="sxs-lookup"><span data-stu-id="2b47a-123">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="2b47a-124">**Interfaccia ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="2b47a-124">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

