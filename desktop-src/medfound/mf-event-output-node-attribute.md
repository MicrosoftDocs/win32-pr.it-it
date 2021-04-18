---
description: Identifica il nodo della topologia per un sink di flusso.
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: Attributo MF_EVENT_OUTPUT_NODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309565"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="baa78-103">\_Attributo del \_ nodo di output evento MF \_</span><span class="sxs-lookup"><span data-stu-id="baa78-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="baa78-104">Identifica il nodo della topologia per un sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="baa78-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="baa78-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="baa78-105">Data type</span></span>

<span data-ttu-id="baa78-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="baa78-106">**UINT64**</span></span>

<span data-ttu-id="baa78-107">Considera come [**TOPOID**](topoid.md).</span><span class="sxs-lookup"><span data-stu-id="baa78-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="baa78-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="baa78-108">Remarks</span></span>

<span data-ttu-id="baa78-109">Il valore di questo attributo è un identificatore di nodo per un nodo di output nella topologia corrente.</span><span class="sxs-lookup"><span data-stu-id="baa78-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="baa78-110">Per ottenere un puntatore al nodo associato, chiamare [**IMFTopology:: GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) nella topologia.</span><span class="sxs-lookup"><span data-stu-id="baa78-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="baa78-111">Questo attributo viene usato con gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="baa78-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="baa78-112">MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="baa78-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="baa78-113">MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="baa78-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="baa78-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="baa78-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa78-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baa78-115">Requirements</span></span>



| <span data-ttu-id="baa78-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="baa78-116">Requirement</span></span> | <span data-ttu-id="baa78-117">Valore</span><span class="sxs-lookup"><span data-stu-id="baa78-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="baa78-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baa78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="baa78-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baa78-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="baa78-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="baa78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="baa78-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="baa78-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="baa78-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baa78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa78-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="baa78-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa78-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baa78-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa78-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="baa78-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="baa78-126">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="baa78-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="baa78-127">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="baa78-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="baa78-128">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="baa78-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




