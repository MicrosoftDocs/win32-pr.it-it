---
description: Il \_ metodo Put LocalParticipantTypedInfo imposta le informazioni sul partecipante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant: metodo:p ut_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330372"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ITLocalParticipant::p UT \_ LocalParticipantTypedInfo metodo

Il metodo **put \_ LocalParticipantTypedInfo** imposta le informazioni sul partecipante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ in\]
</dt> <dd>

[**Partecipante \_ Identificatore \_ info tipizzato**](participant-typed-info.md) del tipo di informazioni richieste.

</dd> <dt>

*ppInfo* \[ in\]
</dt> <dd>

**BSTR** che contiene il nuovo valore necessario per le informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'applicazione deve usare [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PpInfo* e usare [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

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

 

