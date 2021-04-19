---
title: Messaggio WM_NCHITTEST (winuser. h)
description: Inviato a una finestra per determinare quale parte della finestra corrisponde a una determinata coordinata dello schermo.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- Input della tastiera e del mouse WM_NCHITTEST messaggio
topic_type:
- apiref
api_name:
- WM_NCHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf14e817831c099988e9fb3fee57ae0731ef621
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301422"
---
# <a name="wm_nchittest-message"></a>\_Messaggio NCHITTEST WM

Inviato a una finestra per determinare quale parte della finestra corrisponde a una determinata coordinata dello schermo. Questo può accadere, ad esempio, quando il cursore viene spostato, quando viene premuto o rilasciato un pulsante del mouse o in risposta a una chiamata a una funzione come [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore. In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCHITTEST                    0x0084
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dello schermo.

La parola di ordine superiore specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito della funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) è uno dei valori seguenti, che indica la posizione dell'area sensibile del cursore.



| Codice/valore restituito                                                                                                                                    | Descrizione                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | Nel bordo di una finestra che non dispone di un bordo di ridimensionamento.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | Nel bordo inferiore orizzontale di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra verticalmente).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | Nell'angolo inferiore sinistro di un bordo di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra in diagonale).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | Nell'angolo in basso a destra di un bordo di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra in diagonale).<br/>                                                                             |
| <dl> <dt>**HTCAPTION**</dt> <dt>2</dt> </dl>      | In una barra del titolo.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | In un'area client.<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | In un pulsante **Chiudi** .<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | Sullo sfondo dello schermo o su una linea di divisione tra le finestre (uguale a **HTNOWHERE**, con la differenza che la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera un segnale acustico di sistema per indicare un errore).<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | In una casella delle dimensioni (uguale a **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | In un pulsante della **Guida** .<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | In una barra di scorrimento orizzontale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | Sul bordo sinistro di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra orizzontalmente).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | In un menu.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | In un pulsante **Ingrandisci** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | In un pulsante **Riduci a icona** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | Sullo sfondo dello schermo o su una linea di divisione tra le finestre.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | In un pulsante **Riduci a icona** .<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | Sul bordo destro di una finestra ridimensionabile (l'utente può fare clic sul mouse per ridimensionare la finestra orizzontalmente).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | In una casella delle dimensioni (uguale a **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | In un menu finestra o in un pulsante **Chiudi** in una finestra figlio.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | Nel bordo superiore orizzontale di una finestra.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | Nell'angolo superiore sinistro del bordo di una finestra.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | Nell'angolo superiore destro del bordo di una finestra.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | In una finestra attualmente coperta da un'altra finestra nello stesso thread (il messaggio verrà inviato alle finestre sottostanti nello stesso thread fino a quando uno di essi non restituisce un codice non **HTTRANSPARENT**).<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | Sulla barra di scorrimento verticale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | In un pulsante **Ingrandisci** .<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Come indicato in precedenza, la coordinata x è **nell'ordine inferiore** del valore restituito. la coordinata y si trova nell'ordine **breve** (entrambi rappresentano valori *firmati* perché possono assumere valori negativi nei sistemi con più monitoraggi). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una struttura [**Points**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. Per estrarre la coordinata x o y, è anche possibile usare la macro [**get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**get \_ y \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitoraggi. I sistemi con più monitoraggi possono avere coordinate x e y negative e **LOWORD** e **HIWORD** considerano le coordinate come quantità senza segno.

 

**Windows Vista:** Quando si creano frame personalizzati che includono i pulsanti della didascalia standard, questo messaggio deve essere prima passato alla funzione [**DwmDefWindowProc**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) . Ciò consente all'Gestione finestre desktop (DWM) di fornire hit testing per i pulsanti didascalie. Se **DwmDefWindowProc** non gestisce il messaggio, potrebbe essere necessaria un'ulteriore elaborazione di **WM \_ NCHITTEST** .

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

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
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

 

