---
title: Messaggio WM_DRAWITEM (winuser. h)
description: Inviato alla finestra padre di un pulsante creato dal proprietario, una casella combinata, una casella di riepilogo o un menu quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Controlli di Windows Message WM_DRAWITEM
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
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741362"
---
# <a name="wm_drawitem-message"></a>Messaggio di WM \_ DrawItem

Inviato alla finestra padre di un pulsante creato dal proprietario, una casella combinata, una casella di riepilogo o un menu quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.

Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ DrawItem** . Se il messaggio è stato inviato da un menu, questo parametro è zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente le informazioni sull'elemento da disegnare e il tipo di disegno necessario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna il rettangolo di attivazione per un elemento della casella di riepilogo creato dal proprietario.

Il membro *itemAction* della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.

Prima di restituire l'elaborazione di questo messaggio, un'applicazione deve garantire che il contesto di dispositivo identificato dal membro *HDC* della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



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

 

