---
description: Offset tra l'ora di presentazione e i timestamp dei sorgenti multimediali.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Attributo MF_EVENT_PRESENTATION_TIME_OFFSET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879602"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="00421-103">\_ \_ \_ Attributo offset ora presentazione evento MF \_</span><span class="sxs-lookup"><span data-stu-id="00421-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="00421-104">Offset tra l'ora di presentazione e i timestamp dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="00421-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="00421-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="00421-105">Data type</span></span>

<span data-ttu-id="00421-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="00421-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="00421-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="00421-107">Remarks</span></span>

<span data-ttu-id="00421-108">L'offset viene calcolato come segue: offset = tempo di presentazione-ora di origine.</span><span class="sxs-lookup"><span data-stu-id="00421-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="00421-109">Questo attributo viene usato con gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="00421-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="00421-110">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="00421-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="00421-111">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="00421-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="00421-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="00421-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="00421-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00421-113">Requirements</span></span>



| <span data-ttu-id="00421-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="00421-114">Requirement</span></span> | <span data-ttu-id="00421-115">Valore</span><span class="sxs-lookup"><span data-stu-id="00421-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00421-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00421-116">Minimum supported client</span></span><br/> | <span data-ttu-id="00421-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00421-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00421-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00421-118">Minimum supported server</span></span><br/> | <span data-ttu-id="00421-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00421-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00421-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00421-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="00421-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="00421-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00421-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00421-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00421-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="00421-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="00421-124">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="00421-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="00421-125">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="00421-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="00421-126">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="00421-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




