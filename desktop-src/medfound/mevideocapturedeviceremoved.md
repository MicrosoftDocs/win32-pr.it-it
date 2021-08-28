---
description: Inviato da IMFMediaSource che incapsula il dispositivo per indicare che il dispositivo è stato rimosso.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f209dc4be6e8f45639b060de1328cb04c932463f6b76355b7538b5649a69634e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013481"
---
# <a name="mevideocapturedeviceremoved-event"></a>Evento MEVideoCaptureDeviceRemoved

Inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo per indicare che il dispositivo è stato rimosso.

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

 

 




