---
description: Generato quando un sink multimediale diventa non valido.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Evento MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226272"
---
# <a name="mesinkinvalidated-event"></a>Evento MESinkInvalidated

Generato quando un sink multimediale diventa non valido.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE              | Descrizione                           |
|----------------------|---------------------------------------|
| VT \_ vuoto<br/> | Nessun dato dell'evento.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                    | Descrizione                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_nodo di \_ output \_ evento MF**](mf-event-output-node-attribute.md)<br/> | Identifica il nodo della topologia per questo sink multimediale.<br/> <br/> |



## <a name="remarks"></a>Commenti

La sessione multimediale genera questo evento se riceve uno qualsiasi degli eventi seguenti dal sink multimediale:

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

Un sink multimediale può anche generare questo evento, nel qual caso la sessione multimediale imposta l'attributo del [**\_ \_ \_ nodo di output eventi MF**](mf-event-output-node-attribute.md) nell'evento e lo trasmette all'applicazione.

Se l'applicazione riceve questo evento, deve ricreare il sink multimediale e accodare nuovamente la topologia.

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

 

 




