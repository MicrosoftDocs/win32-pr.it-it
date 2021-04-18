---
title: Messaggio WM_RBUTTONUP (winuser. h)
description: Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 12d148ba-9324-4db3-b537-b2cd4d0b8f32
keywords:
- Input della tastiera e del mouse WM_RBUTTONUP messaggio
topic_type:
- apiref
api_name:
- WM_RBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85a1426b92e8f3aa05c25b551b42ce271b35c673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302389"
---
# <a name="wm_rbuttonup-message"></a>\_Messaggio RBUTTONUP WM

Inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova nell'area client di una finestra. Se il mouse non viene acquisito, il messaggio viene inserito nella finestra sotto il cursore. In caso contrario, il messaggio viene inserito nella finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RBUTTONUP                    0x0205
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se varie chiavi virtuali sono inattive. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_**</dt> <dt>0x0008</dt> di controllo </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0001</dt> LBUTTON </dl>    | Il pulsante sinistro del mouse è premuto.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0010</dt> MBUTTON </dl>    | Il pulsante centrale del mouse è inattivo.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_**</dt> <dt>0x0002</dt> RBUTTON </dl>    | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_**</dt> <dt>0x0020</dt> XBUTTON1 </dl> | Il primo pulsante X è inattivo.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_**</dt> <dt>0x0040</dt> XBUTTON2 </dl> | Il secondo pulsante X è inattivo.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

La parola di ordine superiore specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire zero.

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

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

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetCapture**](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**\_RBUTTONDBLCLK WM**](wm-rbuttondblclk.md)
</dt> <dt>

[**\_RBUTTONDOWN WM**](wm-rbuttondown.md)
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

 

