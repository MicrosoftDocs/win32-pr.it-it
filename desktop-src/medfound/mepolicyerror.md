---
description: Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309625"
---
# <a name="mepolicyerror-event"></a><span data-ttu-id="9e2af-103">Evento MEPolicyError</span><span class="sxs-lookup"><span data-stu-id="9e2af-103">MEPolicyError event</span></span>

<span data-ttu-id="9e2af-104">Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.</span><span class="sxs-lookup"><span data-stu-id="9e2af-104">Raised by a trusted output if an error occurs while enforcing the output policy.</span></span>

<span data-ttu-id="9e2af-105">Se la sessione multimediale riceve questo evento, interrompe la riproduzione e inoltra l'evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e2af-105">If the Media Session receives this event, it stops playback and forwards the event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="9e2af-106">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="9e2af-106">Event values</span></span>

<span data-ttu-id="9e2af-107">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e2af-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9e2af-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9e2af-108">VARTYPE</span></span>              | <span data-ttu-id="9e2af-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e2af-109">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9e2af-110">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="9e2af-110">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9e2af-111">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9e2af-111">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9e2af-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e2af-112">Remarks</span></span>

<span data-ttu-id="9e2af-113">I valori possibili recuperati da [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9e2af-113">Possible values retrieved from [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) include the following.</span></span>



| <span data-ttu-id="9e2af-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9e2af-114">Value</span></span>                      | <span data-ttu-id="9e2af-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e2af-115">Description</span></span>                                                    |
|----------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9e2af-116">\_criteri MF E non \_ \_ supportati</span><span class="sxs-lookup"><span data-stu-id="9e2af-116">MF\_E\_POLICY\_UNSUPPORTED</span></span> | <span data-ttu-id="9e2af-117">L'output attendibile non supporta i criteri di output correnti.</span><span class="sxs-lookup"><span data-stu-id="9e2af-117">The trusted output does not support the current output policy.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9e2af-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e2af-118">Requirements</span></span>



| <span data-ttu-id="9e2af-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e2af-119">Requirement</span></span> | <span data-ttu-id="9e2af-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9e2af-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e2af-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e2af-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e2af-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e2af-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9e2af-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e2af-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e2af-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e2af-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9e2af-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e2af-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e2af-126"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e2af-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e2af-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e2af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e2af-128">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9e2af-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




