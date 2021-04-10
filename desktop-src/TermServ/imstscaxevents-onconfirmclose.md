---
title: Metodo IMsTscAxEvents OnConfirmClose
description: Chiamato quando il client chiama il Metodo RequestClose di IMsRdpClient.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnConfirmClose
- Metodo OnConfirmClose Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121642"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>Metodo IMsTscAxEvents:: OnConfirmClose

Chiamato quando il client chiama il metodo [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) . In risposta a questo evento, all'utente viene richiesto di confermare la chiusura della connessione. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

## <a name="syntax"></a>Sintassi


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfAllowClose* \[ out\]
</dt> <dd>

Se **Variant \_ true**, il valore predefinito indica che l'utente desidera chiudere la connessione. Se **Variant \_ false** indica che l'utente non desidera chiudere la connessione. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando un'applicazione contenitore chiama il metodo [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , il metodo restituisce un valore che indica se il contenitore deve attendere che si verifichi un evento **OnConfirmClose** prima di chiudere la connessione al controllo. Se **RequestClose** restituisce **controlCloseWaitForEvents** e l'utente è connesso e connesso alla sessione di Servizi Desktop remoto, viene generato l'evento **OnConfirmClose** . A questo punto l'applicazione contenitore può richiedere conferma all'utente, chiedendo se l'utente desidera chiudere la connessione. Se l'utente desidera chiudere la connessione, l'applicazione deve impostare il parametro *pfAllowClose* su **Variant \_ true** e procedere alla chiusura della connessione. Se l'utente non desidera chiudere, l'applicazione deve impostare *pfAllowClose* su **Variant \_ false** e lasciare aperta la connessione.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





