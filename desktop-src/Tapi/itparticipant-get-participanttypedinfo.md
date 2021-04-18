---
description: Il \_ metodo Get ParticipantTypedInfo ottiene una rappresentazione BSTR del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'Metodo ITParticipant:: get_ParticipantTypedInfo (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325595"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>Metodo ITParticipant:: Get \_ ParticipantTypedInfo

\[**ottenere \_ ParticipantTypedInfo** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ ParticipantTypedInfo** ottiene una rappresentazione **BSTR** del tipo di informazioni necessarie, ad esempio PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Partecipante \_ Descrittore di \_ informazioni tipizzato**](participant-typed-info.md) del tipo di informazioni necessarie.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Puntatore alla rappresentazione **BSTR** delle informazioni necessarie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                    | Descrizione                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>           | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ non riescono**</dt> </dl>         | L'archiviazione delle informazioni in *ppInfo* non è riuscita.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | Il parametro *InfoType* non è valido.<br/>               |
| <dl> <dt>**\_puntatore E**</dt> </dl>      | Il parametro *ppInfo* non è un puntatore valido.<br/>       |
| <dl> <dt>**TAPI \_ E \_ noitem**</dt> </dl> | TAPI non contiene informazioni sul tipo specificato.<br/>       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>  | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppInfo* .

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

[**\_informazioni digitate del partecipante \_**](participant-typed-info.md)
</dt> <dt>

[**tipi di supporto**](tapimediatype--constants.md)
</dt> </dl>

 

