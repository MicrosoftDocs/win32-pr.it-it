---
title: Messaggio WM_PARENTNOTIFY
description: Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente.
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- Messaggi e notifiche di input del messaggio WM_PARENTNOTIFY
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
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518321"
---
# <a name="wm_parentnotify-message"></a>Messaggio WM_PARENTNOTIFY

Inviato a una finestra quando si verifica un'azione significativa in una finestra discendente. Questo messaggio è ora esteso per includere l'evento [**WM_POINTERDOWN**](wm-pointerdown.md) . Quando viene creata la finestra figlio, il sistema invia [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) appena prima della funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) che crea la finestra restituisce. Quando la finestra figlio viene distrutta, il sistema invia il messaggio prima che venga eseguita un'elaborazione per eliminare la finestra.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> \[! Importante\]  
> Le applicazioni desktop devono essere compatibili con DPI. Se l'app non è compatibile con DPI, le coordinate dello schermo contenute nei messaggi puntatore e le strutture correlate potrebbero sembrare non accurate a causa della virtualizzazione DPI. La virtualizzazione DPI fornisce il supporto per il ridimensionamento automatico per le applicazioni che non sono compatibili con DPI ed è attivo per impostazione predefinita (gli utenti possono disabilitarlo). Per altre informazioni, vedere [scrittura di applicazioni Win32 ad alta risoluzione](/previous-versions//dd464660(v=vs.85)).

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

La parola più bassa di *wParam* specifica l'evento per il quale l'elemento padre riceve la notifica. Il valore della parola più ordinata dipende dal valore della parola di basso livello. Questo parametro può avere uno dei valori seguenti.



| LOWORD (*wParam*)                                                                                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <dt>**WM_CREATE**</dt> <dt>0x0001</dt> </dl>                | È in corso la creazione della finestra figlio.<br/> HIWORD (*wParam*) è l'identificatore della finestra figlio.<br/> *lParam* è un handle per la finestra figlio.<br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <dt>**WM_DESTROY**</dt> <dt>0x0002</dt> </dl>             | La finestra figlio verrà eliminata definitivamente.<br/> HIWORD (*wParam*) è l'identificatore della finestra figlio.<br/> *lParam* è un handle per la finestra figlio.<br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic con il pulsante sinistro del mouse.<br/> HIWORD (*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.<br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul pulsante centrale del mouse.<br/> HIWORD (*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.<br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic con il pulsante destro del mouse.<br/> HIWORD (*wParam*) non è definito.<br/> *lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.<br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <dt>**WM_xBUTTONDOWN**</dt> <dt>0x020B</dt> </dl> | L'utente ha posizionato il cursore sulla finestra figlio e ha fatto clic sul primo o sul secondo pulsante X.<br/> HIWORD (*wParam*) indica quale pulsante è stato premuto. Questo parametro può essere uno dei valori seguenti: XBUTTON1 o XBUTTON2.<br/> *lParam* è la coordinata x del cursore è la parola di basso livello e la coordinata y del cursore è la parola più ordinata.<br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt> </dl> | Un puntatore ha effettuato il contatto con la finestra figlio.<br/> HIWORD (*wParam*) contiene l'identificatore del puntatore che ha generato l'evento [**WM_POINTERDOWN**](wm-pointerdown.md) .<br/>                                                                                                                                                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Contiene la posizione del punto del puntatore.

> [!Note]  
> Poiché il puntatore può rendere il contatto con il dispositivo su un'area non banale, questa posizione del punto può essere una semplificazione di un'area del puntatore più complessa. Laddove possibile, un'applicazione deve usare le informazioni complete sull'area del puntatore anziché la posizione del punto.

 

Utilizzare le macro seguenti per recuperare le coordinate dello schermo fisico del punto.

-   [**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): coordinata X (punto orizzontale).
-   [**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): coordinata Y (punto verticale).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'applicazione elabora il messaggio, viene restituito zero.

Se l'applicazione non elabora questo messaggio, chiama [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato anche a tutte le finestre predecessori della finestra figlio, inclusa la finestra di primo livello.

Tutte le finestre figlio, ad eccezione di quelle con lo stile **WS_EX_NOPARENTNOTIFY** finestra estesa, inviano questo messaggio alle finestre padre. Per impostazione predefinita, le finestre figlio in una finestra di dialogo hanno lo stile **WS_EX_NOPARENTNOTIFY** , a meno che non venga chiamata la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) per creare la finestra figlio senza questo stile.

Questa notifica fornisce alle finestre predecessore della finestra figlio un'opportunità per esaminare le informazioni del puntatore e, se necessario, acquisire il puntatore usando le funzioni di acquisizione del puntatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Messaggi](messages.md)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM_CREATE**](../winmsg/wm-create.md)
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

 

