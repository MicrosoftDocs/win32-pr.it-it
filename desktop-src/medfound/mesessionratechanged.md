---
description: 'Generato dalla sessione multimediale quando cambia la velocità di riproduzione. Questo evento viene inviato dopo che il metodo IMFRateControl:: SetValue viene completato in modo asincrono.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Evento MESessionRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880257"
---
# <a name="mesessionratechanged-event"></a><span data-ttu-id="9222f-104">Evento MESessionRateChanged</span><span class="sxs-lookup"><span data-stu-id="9222f-104">MESessionRateChanged event</span></span>

<span data-ttu-id="9222f-105">Generato dalla sessione multimediale quando cambia la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="9222f-105">Raised by the Media Session when the playback rate changes.</span></span> <span data-ttu-id="9222f-106">Questo evento viene inviato dopo che il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="9222f-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="9222f-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="9222f-107">Event values</span></span>

<span data-ttu-id="9222f-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9222f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9222f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9222f-109">VARTYPE</span></span>           | <span data-ttu-id="9222f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9222f-110">Description</span></span>                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9222f-111">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="9222f-111">VT\_R4</span></span><br/> | <span data-ttu-id="9222f-112">Nuova velocità di riproduzione, espressa come rapporto della frequenza di riproduzione normale.</span><span class="sxs-lookup"><span data-stu-id="9222f-112">The new playback rate, expressed as a ratio of the normal playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="9222f-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9222f-113">Requirements</span></span>



| <span data-ttu-id="9222f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9222f-114">Requirement</span></span> | <span data-ttu-id="9222f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9222f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9222f-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9222f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9222f-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9222f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9222f-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9222f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9222f-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9222f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9222f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9222f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9222f-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9222f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9222f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9222f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9222f-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9222f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




