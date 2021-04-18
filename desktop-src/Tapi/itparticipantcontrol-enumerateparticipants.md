---
description: Il metodo EnumerateParticipants enumera i partecipanti associati alla conferenza corrente.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'Metodo ITParticipantControl:: EnumerateParticipants (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324590"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>Metodo ITParticipantControl:: EnumerateParticipants

\[**EnumerateParticipants** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **EnumerateParticipants** enumera i partecipanti associati alla conferenza corrente. Questo metodo viene fornito per le applicazioni C e C++. Le applicazioni client di automazione, ad esempio quelle scritte in Visual Basic, devono usare il metodo [**get \_ participates**](itparticipantcontrol-get-participants.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppEnumParticipants* \[ out\]
</dt> <dd>

Puntatore all'interfaccia [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Valore                                                                                         | Significato                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *ppEnumParticipants* non è un puntatore valido.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/>       |



 

## <a name="remarks"></a>Commenti

TAPI chiama il metodo **AddRef** sull'interfaccia [**IEnumParticipant**](ienumparticipant.md) restituita da **ITParticipantControl:: EnumerateParticipants**. L'applicazione deve chiamare **Release** sull'interfaccia **IEnumParticipant** per liberare risorse associate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**Ricevi \_ i partecipanti**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




