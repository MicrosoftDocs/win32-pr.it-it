---
title: Metodo WSMan.EnumerationFlagReturnObject (WSManDisp.h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagReturnObject da usare nel parametro flags di Session.Enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Metodo EnumerationFlagReturnObject Windows Remote Management
- Metodo EnumerationFlagReturnObject Windows gestione remota , oggetto WSMan
- Metodo EnumerationFlagReturnObject dell'oggetto WSMan Windows gestione remota
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObject
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72d070770cdfe23083dc588ab2111fe9d891d0b8462ee66fa930e2e2fea444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742260"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>Metodo WSMan.EnumerationFlagReturnObject

Il **metodo WSMan.EnumerationFlagReturnObject** restituisce il valore del flag di enumerazione **EnumerationFlagReturnObject** da usare nel parametro *flags* di [**Session.Enumerate**](session-enumerate.md). Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione](session-constants.md).

**EnumerationFlagReturnObject** è una costante **\_ nell'enumerazione WSManEnumFlags** ed è descritta in [**Costanti di enumerazione**](enumeration-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagReturnObject( _
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

 

 





