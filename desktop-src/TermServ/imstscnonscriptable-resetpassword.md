---
title: Metodo IMsTscNonScriptable ResetPassword
description: Reimposta tutti gli Stati delle password nel controllo ActiveX Desktop remoto.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ResetPassword
- Metodo ResetPassword Servizi Desktop remoto, interfaccia IMsTscNonScriptable
- Interfaccia IMsTscNonScriptable Servizi Desktop remoto, metodo ResetPassword
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
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478881"
---
# <a name="imstscnonscriptableresetpassword-method"></a>Metodo IMsTscNonScriptable:: ResetPassword

Reimposta tutti gli Stati delle password nel controllo ActiveX Desktop remoto. È possibile chiamare questo metodo per cancellare le password archiviate in uno dei tre formati supportati, ovvero testo non crittografato, codificato portatile o binario (non portabile) codificato. Si noti che le password codificate non devono essere considerate crittografate in modo sicuro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

È possibile chiamare questo metodo per reimpostare la password del controllo dopo la disconnessione. Ciò garantisce che le connessioni successive che usano la stessa istanza del controllo non accedano automaticamente con una password impostata in precedenza.

È possibile chiamare questo metodo solo quando il Desktop remoto controllo ActiveX non si trova nello stato connesso. Questo metodo restituisce **E ha \_ esito negativo** se viene chiamato quando il controllo è connesso. Per verificare lo stato connesso, chiamare il metodo [**get \_ Connected**](imstscax-connected.md) tramite l'interfaccia [**IMsTscAx**](imstscax-interface.md) o una delle interfacce che ereditano da esso.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable è definito come c1e6743a-41C1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





