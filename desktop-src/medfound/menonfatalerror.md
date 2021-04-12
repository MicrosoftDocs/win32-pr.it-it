---
description: Si è verificato un errore non irreversibile durante il flusso.
ms.assetid: 04afcca5-34d9-4c99-86bc-b37c19232ec1
title: Evento MENonFatalError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6af26a87b99e9c2ef649684c4ede53e707e7084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344621"
---
# <a name="menonfatalerror-event"></a><span data-ttu-id="35fe5-103">Evento MENonFatalError</span><span class="sxs-lookup"><span data-stu-id="35fe5-103">MENonFatalError event</span></span>

<span data-ttu-id="35fe5-104">Si è verificato un errore non irreversibile durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="35fe5-104">A non-fatal error occurred during streaming.</span></span> <span data-ttu-id="35fe5-105">Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="35fe5-105">Any Media Foundation component can send this event at any time.</span></span>

## <a name="event-values"></a><span data-ttu-id="35fe5-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="35fe5-106">Event values</span></span>

<span data-ttu-id="35fe5-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="35fe5-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="35fe5-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="35fe5-108">VARTYPE</span></span>            | <span data-ttu-id="35fe5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35fe5-109">Description</span></span>                                                        |
|--------------------|--------------------------------------------------------------------|
| <span data-ttu-id="35fe5-110">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="35fe5-110">VT\_UI4</span></span><br/> | <span data-ttu-id="35fe5-111">Valore **HRESULT** che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="35fe5-111">**HRESULT** value that describes the error.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="35fe5-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="35fe5-112">Attributes</span></span>

<span data-ttu-id="35fe5-113">Per questo evento non sono definiti attributi.</span><span class="sxs-lookup"><span data-stu-id="35fe5-113">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="35fe5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="35fe5-114">Remarks</span></span>

<span data-ttu-id="35fe5-115">Questo evento segnala un errore imprevisto ma reversibile durante il flusso.</span><span class="sxs-lookup"><span data-stu-id="35fe5-115">This event signals an unexpected but recoverable error during streaming.</span></span> <span data-ttu-id="35fe5-116">Ad esempio, un'origine multimediale può inviare questo evento se elimina un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="35fe5-116">For example, a media source might send this event if it drops a packet.</span></span>

<span data-ttu-id="35fe5-117">Non inviare questo evento per segnalare che un metodo asincrono ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="35fe5-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="35fe5-118">Se un metodo asincrono ha esito negativo, il codice di errore viene restituito nell'evento normale per il metodo.</span><span class="sxs-lookup"><span data-stu-id="35fe5-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="35fe5-119">Se si verifica un errore di streaming non reversibile, inviare l'evento [MEError](meerror.md) .</span><span class="sxs-lookup"><span data-stu-id="35fe5-119">If a non-recoverable streaming error occurs, send the [MEError](meerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fe5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35fe5-120">Requirements</span></span>



| <span data-ttu-id="35fe5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35fe5-121">Requirement</span></span> | <span data-ttu-id="35fe5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="35fe5-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fe5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35fe5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35fe5-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="35fe5-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="35fe5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35fe5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35fe5-126">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35fe5-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="35fe5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35fe5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fe5-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35fe5-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fe5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35fe5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35fe5-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35fe5-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




