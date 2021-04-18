---
title: Metodo WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseCredSsp per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUseCredSsp
- Metodo SessionFlagUseCredSsp Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUseCredSsp
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
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476864"
---
# <a name="wsmansessionflagusecredssp-method"></a>WSMan. SessionFlagUseCredSsp, metodo

Restituisce il valore del flag di autenticazione **WSManFlagUseCredSsp** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) . Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante. Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).

**WSManFlagUseCredSsp** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** . Per altre informazioni, vedere [costanti di autenticazione](authentication-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagUseCredSsp( _
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
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                                        |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                                           |
| Componente ridistribuibile<br/>          | Windows Management Framework in Windows Server 2008 con SP2, Windows Vista con SP1 e Windows Vista con SP2<br/> |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>                                      |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl>                                    |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl>                                    |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>                                      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





