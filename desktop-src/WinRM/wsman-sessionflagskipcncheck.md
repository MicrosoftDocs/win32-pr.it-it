---
title: Metodo WSMan.SessionFlagSkipCNCheck (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagSkipCNCheck da usare nel parametro flags di WSMan.CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagSkipCNCheck Windows gestione remota
- Metodo SessionFlagSkipCNCheck Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota , metodo SessionFlagSkipCNCheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCNCheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339246d88dd7dc86e23b1a97442788fb969eb9de5a36f89c4ebadecd9f6e32ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613481"
---
# <a name="wsmansessionflagskipcncheck-method"></a>Metodo WSMan.SessionFlagSkipCNCheck

Il metodo **WSMan.SessionFlagSkipCNCheck** restituisce il valore del flag di autenticazione **WSManFlagSkipCNCheck** da usare nel parametro *flags* di [**WSMan.CreateSession**](wsman-createsession.md). Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione](session-constants.md).

**WSManFlagSkipCNCheck** è una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [**Costanti di autenticazione**](authentication-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagSkipCNCheck( _
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

 

 





