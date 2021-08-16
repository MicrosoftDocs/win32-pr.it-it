---
title: WM_XBUTTONDBLCLK messaggio (Winuser.h)
description: Pubblicato quando l'utente fa doppio clic sul primo o secondo pulsante X mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f15ed64871cee3b5a97ad8067e883d7ad31206896f6b20150acdb490a2f44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757150"
---
# <a name="wm_xbuttondblclk-message"></a>Messaggio \_ WM XBUTTONDBLCLK

Pubblicato quando l'utente fa doppio clic sul primo o secondo pulsante X mentre il cursore si trova nell'area client di una finestra. Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore. In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola di ordine basso indica se varie chiavi virtuali sono in stato di insoddggi. Può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Controllo**</dt> <dt>0x0008</dt> </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Il pulsante sinistro del mouse è in basso.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Il pulsante centrale del mouse è in basso.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Il pulsante destro del mouse è verso il basso.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Il primo pulsante X è in basso.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Il secondo pulsante X è in basso.<br/>     |



 

La parola di ordine alto indica il pulsante su cui è stato fatto doppio clic. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt>**XBUTTON1**</dt> <dt>0x0001</dt> </dl> | È stato fatto doppio clic sul primo pulsante X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt>**XBUTTON2**</dt> <dt>0x0002</dt> </dl> | È stato fatto doppio clic sul secondo pulsante X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

La parola più alta specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.** Per altre informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel *parametro wParam:*


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Come indicato in precedenza, la coordinata x si trova nell'ordine più basso **del** valore restituito. la coordinata y è nell'ordine più  alto **(entrambe** rappresentano valori firmati perché possono assumere valori negativi nei sistemi con più monitor). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

Solo le finestre con lo stile **\_ CS DBLCLKS** possono ricevere messaggi **WM \_ XBUTTONDBLCLK** generati dal sistema ogni volta che l'utente preme, rilascia e di nuovo preme un pulsante X entro il limite di tempo del doppio clic del sistema. Facendo doppio clic su uno di questi pulsanti vengono effettivamente generati quattro messaggi: [**WM \_ XBUTTONDOWN,**](wm-xbuttondown.md) [**WM \_ XBUTTONUP,**](wm-xbuttonup.md) **WM \_ XBUTTONDBLCLK** e **WM \_ XBUTTONUP.**

A differenza dei messaggi [**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)e [**WM \_ RBUTTONDBLCLK,**](wm-rbuttondblclk.md) un'applicazione deve restituire **TRUE** da questo messaggio se lo elabora. In questo modo il software che simula questo messaggio nei sistemi Windows precedenti Windows 2000 sarà in grado di determinare se la routine della finestra ha elaborato il messaggio o ha chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windowsx.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ KEYSTATE \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ XBUTTON \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ XBUTTONDOWN**](wm-xbuttondown.md)
</dt> <dt>

[**WM \_ XBUTTONUP**](wm-xbuttonup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINT**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

