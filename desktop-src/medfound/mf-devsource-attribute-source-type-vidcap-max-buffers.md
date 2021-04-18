---
description: Specifica il numero massimo di frame che l'origine di acquisizione video registrerà nel buffer.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307971"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a><span data-ttu-id="927ee-103">\_Attributo MF DEVSOURCE \_ tipo di origine attributo \_ \_ \_ VidCap \_ Max \_ buffers</span><span class="sxs-lookup"><span data-stu-id="927ee-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_MAX\_BUFFERS attribute</span></span>

<span data-ttu-id="927ee-104">Specifica il numero massimo di frame che l'origine di acquisizione video registrerà nel buffer.</span><span class="sxs-lookup"><span data-stu-id="927ee-104">Specifies the maximum number of frames that the video capture source will buffer.</span></span>

## <a name="data-type"></a><span data-ttu-id="927ee-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="927ee-105">Data type</span></span>

<span data-ttu-id="927ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="927ee-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="927ee-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="927ee-107">Get/set</span></span>

<span data-ttu-id="927ee-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="927ee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="927ee-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="927ee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="927ee-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="927ee-110">Remarks</span></span>

<span data-ttu-id="927ee-111">Per impostazione predefinita, l'origine di acquisizione video memorizza nel buffer un massimo di un frame alla volta.</span><span class="sxs-lookup"><span data-stu-id="927ee-111">By default, the video capture source buffers a maximum of one frame at a time.</span></span> <span data-ttu-id="927ee-112">È possibile aumentare il limite del buffer impostando questo attributo.</span><span class="sxs-lookup"><span data-stu-id="927ee-112">You can increase the buffer limit by setting this attribute.</span></span>

<span data-ttu-id="927ee-113">Il modo corretto per impostare questo attributo dipende dalla funzione usata per creare l'origine multimediale:</span><span class="sxs-lookup"><span data-stu-id="927ee-113">The correct way to set this attribute depends on the function used to create the media source:</span></span>

-   <span data-ttu-id="927ee-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): impostare l'attributo tramite il parametro *pAttributes* della funzione.</span><span class="sxs-lookup"><span data-stu-id="927ee-114">[**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="927ee-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): impostare l'attributo tramite il parametro *pAttributes* della funzione.</span><span class="sxs-lookup"><span data-stu-id="927ee-115">[**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): Set the attribute through the *pAttributes* parameter of the function.</span></span>
-   <span data-ttu-id="927ee-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): impostare l'attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla funzione.</span><span class="sxs-lookup"><span data-stu-id="927ee-116">[**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): Set the attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned by the function.</span></span> <span data-ttu-id="927ee-117">Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="927ee-117">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="927ee-118">L'attributo si applica solo ai dispositivi di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="927ee-118">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="927ee-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="927ee-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="927ee-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="927ee-120">Requirements</span></span>



| <span data-ttu-id="927ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="927ee-121">Requirement</span></span> | <span data-ttu-id="927ee-122">Valore</span><span class="sxs-lookup"><span data-stu-id="927ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="927ee-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="927ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="927ee-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="927ee-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="927ee-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="927ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="927ee-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="927ee-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="927ee-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="927ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="927ee-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="927ee-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="927ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927ee-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="927ee-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="927ee-131">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="927ee-131">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="927ee-132">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="927ee-132">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




