---
description: Pulisce lo stato della sessione aperta o della sessione attualmente aperta.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Funzione WFDDisplaySinkCloseSession (Wfdsink.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7e8169c541535eb2c5adfd0959da47cee4951750687f7d926798534ddc7cbf88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064901"
---
# <a name="wfddisplaysinkclosesession-function"></a>Funzione WFDDisplaySinkCloseSession

Pulisce lo stato della sessione aperta o della sessione attualmente aperta.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSessionHandle* \[ Pollici\]
</dt> <dd>

Handle ricevuto tramite la chiamata [**WFD \_ DISPLAY SINK NOTIFICATION \_ \_ \_ CALLBACK**](wfd-display-sink-notification-callback.md) più recente che ne include una.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ SUCCESS.

## <a name="remarks"></a>Commenti

L'app può chiamare questa funzione per terminare Miracast sessione per qualsiasi motivo. L'app non deve chiamarla quando riceve il **tipo DisconnectedNotification** nel callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink.h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CALLBACK DI NOTIFICA SINK DI VISUALIZZAZIONE WFD \_ \_ \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




