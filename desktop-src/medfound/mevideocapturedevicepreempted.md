---
description: Inviato da IMFMediaSource che incapsula il dispositivo per indicare che il dispositivo è stato preempted.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78246d6560344735167fc6efd45ba0481095534977c67dac11a76ffae0947d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061164"
---
# <a name="mevideocapturedevicepreempted-event"></a>EVENTO MEVideoCaptureDevicePreempted

Inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo per indicare che il dispositivo è stato preempted.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




