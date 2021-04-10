---
description: Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se l'origine richiede anche l'assottigliamento. Per una definizione di assottigliamento, vedere informazioni sul controllo della frequenza.
ms.assetid: 42b6d0b3-e5af-4a48-969c-53628d1b7c31
title: Attributo MF_EVENT_DO_THINNING (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a08807413881a13789c50dbf2d063693e7e4539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966800"
---
# <a name="mf_event_do_thinning-attribute"></a><span data-ttu-id="1f9c6-104">\_Attributo di \_ assottigliamento dell'evento MF \_</span><span class="sxs-lookup"><span data-stu-id="1f9c6-104">MF\_EVENT\_DO\_THINNING attribute</span></span>

<span data-ttu-id="1f9c6-105">Quando un'origine multimediale richiede una nuova velocità di riproduzione, questo attributo specifica se l'origine richiede anche l'assottigliamento.</span><span class="sxs-lookup"><span data-stu-id="1f9c6-105">When a media source requests a new playback rate, this attribute specifies whether the source also requests thinning.</span></span> <span data-ttu-id="1f9c6-106">Per una definizione di assottigliamento, vedere [informazioni sul controllo della frequenza](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="1f9c6-106">For a definition of thinning, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="1f9c6-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1f9c6-107">Data type</span></span>

<span data-ttu-id="1f9c6-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1f9c6-108">**UINT32**</span></span>

<span data-ttu-id="1f9c6-109">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="1f9c6-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f9c6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f9c6-110">Remarks</span></span>

<span data-ttu-id="1f9c6-111">Questo attributo viene utilizzato con l'evento [MESourceRateChangeRequested](mesourceratechangerequested.md) .</span><span class="sxs-lookup"><span data-stu-id="1f9c6-111">This attribute is used with the [MESourceRateChangeRequested](mesourceratechangerequested.md) event.</span></span> <span data-ttu-id="1f9c6-112">Se il valore è **true**, l'origine del supporto richiede un passaggio alla riproduzione diluita.</span><span class="sxs-lookup"><span data-stu-id="1f9c6-112">If the value is **TRUE**, the media source is requesting a switch to thinned playback.</span></span>

<span data-ttu-id="1f9c6-113">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="1f9c6-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="1f9c6-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1f9c6-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9c6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f9c6-115">Requirements</span></span>



| <span data-ttu-id="1f9c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f9c6-116">Requirement</span></span> | <span data-ttu-id="1f9c6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f9c6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9c6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9c6-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f9c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1f9c6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f9c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9c6-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f9c6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f9c6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f9c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9c6-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9c6-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9c6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f9c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9c6-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f9c6-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f9c6-126">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="1f9c6-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1f9c6-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1f9c6-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1f9c6-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1f9c6-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




