---
title: WM_LBUTTONDOWN messaggio (Winuser.h)
description: Pubblicato quando l'utente preme il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- WM_LBUTTONDOWN messaggio Input tastiera e mouse
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 8521bc5319919855f734f6b7ac75a58af1af99a58ca360e833984649eb574bbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351621"
---
# <a name="wm_lbuttondown-message"></a>Messaggio WM \_ LBUTTONDOWN

Pubblicato quando l'utente preme il pulsante sinistro del mouse mentre il cursore si trova nell'area client di una finestra. Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore. In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se varie chiavi virtuali non sono disponibili. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                               | Significato                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <dt>**MK \_ CONTROLLO**</dt> <dt>0x0008</dt> </dl>    | Il tasto CTRL è premuto.<br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <dt>**MK \_ LBUTTON**</dt> <dt>0x0001</dt> </dl>    | Il pulsante sinistro del mouse è in basso.<br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <dt>**MK \_ MBUTTON**</dt> <dt>0x0010</dt> </dl>    | Il pulsante centrale del mouse è in basso.<br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <dt>**MK \_ RBUTTON**</dt> <dt>0x0002</dt> </dl>    | Il pulsante destro del mouse è verso il basso.<br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <dt>**MK \_ MAIUSC**</dt> <dt>0x0004</dt> </dl>          | Il tasto MAIUSC è premuto.<br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt> </dl> | Il primo pulsante X è in basso.<br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt> </dl> | Il secondo pulsante X è in basso.<br/>     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

La parola più alta specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="example"></a>Esempio


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

Per altri esempi, [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples) in GitHub.

## <a name="remarks"></a>Commenti

Come indicato in precedenza, la coordinata x si trova nell'ordine più basso **del** valore restituito. la coordinata y è nell'ordine più  alto **(** entrambe rappresentano valori firmati perché possono assumere valori negativi nei sistemi con più monitor). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

Per rilevare che il tasto ALT è stato premuto, controllare se [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) con **VK \_ MENU** < 0. Si noti che non deve essere [**GetAsyncKeyState.**](/windows/win32/api/winuser/nf-winuser-getasynckeystate)

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

[**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[**SetCapture**](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[**WM \_ LBUTTONDBLCLK**](wm-lbuttondblclk.md)
</dt> <dt>

[**WM \_ LBUTTONUP**](wm-lbuttonup.md)
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

 

