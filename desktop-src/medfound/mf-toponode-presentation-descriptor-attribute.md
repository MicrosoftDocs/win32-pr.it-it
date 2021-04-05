---
description: Contiene un puntatore al descrittore di presentazione per l'origine multimediale.
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: Attributo MF_TOPONODE_PRESENTATION_DESCRIPTOR (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753159"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="afc21-103">\_Attributo del \_ descrittore di presentazione MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="afc21-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="afc21-104">Contiene un puntatore al descrittore di presentazione per l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="afc21-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="afc21-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="afc21-105">Data type</span></span>

<span data-ttu-id="afc21-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="afc21-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="afc21-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="afc21-107">Remarks</span></span>

<span data-ttu-id="afc21-108">Questo attributo si applica ai nodi di origine (_ \* MF \_ topologia \_ SOURCESTREAM \_ nodo \* \*).</span><span class="sxs-lookup"><span data-stu-id="afc21-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="afc21-109">Il valore dell'attributo è un puntatore all'interfaccia [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) del descrittore di presentazione.</span><span class="sxs-lookup"><span data-stu-id="afc21-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="afc21-110">Questo attributo è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="afc21-110">This attribute is required.</span></span>

<span data-ttu-id="afc21-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="afc21-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc21-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afc21-112">Requirements</span></span>



| <span data-ttu-id="afc21-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="afc21-113">Requirement</span></span> | <span data-ttu-id="afc21-114">Valore</span><span class="sxs-lookup"><span data-stu-id="afc21-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afc21-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="afc21-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afc21-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="afc21-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afc21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="afc21-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="afc21-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="afc21-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afc21-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc21-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc21-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afc21-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afc21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afc21-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="afc21-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="afc21-123">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="afc21-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="afc21-124">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="afc21-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="afc21-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="afc21-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="afc21-126">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="afc21-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




