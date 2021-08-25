---
title: WM_RBUTTONDBLCLK messaggio (Winuser.h)
description: Inviato quando l'utente fa doppio clic sul pulsante destro del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 2db9a947-f052-4738-9fae-6ecaba3de9b9
keywords:
- WM_RBUTTONDBLCLK messaggio Input da tastiera e mouse
topic_type:
- apiref
api_name:
- WM_RBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4b2ee4722825f0404d590d593a2c7f72c815f8cfd2ad4991b0a604c188bfbfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829871"
---
# <a name="wm_rbuttondblclk-message"></a>Messaggio \_ WM RBUTTONDBLCLK

Inviato quando l'utente fa doppio clic sul pulsante destro del mouse mentre il cursore si trova nell'area client di una finestra. Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore. In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_RBUTTONDBLCLK                0x0206
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se varie chiavi virtuali non sono disponibili. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ Controllo**</dt> <dt>0x0008</dt> </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Il pulsante sinistro del mouse è in basso.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Il pulsante centrale del mouse è in basso.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Il pulsante destro del mouse è in basso.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Il primo pulsante X è in basso.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Il secondo pulsante X è in basso.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

La parola più alta specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Solo le finestre con lo stile **CS \_ DBLCLKS** possono ricevere messaggi **WM \_ RBUTTONDBLCLK,** generati dal sistema ogni volta che l'utente preme, rilascia e preme di nuovo il pulsante destro del mouse entro il limite di tempo del doppio clic del sistema. Facendo doppio clic con il pulsante destro del mouse vengono effettivamente generati quattro messaggi: [**WM \_ RBUTTONDOWN,**](wm-rbuttondown.md) [**WM \_ RBUTTONUP,**](wm-rbuttonup.md) **WM \_ RBUTTONDBLCLK** e **WM \_ RBUTTONUP.**

Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Come indicato in precedenza, la coordinata x si trova nell'ordine più basso **del** valore restituito. La coordinata y si trova nell'ordine  più breve **(entrambi** rappresentano valori con segno perché possono assumere valori negativi nei sistemi con più monitor). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

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

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**WM \_ RBUTTONDOWN**](wm-rbuttondown.md)
</dt> <dt>

[**WM \_ RBUTTONUP**](wm-rbuttonup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Mouse Input](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**PUNTI DI APPLICAZIONE**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**Punti**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

