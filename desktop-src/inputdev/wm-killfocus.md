---
title: WM_KILLFOCUS messaggio (Winuser.h)
description: Inviato a una finestra immediatamente prima di perdere lo stato attivo della tastiera.
ms.assetid: 6d32a09b-a856-4f94-9544-3345b3a700f4
keywords:
- WM_KILLFOCUS messaggio Input tastiera e mouse
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
ms.openlocfilehash: 644ea7d82a2ae3f316985a882c284d77f3869a75341142d4372b612d66ada1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757455"
---
# <a name="wm_killfocus-message"></a>Messaggio \_ KILLFOCUS WM

Inviato a una finestra immediatamente prima di perdere lo stato attivo della tastiera.


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

Se un'applicazione visualizza un punto di inserimento, il punto di inserimento deve essere eliminato a questo punto.

Durante l'elaborazione di questo messaggio, non effettuare chiamate di funzione che visualizzano o attivano una finestra. In questo modo il thread produce il controllo e può causare l'arresto dell'applicazione ai messaggi. Per altre informazioni, vedere [Deadlock dei messaggi](/windows/desktop/winmsg/about-messages-and-message-queues).

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

[**Setfocus**](/windows/win32/api/winuser/nf-winuser-setfocus)
</dt> <dt>

[**WM \_ SETFOCUS**](wm-setfocus.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input da tastiera](keyboard-input.md)
</dt> </dl>

 

