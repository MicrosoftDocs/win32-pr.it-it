---
description: Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.
ms.assetid: 81ef7005-a9ab-4f26-bc39-68b27c4f92aa
title: Attributo MF_TOPONODE_RATELESS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5c5ded4d8d09e8d45f766b03737954329c9202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308438"
---
# <a name="mf_toponode_rateless-attribute"></a><span data-ttu-id="df6f1-103">\_ \_ Attributo senza valore MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="df6f1-103">MF\_TOPONODE\_RATELESS attribute</span></span>

<span data-ttu-id="df6f1-104">Specifica se il sink multimediale associato a questo nodo della topologia è senza frequenza.</span><span class="sxs-lookup"><span data-stu-id="df6f1-104">Specifies whether the media sink associated with this topology node is rateless.</span></span>

## <a name="data-type"></a><span data-ttu-id="df6f1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="df6f1-105">Data type</span></span>

<span data-ttu-id="df6f1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="df6f1-106">**UINT32**</span></span>

<span data-ttu-id="df6f1-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="df6f1-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df6f1-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="df6f1-108">Remarks</span></span>

<span data-ttu-id="df6f1-109">Questo attributo si applica ai nodi di output (**\_ nodo di \_ output \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="df6f1-109">This attribute applies to output nodes (**MF\_TOPOLOGY\_OUTPUT\_NODE**).</span></span>

<span data-ttu-id="df6f1-110">Se il valore di questo attributo è diverso da zero, la sessione multimediale considera il sink multimediale come un sink senza frequenza, indipendentemente dal fatto che il sink multimediale restituisca la caratteristica **MEDIASINK \_ senza frequenza** .</span><span class="sxs-lookup"><span data-stu-id="df6f1-110">If the value of this attribute is nonzero, the Media Session treats the media sink as a rateless sink, regardless of whether the media sink returns the **MEDIASINK\_RATELESS** characteristic.</span></span> <span data-ttu-id="df6f1-111">Se questo attributo non è impostato, si presuppone che il sink multimediale non sia senza frequenza.</span><span class="sxs-lookup"><span data-stu-id="df6f1-111">If this attribute is not set, the media sink is assumed not to be rateless.</span></span>

<span data-ttu-id="df6f1-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="df6f1-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="df6f1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df6f1-113">Requirements</span></span>



| <span data-ttu-id="df6f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="df6f1-114">Requirement</span></span> | <span data-ttu-id="df6f1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="df6f1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="df6f1-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="df6f1-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="df6f1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="df6f1-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df6f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="df6f1-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="df6f1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="df6f1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df6f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="df6f1-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="df6f1-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df6f1-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df6f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6f1-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="df6f1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="df6f1-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="df6f1-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="df6f1-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="df6f1-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="df6f1-126">**IMFMediaSink:: getcaratteristiche**</span><span class="sxs-lookup"><span data-stu-id="df6f1-126">**IMFMediaSink::GetCharacteristics**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)
</dt> <dt>

[<span data-ttu-id="df6f1-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="df6f1-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="df6f1-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="df6f1-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




