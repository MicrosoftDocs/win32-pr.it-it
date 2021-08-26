---
title: WM_MENUSELECT messaggio (Winuser.h)
description: Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1708aabf8ea12bf20c919f1306672358c2966a3d23aa0badccb1f4592c543f3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952221"
---
# <a name="wm_menuselect-message"></a>Messaggio WM \_ MENUSELECT

Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola meno ordinata specifica la voce di menu o l'indice del sottomenu. Se l'elemento selezionato è una voce di comando, questo parametro contiene l'identificatore della voce di menu. Se l'elemento selezionato apre un menu a discesa o un sottomenu, questo parametro contiene l'indice del menu a discesa o del sottomenu nel menu principale e il parametro *lParam* contiene l'handle per il menu principale (selezionato). usare la [**funzione GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) per ottenere l'handle di menu per il menu a discesa o il sottomenu.

La parola più alta specifica uno o più flag di menu. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                             | Significato                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ BITMAP**</dt> <dt>0x00000004L</dt> </dl>                | L'elemento visualizza una bitmap.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_ CHECKED**</dt> <dt>0x00000008L</dt> </dl>             | L'elemento è selezionato.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ DISABLED**</dt> <dt>0x00000002L</dt> </dl>          | La voce è disabilitata.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ GRIGIO**</dt> <dt>0x00000001L</dt> </dl>                | L'elemento è in grigio.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | L'elemento è evidenziato.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | L'elemento viene selezionato con il mouse.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | Item è un elemento disegnato dal proprietario.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>                   | L'elemento apre un menu a discesa o un sottomenu.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | L'elemento è contenuto nel menu della finestra. Il *parametro lParam* contiene un handle per il menu associato al messaggio.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu su cui è stato fatto clic.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Se la parola più alta di *wParam* contiene 0xFFFF e il *parametro lParam* contiene **NULL,** il menu è stato chiuso dal sistema.

Non usare il valore 1 per la parola di ordine superiore di *wParam*, perché questo valore viene specificato come (**UINT**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Se il valore è 0xFFFF, verrà interpretato come 0x0000FFFF, non 1, a causa del cast a **un UINT**.

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

