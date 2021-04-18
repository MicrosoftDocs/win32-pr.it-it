---
description: Specifica un tipo di dispositivi, ad esempio acquisizione audio o acquisizione video.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307970"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a><span data-ttu-id="55449-103">\_Attributo del \_ tipo di origine dell'attributo MF DEVSOURCE \_ \_</span><span class="sxs-lookup"><span data-stu-id="55449-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE attribute</span></span>

<span data-ttu-id="55449-104">Specifica un tipo di dispositivo, ad esempio acquisizione audio o acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="55449-104">Specifies a device's type, such as audio capture or video capture.</span></span>

## <a name="data-type"></a><span data-ttu-id="55449-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="55449-105">Data type</span></span>

<span data-ttu-id="55449-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="55449-106">**GUID**</span></span>

<span data-ttu-id="55449-107">Per questo attributo sono definiti i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="55449-107">The following values are defined for this attribute:</span></span>



| <span data-ttu-id="55449-108">Valore</span><span class="sxs-lookup"><span data-stu-id="55449-108">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="55449-109">Significato</span><span class="sxs-lookup"><span data-stu-id="55449-109">Meaning</span></span>                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <span data-ttu-id="55449-110"><dt>**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="55449-110"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_AUDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="55449-111">Dispositivo di acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="55449-111">Audio capture device.</span></span><br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <span data-ttu-id="55449-112"><dt>**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ VidCap \_ GUID**</dt></span><span class="sxs-lookup"><span data-stu-id="55449-112"><dt>**MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**</dt></span></span> </dl> | <span data-ttu-id="55449-113">Dispositivo di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="55449-113">Video capture device.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="55449-114">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="55449-114">Get/set</span></span>

<span data-ttu-id="55449-115">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="55449-115">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="55449-116">Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="55449-116">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="55449-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="55449-117">Remarks</span></span>

<span data-ttu-id="55449-118">Utilizzare questo attributo come input per le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="55449-118">Use this attribute as input to the following functions:</span></span>

-   [<span data-ttu-id="55449-119">**MFCreateDeviceSource**</span><span class="sxs-lookup"><span data-stu-id="55449-119">**MFCreateDeviceSource**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [<span data-ttu-id="55449-120">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="55449-120">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="55449-121">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="55449-121">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="55449-122">Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalla funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .</span><span class="sxs-lookup"><span data-stu-id="55449-122">In addition, this attribute is set on the activation objects returned by the [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) function.</span></span>

<span data-ttu-id="55449-123">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="55449-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="55449-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55449-124">Requirements</span></span>



| <span data-ttu-id="55449-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="55449-125">Requirement</span></span> | <span data-ttu-id="55449-126">Valore</span><span class="sxs-lookup"><span data-stu-id="55449-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55449-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55449-127">Minimum supported client</span></span><br/> | <span data-ttu-id="55449-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="55449-128">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55449-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55449-129">Minimum supported server</span></span><br/> | <span data-ttu-id="55449-130">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="55449-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="55449-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55449-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="55449-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="55449-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55449-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55449-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55449-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="55449-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="55449-135">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="55449-135">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="55449-136">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="55449-136">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




