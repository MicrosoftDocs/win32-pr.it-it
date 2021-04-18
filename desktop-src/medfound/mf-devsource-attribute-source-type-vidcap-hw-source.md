---
description: Specifica se un'origine di acquisizione video è un dispositivo hardware o software.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309567"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a><span data-ttu-id="44679-103">\_Tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ VidCap \_ \_ attributo Source HW</span><span class="sxs-lookup"><span data-stu-id="44679-103">MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_HW\_SOURCE attribute</span></span>

<span data-ttu-id="44679-104">Specifica se un'origine di acquisizione video è un dispositivo hardware o software.</span><span class="sxs-lookup"><span data-stu-id="44679-104">Specifies whether a video capture source is a hardware device or a software device.</span></span>

## <a name="data-type"></a><span data-ttu-id="44679-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="44679-105">Data type</span></span>

<span data-ttu-id="44679-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="44679-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="44679-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="44679-107">Get/set</span></span>

<span data-ttu-id="44679-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="44679-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="44679-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="44679-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="44679-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="44679-110">Remarks</span></span>

<span data-ttu-id="44679-111">Se il valore è **true**, l'origine di acquisizione è un dispositivo hardware.</span><span class="sxs-lookup"><span data-stu-id="44679-111">If the value is **TRUE**, the capture source is a hardware device.</span></span> <span data-ttu-id="44679-112">Se il valore è **false**, si tratta di un dispositivo software.</span><span class="sxs-lookup"><span data-stu-id="44679-112">If the value is **FALSE**, it is a software device.</span></span> <span data-ttu-id="44679-113">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="44679-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="44679-114">Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="44679-114">This attribute is set on the activation objects returned by the following functions:</span></span>

-   [<span data-ttu-id="44679-115">**MFCreateDeviceSourceActivate**</span><span class="sxs-lookup"><span data-stu-id="44679-115">**MFCreateDeviceSourceActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [<span data-ttu-id="44679-116">**MFEnumDeviceSources**</span><span class="sxs-lookup"><span data-stu-id="44679-116">**MFEnumDeviceSources**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

<span data-ttu-id="44679-117">L'attributo si applica solo ai dispositivi di acquisizione video.</span><span class="sxs-lookup"><span data-stu-id="44679-117">The attribute applies only to video capture devices.</span></span>

<span data-ttu-id="44679-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="44679-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="44679-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44679-119">Requirements</span></span>



| <span data-ttu-id="44679-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="44679-120">Requirement</span></span> | <span data-ttu-id="44679-121">Valore</span><span class="sxs-lookup"><span data-stu-id="44679-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44679-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44679-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44679-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="44679-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44679-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44679-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44679-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="44679-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="44679-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44679-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="44679-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44679-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44679-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44679-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44679-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="44679-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="44679-130">Acquisizione di audio/video</span><span class="sxs-lookup"><span data-stu-id="44679-130">Audio/Video Capture</span></span>](audio-video-capture.md)
</dt> <dt>

[<span data-ttu-id="44679-131">Acquisisci attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="44679-131">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




