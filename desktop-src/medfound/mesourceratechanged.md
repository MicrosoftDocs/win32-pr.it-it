---
description: "Generato da un'origine multimediale quando cambia la velocità di riproduzione. Questo evento viene inviato dopo che il metodo IMFRateControl:: SetValue viene completato in modo asincrono."
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Evento MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129810"
---
# <a name="mesourceratechanged-event"></a><span data-ttu-id="49dc0-104">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="49dc0-104">MESourceRateChanged event</span></span>

<span data-ttu-id="49dc0-105">Generato da un'origine multimediale quando cambia la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="49dc0-105">Raised by a media source when the playback rate changes.</span></span> <span data-ttu-id="49dc0-106">Questo evento viene inviato dopo che il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="49dc0-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="49dc0-107">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="49dc0-107">Event values</span></span>

<span data-ttu-id="49dc0-108">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="49dc0-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="49dc0-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="49dc0-109">VARTYPE</span></span>           | <span data-ttu-id="49dc0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49dc0-110">Description</span></span>                                   |
|-------------------|-----------------------------------------------|
| <span data-ttu-id="49dc0-111">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="49dc0-111">VT\_R4</span></span><br/> | <span data-ttu-id="49dc0-112">Nuova velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="49dc0-112">The new playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="49dc0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49dc0-113">Requirements</span></span>



| <span data-ttu-id="49dc0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49dc0-114">Requirement</span></span> | <span data-ttu-id="49dc0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49dc0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49dc0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49dc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49dc0-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49dc0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49dc0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49dc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49dc0-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49dc0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49dc0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49dc0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49dc0-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49dc0-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49dc0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49dc0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49dc0-123">Implementazione del controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="49dc0-123">Implementing Rate Control</span></span>](implementing-rate-control.md)
</dt> <dt>

[<span data-ttu-id="49dc0-124">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="49dc0-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="49dc0-125">Controllo della frequenza</span><span class="sxs-lookup"><span data-stu-id="49dc0-125">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="49dc0-126">**IMFRateControl:: serate**</span><span class="sxs-lookup"><span data-stu-id="49dc0-126">**IMFRateControl::SetRate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




