---
title: Messaggio WM_MENUSELECT (winuser. h)
description: Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- Menu del messaggio WM_MENUSELECT e altre risorse
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
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302727"
---
# <a name="wm_menuselect-message"></a>\_Messaggio MENUSELECT WM

Inviato alla finestra proprietaria di un menu quando l'utente seleziona una voce di menu.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine inferiore specifica la voce di menu o l'indice del sottomenu. Se l'elemento selezionato è un elemento di comando, questo parametro contiene l'identificatore della voce di menu. Se l'elemento selezionato apre un menu a discesa o un sottomenu, questo parametro contiene l'indice del menu a discesa o del sottomenu nel menu principale e il parametro *lParam* contiene l'handle per il menu principale (selezionato); usare la funzione [**getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) per ottenere l'handle di menu nel menu a discesa o nel sottomenu.

La parola più ordinata specifica uno o più flag di menu. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                             | Significato                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_ BITMAP**</dt> <dt>0x00000004L</dt> </dl>                | Elemento consente di visualizzare una bitmap.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_**</dt> <dt>0x00000008L</dt> selezionata </dl>             | L'elemento è selezionato.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ 0x00000002L DISABILITAto**</dt> <dt></dt> </dl>          | La voce è disabilitata.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_**</dt> <dt>0x00000001L</dt> grigio </dl>                | L'elemento è disattivato.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_**</dt> <dt>0x00000080L</dt> HILITE </dl>                | L'elemento è evidenziato.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_**</dt> <dt>0x00008000L</dt> MOUSESELECT </dl> | L'elemento viene selezionato con il mouse.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_**</dt> <dt>0x00000100L</dt> OWNERDRAW </dl>       | Item è un elemento creato dal proprietario.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ POPUP**</dt> <dt>0x00000010L</dt> </dl>                   | Elemento consente di aprire un menu a discesa o un sottomenu.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_**</dt> <dt>0x00002000L</dt> SYSMENU </dl>             | L'elemento è contenuto nel menu finestra. Il parametro *lParam* contiene un handle per il menu associato al messaggio.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per il menu su cui è stato fatto clic.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Se la parola più ordinata di *wParam* contiene 0xFFFF e il parametro *lParam* contiene **null**, il menu è stato chiuso dal sistema.

Non usare il valore 1 per la parola più ordinata di *wParam*, perché questo valore è specificato come (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Se il valore è 0xFFFF, verrebbe interpretato come 0x0000FFFF, non 1, a causa del cast a **uint**.

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

[**Getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

 

