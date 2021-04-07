---
title: Messaggio WM_SETCURSOR (winuser. h)
description: Inviato a una finestra se il mouse determina lo spostamento del cursore all'interno di una finestra e l'input del mouse non viene acquisito.
ms.assetid: b722689e-925f-40ac-ba4a-55be9dc6a8f8
keywords:
- Menu del messaggio WM_SETCURSOR e altre risorse
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
ms.openlocfilehash: e941919b447659e67fdcdd9e4e5f4ff2630f8bf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048452"
---
# <a name="wm_setcursor-message"></a>\_Messaggio di cursore WM

Inviato a una finestra se il mouse determina lo spostamento del cursore all'interno di una finestra e l'input del mouse non viene acquisito.


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

La parola di ordine inferiore di *lParam* specifica il risultato dell'hit test per la posizione del cursore. Per i valori possibili, vedere i valori restituiti per [WM_NCHITTEST](../inputdev/wm-nchittest.md) .

La parola più ordinata di *lParam* specifica il messaggio della finestra del mouse che ha generato l'evento, ad esempio [WM_MOUSEMOVE](../inputdev/wm-mousemove.md). Quando la finestra entra in modalità menu, questo valore è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true** per arrestare l'ulteriore elaborazione o **false** per continuare.

## <a name="remarks"></a>Commenti

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowprocw) passa il messaggio del **\_ cursore WM** a una finestra padre prima dell'elaborazione. Se la finestra padre restituisce **true**, l'ulteriore elaborazione viene interrotta. Se si passa il messaggio alla finestra padre di una finestra, il controllo della finestra padre viene posizionato sull'impostazione del cursore in una finestra figlio. La funzione **DefWindowProc** utilizza inoltre questo messaggio per impostare il cursore su una freccia se non è presente nell'area client o sul cursore della classe registrata se si trova nell'area client. Se la parola di ordine inferiore del parametro *lParam* è **HTERROR** e la parola più significativa di *lParam* specifica che uno dei pulsanti del mouse è premuto, **DefWindowProc** chiama la funzione [**MessageBeep**](/windows/desktop/api/winuser/nf-winuser-messagebeep) .

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

 

