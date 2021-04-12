---
description: Specifica se un oggetto sottostante di nodi della topologia è un decodificatore.
ms.assetid: b6d576dc-b12f-49bf-b938-db2c629df400
title: Attributo MF_TOPONODE_DECODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab16d14a91608fb6b21c901e3fb055ce5e4dfbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233619"
---
# <a name="mf_toponode_decoder-attribute"></a><span data-ttu-id="e5b19-103">\_Attributo del \_ decodificatore MF TOPONODE</span><span class="sxs-lookup"><span data-stu-id="e5b19-103">MF\_TOPONODE\_DECODER attribute</span></span>

<span data-ttu-id="e5b19-104">Specifica se l'oggetto sottostante di un nodo di topologia è un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e5b19-104">Specifies whether a topology node's underlying object is a decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e5b19-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e5b19-105">Data type</span></span>

<span data-ttu-id="e5b19-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e5b19-106">**UINT32**</span></span>

<span data-ttu-id="e5b19-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="e5b19-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b19-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5b19-108">Remarks</span></span>

<span data-ttu-id="e5b19-109">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="e5b19-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="e5b19-110">Se il valore di questo attributo è diverso da zero, l'oggetto sottostante del nodo è un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e5b19-110">If the value of this attribute is nonzero, the node's underlying object is a decoder.</span></span>

<span data-ttu-id="e5b19-111">Il caricatore della topologia imposta questo attributo quando crea un nodo del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e5b19-111">The topology loader sets this attribute when it creates a decoder node.</span></span> <span data-ttu-id="e5b19-112">Un'applicazione deve impostare questo attributo se l'applicazione aggiunge manualmente un decodificatore alla topologia.</span><span class="sxs-lookup"><span data-stu-id="e5b19-112">An application should set this attribute if the application manually adds a decoder to the topology.</span></span>

<span data-ttu-id="e5b19-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e5b19-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b19-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5b19-114">Requirements</span></span>



| <span data-ttu-id="e5b19-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b19-115">Requirement</span></span> | <span data-ttu-id="e5b19-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e5b19-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b19-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b19-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b19-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5b19-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e5b19-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e5b19-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b19-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5b19-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e5b19-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e5b19-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b19-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5b19-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b19-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e5b19-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5b19-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5b19-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e5b19-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="e5b19-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="e5b19-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="e5b19-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="e5b19-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e5b19-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e5b19-128">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="e5b19-128">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




