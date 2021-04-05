---
title: Messaggio WM_XBUTTONDBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- Input della tastiera e del mouse WM_XBUTTONDBLCLK messaggio
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
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742343"
---
# <a name="wm_xbuttondblclk-message"></a>\_Messaggio XBUTTONDBLCLK WM

Inviato quando l'utente fa doppio clic sul primo o sul secondo pulsante X mentre il cursore si trova nell'area client di una finestra. Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore. In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa indica se le varie chiavi virtuali sono inattive. Può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0x0008</dt> di controllo </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON </dl>    | Il pulsante sinistro del mouse è premuto.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON </dl>    | Il pulsante centrale del mouse è inattivo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON </dl>    | Il pulsante destro del mouse è inattivo.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1 </dl> | Il primo pulsante X è inattivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2 </dl> | Il secondo pulsante X è inattivo.<br/>     |



 

La parola più ordinata indica il pulsante su cui è stato fatto doppio clic. Può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                     | Significato                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <dt></dt> <dt>0x0001</dt> XBUTTON1 </dl> | È stato fatto doppio clic sul primo pulsante X.<br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <dt></dt> <dt>0x0002</dt> XBUTTON2 </dl> | È stato fatto doppio clic sul secondo pulsante X.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

La parola di ordine superiore specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**. Per ulteriori informazioni sull'elaborazione del valore restituito, vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere le informazioni nel parametro *wParam* :


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

Solo le finestre con lo stile **cs \_ DBLCLKS** possono ricevere messaggi **WM \_ XBUTTONDBLCLK** , generati dal sistema ogni volta che l'utente preme, rilascia e preme di nuovo un pulsante X entro il limite di tempo doppio clic del sistema. Facendo doppio clic su uno di questi pulsanti vengono effettivamente generati quattro messaggi: [**WM \_ XBUTTONDOWN**](wm-xbuttondown.md), [**WM \_ XBUTTONUP**](wm-xbuttonup.md), **WM \_ XBUTTONDBLCLK** e **WM \_ XBUTTONUP** .

A differenza dei [**messaggi \_ WM LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM \_ MBUTTONDBLCLK**](wm-mbuttondblclk.md)e [**WM \_ RBUTTONDBLCLK**](wm-rbuttondblclk.md) , un'applicazione deve restituire **true** da questo messaggio se viene elaborata. In questo modo si consentirà il software che simula questo messaggio nei sistemi Windows precedenti a Windows 2000 per determinare se la routine della finestra ha elaborato il messaggio o chiamato [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per elaborarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include WINDOWSX. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OTTENERE \_ lo stato di un \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ XBUTTON \_ wParam**](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**GetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[**SetDoubleClickTime**](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[**\_XBUTTONDOWN WM**](wm-xbuttondown.md)
</dt> <dt>

[**\_XBUTTONUP WM**](wm-xbuttonup.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Input del mouse](mouse-input.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

[**PUNTI**](/previous-versions//dd162808(v=vs.85))
</dt> </dl>

 

