---
title: WM_SYSCOMMAND messaggio (Winuser.h)
description: Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu Finestra (precedentemente noto come menu di sistema o di controllo) o quando l'utente sceglie il pulsante ingrandisci, il pulsante riduci a icona, il pulsante ripristina o il pulsante chiudi.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menu e altre risorse del messaggio
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482177"
---
# <a name="wm_syscommand-message"></a>Messaggio \_ SYSCOMMAND WM

Una finestra riceve questo messaggio quando l'utente sceglie un comando dal **menu** Finestra (precedentemente noto come menu di sistema o di controllo) o quando l'utente sceglie il pulsante ingrandisci, il pulsante riduci a icona, il pulsante ripristina o il pulsante chiudi.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Esempio

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) in GitHub.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di comando di sistema richiesto. Questo parametro può avere uno dei valori seguenti.




| Valore | Significato | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Chiude la finestra.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Modifica il cursore in un punto interrogativo con un puntatore. Se l'utente fa clic su un controllo nella finestra di dialogo, il controllo riceve un <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> messaggio.<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Seleziona l'elemento predefinito. L'utente ha fatto doppio clic sul menu della finestra.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Attiva la finestra associata al tasto di scelta rapida specificato dall'applicazione. Il <em>parametro lParam</em> identifica la finestra da attivare.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Scorre orizzontalmente.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Indica se il screen saver è sicuro. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Recupera il menu della finestra in seguito a una sequenza di tasti. Per altre informazioni, vedere la sezione Osservazioni.<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Ingrandisce la finestra.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Riduce a icona la finestra.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Imposta lo stato della visualizzazione. Questo comando supporta i dispositivi con funzionalità di risparmio energia, ad esempio un dispositivo a batteria personal computer. <br /> Il <em>parametro lParam</em> può avere i valori seguenti:<br /><ul><li>-1 (lo schermo è alimentato)</li><li>1 (lo schermo sta per essere alimentato a basso consumo)</li><li>2 (lo schermo è in fase di arresto)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Recupera il menu della finestra in seguito a un clic del mouse.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Sposta la finestra.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Passa alla finestra successiva.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Passa alla finestra precedente.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Ripristina la posizione e le dimensioni normali della finestra.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Esegue l screen saver applizione specificata nella sezione [boot] del file System.ini.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>0xF000</dt></dl> | Ridimensiona la finestra.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Attiva il menu <strong>Start.</strong><br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Scorre verticalmente.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa specifica la posizione orizzontale del cursore, nelle coordinate dello schermo, se si sceglie un comando di menu della finestra con il mouse. In caso contrario, questo parametro non viene utilizzato.

La parola di ordine superiore specifica la posizione verticale del cursore, nelle coordinate dello schermo, se si sceglie un comando di menu della finestra con il mouse. Questo parametro è 1 se il comando viene scelto usando un acceleratore di sistema oppure zero se si usa un tasto di scelta rapida.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Per ottenere le coordinate di posizione nelle coordinate dello schermo, usare il codice seguente:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esegue la richiesta di menu della finestra per le azioni predefinite specificate nella tabella precedente.

Nei **messaggi \_ SYSCOMMAND** WM, i quattro bit meno usati del *parametro wParam* vengono usati internamente dal sistema. Per ottenere il risultato corretto durante il test del valore di *wParam*, un'applicazione deve combinare il valore 0xFFF0 con il valore *wParam* usando l'operatore AND bit per bit.

Le voci di menu in un menu finestra possono essere modificate usando le funzioni [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) Le applicazioni che modificano il menu della finestra devono **elaborare i \_ messaggi SYSCOMMAND WM.**

Un'applicazione può eseguire qualsiasi comando di sistema in qualsiasi momento passando un messaggio **\_ SYSCOMMAND WM** a [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Tutti **i \_ messaggi SYSCOMMAND WM** non gestiti dall'applicazione devono essere passati a **DefWindowProc.** I valori dei comandi aggiunti da un'applicazione devono essere elaborati dall'applicazione e non possono essere passati **a DefWindowProc.**

Se la protezione password è abilitata dai criteri, il screen saver viene avviato indipendentemente dalle attività che un'applicazione esegue con la notifica **SC \_ SCREENSAVE** anche se non riesce a passarla a [**DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

I tasti di scelta rapida definiti per scegliere le voci dal menu della finestra vengono convertiti in messaggi **\_ SYSCOMMAND WM.** Tutte le altre sequenze di tasti vengono convertite in [**messaggi WM \_ COMMAND.**](wm-command.md)

Se *wParam è* **SC \_ KEYMENU**, *lParam* contiene il codice carattere del tasto usato con il tasto ALT per visualizzare il menu popup. Ad esempio, se si preme ALT+F per visualizzare il popup File, wm **\_ SYSCOMMAND** con *wParam* uguale a **SC \_ KEYMENU** e *lParam* uguale a 'f'.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**COMANDO \_ WM**](wm-command.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

