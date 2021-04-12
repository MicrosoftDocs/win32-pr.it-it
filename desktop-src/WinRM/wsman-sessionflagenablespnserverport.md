---
title: Metodo WSMan. SessionFlagEnableSPNServerPort (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagEnableSPNServerPort per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagEnableSPNServerPort
- Metodo SessionFlagEnableSPNServerPort Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagEnableSPNServerPort
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518136"
---
# <a name="wsmansessionflagenablespnserverport-method"></a>WSMan. SessionFlagEnableSPNServerPort, metodo

Il metodo **WSMan. SessionFlagEnableSPNServerPort** restituisce il valore del flag di autenticazione **WSManFlagEnableSPNServerPort** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) . Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante. Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).

**WSManFlagEnableSPNServerPort** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** . Per ulteriori informazioni, vedere [**altre costanti della sessione**](other-session-constants.md).

## <a name="syntax"></a>Sintassi


```VB
WSMan.SessionFlagEnableSPNServerPort( _
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

 

 





