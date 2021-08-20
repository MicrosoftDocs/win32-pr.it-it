---
description: Registra una nuova barra delle app e specifica l'identificatore del messaggio che il sistema deve usare per inviare messaggi di notifica. Un'appbar deve inviare questo messaggio prima di inviare qualsiasi altro messaggio della barra delle app.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400439e6808d40eb74c18fa4219109a0abca1973cdac4dcb9de5154384fd0071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460968"
---
# <a name="abm_new-message"></a>Nuovo messaggio ABM \_

Registra una nuova barra delle app e specifica l'identificatore del messaggio che il sistema deve usare per inviare messaggi di notifica. Un'appbar deve inviare questo messaggio prima di inviare qualsiasi altro messaggio della barra delle app.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una [**struttura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che contiene l'handle di finestra e l'identificatore del messaggio della nuova barra dell'app. È necessario specificare i **membri cbSize**, **hWnd** e **uCallbackMessage** quando si invia questo messaggio; tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** in caso di esito positivo oppure **FALSE** se si verifica un errore o se la barra dell'app è già registrata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




