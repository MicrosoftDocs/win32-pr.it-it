---
title: WM_CHANGECBCHAIN messaggio (Winuser.h)
description: Inviato alla prima finestra nella catena del visualizzatore Appunti quando una finestra viene rimossa dalla catena. Una finestra riceve questo messaggio tramite la relativa funzione WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN messaggio Dati Exchange
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25dac74784a214f77f8b2912e2fd643624ae767027121e2262d81989d54d3831
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736315"
---
# <a name="wm_changecbchain-message"></a>Messaggio \_ WM CHANGECBCHAIN

Inviato alla prima finestra nella catena del visualizzatore Appunti quando una finestra viene rimossa dalla catena.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra da rimuovere dalla catena del visualizzatore appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra successiva nella catena dopo la rimozione della finestra. Questo parametro è **NULL** se la finestra da rimuovere è l'ultima finestra della catena.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Ogni finestra del visualizzatore Appunti salva l'handle nella finestra successiva nella catena del visualizzatore Appunti. Inizialmente, questo handle è il valore restituito della [**funzione SetClipboardViewer.**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

Quando una finestra del visualizzatore Appunti riceve il messaggio **WM \_ CHANGECBCHAIN,** deve chiamare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per passare il messaggio alla finestra successiva della catena, a meno che la finestra successiva non sia la finestra da rimuovere. In questo caso, il visualizzatore appunti deve salvare l'handle specificato dal *parametro lParam* come finestra successiva nella catena.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

