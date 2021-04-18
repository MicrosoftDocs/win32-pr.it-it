---
description: Contiene un puntatore al descrittore di flusso per l'origine multimediale.
ms.assetid: 5acafbc1-823f-4b6d-8737-04b3a6a0cf87
title: Attributo MF_TOPONODE_STREAM_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f074a1c1ffde3671779362724676f884c3b6b0b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308437"
---
# <a name="mf_toponode_stream_descriptor-attribute"></a><span data-ttu-id="4aa77-103">\_Attributo del \_ descrittore di flusso MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="4aa77-103">MF\_TOPONODE\_STREAM\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="4aa77-104">Contiene un puntatore al descrittore di flusso per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="4aa77-104">Contains a pointer to the stream descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="4aa77-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4aa77-105">Data type</span></span>

<span data-ttu-id="4aa77-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="4aa77-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="4aa77-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4aa77-107">Remarks</span></span>

<span data-ttu-id="4aa77-108">Questo attributo si applica ai nodi di origine (_ \* MF \_ topologia \_ SOURCESTREAM \_ nodo \* \*).</span><span class="sxs-lookup"><span data-stu-id="4aa77-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="4aa77-109">Il valore dell'attributo è un puntatore all'interfaccia [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) del descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="4aa77-109">The value of the attribute is a pointer to the stream descriptor's [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) interface.</span></span> <span data-ttu-id="4aa77-110">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4aa77-110">This attribute is required.</span></span>

<span data-ttu-id="4aa77-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4aa77-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aa77-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4aa77-112">Requirements</span></span>



| <span data-ttu-id="4aa77-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aa77-113">Requirement</span></span> | <span data-ttu-id="4aa77-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4aa77-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa77-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa77-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4aa77-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4aa77-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4aa77-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4aa77-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4aa77-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4aa77-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4aa77-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4aa77-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4aa77-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4aa77-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aa77-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4aa77-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aa77-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4aa77-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4aa77-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="4aa77-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="4aa77-124">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="4aa77-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="4aa77-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="4aa77-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4aa77-126">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="4aa77-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




