---
description: Pulisce lo stato della sessione aperta o della sessione attualmente aperta.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Funzione WFDDisplaySinkCloseSession (Wfdsink. h)
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
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528159"
---
# <a name="wfddisplaysinkclosesession-function"></a>WFDDisplaySinkCloseSession (funzione)

Pulisce lo stato della sessione aperta o della sessione attualmente aperta.

## <a name="syntax"></a>Sintassi


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSessionHandle* \[ in\]
</dt> <dd>

Il punto di controllo ricevuto tramite la [**\_ \_ \_ \_ richiamata del callback della notifica del sink di visualizzazione**](wfd-display-sink-notification-callback.md) più recente che ne include uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.

## <a name="remarks"></a>Commenti

L'app può chiamare questa funzione per terminare la sessione Miracast per qualsiasi motivo. Non è necessario che l'app lo chiami quando riceve il tipo **DisconnectedNotification** nel callback.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows 10<br/>                                                                      |
| Fine del supporto server<br/>    | Windows Server 2016<br/>                                                             |
| Intestazione<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**richiamata della notifica del sink di \_ visualizzazione della direttiva. \_ \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




