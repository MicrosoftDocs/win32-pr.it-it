---
title: Messaggio WM_DRAWCLIPBOARD (winuser. h)
description: Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando il contenuto degli Appunti viene modificato. Ciò consente a una finestra del visualizzatore degli Appunti di visualizzare il nuovo contenuto degli Appunti. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- Scambio di dati del messaggio WM_DRAWCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301598"
---
# <a name="wm_drawclipboard-message"></a>\_Messaggio DRAWCLIPBOARD WM

Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando il contenuto degli Appunti viene modificato. Ciò consente a una finestra del visualizzatore degli Appunti di visualizzare il nuovo contenuto degli Appunti.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo messaggio viene ricevuto solo dalle finestre del visualizzatore degli Appunti. Si tratta di finestre che sono state aggiunte alla catena del visualizzatore degli Appunti tramite la funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Ogni finestra che riceve il messaggio **WM \_ DRAWCLIPBOARD** deve chiamare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per passare il messaggio alla finestra successiva nella catena del visualizzatore degli Appunti. L'handle per la finestra successiva nella catena viene restituito da [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)e può cambiare in risposta a un messaggio [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**\_CHANGECBCHAIN WM**](wm-changecbchain.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

