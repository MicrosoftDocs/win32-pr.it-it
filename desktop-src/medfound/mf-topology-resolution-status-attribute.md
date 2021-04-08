---
description: Specifica lo stato di un tentativo di risoluzione di una topologia.
ms.assetid: 7c2410ce-e70b-4303-9dbc-caff4a355d6b
title: Attributo MF_TOPOLOGY_RESOLUTION_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb98db0de67e228606d9f37216d1ea13cbc2f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880222"
---
# <a name="mf_topology_resolution_status-attribute"></a><span data-ttu-id="19f16-103">\_Attributo di \_ stato di risoluzione TOPOLOGIa MF \_</span><span class="sxs-lookup"><span data-stu-id="19f16-103">MF\_TOPOLOGY\_RESOLUTION\_STATUS attribute</span></span>

<span data-ttu-id="19f16-104">Specifica lo stato di un tentativo di risoluzione di una topologia.</span><span class="sxs-lookup"><span data-stu-id="19f16-104">Specifies the status of an attempt to resolve a topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="19f16-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="19f16-105">Data type</span></span>

<span data-ttu-id="19f16-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="19f16-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="19f16-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="19f16-107">Remarks</span></span>

<span data-ttu-id="19f16-108">Il caricatore della topologia o la sessione multimediale potrebbe impostare questo attributo su una topologia.</span><span class="sxs-lookup"><span data-stu-id="19f16-108">The topology loader or the Media Session might set this attribute on a topology.</span></span> <span data-ttu-id="19f16-109">Il valore di questo attributo è un operatore OR bit per bit di **flag dell'enumerazione** di flag di [**stato di \_ risoluzione della topologia \_ \_ \_ MF**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) .</span><span class="sxs-lookup"><span data-stu-id="19f16-109">The value of this attribute is a bitwise **OR** of flags from the [**MF\_TOPOLOGY\_RESOLUTION\_STATUS\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_topology_resolution_status_flags) enumeration.</span></span>

<span data-ttu-id="19f16-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="19f16-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f16-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19f16-111">Requirements</span></span>



| <span data-ttu-id="19f16-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f16-112">Requirement</span></span> | <span data-ttu-id="19f16-113">Valore</span><span class="sxs-lookup"><span data-stu-id="19f16-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19f16-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19f16-114">Minimum supported client</span></span><br/> | <span data-ttu-id="19f16-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19f16-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19f16-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19f16-116">Minimum supported server</span></span><br/> | <span data-ttu-id="19f16-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19f16-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="19f16-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19f16-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="19f16-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="19f16-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19f16-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19f16-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f16-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="19f16-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="19f16-122">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="19f16-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="19f16-123">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="19f16-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="19f16-124">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="19f16-124">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)
</dt> <dt>

[<span data-ttu-id="19f16-125">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="19f16-125">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




