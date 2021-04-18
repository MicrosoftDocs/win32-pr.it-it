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
# <a name="mevideocapturedevicepreempted-event"></a>Evento MEVideoCaptureDevicePreempted

Inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo per indicare che il dispositivo è stato interrotto.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE               | Descrizione                           |
|-----------------------|---------------------------------------|
| VT \_ vuoto <br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="remarks"></a>Commenti

Questo evento viene inviato da [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) che incapsula il dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




