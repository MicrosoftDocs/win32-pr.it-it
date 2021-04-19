---
description: Il \_ metodo Get LocalParticipantTypedInfo ottiene informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Metodo ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330375"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Metodo ITLocalParticipant:: Get \_ LocalParticipantTypedInfo

Il metodo **get \_ LocalParticipantTypedInfo** ottiene informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Partecipante \_ Identificatore di \_ informazioni tipizzato**](participant-typed-info.md) di tipo delle informazioni necessarie.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Puntatore a un **BSTR** che conterrà le informazioni necessarie in seguito a una restituzione corretta del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'applicazione deve usare [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppInfo* .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**\_informazioni digitate del partecipante \_**](participant-typed-info.md)
</dt> </dl>

 

