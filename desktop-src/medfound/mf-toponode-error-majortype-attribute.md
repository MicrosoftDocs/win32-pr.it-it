---
description: Contiene il tipo di supporto principale per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: Attributo MF_TOPONODE_ERROR_MAJORTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308451"
---
# <a name="mf_toponode_error_majortype-attribute"></a><span data-ttu-id="3d8dd-104">\_ \_ Attributo MAJORTYPE dell'errore MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="3d8dd-104">MF\_TOPONODE\_ERROR\_MAJORTYPE attribute</span></span>

<span data-ttu-id="3d8dd-105">Contiene il tipo di supporto principale per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-105">Contains the major media type for a topology node.</span></span> <span data-ttu-id="3d8dd-106">Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d8dd-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3d8dd-107">Data type</span></span>

<span data-ttu-id="3d8dd-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3d8dd-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8dd-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d8dd-109">Remarks</span></span>

<span data-ttu-id="3d8dd-110">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="3d8dd-111">Il caricatore della topologia potrebbe impostare l'attributo.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="3d8dd-112">Le applicazioni in genere leggono questo attributo ma non lo impostano.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="3d8dd-113">Per un elenco di valori possibili, vedere [principali tipi di supporti](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="3d8dd-113">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="3d8dd-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3d8dd-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d8dd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d8dd-115">Requirements</span></span>



| <span data-ttu-id="3d8dd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d8dd-116">Requirement</span></span> | <span data-ttu-id="3d8dd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3d8dd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8dd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d8dd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8dd-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d8dd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d8dd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d8dd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8dd-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3d8dd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d8dd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d8dd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d8dd-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8dd-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8dd-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d8dd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8dd-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d8dd-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3d8dd-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="3d8dd-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="3d8dd-127">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="3d8dd-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="3d8dd-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3d8dd-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3d8dd-129">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="3d8dd-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




