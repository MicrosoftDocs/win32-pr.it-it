---
description: Il \_ metodo Get MediaTypes ottiene i tipi di supporto associati a un partecipante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Metodo ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324234"
---
# <a name="itparticipantget_mediatypes-method"></a>Metodo ITParticipant:: Get \_ MediaTypes

\[**ottenere \_ MediaTypes** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ MediaTypes** ottiene i [**tipi di supporto**](tapimediatype--constants.md) associati a un partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*plMediaType* \[ out\]
</dt> <dd>

Puntatore ai flag del tipo di supporto, ad esempio \_ video TAPIMEDIATYPE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *plMediaType* non è un puntatore valido.<br/>  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**tipi di supporto**](tapimediatype--constants.md)
</dt> </dl>

 

 




