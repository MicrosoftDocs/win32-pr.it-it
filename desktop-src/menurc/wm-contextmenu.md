---
title: WM_CONTEXTMENU messaggio (Winuser.h)
description: Notifica a una finestra che l'utente ha fatto clic con il pulsante destro del mouse (con il pulsante destro del mouse) nella finestra.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU messaggio Menu e altre risorse
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472506"
---
# <a name="wm_contextmenu-message"></a>Messaggio \_ WM CONTEXTMENU

Notifica a una finestra che l'utente desidera visualizzare un menu di scelta rapida.  L'utente potrebbe aver fatto clic con il pulsante destro del mouse (con il pulsante destro del mouse) nella finestra, premuto MAIUSC+F10 o premuto il tasto applicazioni (tasto del menu di scelta rapida) disponibile in alcune tastiere.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle della finestra in cui l'utente ha fatto clic con il pulsante destro del mouse. Può trattarsi di una finestra figlio della finestra che riceve il messaggio. Per altre informazioni sull'elaborazione di questo messaggio, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine basso specifica la posizione orizzontale del cursore, in coordinate dello schermo, al momento del clic del mouse.

La parola più alta specifica la posizione verticale del cursore, in coordinate dello schermo, al momento del clic del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Una finestra può elaborare questo messaggio visualizzando un menu di scelta rapida usando le [**funzioni TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Per ottenere le posizioni orizzontale e verticale, usare il codice seguente.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Se una finestra non visualizza un menu di scelta rapida, deve passare questo messaggio alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Se una finestra è una finestra figlio, **DefWindowProc** invia il messaggio all'elemento padre. In caso **contrario, DefWindowProc** visualizza un menu di scelta rapida predefinito se la posizione specificata si trova nella didascalia della finestra.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera il **messaggio WM \_ CONTEXTMENU** quando elabora il messaggio [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o quando l'utente preme MAIUSC+F10. Il **messaggio WM \_ CONTEXTMENU** viene generato anche quando l'utente preme e rilascia il [**tasto VK \_ APPS.**](/windows/desktop/inputdev/virtual-key-codes)

Se il menu di scelta rapida viene generato dalla tastiera, ad esempio, se l'utente preme MAIUSC+F10, le coordinate x e y sono -1 e l'applicazione deve visualizzare il menu di scelta rapida nella posizione della selezione corrente anziché in (xPos, yPos).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

