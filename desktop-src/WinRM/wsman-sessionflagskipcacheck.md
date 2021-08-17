---
title: Metodo WSMan.SessionFlagSkipCACheck (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagSkipCACheck da usare nel parametro flags di WSMan.CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagSkipCACheck Windows Gestione remota
- Metodo SessionFlagSkipCACheck Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota, metodo SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe24e10ca7a568a6dc9b3af6efed6e31a3a9fde5acac70e2badab37d24373350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742030"
---
# <a name="wsmansessionflagskipcacheck-method"></a>Metodo WSMan.SessionFlagSkipCACheck

Il metodo **WSMan.SessionFlagSkipCACheck** restituisce il valore del flag di autenticazione **WSManFlagSkipCACheck** da usare nel parametro *flags* di [**WSMan.CreateSession**](wsman-createsession.md). Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo ed esempi di codice, vedere [Costanti di sessione](session-constants.md).

**WSManFlagSkipCACheck** è una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [**Costanti di autenticazione**](authentication-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagSkipCACheck( _
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

 

 





