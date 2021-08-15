---
description: Il metodo get Participant ottiene un puntatore a una matrice di \_ interfacce ITParticipant che rappresentano i partecipanti coinvolti nell'evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: Metodo ITParticipantEvent::get_Participant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d53b5269b0940888ca5a849e4ecc8cc98d053bbe80340dcfa1a858eabd6ceed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864515"
---
# <a name="itparticipanteventget_participant-method"></a>Metodo ITParticipantEvent::get \_ Participant

\[**get \_ Il** partecipante non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Il **metodo get \_ Participant** ottiene un puntatore a una matrice di [**interfacce ITParticipant**](itparticipant.md) che rappresentano i partecipanti coinvolti nell'evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppParticipant* \[ Cambio\]
</dt> <dd>

Puntatore alla matrice [**di interfacce ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                           | Significato                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | Memoria insufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | All'evento non sono associati partecipanti.<br/>  |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>       | Il *parametro ppParticipant* non è un puntatore valido.<br/> |



 

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

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




