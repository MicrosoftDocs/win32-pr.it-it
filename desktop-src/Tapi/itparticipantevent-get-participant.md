---
description: Il \_ metodo Get partecipante ottiene un puntatore a una matrice di interfacce ITParticipant che rappresenta i partecipanti coinvolti nell'evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Metodo ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329088"
---
# <a name="itparticipanteventget_participant-method"></a>Metodo ITParticipantEvent:: Get \_ partecipante

\[**ottenere \_ Il partecipante** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ partecipante** ottiene un puntatore a una matrice di interfacce [**ITParticipant**](itparticipant.md) che rappresenta i partecipanti coinvolti nell'evento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppParticipant* \[ out\]
</dt> <dd>

Puntatore alla matrice di interfacce [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                           | Significato                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>            | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>   | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>  |
| <dl> <dt>**TAPI \_ E \_ noitems**</dt> </dl> | Nessun partecipante associato all'evento.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>       | Il parametro *ppParticipant* non è un puntatore valido.<br/> |



 

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

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




