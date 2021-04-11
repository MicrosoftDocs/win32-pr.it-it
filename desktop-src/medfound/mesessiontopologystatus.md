---
description: Generato dalla sessione multimediale quando lo stato di una topologia cambia.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11948e27997037c1e875e192fd712a2f8a132b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967053"
---
# <a name="mesessiontopologystatus-event"></a>Evento MESessionTopologyStatus

Generato dalla sessione multimediale quando lo stato di una topologia cambia.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE                | Descrizione                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ sconosciuto<br/> | Puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                            | Descrizione                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**\_ \_ stato topologia evento MF \_**](mf-event-topology-status-attribute.md)<br/> | Specifica il nuovo stato della topologia.<br/> <br/> |



## <a name="remarks"></a>Commenti

Per un esempio di codice che recupera il puntatore [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) dall'evento, vedere evento [MESessionTopologySet](mesessiontopologyset.md) .

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

 

 




