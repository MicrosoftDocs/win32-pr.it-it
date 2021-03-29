---
description: Notifica al sistema che è stato attivato un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio di \_ attivazione WM.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Messaggio ABM_ACTIVATE (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128482"
---
# <a name="abm_activate-message"></a>Messaggio di attivazione di ABM \_

Notifica al sistema che è stato attivato un AppBar. Un AppBar deve chiamare questo messaggio in risposta al messaggio [**di \_ attivazione WM**](/windows/desktop/inputdev/wm-activate) .


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
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

Questo messaggio viene ignorato se il membro **HWND** della struttura a cui punta *pabd* identifica un AppBar di Nascondi automaticamente. Il sistema imposta automaticamente lo z-order per Nascondi automaticamente AppBar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

