---
description: Contiene un puntatore all'origine multimediale associata a un nodo di topologia.
ms.assetid: 73b84ab6-bdc2-4b22-9ce4-b79b954476e5
title: Attributo MF_TOPONODE_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57904e9797e0f669b2cb782750e4ae9199059d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527421"
---
# <a name="mf_toponode_source-attribute"></a><span data-ttu-id="267f9-103">\_Attributo di \_ origine MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="267f9-103">MF\_TOPONODE\_SOURCE attribute</span></span>

<span data-ttu-id="267f9-104">Contiene un puntatore all'origine multimediale associata a un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="267f9-104">Contains a pointer to the media source associated with a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="267f9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="267f9-105">Data type</span></span>

<span data-ttu-id="267f9-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="267f9-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="267f9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="267f9-107">Remarks</span></span>

<span data-ttu-id="267f9-108">Questo attributo si applica ai nodi di origine (_ \* MF \_ topologia \_ SOURCESTREAM \_ nodo \* \*).</span><span class="sxs-lookup"><span data-stu-id="267f9-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="267f9-109">Il valore dell'attributo è un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="267f9-109">The value of the attribute is a pointer to the media source's [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span> <span data-ttu-id="267f9-110">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="267f9-110">This attribute is required.</span></span>

<span data-ttu-id="267f9-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="267f9-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="267f9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="267f9-112">Requirements</span></span>



| <span data-ttu-id="267f9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="267f9-113">Requirement</span></span> | <span data-ttu-id="267f9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="267f9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="267f9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="267f9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="267f9-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="267f9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="267f9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="267f9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="267f9-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="267f9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="267f9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="267f9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="267f9-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="267f9-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267f9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="267f9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267f9-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="267f9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="267f9-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="267f9-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="267f9-124">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="267f9-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="267f9-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="267f9-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="267f9-126">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="267f9-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




