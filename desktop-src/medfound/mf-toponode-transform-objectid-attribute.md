---
description: Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: Attributo MF_TOPONODE_TRANSFORM_OBJECTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527420"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="3f078-103">\_ \_ Attributo ObjectID della trasformazione MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="3f078-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="3f078-104">Identificatore di classe (CLSID) della trasformazione Media Foundation (MFT) associata a questo nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="3f078-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="3f078-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3f078-105">Data type</span></span>

<span data-ttu-id="3f078-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="3f078-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="3f078-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f078-107">Remarks</span></span>

<span data-ttu-id="3f078-108">Questo attributo si applica ai nodi di trasformazione (**\_ nodo di \_ trasformazione \_ della topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="3f078-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="3f078-109">Le applicazioni possono utilizzare questo attributo per inizializzare un nodo transfrom.</span><span class="sxs-lookup"><span data-stu-id="3f078-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="3f078-110">Se si imposta questo attributo, non è necessario chiamare [**IMFTopologyNode::**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) SetAttribute con un puntatore a un oggetto MFT o Activation.</span><span class="sxs-lookup"><span data-stu-id="3f078-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="3f078-111">Viceversa, se si chiama **seobject**, non è necessario impostare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="3f078-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="3f078-112">Per ulteriori informazioni, vedere [creazione di topologie](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="3f078-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="3f078-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="3f078-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f078-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f078-114">Requirements</span></span>



| <span data-ttu-id="3f078-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f078-115">Requirement</span></span> | <span data-ttu-id="3f078-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3f078-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3f078-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f078-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3f078-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f078-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3f078-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f078-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3f078-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f078-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3f078-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f078-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f078-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f078-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f078-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f078-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f078-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f078-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f078-125">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="3f078-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="3f078-126">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="3f078-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="3f078-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3f078-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="3f078-128">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f078-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3f078-129">Creazione di topologie</span><span class="sxs-lookup"><span data-stu-id="3f078-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="3f078-130">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="3f078-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




