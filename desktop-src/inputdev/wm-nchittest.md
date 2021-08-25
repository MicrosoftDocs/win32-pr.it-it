---
title: WM_NCHITTEST messaggio (Winuser.h)
description: Inviato a una finestra per determinare quale parte della finestra corrisponde a una particolare coordinata dello schermo.
ms.assetid: 4c860466-a9f8-4af8-96b9-cee005481875
keywords:
- WM_NCHITTEST messaggio Input tastiera e mouse
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
ms.openlocfilehash: 2f54c397db10e8ecd6b2ed3c67a73affde4507ea59a265d502f28ada97b8a68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778641"
---
# <a name="wm_nchittest-message"></a>Messaggio \_ WM NCHITTEST

Inviato a una finestra per determinare quale parte della finestra corrisponde a una particolare coordinata dello schermo. Ciò può verificarsi, ad esempio, quando il cursore viene spostato, quando viene premuto o rilasciato un pulsante del mouse o in risposta a una chiamata a una funzione, ad esempio [**WindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-windowfrompoint). Se il mouse non viene acquisito, il messaggio viene inviato alla finestra sotto il cursore. In caso contrario, il messaggio viene inviato alla finestra che ha acquisito il mouse.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

La parola di ordine basso specifica la coordinata x del cursore. La coordinata è relativa all'angolo superiore sinistro dello schermo.

La parola più alta specifica la coordinata y del cursore. La coordinata è relativa all'angolo superiore sinistro dello schermo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito della [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) è uno dei valori seguenti, che indica la posizione dell'area sensibile del cursore.



| Codice/valore restituito                                                                                                                                    | Descrizione                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**HTBORDER**</dt> <dt>18</dt> </dl>      | Nel bordo di una finestra che non ha un bordo di ridimensionamento.<br/>                                                                                                                                           |
| <dl> <dt>**HTBOTTOM**</dt> <dt>15</dt> </dl>      | Nel bordo orizzontale inferiore di una finestra ridimensionabile (l'utente può fare clic con il mouse per ridimensionare la finestra verticalmente).<br/>                                                                                    |
| <dl> <dt>**HTBOTTOMLEFT**</dt> <dt>16</dt> </dl>  | Nell'angolo inferiore sinistro di un bordo di una finestra ridimensionabile (l'utente può fare clic con il mouse per ridimensionare la finestra in diagonale).<br/>                                                                              |
| <dl> <dt>**HTBOTTOMRIGHT**</dt> <dt>17</dt> </dl> | Nell'angolo inferiore destro di un bordo di una finestra ridimensionabile (l'utente può fare clic con il mouse per ridimensionare la finestra in diagonale).<br/>                                                                             |
| <dl> <dt>**CONTROLLO DI STATO 2**</dt> <dt></dt> </dl>      | In una barra del titolo.<br/>                                                                                                                                                                                         |
| <dl> <dt>**HTCLIENT**</dt> <dt>1</dt> </dl>       | In un'area client.<br/>                                                                                                                                                                                       |
| <dl> <dt>**HTCLOSE**</dt> <dt>20</dt> </dl>       | In un **pulsante** Chiudi.<br/>                                                                                                                                                                                  |
| <dl> <dt>**HTERROR**</dt> <dt>-2</dt> </dl>       | Sullo sfondo dello schermo o su una linea di divisione tra le finestre (come **HTNOWHERE**), ad eccezione del fatto che la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) produce un segnale acustico di sistema per indicare un errore.<br/> |
| <dl> <dt>**HTGROWBOX**</dt> <dt>4</dt> </dl>      | In una casella delle dimensioni (uguale a **HTSIZE**).<br/>                                                                                                                                                                     |
| <dl> <dt>**HTHELP**</dt> <dt>21</dt> </dl>        | In un **pulsante ?**<br/>                                                                                                                                                                                   |
| <dl> <dt>**HTHSCROLL**</dt> <dt>6</dt> </dl>      | In una barra di scorrimento orizzontale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTLEFT**</dt> <dt>10</dt> </dl>        | Nel bordo sinistro di una finestra ridimensionabile (l'utente può fare clic con il mouse per ridimensionare la finestra orizzontalmente).<br/>                                                                                              |
| <dl> <dt>**HTMENU**</dt> <dt>5</dt> </dl>         | In un menu.<br/>                                                                                                                                                                                              |
| <dl> <dt>**HTMAXBUTTON**</dt> <dt>9</dt> </dl>    | In un **pulsante Ingrandisci.**<br/>                                                                                                                                                                               |
| <dl> <dt>**HTMINBUTTON**</dt> <dt>8</dt> </dl>    | In un **pulsante Riduci** a icona.<br/>                                                                                                                                                                               |
| <dl> <dt>**HTNOWHERE**</dt> <dt>0</dt> </dl>      | Sullo sfondo dello schermo o su una linea di divisione tra le finestre.<br/>                                                                                                                                         |
| <dl> <dt>**HTREDUCE**</dt> <dt>8</dt> </dl>       | In un **pulsante Riduci** a icona.<br/>                                                                                                                                                                               |
| <dl> <dt>**HTRIGHT**</dt> <dt>11</dt> </dl>       | Nel bordo destro di una finestra ridimensionabile (l'utente può fare clic con il mouse per ridimensionare la finestra orizzontalmente).<br/>                                                                                             |
| <dl> <dt>**HTSIZE**</dt> <dt>4</dt> </dl>         | In una casella delle dimensioni (uguale a **HTGROWBOX**).<br/>                                                                                                                                                                  |
| <dl> <dt>**HTSYSMENU**</dt> <dt>3</dt> </dl>      | In un menu della finestra o in **un pulsante** Chiudi in una finestra figlio.<br/>                                                                                                                                            |
| <dl> <dt>**HTTOP**</dt> <dt>12</dt> </dl>         | Bordo superiore orizzontale di una finestra.<br/>                                                                                                                                                             |
| <dl> <dt>**HTTOPLEFT**</dt> <dt>13</dt> </dl>     | Nell'angolo superiore sinistro del bordo di una finestra.<br/>                                                                                                                                                            |
| <dl> <dt>**HTTOPRIGHT**</dt> <dt>14</dt> </dl>    | Nell'angolo superiore destro del bordo di una finestra.<br/>                                                                                                                                                           |
| <dl> <dt>**HTTRANSPARENT**</dt> <dt>-1</dt> </dl> | In una finestra attualmente coperta da un'altra finestra nello stesso thread (il messaggio verrà inviato alle finestre sottostanti nello stesso thread finché una di esse non restituisce un codice diverso da **HTTRANSPARENT).**<br/>  |
| <dl> <dt>**HTVSCROLL**</dt> <dt>7</dt> </dl>      | Nella barra di scorrimento verticale.<br/>                                                                                                                                                                             |
| <dl> <dt>**HTZOOM**</dt> <dt>9</dt> </dl>         | In un **pulsante Ingrandisci.**<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Usare il codice seguente per ottenere la posizione orizzontale e verticale:


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



Come indicato in precedenza, la coordinata x si trova nell'ordine più basso **del** valore restituito. la coordinata y è nell'ordine più  alto **(entrambe** rappresentano valori firmati perché possono assumere valori negativi nei sistemi con più monitor). Se il valore restituito viene assegnato a una variabile, è possibile usare la macro [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) per ottenere una [**struttura POINTS**](/previous-versions//dd162808(v=vs.85)) dal valore restituito. È anche possibile usare la macro [**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) o [**GET Y \_ \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) per estrarre la coordinata x o y.

> [!IMPORTANT]
> Non usare le macro [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) per estrarre le coordinate x e y della posizione del cursore perché queste macro restituiscono risultati non corretti nei sistemi con più monitor. I sistemi con più monitor possono avere coordinate x e y negative e **LOWORD** e **HIWORD** trattano le coordinate come quantità senza segno.

 

**Windows Vista:** Quando si creano frame personalizzati che includono i pulsanti della didascalia standard, questo messaggio deve essere passato prima alla [**funzione DwmDefWindowProc.**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmdefwindowproc) Ciò consente al Gestione finestre desktop (DWM) di fornire l'hit testing per i pulsanti dei sottotitoli. Se **DwmDefWindowProc** non gestisce il messaggio, potrebbe essere necessaria un'ulteriore elaborazione di **WM \_ NCHITTEST.**

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

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
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

 

