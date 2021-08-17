---
title: Metodo WSMan.SessionFlagUseBasic (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseBasic da usare nel parametro flags del metodo WSMan.CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagUseBasic Windows gestione remota
- Metodo SessionFlagUseBasic Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo SessionFlagUseBasic
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf908ad4cbe70f9480c23dbc26d5a0593212a285cd541ad70605e990e30792d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742003"
---
# <a name="wsmansessionflagusebasic-method"></a>Metodo WSMan.SessionFlagUseBasic

Il **metodo WSMan.SessionFlagUseBasic** restituisce il valore del flag di autenticazione **WSManFlagUseBasic** da usare nel parametro *flags* del [**metodo WSMan.CreateSession.**](wsman-createsession.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**WSManFlagUseBasic** è una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [**Costanti di autenticazione.**](authentication-constants.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUseBasic( _
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

 

 





