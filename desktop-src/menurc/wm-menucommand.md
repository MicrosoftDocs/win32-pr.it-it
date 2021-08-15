---
title: WM_MENUCOMMAND messaggio (Winuser.h)
description: Inviato quando l'utente effettua una selezione da un menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d97f629b5d4b0c245606b36efea9ebcb230c4c9fd14d837e18949880a7e7e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971810"
---
# <a name="wm_menucommand-message"></a>Messaggio \_ MENUCOMMAND WM

Inviato quando l'utente effettua una selezione da un menu.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero dell'elemento selezionato.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu per l'elemento selezionato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **messaggio \_ WM MENUCOMMAND** fornisce un handle al menu in modo da poter accedere ai dati di menu nella struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) e fornisce anche l'indice dell'elemento selezionato, che in genere è quello necessario per le applicazioni. Al contrario, il [**messaggio WM \_ COMMAND**](wm-command.md) visualizza l'identificatore della voce di menu.

Il **messaggio \_ WM MENUCOMMAND** viene inviato solo per i menu definiti con il flag **MNS \_ NOTIFYBYPOS** impostato nel membro **dwStyle** della [**struttura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Cenni preliminari sui menu](menus.md)
</dt> </dl>

 

 





