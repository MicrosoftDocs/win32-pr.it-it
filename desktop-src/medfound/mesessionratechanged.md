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
# <a name="mesessionratechanged-event"></a>Evento MESessionRateChanged

Generato dalla sessione multimediale quando cambia la velocità di riproduzione. Questo evento viene inviato dopo che il metodo [**IMFRateControl::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) SetValue viene completato in modo asincrono.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| \_R4 VT<br/> | Nuova velocità di riproduzione, espressa come rapporto della frequenza di riproduzione normale.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Eventi Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




