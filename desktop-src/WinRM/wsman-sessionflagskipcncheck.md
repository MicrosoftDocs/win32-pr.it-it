---
title: Metodo WSMan. SessionFlagSkipCNCheck (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagSkipCNCheck per l'utilizzo nel parametro Flags di WSMan. CreateSession.
ms.assetid: 44884a9d-ec5f-4822-945d-2681d214a902
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagSkipCNCheck
- Metodo SessionFlagSkipCNCheck Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagSkipCNCheck
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
ms.openlocfilehash: c98981ac166ea7b1b76f1ab322db6c48679a4bf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964496"
---
# <a name="wsmansessionflagskipcncheck-method"></a>WSMan. SessionFlagSkipCNCheck, metodo

Il metodo **WSMan. SessionFlagSkipCNCheck** restituisce il valore del flag di autenticazione **WSManFlagSkipCNCheck** da usare nel parametro *Flags* di [**WSMan. CreateSession**](wsman-createsession.md). Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante. Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).

**WSManFlagSkipCNCheck** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** . Per altre informazioni, vedere [**costanti di autenticazione**](authentication-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagSkipCNCheck( _
  ByRef flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ out\]
</dt> <dd>

Valore della costante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





