---
description: Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: Attributo MF_TOPONODE_CONNECT_METHOD (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233347"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="18706-103">\_Attributo del \_ metodo di connessione MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="18706-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="18706-104">Specifica il modo in cui il caricatore della topologia connette il nodo della topologia e se il nodo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="18706-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="18706-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="18706-105">Data type</span></span>

<span data-ttu-id="18706-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18706-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="18706-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="18706-107">Remarks</span></span>

<span data-ttu-id="18706-108">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="18706-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="18706-109">Il **valore dell'attributo è un operatore OR** bit per bit di flag dell'enumerazione del [**\_ \_ Metodo MF Connect**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) .</span><span class="sxs-lookup"><span data-stu-id="18706-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="18706-110">Se questo attributo non è impostato, il valore predefinito è **MF \_ Connect \_ allow \_ decoder**.</span><span class="sxs-lookup"><span data-stu-id="18706-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="18706-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="18706-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="18706-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18706-112">Requirements</span></span>



| <span data-ttu-id="18706-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="18706-113">Requirement</span></span> | <span data-ttu-id="18706-114">Valore</span><span class="sxs-lookup"><span data-stu-id="18706-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18706-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18706-115">Minimum supported client</span></span><br/> | <span data-ttu-id="18706-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18706-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18706-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18706-117">Minimum supported server</span></span><br/> | <span data-ttu-id="18706-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18706-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="18706-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18706-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="18706-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="18706-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18706-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18706-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18706-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18706-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18706-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="18706-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="18706-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="18706-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="18706-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="18706-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="18706-126">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="18706-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




