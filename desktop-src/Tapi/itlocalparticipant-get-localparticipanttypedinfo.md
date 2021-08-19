---
description: Il metodo get LocalParticipantTypedInfo ottiene le informazioni sul partecipante, ad esempio \_ il nome di posta elettronica o la posizione geografica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: Metodo ITLocalParticipant::get_LocalParticipantTypedInfo (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41afb4c55ba769e341b81e5ec1ca721745509ba8bf2bdfd88ae22ebc48bb535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003369"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>Metodo ITLocalParticipant::get \_ LocalParticipantTypedInfo

Il **metodo get \_ LocalParticipantTypedInfo** ottiene le informazioni sul partecipante, ad esempio il nome di posta elettronica o la posizione geografica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InfoType* \[ Pollici\]
</dt> <dd>

[**PARTECIPANTE \_ Identificatore TYPED \_ INFO**](participant-typed-info.md) del tipo di informazioni necessarie.

</dd> <dt>

*ppInfo* \[ Cambio\]
</dt> <dd>

Puntatore a **un oggetto BSTR** che conterrà le informazioni necessarie dopo la corretta restituzione del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

L'applicazione deve [usare SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il *parametro ppInfo.*

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

 

