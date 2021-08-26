---
title: WM_SETCURSOR messaggio (Winuser.h)
description: Inviato a una finestra se il mouse fa sì che il cursore si sposti all'interno di una finestra e l'input del mouse non viene acquisito.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- WM_SETCURSOR menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_SETCURSOR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19dccc4fab0d24dd233133e97b3ddcc71f615d9abb27a4684821099b6ad15802
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846871"
---
# <a name="wm_setcursor-message"></a>Messaggio \_ WM SETCURSOR

Inviato a una finestra se il mouse fa sì che il cursore si sposti all'interno di una finestra e l'input del mouse non viene acquisito.


```C++
#define WM_SETCURSOR                    0x0020
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra che contiene il cursore.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa di *lParam* specifica il risultato dell'hit test per la posizione del cursore. Vedere i valori restituiti per [WM_NCHITTEST](../inputdev/wm-nchittest.md) per i valori possibili.

La parola più alta di *lParam* specifica il messaggio della finestra del mouse che ha attivato questo evento, ad esempio [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Quando la finestra entra in modalità menu, questo valore è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE** per interrompere l'ulteriore elaborazione o **FALSE** per continuare.

## <a name="remarks"></a>Commenti

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) passa il **messaggio WM \_ SETCURSOR** a una finestra padre prima dell'elaborazione. Se la finestra padre restituisce **TRUE,** l'ulteriore elaborazione viene interrotta. Il passaggio del messaggio alla finestra padre di una finestra consente alla finestra padre di controllare l'impostazione del cursore in una finestra figlio. La **funzione DefWindowProc** usa anche questo messaggio per impostare il cursore su una freccia se non si trova nell'area client o sul cursore della classe registrata se si trova nell'area client. Se la parola più bassa del parametro *lParam* è **HTERROR** e la parola di ordine superiore *di lParam* specifica che viene premuto uno dei pulsanti del mouse, **DefWindowProc** chiama la funzione [**MessageBeep.**](/windows/desktop/api/winuser/nf-winuser-messagebeep)

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cursori](cursors.md)
</dt> </dl>

 

