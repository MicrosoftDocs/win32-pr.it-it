---
description: Specifica se i tipi di supporto possono essere modificati in questo nodo di topologia.
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: Attributo MF_TOPONODE_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753167"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="638e3-103">\_Attributo di \_ blocco MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="638e3-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="638e3-104">Specifica se i tipi di supporto possono essere modificati in questo nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="638e3-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="638e3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="638e3-105">Data type</span></span>

<span data-ttu-id="638e3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="638e3-106">**UINT32**</span></span>

<span data-ttu-id="638e3-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="638e3-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="638e3-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="638e3-108">Remarks</span></span>

<span data-ttu-id="638e3-109">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="638e3-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="638e3-110">Se il valore di questo attributo è diverso da zero, il caricatore della topologia non modificherà i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="638e3-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="638e3-111">Questo attributo è impostato su **true** quando il nodo è in uso.</span><span class="sxs-lookup"><span data-stu-id="638e3-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="638e3-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="638e3-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="638e3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="638e3-113">Requirements</span></span>



| <span data-ttu-id="638e3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="638e3-114">Requirement</span></span> | <span data-ttu-id="638e3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="638e3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="638e3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="638e3-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="638e3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="638e3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="638e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="638e3-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="638e3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="638e3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="638e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="638e3-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="638e3-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638e3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="638e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638e3-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="638e3-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="638e3-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="638e3-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="638e3-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="638e3-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="638e3-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="638e3-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="638e3-127">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="638e3-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




