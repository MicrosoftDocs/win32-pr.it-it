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
# <a name="mesourceratechanged-event"></a>Evento MESourceRateChanged

Generato da un'origine multimediale quando cambia la velocità di riproduzione. Questo evento viene inviato dopo che il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue viene completato in modo asincrono.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                   |
|-------------------|-----------------------------------------------|
| \_R4 VT<br/> | Nuova velocità di riproduzione.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Implementazione del controllo della frequenza](implementing-rate-control.md)
</dt> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> <dt>

[Controllo della frequenza](rate-control.md)
</dt> <dt>

[**IMFRateControl:: serate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




