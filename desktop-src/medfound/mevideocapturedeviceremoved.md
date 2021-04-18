---
description: Inviato da IMFMediaSource che incapsula il dispositivo per indicare che il dispositivo è stato rimosso.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315044"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="4ba9c-103">Evento MEVideoCaptureDeviceRemoved</span><span class="sxs-lookup"><span data-stu-id="4ba9c-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="4ba9c-104">Inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo per indicare che il dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="4ba9c-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="4ba9c-105">Valori dell'evento</span><span class="sxs-lookup"><span data-stu-id="4ba9c-105">Event values</span></span>

<span data-ttu-id="4ba9c-106">I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="4ba9c-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="4ba9c-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="4ba9c-107">VARTYPE</span></span>               | <span data-ttu-id="4ba9c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ba9c-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="4ba9c-109">VT \_ vuoto</span><span class="sxs-lookup"><span data-stu-id="4ba9c-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="4ba9c-110">Nessun dato dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4ba9c-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4ba9c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ba9c-111">Remarks</span></span>

<span data-ttu-id="4ba9c-112">Questo evento viene inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ba9c-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ba9c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ba9c-113">Requirements</span></span>



| <span data-ttu-id="4ba9c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ba9c-114">Requirement</span></span> | <span data-ttu-id="4ba9c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4ba9c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ba9c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ba9c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4ba9c-117">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ba9c-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4ba9c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ba9c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4ba9c-119">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ba9c-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ba9c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ba9c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ba9c-121"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ba9c-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ba9c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ba9c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ba9c-123">Eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ba9c-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




