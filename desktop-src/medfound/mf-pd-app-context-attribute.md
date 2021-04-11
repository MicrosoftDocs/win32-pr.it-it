---
description: Contiene un puntatore al descrittore di presentazione dal percorso multimediale protetto (PMP).
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: Attributo MF_PD_APP_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233045"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="85c72-103">\_Attributo di \_ contesto dell'app MF PD \_</span><span class="sxs-lookup"><span data-stu-id="85c72-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="85c72-104">Contiene un puntatore al descrittore di presentazione dal percorso multimediale protetto (PMP).</span><span class="sxs-lookup"><span data-stu-id="85c72-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="85c72-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="85c72-105">Data type</span></span>

<span data-ttu-id="85c72-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="85c72-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="85c72-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="85c72-107">Remarks</span></span>

<span data-ttu-id="85c72-108">Il proxy di origine multimediale, creato nel processo PMP, usa questo attributo per archiviare il descrittore della presentazione remota nel descrittore di presentazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="85c72-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="85c72-109">Il valore di questo attributo è un puntatore all'interfaccia [_ *IMFPresentationDescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="85c72-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="85c72-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="85c72-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c72-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c72-111">Requirements</span></span>



| <span data-ttu-id="85c72-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c72-112">Requirement</span></span> | <span data-ttu-id="85c72-113">Valore</span><span class="sxs-lookup"><span data-stu-id="85c72-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="85c72-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85c72-114">Minimum supported client</span></span><br/> | <span data-ttu-id="85c72-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85c72-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="85c72-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85c72-116">Minimum supported server</span></span><br/> | <span data-ttu-id="85c72-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85c72-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="85c72-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85c72-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="85c72-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85c72-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85c72-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85c72-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85c72-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85c72-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="85c72-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="85c72-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="85c72-123">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="85c72-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="85c72-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="85c72-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




