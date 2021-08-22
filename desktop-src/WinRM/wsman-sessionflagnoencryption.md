---
title: Metodo WSMan.SessionFlagNoEncryption (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagNoEncryption da usare nel parametro flags del metodo WSMan.CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagNoEncryption Windows gestione remota
- Metodo SessionFlagNoEncryption Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota , metodo SessionFlagNoEncryption
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22b1f3e278a5deafc890ee8aacf21e36174255dac82fc123647e890323a34b28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613501"
---
# <a name="wsmansessionflagnoencryption-method"></a>Metodo WSMan.SessionFlagNoEncryption

Il metodo **WSMan.SessionFlagNoEncryption** restituisce il valore del flag di autenticazione **WSManFlagNoEncryption** da usare nel parametro *flags* del metodo [**WSMan.CreateSession.**](wsman-createsession.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**WSManFlagNoEncryption è** una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [Altre costanti di sessione.](other-session-constants.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagNoEncryption( _
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

 

 





