---
title: Messaggio WM_MENUCOMMAND (winuser. h)
description: Inviato quando l'utente effettua una selezione da un menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- Menu del messaggio WM_MENUCOMMAND e altre risorse
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
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400934"
---
# <a name="wm_menucommand-message"></a>Messaggio dell'MENUCOMMAND di WM \_

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

Il messaggio **WM \_ MENUCOMMAND** fornisce un handle per il menu in modo da poter accedere ai dati del menu nella struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) e fornisce anche l'indice dell'elemento selezionato, che corrisponde in genere alle applicazioni necessarie. Al contrario, il messaggio del [**\_ comando WM**](wm-command.md) fornisce l'identificatore della voce di menu.

Il **messaggio WM \_ MENUCOMMAND** viene inviato solo per i menu definiti con il flag **\_ NOTIFYBYPOS di MNS** impostato nel membro **dwStyle** della struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica sui menu](menus.md)
</dt> </dl>

 

 





