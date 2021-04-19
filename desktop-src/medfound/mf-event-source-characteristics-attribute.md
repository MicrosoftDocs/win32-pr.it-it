---
description: Specifica le caratteristiche correnti dell'origine multimediale.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: Attributo MF_EVENT_SOURCE_CHARACTERISTICS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307967"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="ae877-103">\_ \_ Attributo caratteristiche origine evento MF \_</span><span class="sxs-lookup"><span data-stu-id="ae877-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="ae877-104">Specifica le caratteristiche correnti dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="ae877-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae877-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ae877-105">Data type</span></span>

<span data-ttu-id="ae877-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ae877-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ae877-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae877-107">Remarks</span></span>

<span data-ttu-id="ae877-108">Il valore di questo attributo è **un operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="ae877-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="ae877-109">Questo attributo viene utilizzato con l'evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="ae877-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="ae877-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ae877-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae877-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae877-111">Requirements</span></span>



| <span data-ttu-id="ae877-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae877-112">Requirement</span></span> | <span data-ttu-id="ae877-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ae877-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae877-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae877-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ae877-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae877-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae877-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae877-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ae877-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae877-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae877-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae877-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae877-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae877-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae877-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae877-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae877-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae877-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae877-122">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="ae877-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae877-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ae877-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ae877-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ae877-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




