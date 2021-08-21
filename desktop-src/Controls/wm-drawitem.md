---
title: WM_DRAWITEM messaggio (Winuser.h)
description: Inviato alla finestra padre di un pulsante, una casella combinata, una casella di riepilogo o un menu disegnato dal proprietario quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f5d4b2addfa2de5f8c76ded636ca29a96fb3af7e0ab4157d25ac26a78c462c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957520"
---
# <a name="wm_drawitem-message"></a>Messaggio \_ WM DRAWITEM

Inviato alla finestra padre di un pulsante, una casella combinata, una casella di riepilogo o un menu disegnato dal proprietario quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.

Una finestra riceve questo messaggio tramite la relativa [*funzione WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il **messaggio WM \_ DRAWITEM.** Se il messaggio è stato inviato da un menu, questo parametro è zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente informazioni sull'elemento da disegnare e sul tipo di disegno richiesto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna il rettangolo di attivazione per un elemento della casella di riepilogo disegnato dal proprietario.

Il *membro itemAction* della [**struttura DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.

Prima di restituire dall'elaborazione di questo messaggio, un'applicazione deve assicurarsi che il contesto di dispositivo identificato dal membro *hDC* della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

