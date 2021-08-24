---
description: Il metodo put \_ LocalParticipantTypedInfo imposta le informazioni sui partecipanti.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: Metodo ITLocalParticipant::p ut_LocalParticipantTypedInfo (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acca83d7ad68ed0974aaa2e7d4fb4755c11939d0711473c406cb09d78451ac41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774901"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>Metodo ITLocalParticipant::p ut \_ LocalParticipantTypedInfo

Il **metodo put \_ LocalParticipantTypedInfo** imposta le informazioni sui partecipanti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ Pollici\]
</dt> <dd>

[**PARTECIPANTE \_ Identificatore TYPED \_ INFO**](participant-typed-info.md) del tipo di informazioni necessarie.

</dd> <dt>

*ppInfo* \[ Pollici\]
</dt> <dd>

**BSTR** contenente il nuovo valore necessario per le informazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

L'applicazione deve [usare SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il *parametro ppInfo* e [usare SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**INFORMAZIONI \_ DIGITATE DAL \_ PARTECIPANTE**](participant-typed-info.md)
</dt> </dl>

 

