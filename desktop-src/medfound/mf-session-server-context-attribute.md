---
description: Consente a due istanze della sessione multimediale di condividere lo stesso processo di percorso multimediale protetto (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Attributo MF_SESSION_SERVER_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131958"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="cde68-103">\_Attributo di \_ contesto del server di sessione MF \_</span><span class="sxs-lookup"><span data-stu-id="cde68-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="cde68-104">Consente a due istanze della sessione multimediale di condividere lo stesso processo di percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="cde68-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="cde68-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cde68-105">Data type</span></span>

<span data-ttu-id="cde68-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="cde68-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="cde68-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cde68-107">Remarks</span></span>

<span data-ttu-id="cde68-108">Usare questo attributo se si vuole creare la sessione multimediale PMP in un processo PMP esistente.</span><span class="sxs-lookup"><span data-stu-id="cde68-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="cde68-109">Il valore dell'attributo è un puntatore all'interfaccia [_ *IMFPMPServer* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="cde68-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="cde68-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cde68-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde68-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cde68-111">Requirements</span></span>



| <span data-ttu-id="cde68-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde68-112">Requirement</span></span> | <span data-ttu-id="cde68-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cde68-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cde68-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde68-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cde68-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cde68-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cde68-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cde68-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cde68-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cde68-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cde68-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cde68-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cde68-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde68-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cde68-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cde68-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde68-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cde68-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cde68-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="cde68-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="cde68-123">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="cde68-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="cde68-124">Attributi della sessione multimediale</span><span class="sxs-lookup"><span data-stu-id="cde68-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




