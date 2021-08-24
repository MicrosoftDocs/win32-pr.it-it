---
title: Metodo WSMan.SessionFlagUseDigest (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseDigest da usare nel parametro flags del metodo WSMan.CreateSession.
ms.assetid: dba2448a-4f72-4000-8687-4c1be812fc3b
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagUseDigest Windows Remote Management
- Metodo SessionFlagUseDigest Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota , metodo SessionFlagUseDigest
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseDigest
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 888eec55e2c2ec4efc4613c9fa2bdda2713bcfd1761918f00d29816fb6bf43b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795111"
---
# <a name="wsmansessionflagusedigest-method"></a>Metodo WSMan.SessionFlagUseDigest

Il metodo **WSMan.SessionFlagUseDigest** restituisce il valore del flag di autenticazione **WSManFlagUseDigest** da usare nel parametro *flags* del metodo [**WSMan.CreateSession.**](wsman-createsession.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione](session-constants.md).

**WSManFlagUseDigest** è un valore **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [Costanti di autenticazione](authentication-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUseDigest( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Cambio\]
</dt> <dd>

Valore della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





