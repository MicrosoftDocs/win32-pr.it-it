---
description: Il metodo get \_ Event ottiene un descrittore PARTICIPANT EVENT del \_ tipo di evento che si è verificato.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: Metodo ITParticipantEvent::get_Event (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864702"
---
# <a name="itparticipanteventget_event-method"></a>Metodo ITParticipantEvent::get \_ Event

\[**get \_ L'evento** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ Event** ottiene un [**descrittore PARTICIPANT \_ EVENT**](participant-event.md) del tipo di evento che si è verificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParticipantEvent* \[ Cambio\]
</dt> <dd>

Puntatore a [**un descrittore \_ EVENTO PARTICIPANT**](participant-event.md) dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/>      |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Il *parametro pParticipantEvent* non è un puntatore valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**EVENTO \_ PARTECIPANTE**](participant-event.md)
</dt> </dl>

 

 




