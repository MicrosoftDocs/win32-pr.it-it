---
description: Specifica se i flussi audio in una presentazione presentano una velocità in bit variabile.
ms.assetid: 2bd7eee1-5a93-4bde-8b58-80b6395a094e
title: Attributo MF_PD_AUDIO_ISVARIABLEBITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a34d3dd64f9100050dc9aae37e811d00c9d58af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232383"
---
# <a name="mf_pd_audio_isvariablebitrate-attribute"></a><span data-ttu-id="495bf-103">\_ \_ Attributo ISVARIABLEBITRATE MF PD audio \_</span><span class="sxs-lookup"><span data-stu-id="495bf-103">MF\_PD\_AUDIO\_ISVARIABLEBITRATE attribute</span></span>

<span data-ttu-id="495bf-104">Specifica se i flussi audio in una presentazione presentano una velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="495bf-104">Specifies whether the audio streams in a presentation have a variable bit rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="495bf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="495bf-105">Data type</span></span>

<span data-ttu-id="495bf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="495bf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="495bf-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="495bf-107">Get/set</span></span>

<span data-ttu-id="495bf-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="495bf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="495bf-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="495bf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="495bf-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="495bf-110">Applies To</span></span>

[<span data-ttu-id="495bf-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="495bf-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="495bf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="495bf-112">Remarks</span></span>

<span data-ttu-id="495bf-113">Si tratta di un attributo facoltativo per i descrittori di presentazione.</span><span class="sxs-lookup"><span data-stu-id="495bf-113">This is an optional attribute for presentation descriptors.</span></span> <span data-ttu-id="495bf-114">Se l'attributo è **true** (diverso da zero), la presentazione contiene almeno un flusso audio con velocità in bit (VBR) variabile.</span><span class="sxs-lookup"><span data-stu-id="495bf-114">If the attribute is **TRUE** (nonzero), the presentation contains at least one variable-bit-rate (VBR) audio stream.</span></span> <span data-ttu-id="495bf-115">Se l'attributo è **false**, tutti i flussi audio hanno una velocità in bit costante.</span><span class="sxs-lookup"><span data-stu-id="495bf-115">If the attribute is **FALSE**, all of the audio streams have a constant bit rate.</span></span>

<span data-ttu-id="495bf-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="495bf-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="495bf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="495bf-117">Requirements</span></span>



| <span data-ttu-id="495bf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="495bf-118">Requirement</span></span> | <span data-ttu-id="495bf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="495bf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="495bf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="495bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="495bf-121">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="495bf-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="495bf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="495bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="495bf-123">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="495bf-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="495bf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="495bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="495bf-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="495bf-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="495bf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="495bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="495bf-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="495bf-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="495bf-128">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="495bf-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




