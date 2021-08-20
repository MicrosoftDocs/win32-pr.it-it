---
title: Metodo IMsTscNonScriptable ResetPassword
description: Reimposta tutti gli stati della password nel Desktop remoto ActiveX controllo.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Metodo ResetPassword Servizi Desktop remoto
- Metodo ResetPassword Servizi Desktop remoto, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto , metodo ResetPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b039a66889dcbcab302223003d642dab71545772bb99db82d3ae40ae70cd3ff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118853580"
---
# <a name="imstscnonscriptableresetpassword-method"></a>Metodo IMsTscNonScriptable::ResetPassword

Reimposta tutti gli stati della password nel Desktop remoto ActiveX controllo. È possibile chiamare questo metodo per cancellare le password archiviate in uno dei tre formati supportati: testo non crittografato, codificato portabile o codificato binario (non portabile). Si noti che le password codificate non devono essere considerate crittografate in modo sicuro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="remarks"></a>Commenti

È possibile chiamare questo metodo per reimpostare la password del controllo dopo la disconnessione. In questo modo si garantisce che le connessioni successive che usano la stessa istanza del controllo non accertino automaticamente l'accesso con una password impostata in precedenza.

È possibile chiamare questo metodo solo quando il controllo Desktop remoto ActiveX non si trova nello stato connesso. Questo metodo restituisce **E \_ FAIL** se chiamato quando il controllo è connesso. Per verificare lo stato connesso, chiamare il metodo [**get \_ Connected**](imstscax-connected.md) tramite [**l'interfaccia IMsTscAx**](imstscax-interface.md) o una delle interfacce che eredita da esso.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscNonScriptable IID è definito \_ come c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





