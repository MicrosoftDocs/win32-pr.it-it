---
description: Registra un nuovo AppBar e specifica l'identificatore del messaggio che il sistema deve utilizzare per inviare i messaggi di notifica. Un AppBar deve inviare questo messaggio prima di inviare altri messaggi di AppBar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Messaggio ABM_NEW (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750311"
---
# <a name="abm_new-message"></a>\_Nuovo messaggio di ABM

Registra un nuovo AppBar e specifica l'identificatore del messaggio che il sistema deve utilizzare per inviare i messaggi di notifica. Un AppBar deve inviare questo messaggio prima di inviare altri messaggi di AppBar.


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che contiene il nuovo handle della finestra di AppBar e l'identificatore del messaggio. Quando si invia questo messaggio, è necessario specificare i membri **cbSize**, **HWND** e **uCallbackMessage** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se ha esito positivo o **false** se si verifica un errore o se il AppBar è già registrato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




