---
description: Inviato da IMFMediaSource che incapsula il dispositivo per indicare che il dispositivo è stato interrotto.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309599"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="85424-103">Evento MEVideoCaptureDevicePreempted</span><span class="sxs-lookup"><span data-stu-id="85424-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="85424-104">Inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo per indicare che il dispositivo è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="85424-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="85424-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="85424-105">Event values</span></span>

<span data-ttu-id="85424-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="85424-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="85424-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="85424-107">VARTYPE</span></span>               | <span data-ttu-id="85424-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85424-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="85424-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="85424-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="85424-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="85424-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="85424-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="85424-111">Remarks</span></span>

<span data-ttu-id="85424-112">Questo evento viene inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="85424-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="85424-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85424-113">Requirements</span></span>



| <span data-ttu-id="85424-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="85424-114">Requirement</span></span> | <span data-ttu-id="85424-115">Valore</span><span class="sxs-lookup"><span data-stu-id="85424-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85424-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85424-116">Minimum supported client</span></span><br/> | <span data-ttu-id="85424-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="85424-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="85424-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85424-118">Minimum supported server</span></span><br/> | <span data-ttu-id="85424-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="85424-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85424-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85424-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="85424-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85424-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85424-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85424-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85424-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="85424-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




