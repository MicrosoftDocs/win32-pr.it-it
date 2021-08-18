---
title: Metodo WSMan.SessionFlagUTF8 (WSManDisp.h)
description: Restituisce il valore del flag di autenticazione WSManFlagUTF8 da usare nel parametro flags di WSMan.CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Metodo SessionFlagUTF8 Windows gestione remota
- Metodo SessionFlagUTF8 Windows gestione remota , oggetto WSMan
- Oggetto WSMan Windows gestione remota , metodo SessionFlagUTF8
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
ms.openlocfilehash: 44fe6cc1b5f18fa316656d2b6974bd47c8209277ed24ef2798479227f9876e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741919"
---
# <a name="wsmansessionflagutf8-method"></a>Metodo WSMan.SessionFlagUTF8

Il **metodo WSMan.SessionFlagUTF8** restituisce il valore del flag di autenticazione **WSManFlagUTF8** da usare nel parametro *flags* di [**WSMan.CreateSession**](wsman-createsession.md). Questo metodo fornisce una sintassi più efficiente per l'uso della costante in modo che gli script non siano necessari per impostare un valore costante. Per altre informazioni su come chiamare questo metodo, vedere [Costanti di sessione](session-constants.md).

**WSManFlagUTF8** è una costante **\_ \_ nell'enumerazione WSManSessionFlags.** Per altre informazioni, vedere [Altre costanti di sessione](other-session-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUTF8( _
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

 

 





