---
title: Metodo WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUTF8 per l'utilizzo nel parametro Flags di WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUTF8
- Metodo SessionFlagUTF8 Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743215"
---
# <a name="wsmansessionflagutf8-method"></a>WSMan. SessionFlagUTF8, metodo

Il metodo **WSMan. SessionFlagUTF8** restituisce il valore del flag di autenticazione **WSManFlagUTF8** da usare nel parametro *Flags* di [**WSMan. CreateSession**](wsman-createsession.md). Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante. Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).

**WSManFlagUTF8** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** . Per ulteriori informazioni, vedere [altre costanti della sessione](other-session-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUTF8( _
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

 

 





