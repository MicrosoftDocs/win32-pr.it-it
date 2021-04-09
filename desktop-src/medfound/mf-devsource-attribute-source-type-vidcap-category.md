---
description: Specifica la categoria del dispositivo per un dispositivo di acquisizione video.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129786"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a><span data-ttu-id="e51a1-103">\_Attributo di \_ tipo Source dell'attributo MF DEVSOURCE \_ \_ \_ VidCap \_ Category</span><span class="sxs-lookup"><span data-stu-id="e51a1-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_CATEGORY attribute</span></span>

<span data-ttu-id="e51a1-104">Specifica la categoria del dispositivo per un dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="e51a1-104">Specifies the device category for a video capture device.</span></span>

## <a name="data-type"></a><span data-ttu-id="e51a1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e51a1-105">Data type</span></span>

<span data-ttu-id="e51a1-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e51a1-106">**GUID**</span></span>

<span data-ttu-id="e51a1-107">Viene definito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="e51a1-107">The following value is defined.</span></span>



| <span data-ttu-id="e51a1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e51a1-108">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="e51a1-109">Significato</span><span class="sxs-lookup"><span data-stu-id="e51a1-109">Meaning</span></span>                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <span data-ttu-id="e51a1-110"><dt>**\_VIDEOINPUTDEVICECATEGORY CLSID**</dt></span><span class="sxs-lookup"><span data-stu-id="e51a1-110"><dt>**CLSID\_VideoInputDeviceCategory**</dt></span></span> </dl> | <span data-ttu-id="e51a1-111">Dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="e51a1-111">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="e51a1-112">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="e51a1-112">Get/set</span></span>

<span data-ttu-id="e51a1-113">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="e51a1-113">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="e51a1-114">Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="e51a1-114">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="e51a1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e51a1-115">Remarks</span></span>

<span data-ttu-id="e51a1-116">Usare questo attributo come input per la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) durante l'enumerazione dei dispositivi di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="e51a1-116">Use this attribute as input to the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function when enumerating video capture devices.</span></span>

<span data-ttu-id="e51a1-117">Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e51a1-117">In addition, this attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="e51a1-118">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="e51a1-118">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="e51a1-119">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="e51a1-119">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="e51a1-120">L'attributo si applica solo ai dispositivi di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="e51a1-120">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="e51a1-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e51a1-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e51a1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e51a1-122">Requirements</span></span>



| <span data-ttu-id="e51a1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51a1-123">Requirement</span></span> | <span data-ttu-id="e51a1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e51a1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e51a1-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e51a1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e51a1-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e51a1-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e51a1-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e51a1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e51a1-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e51a1-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e51a1-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e51a1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e51a1-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e51a1-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e51a1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e51a1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51a1-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e51a1-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e51a1-133">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="e51a1-133">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="e51a1-134">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e51a1-134">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




