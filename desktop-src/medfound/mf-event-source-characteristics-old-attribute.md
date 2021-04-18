---
description: Specifica le caratteristiche precedenti dell'origine multimediale.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Attributo MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309563"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="7deca-103">\_Caratteristiche dell' \_ origine evento MF \_ \_ attributo obsoleto</span><span class="sxs-lookup"><span data-stu-id="7deca-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="7deca-104">Specifica le caratteristiche precedenti dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="7deca-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="7deca-105">I dati dell'attributo sono un **operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="7deca-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="7deca-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7deca-106">Data type</span></span>

<span data-ttu-id="7deca-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7deca-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7deca-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7deca-108">Remarks</span></span>

<span data-ttu-id="7deca-109">Questo attributo viene utilizzato con l'evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7deca-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="7deca-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7deca-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7deca-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7deca-111">Requirements</span></span>



| <span data-ttu-id="7deca-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7deca-112">Requirement</span></span> | <span data-ttu-id="7deca-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7deca-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7deca-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7deca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7deca-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7deca-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7deca-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7deca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7deca-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7deca-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7deca-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7deca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7deca-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7deca-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7deca-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7deca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7deca-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7deca-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7deca-122">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="7deca-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="7deca-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="7deca-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7deca-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="7deca-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7deca-125">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="7deca-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




