---
title: Messaggio WM_KILLFOCUS (winuser. h)
description: Inviato a una finestra immediatamente prima che perda lo stato attivo della tastiera.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- Input della tastiera e del mouse WM_KILLFOCUS messaggio
topic_type:
- apiref
api_name:
- WM_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e3bba54f2cdb500ba2ba691ffd30419d5beff1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048227"
---
# <a name="wm_killfocus-message"></a>\_Messaggio KILLFOCUS WM

Inviato a una finestra immediatamente prima che perda lo stato attivo della tastiera.


```C++
#define WM_KILLFOCUS                    0x0008
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra che riceve lo stato attivo della tastiera. Questo parametro può essere **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Se in un'applicazione viene visualizzato un accento circonflesso, il punto di inserimento deve essere eliminato.

Durante l'elaborazione di questo messaggio, non eseguire chiamate di funzione che visualizzano o attivano una finestra. In questo modo il thread genera il controllo e può causare l'interruzione della risposta dei messaggi da parte dell'applicazione. Per ulteriori informazioni, vedere [deadlock dei messaggi](/windows/desktop/winmsg/about-messages-and-message-queues).

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

[**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**\_stato attivo WM**](wm-setfocus.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

