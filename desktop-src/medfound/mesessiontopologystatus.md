---
description: Generato dalla sessione multimediale quando cambia lo stato di una topologia.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42adfd1a86319f65077e87925eb23807253f12b06e977ee1eb9e494a4c7df180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723721"
---
# <a name="mesessiontopologystatus-event"></a>EVENTO MESessionTopologyStatus

Generato dalla sessione multimediale quando cambia lo stato di una topologia.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati [**da IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntatore [**all'interfaccia IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                            | Descrizione                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**STATO DELLA \_ TOPOLOGIA \_ DI EVENTI \_ MF**](mf-event-topology-status-attribute.md)<br/> | Specifica il nuovo stato della topologia.<br/> <br/> |



## <a name="remarks"></a>Commenti

Per un esempio di codice che recupera il [**puntatore IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) dall'evento , vedere [Evento MESessionTopologySet.](mesessiontopologyset.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




