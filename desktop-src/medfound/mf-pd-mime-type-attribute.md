---
description: Specifica il tipo MIME del contenuto.
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: Attributo MF_PD_MIME_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314538"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="55cc5-103">\_Attributo di \_ tipo MIME PD \_ MF</span><span class="sxs-lookup"><span data-stu-id="55cc5-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="55cc5-104">Specifica il tipo MIME del contenuto.</span><span class="sxs-lookup"><span data-stu-id="55cc5-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="55cc5-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="55cc5-105">Data type</span></span>

<span data-ttu-id="55cc5-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="55cc5-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="55cc5-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="55cc5-107">Remarks</span></span>

<span data-ttu-id="55cc5-108">Questo attributo si applica ai descrittori di presentazione.</span><span class="sxs-lookup"><span data-stu-id="55cc5-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="55cc5-109">Il tipo MIME esposto tramite [System. MimeType](../properties/props-system-mimetype.md) per i file multimediali può avere una distorsione rispetto alla scelta dei tipi MIME appropriati per Digital Living Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="55cc5-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="55cc5-110">Il \_ \_ tipo MIME PD \_ di MF e [System. MimeType](../properties/props-system-mimetype.md) potrebbero non corrispondere sempre.</span><span class="sxs-lookup"><span data-stu-id="55cc5-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="55cc5-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="55cc5-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="55cc5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55cc5-112">Requirements</span></span>



| <span data-ttu-id="55cc5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="55cc5-113">Requirement</span></span> | <span data-ttu-id="55cc5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="55cc5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55cc5-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55cc5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="55cc5-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="55cc5-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="55cc5-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55cc5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="55cc5-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="55cc5-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="55cc5-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55cc5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="55cc5-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55cc5-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55cc5-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55cc5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cc5-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55cc5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55cc5-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="55cc5-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="55cc5-124">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="55cc5-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="55cc5-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="55cc5-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="55cc5-126">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="55cc5-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
