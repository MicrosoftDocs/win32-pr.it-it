---
description: "Segnala un errore grave. Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento. Chiamare IMFMediaEvent:: GetStatus per ottenere il codice di errore dell'operazione non riuscita."
ms.assetid: bff80041-77d8-43b1-a410-9cefaf45eb2c
title: Evento MEError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb557dffb2c73a63031a193c331edabe470db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309640"
---
# <a name="meerror-event"></a><span data-ttu-id="5861a-105">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="5861a-105">MEError event</span></span>

<span data-ttu-id="5861a-106">Segnala un errore grave.</span><span class="sxs-lookup"><span data-stu-id="5861a-106">Signals a serious error.</span></span> <span data-ttu-id="5861a-107">Qualsiasi Media Foundation componente può inviare questo evento in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="5861a-107">Any Media Foundation component can send this event at any time.</span></span> <span data-ttu-id="5861a-108">Chiamare [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) per ottenere il codice di errore dell'operazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="5861a-108">Call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the error code of the operation that failed.</span></span>

## <a name="event-values"></a><span data-ttu-id="5861a-109">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="5861a-109">Event values</span></span>

<span data-ttu-id="5861a-110">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="5861a-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="5861a-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="5861a-111">VARTYPE</span></span>              | <span data-ttu-id="5861a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5861a-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="5861a-113">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="5861a-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="5861a-114">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5861a-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5861a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5861a-115">Remarks</span></span>

<span data-ttu-id="5861a-116">Questo evento deve essere utilizzato solo per gli errori imprevisti.</span><span class="sxs-lookup"><span data-stu-id="5861a-116">This event should be used only for unexpected errors.</span></span> <span data-ttu-id="5861a-117">Non inviare questo evento per segnalare che un metodo asincrono ha avuto esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5861a-117">Do not send this event to signal that an asynchronous method failed.</span></span> <span data-ttu-id="5861a-118">Se un metodo asincrono ha esito negativo, il codice di errore viene restituito nell'evento normale per il metodo.</span><span class="sxs-lookup"><span data-stu-id="5861a-118">If an asynchronous method fails, the error code is returned in the normal event for that method.</span></span>

<span data-ttu-id="5861a-119">Se si verifica un errore reversibile durante il flusso, inviare l'evento [MENonFatalError](menonfatalerror.md) .</span><span class="sxs-lookup"><span data-stu-id="5861a-119">If a recoverable error occurs during streaming, send the [MENonFatalError](menonfatalerror.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5861a-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5861a-120">Requirements</span></span>



| <span data-ttu-id="5861a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5861a-121">Requirement</span></span> | <span data-ttu-id="5861a-122">Valore</span><span class="sxs-lookup"><span data-stu-id="5861a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5861a-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5861a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5861a-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5861a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5861a-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5861a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5861a-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5861a-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5861a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5861a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5861a-128"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5861a-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5861a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5861a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5861a-130">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5861a-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




