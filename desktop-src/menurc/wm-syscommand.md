---
title: Messaggio WM_SYSCOMMAND (winuser. h)
description: Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu finestra (noto in precedenza come menu di sistema o di controllo) o quando l'utente sceglie il pulsante Ingrandisci, Riduci a icona, pulsante Ripristina o Chiudi.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- Menu del messaggio WM_SYSCOMMAND e altre risorse
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
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330437"
---
# <a name="wm_syscommand-message"></a>\_Messaggio SYSCOMMAND WM

Una finestra riceve questo messaggio quando l'utente sceglie un comando dal menu **finestra** (noto in precedenza come menu di sistema o di controllo) o quando l'utente sceglie il pulsante Ingrandisci, Riduci a icona, pulsante Ripristina o Chiudi.


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
Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) in GitHub.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di comando di sistema richiesto. Questo parametro può avere uno dei valori seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </dl></td>
<td>Chiude la finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </dl></td>
<td>Imposta il cursore su un punto interrogativo con un puntatore. Se l'utente fa clic su un controllo nella finestra di dialogo, il controllo riceve un messaggio di <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </dl></td>
<td>Seleziona l'elemento predefinito. l'utente ha fatto doppio clic sul menu finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </dl></td>
<td>Attiva la finestra associata al tasto di scelta rapida specificato dall'applicazione. Il parametro <em>lParam</em> identifica la finestra da attivare.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </dl></td>
<td>Scorre orizzontalmente.<br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </dl></td>
<td>Indica se la screen saver è protetta. <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </dl></td>
<td>Recupera il menu finestra come risultato di una sequenza di tasti. Per altre informazioni, vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </dl></td>
<td>Ingrandisce la finestra.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </dl></td>
<td>Riduce a icona la finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </dl></td>
<td>Imposta lo stato della visualizzazione. Questo comando supporta i dispositivi che dispongono di funzionalità di risparmio energia, ad esempio un personal computer alimentato da batteria. <br/> Il parametro <em>lParam</em> può includere i valori seguenti:<br/>
<ul>
<li>-1 (lo schermo è acceso)</li>
<li>1 (lo schermo sarà a basso consumo)</li>
<li>2 (lo schermo sta per essere spento)</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </dl></td>
<td>Recupera il menu finestra a seguito di un clic del mouse.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </dl></td>
<td>Sposta la finestra.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </dl></td>
<td>Passa alla finestra successiva.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </dl></td>
<td>Passa alla finestra precedente.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </dl></td>
<td>Ripristina la posizione e le dimensioni normali della finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </dl></td>
<td>Esegue l'applicazione screen saver specificata nella sezione [boot] del file di System.ini.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </dl></td>
<td>Ridimensiona la finestra.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </dl></td>
<td>Attiva il menu <strong>Start</strong> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </dl></td>
<td>Scorre verticalmente.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore specifica la posizione orizzontale del cursore, in coordinate dello schermo, se si sceglie un comando di menu finestra con il mouse. In caso contrario, questo parametro non viene utilizzato.

La parola più ordinata specifica la posizione verticale del cursore, in coordinate dello schermo, se si sceglie un comando di menu finestra con il mouse. Questo parametro è 1 se il comando viene scelto utilizzando un acceleratore di sistema oppure zero se si utilizza un tasto di scelta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Un'applicazione deve restituire zero se elabora questo messaggio.

## <a name="remarks"></a>Commenti

Per ottenere le coordinate di posizione nelle coordinate dello schermo, usare il codice seguente:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) esegue la richiesta del menu finestra per le azioni predefinite specificate nella tabella precedente.

Nei messaggi **WM \_ SYSCOMMAND** , i quattro bit di ordine inferiore del parametro *wParam* vengono usati internamente dal sistema. Per ottenere il risultato corretto durante il test del valore di *wParam*, un'applicazione deve combinare il valore 0xFFF0 con il valore *wParam* usando l'operatore and bit per bit.

È possibile modificare le voci di menu in un menu finestra usando le funzioni [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Le applicazioni che modificano il menu finestra devono elaborare i messaggi **WM \_ SYSCOMMAND** .

Un'applicazione può eseguire qualsiasi comando di sistema in qualsiasi momento passando un messaggio **WM \_ SYSCOMMAND** a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Tutti i messaggi **WM \_ SYSCOMMAND** non gestiti dall'applicazione devono essere passati a **DefWindowProc**. Qualsiasi valore di comando aggiunto da un'applicazione deve essere elaborato dall'applicazione e non può essere passato a **DefWindowProc**.

Se la protezione con password è abilitata dal criterio, l'screen saver viene avviata indipendentemente dalle operazioni svolte da un'applicazione con la notifica **SC \_ SCREENSAVE** , anche se non riesce a passarla a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

I tasti di scelta rapida definiti per scegliere gli elementi dal menu finestra vengono convertiti in messaggi **WM \_ SYSCOMMAND** . tutte le altre sequenze di tasti di scelta rapida vengono convertite in messaggi di [**\_ comando WM**](wm-command.md) .

Se il *wParam* è **il \_ menu chiavi SC**, *lParam* contiene il codice carattere della chiave utilizzata con il tasto ALT per visualizzare il menu di scelta rapida. Ad esempio, se si preme ALT + F per visualizzare il popup del file, un **WM \_ SYSCOMMAND** con *wParam* uguale a **SC \_** e *lParam* è uguale a' F '.

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

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Ottieni \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OTTENERE \_ il \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**\_comando WM**](wm-command.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Tasti di scelta rapida](keyboard-accelerators.md)
</dt> </dl>

