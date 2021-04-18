---
description: "Generato quando un'origine multimediale cerca una nuova posizione. Un'origine multimediale genera questo evento se l'origine è in esecuzione o in pausa e l'applicazione chiama IMFMediaSource:: Start con un'ora di inizio che non corrisponde alla posizione corrente."
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Evento MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308003"
---
# <a name="mesourceseeked-event"></a><span data-ttu-id="23276-104">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="23276-104">MESourceSeeked event</span></span>

<span data-ttu-id="23276-105">Generato quando un'origine multimediale cerca una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="23276-105">Raised when a media source seeks to a new position.</span></span> <span data-ttu-id="23276-106">Un'origine multimediale genera questo evento se l'origine è in esecuzione o in pausa e l'applicazione chiama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con un'ora di inizio che non corrisponde alla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="23276-106">A media source raises this event if the source is running or paused and the application calls [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) with a start time that does not equal the current position.</span></span>

## <a name="event-values"></a><span data-ttu-id="23276-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="23276-107">Event values</span></span>

<span data-ttu-id="23276-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="23276-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="23276-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="23276-109">VARTYPE</span></span>           | <span data-ttu-id="23276-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23276-110">Description</span></span>                                                                |
|-------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="23276-111">\_I8 VT</span><span class="sxs-lookup"><span data-stu-id="23276-111">VT\_I8</span></span><br/> | <span data-ttu-id="23276-112">Nuova posizione iniziale, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="23276-112">The new starting position, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="23276-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23276-113">Requirements</span></span>



| <span data-ttu-id="23276-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23276-114">Requirement</span></span> | <span data-ttu-id="23276-115">Valore</span><span class="sxs-lookup"><span data-stu-id="23276-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23276-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23276-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23276-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23276-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="23276-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23276-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23276-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23276-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="23276-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23276-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23276-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23276-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23276-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23276-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23276-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23276-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




