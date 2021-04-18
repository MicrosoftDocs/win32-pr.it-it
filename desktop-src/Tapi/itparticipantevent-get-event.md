---
description: Il \_ metodo Get Event ottiene un \_ descrittore di eventi del partecipante del tipo di evento che si è verificato.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Metodo ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332001"
---
# <a name="itparticipanteventget_event-method"></a>Metodo di evento ITParticipantEvent:: Get \_

\[**ottenere \_ L'evento** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ Event** ottiene un descrittore di [**\_ eventi del partecipante**](participant-event.md) del tipo di evento che si è verificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pParticipantEvent* \[ out\]
</dt> <dd>

Puntatore a un descrittore di [**\_ eventi del partecipante**](participant-event.md) dell'evento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>      |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pParticipantEvent* non è un puntatore valido.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**\_evento partecipante**](participant-event.md)
</dt> </dl>

 

 




