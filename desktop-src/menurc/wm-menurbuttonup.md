---
title: Messaggio WM_MENURBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- Menu del messaggio WM_MENURBUTTONUP e altre risorse
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341352"
---
# <a name="wm_menurbuttonup-message"></a>\_Messaggio MENURBUTTONUP WM

Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della voce di menu in cui è stato rilasciato il pulsante destro del mouse.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu contenente l'elemento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il messaggio **WM \_ MENURBUTTONUP** consente alle applicazioni di fornire un menu sensibile al contesto denominato anche menu di scelta rapida per la voce di menu specificata in questo messaggio. Per visualizzare un menu sensibile al contesto per una voce di menu, chiamare la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) con la **\_ recurse del TPM**.

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

 

 





