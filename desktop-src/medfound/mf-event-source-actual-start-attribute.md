---
description: Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Attributo MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401677"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="bfcb4-103">\_ \_ \_ Attributo iniziale effettivo origine evento MF \_</span><span class="sxs-lookup"><span data-stu-id="bfcb4-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="bfcb4-104">Contiene l'ora di inizio in cui un'origine multimediale viene riavviata dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="bfcb4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bfcb4-105">Data type</span></span>

<span data-ttu-id="bfcb4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="bfcb4-106">**UINT64**</span></span>

<span data-ttu-id="bfcb4-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="bfcb4-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfcb4-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfcb4-108">Remarks</span></span>

<span data-ttu-id="bfcb4-109">Questo attributo viene utilizzato con l'evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="bfcb4-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="bfcb4-110">L'attributo è pertinente quando i dati dell'evento sono vuoti (**VT \_ vuoto**), che indica che l'origine multimediale è stata avviata dalla posizione di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="bfcb4-111">In tal caso, l' **attributo \_ \_ \_ \_ Start effettivo dell'origine eventi MF** specifica l'ora di inizio effettiva.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="bfcb4-112">Se i dati dell'evento sono **VT \_ vuoti** e questo attributo non è impostato, si presuppone che l'ora di inizio sia zero.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="bfcb4-113">Quando i dati dell'evento [MESourceStarted](mesourcestarted.md) contengono l'ora di inizio (**VT \_ i8**), questo attributo non deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="bfcb4-114">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="bfcb4-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bfcb4-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcb4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfcb4-116">Requirements</span></span>



| <span data-ttu-id="bfcb4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfcb4-117">Requirement</span></span> | <span data-ttu-id="bfcb4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bfcb4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcb4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfcb4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcb4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfcb4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bfcb4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfcb4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcb4-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bfcb4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bfcb4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bfcb4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcb4-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcb4-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcb4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bfcb4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcb4-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bfcb4-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bfcb4-127">Attributi dell'evento</span><span class="sxs-lookup"><span data-stu-id="bfcb4-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="bfcb4-128">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="bfcb4-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="bfcb4-129">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="bfcb4-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




