---
title: 'Messaggi dei pulsanti '
description: Un pulsante può inviare messaggi alla relativa finestra padre e una finestra padre può inviare messaggi a un pulsante.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103734042"
---
# <a name="button-messages"></a>Messaggi dei pulsanti 

Un pulsante può inviare messaggi alla relativa finestra padre e una finestra padre può inviare messaggi a un pulsante.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Invio di messaggi ai pulsanti](#sending-messages-to-buttons)
-   [Gestione dei messaggi da un pulsante](#handling-messages-from-a-button)
-   [Messaggi di notifica dai pulsanti](#notification-messages-from-buttons)
-   [Messaggi colori pulsante](#button-color-messages)
-   [Elaborazione dei messaggi predefiniti del pulsante](#button-default-message-processing)
-   [Argomenti correlati](#related-topics)

## <a name="sending-messages-to-buttons"></a>Invio di messaggi ai pulsanti

Una finestra padre può inviare messaggi a un pulsante in una finestra sovrapposta o figlio utilizzando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oppure può inviare messaggi a un pulsante in una finestra di dialogo utilizzando le funzioni [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

Un'applicazione può usare il messaggio [**BM \_ GetCheck**](bm-getcheck.md) per recuperare lo stato di selezione di una casella di controllo o di un pulsante di opzione. Un'applicazione può anche usare il messaggio [**BM \_ GetState**](bm-getstate.md) per recuperare gli stati correnti del pulsante (stato di selezione, stato di push e stato attivo). Per ottenere informazioni su uno stato specifico, utilizzare una maschera di maschera sul valore dello stato restituito.

Il [**messaggio \_ di controllo BM**](bm-setcheck.md) imposta lo stato di selezione di una casella di controllo o di un pulsante di opzione. il messaggio restituisce zero. Il messaggio di [**\_ stato BM**](bm-setstate.md) imposta lo stato di push di un pulsante. il messaggio restituisce anche zero. Il messaggio [**BM \_ Sestyle**](bm-setstyle.md) modifica lo stile di un pulsante. È progettato per modificare gli stili dei pulsanti all'interno di un tipo (ad esempio, la modifica di una casella di controllo in una casella di controllo automatica). Non è progettato per la modifica tra i tipi, ad esempio la modifica di una casella di controllo in un pulsante di opzione. Un'applicazione non deve modificare un pulsante da un tipo a un altro.

Un pulsante della [**\_ bitmap BS**](button-styles.md) o dello stile dell' [**\_ icona BS**](button-styles.md) Visualizza una bitmap o un'icona anziché un testo. Il messaggio [**BM \_ diImage**](bm-setimage.md) associa un handle a una bitmap o a un'icona con un pulsante. Il messaggio [**BM \_ GetImage**](bm-getimage.md) recupera un handle per la bitmap o l'icona associata a un pulsante.

Un'applicazione può inoltre utilizzare il messaggio [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) per recuperare l'identificatore del controllo pulsante di push predefinito in una finestra di dialogo. Un'applicazione può utilizzare il messaggio [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) per impostare il pulsante di push predefinito per una finestra di dialogo.

La chiamata della funzione [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) o [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) equivale all'invio di un messaggio di [**\_ controllo BM**](bm-setcheck.md) . La chiamata della funzione [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) equivale all'invio di un messaggio [**BM \_ GetCheck**](bm-getcheck.md) .

## <a name="handling-messages-from-a-button"></a>Gestione dei messaggi da un pulsante

Le notifiche da un pulsante vengono inviate tramite [**il \_ comando WM**](/windows/desktop/menurc/wm-command) o i messaggi di [**\_ notifica WM**](wm-notify.md) . Le informazioni sul messaggio utilizzato sono reperibili nella pagina di riferimento per ogni notifica.

Per ulteriori informazioni sulla gestione dei messaggi, vedere [Control Messages](control-messages.md). Vedere anche messaggi dei pulsanti.

## <a name="notification-messages-from-buttons"></a>Messaggi di notifica dai pulsanti

Quando l'utente fa clic su un pulsante, lo stato cambia e il pulsante Invia i codici di notifica, sotto forma di messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) , alla finestra padre. Ad esempio, un controllo pulsante di comando Invia il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) ogni volta che l'utente sceglie il pulsante. In tutti i casi (ad eccezione di [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), la parola di basso livello del parametro *wParam* contiene l'identificatore di controllo, la parola più significativa di *wParam* contiene il codice di notifica e il parametro *lParam* contiene l'handle della finestra di controllo.

Il messaggio e la risposta della finestra padre dipendono dal tipo, dallo stile e dallo stato corrente del pulsante. Di seguito sono riportati i codici di notifica dei pulsanti che un'applicazione deve monitorare ed elaborare.



| Codice di notifica                                                        | Descrizione                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [\_HOTITEMCHANGE BCN](bcn-hotitemchange.md)                              | Il mouse è stato immesso o lasciato l'area client di un pulsante. |
| [BN \_ selezionato](bn-clicked.md)                                            | L'utente ha fatto clic su un pulsante.                             |
| [BN \_ DBLCLK](bn-dblclk.md) o [BN con \_ DoubleClick](bn-doubleclicked.md) | L'utente ha fatto doppio clic su un pulsante.                      |
| [BN- \_ disabilitazione](bn-disable.md)                                            | Un pulsante è disabilitato.                                  |
| [BN \_ PUSH](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)               | L'utente ha eseguito il push di un pulsante.                              |
| [BN \_ KILLFOCUS](bn-killfocus.md)                                        | Il pulsante ha perso lo stato attivo della tastiera.                    |
| [\_disegno BN](bn-paint.md)                                                | È necessario disegnare il pulsante.                          |
| [\_CONattivazione BN](bn-setfocus.md)                                          | Il pulsante ha ottenuto lo stato attivo della tastiera.                  |
| [BN \_ Unpushd](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)       | Il pulsante non viene più inserito.                        |



 

Un pulsante Invia i [BN \_ Disable](bn-disable.md), [BN \_ push](bn-pushed.md), [BN \_ KILLFOCUS](bn-killfocus.md), [BN \_ Paint](bn-paint.md), [BN \_ SetFocus](bn-setfocus.md)e BN i codici di notifica [ \_ unpushed](bn-unpushed.md) solo se lo stile di [**\_ notifica BS**](button-styles.md) . [BN \_](bn-dblclk.md) I codici di notifica DBLCLK vengono inviati automaticamente per i pulsanti [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) . Altri tipi di pulsante inviano BN \_ DBLCLK solo se hanno lo stile di **\_ notifica BS** . Tutti i pulsanti inviano il codice di notifica [ \_ fatto clic su BN](bn-clicked.md) indipendentemente dagli stili dei pulsanti.

Per i pulsanti automatici, il sistema modifica lo stato di push e disegna il pulsante. In questo caso, l'applicazione in genere elabora solo i [BN \_ clic](bn-clicked.md) e i codici di notifica [ \_ DBLCLK BN](bn-dblclk.md) . Per i pulsanti non automatici, l'applicazione in genere risponde al codice di notifica inviando un messaggio per modificare lo stato del pulsante. Per informazioni sull'invio di messaggi ai pulsanti, vedere l'argomento relativo [all'invio di messaggi ai pulsanti](#sending-messages-to-buttons).

Quando l'utente seleziona un pulsante creato dal proprietario, il pulsante Invia alla finestra padre un messaggio [**WM \_ DrawItem**](wm-drawitem.md) contenente l'identificatore del controllo da disegnare e le informazioni sulle dimensioni e sullo stato.

## <a name="button-color-messages"></a>Messaggi colori pulsante

Il sistema fornisce valori di colore predefiniti per i pulsanti. Un'applicazione può recuperare i valori predefiniti per questi colori chiamando la funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o impostare i valori chiamando la funzione [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) . Nella tabella seguente vengono illustrati i valori predefiniti dei colori dei pulsanti.



| Valore               | Elemento colorato                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_BTNFACE colore      | Visi pulsante.                                                                                                              |
| \_BTNHIGHLIGHT colore | Area evidenziata (i bordi superiore e sinistro) di un pulsante.                                                                       |
| \_BTNSHADOW colore    | Area ombreggiata (bordi inferiore e destro) di un pulsante.                                                                      |
| \_BTNTEXT colore      | Testo normale (non in grigio) nei pulsanti.                                                                                       |
| \_GRAYTEXT colore     | Testo disabilitato (grigio) nei pulsanti. Questo colore è impostato su 0 se il driver di visualizzazione corrente non supporta un colore grigio a tinta unita. |
| \_finestra colori       | Sfondi della finestra.                                                                                                        |
| \_WINDOWFRAME colore  | Frame della finestra.                                                                                                             |
| \_WINDOWTEXT colore   | Testo di Windows.                                                                                                           |



 

Tuttavia, la chiamata di [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) ha effetto su tutte le applicazioni, pertanto non è necessario chiamare questa funzione per personalizzare i pulsanti per l'applicazione.

Il sistema invia un messaggio [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) alla finestra padre di un pulsante prima di disegnare un pulsante. Questo messaggio contiene un handle per il contesto di dispositivo del pulsante e un handle per la finestra figlio. La finestra padre può usare questi handle per modificare il testo del pulsante e i colori di sfondo. Tuttavia, solo i pulsanti creati dal proprietario rispondono alla finestra padre che elabora il messaggio.

## <a name="button-default-message-processing"></a>Elaborazione dei messaggi predefiniti del pulsante

La routine della finestra per la classe della finestra di controllo Button predefinita esegue l'elaborazione predefinita per tutti i messaggi che la routine di controllo Button non elabora. Quando la procedura di controllo Button restituisce **false** per qualsiasi messaggio, la routine della finestra predefinita controlla i messaggi ed esegue le azioni predefinite elencate nella tabella seguente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Message</th>
<th>Azione predefinita</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Invia al pulsante un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> e un messaggio di <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> e invia alla finestra padre un <a href="bn-clicked.md">BN_CLICKED</a> codice di notifica.</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Restituisce lo stato di selezione del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Restituisce un handle per la bitmap o l'icona associata al pulsante o <strong>null</strong> se il pulsante non dispone di una bitmap o di un'icona.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Restituisce lo stato di selezione corrente, lo stato di push e lo stato di attivazione del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Imposta lo stato di selezione di tutti gli stili di pulsanti di opzione e caselle di controllo. Se il parametro <em>wParam</em> è maggiore di zero per i pulsanti di opzione, al pulsante viene assegnato lo stile <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Associa l'handle di bitmap o icona specificato al pulsante e restituisce un handle per la bitmap o l'icona precedente.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Imposta lo stato di push del pulsante. Per i pulsanti creati dal proprietario, viene inviato un messaggio di <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> alla finestra padre se lo stato del pulsante è stato modificato.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Imposta lo stile del pulsante. Se la parola di ordine inferiore del parametro <em>lParam</em> è <strong>true</strong>, il pulsante viene ridisegnato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Controlla una casella di controllo o una casella di controllo automatica quando l'utente preme le chiavi più (+) o uguale (=). Deseleziona una casella di controllo o una casella di controllo automatica quando l'utente preme il tasto meno (–).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Disegna il pulsante.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Cancella lo sfondo per i pulsanti creati dal proprietario. Gli sfondi di altri pulsanti vengono cancellati come parte del <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> e <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> l'elaborazione.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Restituisce valori che indicano il tipo di input elaborato dalla routine del pulsante predefinito, come illustrato nella tabella seguente. 
<table>
<thead>
<tr class="header">
<th>Stile pulsante</th>
<th>Restituisce</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Restituisce un handle per il tipo di carattere corrente.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Inserisce il pulsante se l'utente preme la barra SPAZIAtrice.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse per tutti i case tranne il tasto TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Rimuove il rettangolo di attivazione da un pulsante. Per i pulsanti di push e i pulsanti di push predefiniti, il rettangolo di attivazione è invalidato. Se il pulsante ha l'acquisizione del mouse, l'acquisizione viene rilasciata, il pulsante non viene selezionato e viene rimosso qualsiasi stato di push.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Invia un codice di notifica <a href="bn-dblclk.md">BN_DBLCLK</a> alla finestra padre per i pulsanti di opzione e i pulsanti creati dal proprietario. Per gli altri pulsanti, un doppio clic viene elaborato come messaggio <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Evidenzia il pulsante se la posizione del cursore del mouse si trova all'interno del rettangolo client del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse se il pulsante ha l'acquisizione del mouse.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Esegue la stessa azione di <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, se il pulsante ha l'acquisizione del mouse. In caso contrario, non viene eseguita alcuna azione.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Consente di trasformare qualsiasi <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> pulsante in un pulsante <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Restituisce HTTRANSPARENT se il controllo Button è una casella di gruppo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Disegna il pulsante in base allo stile e allo stato corrente.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Disegna un rettangolo di attivazione sul pulsante per ottenere lo stato attivo. Per i pulsanti di opzione e i pulsanti di opzione automatici, alla finestra padre viene inviato un <a href="bn-clicked.md">BN_CLICKED</a> codice di notifica.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Imposta un nuovo tipo di carattere e, facoltativamente, aggiorna la finestra.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Imposta il testo del pulsante. Nel caso di una casella di gruppo, il messaggio viene disegnato sul testo preesistente prima di ridisegnare la casella di gruppo con il nuovo testo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse per tutti i case tranne il tasto TAB.</td>
</tr>
</tbody>
</table>



 

La routine della finestra predefinita passa tutti gli altri messaggi alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di controllo](control-messages.md)
</dt> </dl>

 

 