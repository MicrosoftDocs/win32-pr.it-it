---
description: Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione. L'applicazione deve chiamare IMFRateControl::SetRate con la frequenza richiesta. Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla velocità corrente.
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d8a88225fd3a0a95c56d549a712b295ba562cc684c08fe4b762c0169e3637c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974130"
---
# <a name="mesourceratechangerequested-event"></a>Evento MESourceRateChangeRequested

Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione. L'applicazione deve chiamare [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) con la frequenza richiesta. Un'origine multimediale potrebbe generare questo evento se non può continuare la riproduzione alla velocità corrente.

## <a name="event-values"></a>Valori dell'evento

I valori possibili recuperati da [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) includono i seguenti.



| VARTYPE           | Descrizione                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | Nuova velocità di riproduzione richiesta.<br/> <br/> |



## <a name="attributes"></a>Attributi

Per questo evento sono definiti gli attributi seguenti.



| Attributo                                                                    | Descrizione                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**\_DIRADAMENTO DELLE DO DI \_ EVENTI MF \_**](mf-event-do-thinning-attribute.md)<br/> | Specifica se l'origine multimediale richiede anche il thinning.<br/> <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation eventi](media-foundation-events.md)
</dt> </dl>

 

 




