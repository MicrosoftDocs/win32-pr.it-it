---
title: Metodo IMsTscAxEvents OnConfirmClose
description: Chiamato quando il client chiama il metodo IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Metodo OnConfirmClose Servizi Desktop remoto
- Metodo OnConfirmClose Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto , metodo OnConfirmClose
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
ms.openlocfilehash: 2effd50552ab227e8e065844b8b19da0e022f6b8e36d1d86701ad0614b821126
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512471"
---
# <a name="imstscaxeventsonconfirmclose-method"></a>Metodo IMsTscAxEvents::OnConfirmClose

Chiamato quando il client chiama il [**metodo IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md) In risposta a questo evento, all'utente deve essere richiesto di confermare la chiusura della connessione. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

## <a name="syntax"></a>Sintassi


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pfAllowClose* \[ Cambio\]
</dt> <dd>

Se **VARIANT \_ TRUE**, il valore predefinito indica che l'utente vuole chiudere la connessione. Se **VARIANT \_ FALSE,** indica che l'utente non vuole chiudere la connessione. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Quando un'applicazione contenitore chiama il metodo [**IMsRdpClient::RequestClose,**](imsrdpclient-requestclose.md) tale metodo restituisce un valore che indica se il contenitore deve attendere che si verifichi un evento **OnConfirmClose** prima di chiudere la connessione del controllo. Se **RequestClose** restituisce **controlCloseWaitForEvents** e l'utente è connesso e connesso alla sessione Servizi Desktop remoto, viene generato l'evento **OnConfirmClose.** A questo punto l'applicazione contenitore può chiedere all'utente se vuole chiudere la connessione. Se l'utente vuole chiudere la connessione, l'applicazione deve impostare il *parametro pfAllowClose* su **VARIANT \_ TRUE** e procedere con la chiusura della connessione. Se l'utente non vuole chiudere, l'applicazione deve impostare *pfAllowClose* su **VARIANT \_ FALSE** e lasciare aperta la connessione.

Per altre informazioni sui Connessione Web Desktop remoto, vedere [Requisiti per Connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





