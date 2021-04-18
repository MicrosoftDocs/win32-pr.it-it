---
description: 'Generato da un flusso multimediale quando il metodo IMFMediaSource:: Stop viene completato in modo asincrono.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Evento MEStreamStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314553"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="8b1f9-103">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="8b1f9-103">MEStreamStopped event</span></span>

<span data-ttu-id="8b1f9-104">Generato da un flusso multimediale quando il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="8b1f9-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="8b1f9-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="8b1f9-105">Event values</span></span>

<span data-ttu-id="8b1f9-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="8b1f9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8b1f9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8b1f9-107">VARTYPE</span></span>              | <span data-ttu-id="8b1f9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b1f9-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8b1f9-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="8b1f9-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8b1f9-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="8b1f9-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8b1f9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8b1f9-111">Remarks</span></span>

<span data-ttu-id="8b1f9-112">Ogni flusso attivo nella presentazione Invia questo evento.</span><span class="sxs-lookup"><span data-stu-id="8b1f9-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b1f9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b1f9-113">Requirements</span></span>



| <span data-ttu-id="8b1f9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b1f9-114">Requirement</span></span> | <span data-ttu-id="8b1f9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8b1f9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b1f9-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b1f9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8b1f9-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b1f9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b1f9-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8b1f9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8b1f9-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b1f9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8b1f9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b1f9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b1f9-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b1f9-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b1f9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b1f9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b1f9-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b1f9-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




