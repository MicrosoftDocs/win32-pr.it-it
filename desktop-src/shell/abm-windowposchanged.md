---
description: Notifica al sistema la modifica della posizione di un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Messaggio ABM_WINDOWPOSCHANGED (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484396"
---
# <a name="abm_windowposchanged-message"></a>\_Messaggio WINDOWPOSCHANGED ABM

Notifica al sistema la modifica della posizione di un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) .


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pabd* 
</dt> <dd>

Puntatore a una struttura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) che identifica il AppBar da attivare. Quando si invia questo messaggio, è necessario specificare i membri **cbSize** e **HWND** . tutti gli altri membri vengono ignorati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Questo messaggio viene ignorato se il membro **HWND** della struttura a cui punta *pabd* identifica un AppBar di Nascondi automaticamente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

