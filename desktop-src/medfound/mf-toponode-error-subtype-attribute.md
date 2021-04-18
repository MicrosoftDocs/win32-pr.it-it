---
description: Contiene il sottotipo di supporto per un nodo di topologia. Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: Attributo MF_TOPONODE_ERROR_SUBTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308450"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="8aa16-104">\_Attributo del \_ sottotipo di errore MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="8aa16-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="8aa16-105">Contiene il sottotipo di supporto per un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="8aa16-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="8aa16-106">Questo attributo viene impostato quando la topologia non viene caricata perché non è stato possibile trovare il decodificatore corretto.</span><span class="sxs-lookup"><span data-stu-id="8aa16-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="8aa16-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8aa16-107">Data type</span></span>

<span data-ttu-id="8aa16-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8aa16-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa16-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aa16-109">Remarks</span></span>

<span data-ttu-id="8aa16-110">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="8aa16-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="8aa16-111">Il caricatore della topologia potrebbe impostare l'attributo.</span><span class="sxs-lookup"><span data-stu-id="8aa16-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="8aa16-112">Le applicazioni in genere leggono questo attributo ma non lo impostano.</span><span class="sxs-lookup"><span data-stu-id="8aa16-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="8aa16-113">Per un elenco di valori possibili, vedere [GUID di tipo di supporto](media-type-guids.md).</span><span class="sxs-lookup"><span data-stu-id="8aa16-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="8aa16-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8aa16-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa16-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aa16-115">Requirements</span></span>



| <span data-ttu-id="8aa16-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa16-116">Requirement</span></span> | <span data-ttu-id="8aa16-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8aa16-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa16-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa16-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8aa16-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8aa16-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa16-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8aa16-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8aa16-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aa16-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa16-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa16-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa16-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aa16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa16-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8aa16-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8aa16-126">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="8aa16-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="8aa16-127">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="8aa16-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="8aa16-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8aa16-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="8aa16-129">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="8aa16-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




