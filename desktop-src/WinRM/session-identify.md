---
title: Metodo Session. identifi (WSManDisp. h)
description: Esegue una query su un computer remoto per determinare se supporta il protocollo WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identifica Gestione remota Windows del metodo
- Identifica Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo di identificazione
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302401"
---
# <a name="sessionidentify-method"></a>Metodo Session. identifi

Il metodo **Session. identifi** esegue una query su un computer remoto per determinare se supporta il protocollo WS-Management. Per ulteriori informazioni, vedere [rilevare se un computer remoto supporta il protocollo WS-Management](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Sintassi


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Per inviare la richiesta in modalità autenticata, usare la costante di autenticazione dell'enumerazione **WSManSessionFlags** . Per inviare in modalità non autenticata, usare **WSManFlagUseNoAuthentication**. Per altre informazioni, vedere [**costanti di autenticazione**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa XML che specifica la versione del protocollo WS-Management, il fornitore del sistema operativo e, se la richiesta è stata inviata autenticata, la versione del sistema operativo.

## <a name="remarks"></a>Commenti

**Session. identifit** si basa sull'operazione [protocollo WS-Management](ws-management-protocol.md) definita come wsmanIdentity. Questa operazione viene specificata nel pacchetto SOAP, come indicato di seguito:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Esempio

Nell'esempio VBScript seguente viene inviata una richiesta di identificazione non autenticata al computer remoto denominato Remote nello stesso dominio.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



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

[**Sessione**](session.md)
</dt> <dt>

[**IWSManSession:: identifica**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocollo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

 





