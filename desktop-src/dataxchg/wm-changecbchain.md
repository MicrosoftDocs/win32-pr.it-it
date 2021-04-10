---
title: Messaggio WM_CHANGECBCHAIN (winuser. h)
description: Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando una finestra viene rimossa dalla catena. Una finestra riceve questo messaggio tramite la funzione WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- Scambio di dati del messaggio WM_CHANGECBCHAIN
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
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120043"
---
# <a name="wm_changecbchain-message"></a>\_Messaggio CHANGECBCHAIN WM

Inviato alla prima finestra nella catena del visualizzatore degli Appunti quando una finestra viene rimossa dalla catena.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra da rimuovere dalla catena del visualizzatore degli Appunti.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per la finestra successiva nella catena che segue la finestra da rimuovere. Questo parametro è **null** se la finestra da rimuovere è l'ultima finestra nella catena.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Ogni finestra del visualizzatore degli Appunti Salva l'handle nella finestra successiva della catena del visualizzatore degli Appunti. Inizialmente, questo handle è il valore restituito della funzione [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Quando una finestra del visualizzatore degli Appunti riceve il messaggio **WM \_ CHANGECBCHAIN** , deve chiamare la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) per passare il messaggio alla finestra successiva della catena, a meno che la finestra successiva non sia la finestra da rimuovere. In questo caso, il visualizzatore degli Appunti deve salvare l'handle specificato dal parametro *lParam* come finestra successiva nella catena.

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

**Informazioni concettuali**
</dt> <dt>

[Appunti](clipboard.md)
</dt> </dl>

 

