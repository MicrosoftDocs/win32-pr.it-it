---
title: Messaggio WM_CONTEXTMENU (winuser. h)
description: Notifica a una finestra che l'utente ha fatto clic con il pulsante destro del mouse sulla finestra.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- Menu del messaggio WM_CONTEXTMENU e altre risorse
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
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301482"
---
# <a name="wm_contextmenu-message"></a>Messaggio del ContextMenu di WM \_

Notifica a una finestra che l'utente desidera visualizzare un menu di scelta rapida.  È possibile che l'utente abbia fatto clic con il pulsante destro del mouse sulla finestra, ha premuto MAIUSC + F10 o ha premuto il tasto Applications (menu di scelta rapida) disponibile in alcune tastiere.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra in cui l'utente ha fatto clic con il pulsante destro del mouse. Può trattarsi di una finestra figlio della finestra che riceve il messaggio. Per ulteriori informazioni sull'elaborazione di questo messaggio, vedere la sezione Osservazioni.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la posizione orizzontale del cursore, in coordinate dello schermo, al momento del clic del mouse.

La parola più ordinata specifica la posizione verticale del cursore, in coordinate dello schermo, al momento del clic del mouse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Una finestra può elaborare questo messaggio visualizzando un menu di scelta rapida usando le funzioni [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Per ottenere le posizioni orizzontali e verticali, usare il codice seguente.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Se una finestra non visualizza un menu di scelta rapida, deve passare questo messaggio alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Se una finestra è una finestra figlio, **DefWindowProc** invia il messaggio all'elemento padre. In caso contrario, **DefWindowProc** Visualizza un menu di scelta rapida predefinito se la posizione specificata si trova nella didascalia della finestra.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera il messaggio **WM \_ ContextMenu** quando elabora il messaggio [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o quando l'utente digita MAIUSC + F10. Il messaggio **WM \_ ContextMenu** viene generato anche quando l'utente preme e rilascia la chiave [**delle \_ app VK**](/windows/desktop/inputdev/virtual-key-codes) .

Se il menu di scelta rapida viene generato dalla tastiera, ad esempio se l'utente digita MAIUSC + F10, le coordinate x e y sono pari a-1 e l'applicazione deve visualizzare il menu di scelta rapida nella posizione della selezione corrente anziché in (xPos, yPos).

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**\_NCRBUTTONUP WM**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**\_RBUTTONUP WM**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Menu](menus.md)
</dt> </dl>

 

