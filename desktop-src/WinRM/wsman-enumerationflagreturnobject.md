---
title: Metodo WSMan. EnumerationFlagReturnObject (WSManDisp. h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagReturnObject per l'utilizzo nel parametro Flags di Session. enumerate.
ms.assetid: a1d82530-63d7-4050-9e82-e31bec93bf38
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo EnumerationFlagReturnObject
- Metodo EnumerationFlagReturnObject Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo EnumerationFlagReturnObject
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
ms.openlocfilehash: e3019f880503f91d1488a2b7a41574cadc2df987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302328"
---
# <a name="wsmanenumerationflagreturnobject-method"></a>WSMan. EnumerationFlagReturnObject, metodo

Il metodo **WSMan. EnumerationFlagReturnObject** restituisce il valore del flag di enumerazione **EnumerationFlagReturnObject** per l'utilizzo nel parametro *Flags* di [**Session. enumerate**](session-enumerate.md). Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante. Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).

**EnumerationFlagReturnObject** è una costante nell'enumerazione **\_ WSManEnumFlags** ed è descritta in [**costanti di enumerazione**](enumeration-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.EnumerationFlagReturnObject( _
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

 

 





