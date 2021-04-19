---
description: Specifica lo stato di una topologia durante la riproduzione.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: Attributo MF_EVENT_TOPOLOGY_STATUS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319609"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="9944a-103">\_ \_ Attributo stato topologia evento MF \_</span><span class="sxs-lookup"><span data-stu-id="9944a-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="9944a-104">Specifica lo stato di una topologia durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9944a-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="9944a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9944a-105">Data type</span></span>

<span data-ttu-id="9944a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9944a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9944a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="9944a-107">Remarks</span></span>

<span data-ttu-id="9944a-108">Il valore di questo attributo è un membro dell'enumerazione [**MF \_ TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) .</span><span class="sxs-lookup"><span data-stu-id="9944a-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="9944a-109">Questo attributo viene utilizzato con l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="9944a-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="9944a-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9944a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9944a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9944a-111">Requirements</span></span>



| <span data-ttu-id="9944a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9944a-112">Requirement</span></span> | <span data-ttu-id="9944a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9944a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9944a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9944a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9944a-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9944a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9944a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9944a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9944a-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9944a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9944a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9944a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9944a-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9944a-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9944a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9944a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9944a-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9944a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9944a-122">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="9944a-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="9944a-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="9944a-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9944a-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="9944a-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




