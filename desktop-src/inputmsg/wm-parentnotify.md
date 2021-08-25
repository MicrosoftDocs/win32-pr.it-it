---
title: WM_PARENTNOTIFY messaggio
description: Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY messaggi di input e notifiche
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5de0845f906e72a42fa8d9a290c6cd8ac16cc0e96cae21ac25b3e9d7810309e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829571"
---
# <a name="wm_parentnotify-message"></a>WM_PARENTNOTIFY messaggio

Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente. Questo messaggio è ora esteso per includere [**l'WM_POINTERDOWN**](wm-pointerdown.md) eventi. Quando viene creata la finestra figlio, il sistema WM_PARENTNOTIFY prima che venga restituita la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) che crea la finestra. [](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) Quando la finestra figlio viene distrutta, il sistema invia il messaggio prima di qualsiasi elaborazione per eliminare la finestra.

Una finestra riceve questo messaggio tramite la relativa [**funzione WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

> \[! Importante\]  
> Le app desktop devono essere in grado di riconoscere DPI. Se l'app non è in grado di riconoscere DPI, le coordinate dello schermo contenute nei messaggi del puntatore e nelle strutture correlate potrebbero apparire inesatte a causa della virtualizzazione DPI. La virtualizzazione DPI offre il supporto automatico del ridimensionamento per le applicazioni che non supportano DPI ed è attiva per impostazione predefinita (gli utenti possono disattivarla). Per altre informazioni, vedere [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola meno importante di *wParam* specifica l'evento per il quale viene notificata la notifica dell'elemento padre. Il valore della parola più alta dipende dal valore della parola di ordine basso. Questo parametro può avere uno dei valori seguenti.



| LOWORD(*wParam*)                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | Viene creata la finestra figlio.<br/> HIWORD(*wParam*) è l'identificatore della finestra figlio.<br/> *lParam* è un handle per la finestra figlio.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | La finestra figlio viene distrutta.<br/> HIWORD(*wParam*) è l'identificatore della finestra figlio.<br/> *lParam* è un handle per la finestra figlio.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul pulsante sinistro del mouse.<br/> HIWORD(*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di ordine basso e la coordinata y del cursore è la parola di ordine superiore.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul pulsante centrale del mouse.<br/> HIWORD(*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di ordine basso e la coordinata y del cursore è la parola di ordine superiore.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic con il pulsante destro del mouse.<br/> HIWORD(*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di ordine basso e la coordinata y del cursore è la parola di ordine superiore.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul primo o secondo pulsante X.<br/> HIWORD(*wParam*) indica quale pulsante è stato premuto. Questo parametro può essere uno dei valori seguenti: XBUTTON1 o XBUTTON2.<br/> *lParam* è la coordinata x del cursore è la parola di ordine basso e la coordinata y del cursore è la parola di ordine superiore.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Un puntatore ha contattato la finestra figlio.<br/> HIWORD(*wParam*) contiene l'identificatore del puntatore che ha generato [**l'WM_POINTERDOWN**](wm-pointerdown.md) evento.<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la posizione del punto del puntatore.

> [!Note]  
> Poiché il puntatore può contattare il dispositivo su un'area non semplice, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa. Quando possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.

 

Usare le macro seguenti per recuperare le coordinate fisiche dello schermo del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata x (punto orizzontale).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata y (punto verticale).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione elabora questo messaggio, restituisce zero.

Se l'applicazione non elabora questo messaggio, chiama [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato anche a tutte le finestre predecessori della finestra figlio, inclusa la finestra di primo livello.

Tutte le finestre figlio, ad eccezione di quelle con WS_EX_NOPARENTNOTIFY **finestra** estesa, inviano questo messaggio alle finestre padre. Per impostazione predefinita, le finestre figlio in una finestra di dialogo hanno lo stile WS_EX_NOPARENTNOTIFY, **a** meno che non venga chiamata la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) per creare la finestra figlio senza questo stile.

Questa notifica offre alle finestre predecessore della finestra figlio la possibilità di esaminare le informazioni sul puntatore e, se necessario, acquisire il puntatore usando le funzioni di acquisizione del puntatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                               |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Wm_create**](../winmsg/wm-create.md)
</dt> <dt>

[**WM_DESTROY**](../winmsg/wm-destroy.md)
</dt> <dt>

[**WM_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[**WM_MBUTTONDOWN**](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[**WM_RBUTTONDOWN**](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[**WM_XBUTTONDOWN**](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

