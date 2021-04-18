---
description: Specifica l'intervallo nominale delle informazioni sul colore in un tipo di supporto video.
ms.assetid: 7b2b809e-aae4-401c-816a-626fb88f5f87
title: Attributo MF_MT_VIDEO_NOMINAL_RANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4539b06281655e079d9ff6ca4000e0ed75462b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318716"
---
# <a name="mf_mt_video_nominal_range-attribute"></a><span data-ttu-id="62e92-103">\_ \_ \_ Attributo intervallo nominale video MF mt \_</span><span class="sxs-lookup"><span data-stu-id="62e92-103">MF\_MT\_VIDEO\_NOMINAL\_RANGE attribute</span></span>

<span data-ttu-id="62e92-104">Specifica l'intervallo nominale delle informazioni sul colore in un tipo di supporto video.</span><span class="sxs-lookup"><span data-stu-id="62e92-104">Specifies the nominal range of the color information in a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="62e92-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="62e92-105">Data type</span></span>

<span data-ttu-id="62e92-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="62e92-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62e92-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="62e92-107">Remarks</span></span>

<span data-ttu-id="62e92-108">Il valore di questo attributo è un membro dell'enumerazione [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) .</span><span class="sxs-lookup"><span data-stu-id="62e92-108">The value of this attribute is a member of the [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange) enumeration.</span></span>

<span data-ttu-id="62e92-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="62e92-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

<span data-ttu-id="62e92-110">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="62e92-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="62e92-111">Nel tipo di supporto di output, \_ l' \_ intervallo nominale video MF mt \_ \_ può essere impostato con **MFNominalRange \_ 0 \_ 255** e **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="62e92-111">On the output media type, MF\_MT\_VIDEO\_NOMINAL\_RANGE can be set with **MFNominalRange\_0\_255** and **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="62e92-112">Il codificatore H. 264/AVC deve considerare **MFNominalRange \_ Unknown** come **MFNominalRange \_ 16 \_ 235**.</span><span class="sxs-lookup"><span data-stu-id="62e92-112">H.264/AVC encoder shall treat **MFNominalRange\_Unknown** as **MFNominalRange\_16\_235**.</span></span>

<span data-ttu-id="62e92-113">Il codificatore H. 264/AVC deve rifiutare un tipo di supporto di output quando MF \_ mt \_ video \_ Nominal \_ Range è impostato su **MFNominalRange \_ 48 \_ 208**, **MFNominalRange \_ 64 \_ 127** o qualsiasi altro valore non definito in [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span><span class="sxs-lookup"><span data-stu-id="62e92-113">H.264/AVC encoder shall reject a output media type when MF\_MT\_VIDEO\_NOMINAL\_RANGE is set to **MFNominalRange\_48\_208**, **MFNominalRange\_64\_127**, or any other values not defined on [**MFNominalRange**](/windows/desktop/api/mfobjects/ne-mfobjects-mfnominalrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="62e92-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62e92-114">Requirements</span></span>



| <span data-ttu-id="62e92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e92-115">Requirement</span></span> | <span data-ttu-id="62e92-116">Valore</span><span class="sxs-lookup"><span data-stu-id="62e92-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62e92-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62e92-117">Minimum supported client</span></span><br/> | <span data-ttu-id="62e92-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62e92-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="62e92-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62e92-119">Minimum supported server</span></span><br/> | <span data-ttu-id="62e92-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="62e92-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="62e92-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62e92-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e92-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e92-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62e92-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62e92-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e92-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62e92-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62e92-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="62e92-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="62e92-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="62e92-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="62e92-127">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="62e92-127">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="62e92-128">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="62e92-128">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="62e92-129">Informazioni sui colori estesi</span><span class="sxs-lookup"><span data-stu-id="62e92-129">Extended Color Information</span></span>](extended-color-information.md)
</dt> </dl>

 

 




