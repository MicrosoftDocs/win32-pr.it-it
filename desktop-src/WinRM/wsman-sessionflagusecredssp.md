---
title: Metodo WSMan.SessionFlagUseCredSsp (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseCredSsp da usare nel parametro flags del metodo WSMan.CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagUseCredSsp Windows gestione remota
- Metodo SessionFlagUseCredSsp Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb96f1de72bbcceafd40c0ccbcfdd3b990ed2134739195bd29e130dbac5a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642231"
---
# <a name="wsmansessionflagusecredssp-method"></a>Metodo WSMan.SessionFlagUseCredSsp

Restituisce il valore del flag di autenticazione **WSManFlagUseCredSsp** da usare nel parametro *flags* del [**metodo WSMan.CreateSession.**](wsman-createsession.md) Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione.](session-constants.md)

**WSManFlagUseCredSsp** è una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [Costanti di autenticazione.](authentication-constants.md)

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                                        |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Componente ridistribuibile<br/>          | Windows Management Framework in Windows Server 2008 con SP2, Windows Vista con SP1 e Windows Vista con SP2<br/> |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>                                      |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl>                                    |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





