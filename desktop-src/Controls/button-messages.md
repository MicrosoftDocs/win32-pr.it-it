---
title: 'Messaggi dei pulsanti '
description: Un pulsante può inviare messaggi alla finestra padre e una finestra padre può inviare messaggi a un pulsante.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136310a3718f17900f604287bf78186f7c927259
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625717"
---
# <a name="button-messages"></a>Messaggi dei pulsanti 

Un pulsante può inviare messaggi alla finestra padre e una finestra padre può inviare messaggi a un pulsante.

In questa sezione vengono descritti gli argomenti seguenti.

-   [Invio di messaggi ai pulsanti](#sending-messages-to-buttons)
-   [Gestione dei messaggi da un pulsante](#handling-messages-from-a-button)
-   [Messaggi di notifica dai pulsanti](#notification-messages-from-buttons)
-   [Messaggi a colori dei pulsanti](#button-color-messages)
-   [Elaborazione dei messaggi predefinita del pulsante](#button-default-message-processing)
-   [Argomenti correlati](#related-topics)

## <a name="sending-messages-to-buttons"></a>Invio di messaggi ai pulsanti

Una finestra padre può inviare messaggi a un pulsante in una finestra sovrapposta o figlio usando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) oppure può inviare messaggi a un pulsante in una finestra di dialogo usando le funzioni [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

Un'applicazione può usare il [**messaggio BM \_ GETCHECK**](bm-getcheck.md) per recuperare lo stato di controllo di una casella di controllo o di un pulsante di opzione. Un'applicazione può anche usare il [**messaggio \_ GETSTATE BM**](bm-getstate.md) per recuperare gli stati correnti del pulsante (stato del controllo, stato push e stato attivo). Per ottenere informazioni su uno stato specifico, usare una maschera di bit sul valore dello stato restituito.

Il [**messaggio BM \_ SETCHECK**](bm-setcheck.md) imposta lo stato di controllo di una casella di controllo o di un pulsante di opzione. Il messaggio restituisce zero. Il [**messaggio BM \_ SETSTATE**](bm-setstate.md) imposta lo stato push di un pulsante. Anche questo messaggio restituisce zero. Il [**messaggio BM \_ SETSTYLE**](bm-setstyle.md) modifica lo stile di un pulsante. È progettato per la modifica degli stili dei pulsanti all'interno di un tipo, ad esempio la modifica di una casella di controllo in una casella di controllo automatica. Non è progettato per la modifica da un tipo all'altro, ad esempio la modifica di una casella di controllo in un pulsante di opzione. Un'applicazione non deve modificare un pulsante da un tipo a un altro.

Un pulsante dello stile [**BS \_ BITMAP**](button-styles.md) o [**BS \_ ICON**](button-styles.md) visualizza una bitmap o un'icona al posto del testo. Il [**messaggio BM \_ SETIMAGE**](bm-setimage.md) associa un handle a una bitmap o a un'icona a un pulsante. Il [**messaggio \_ BM GETIMAGE**](bm-getimage.md) recupera un handle per la bitmap o l'icona associata a un pulsante.

Un'applicazione può anche usare il [**messaggio \_ DM GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) per recuperare l'identificatore del controllo pulsante di push predefinito in una finestra di dialogo. Un'applicazione può usare il [**messaggio \_ DM SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) per impostare il pulsante push predefinito per una finestra di dialogo.

Chiamare la [**funzione CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) o [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) equivale all'invio di un [**messaggio \_ SETCHECK BM.**](bm-setcheck.md) La chiamata [**della funzione IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) equivale all'invio di un [**messaggio \_ BM GETCHECK.**](bm-getcheck.md)

## <a name="handling-messages-from-a-button"></a>Gestione dei messaggi da un pulsante

Le notifiche da un pulsante vengono inviate [**come messaggi WM \_ COMMAND**](/windows/desktop/menurc/wm-command) [**o WM \_ NOTIFY.**](wm-notify.md) Le informazioni sul messaggio usato sono disponibili nella pagina di riferimento per ogni notifica.

Per altre informazioni su come gestire i messaggi, vedere [Messaggi di controllo](control-messages.md). Vedere anche Messaggi pulsante.

## <a name="notification-messages-from-buttons"></a>Messaggi di notifica dai pulsanti

Quando l'utente fa clic su un pulsante, il relativo stato cambia e il pulsante invia i codici di notifica, sotto forma di messaggi [**WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) alla finestra padre. Ad esempio, un controllo pulsante push invia il codice di notifica [BN \_ CLICKED](bn-clicked.md) ogni volta che l'utente sceglie il pulsante. In tutti i casi (ad eccezione di [BCN \_ HOTITEMCHANGE),](bcn-hotitemchange.md)la parola meno ordinata del *parametro wParam* contiene l'identificatore di controllo, la parola di ordine superiore *di wParam* contiene il codice di notifica e il *parametro lParam* contiene l'handle della finestra di controllo.

Sia il messaggio che la risposta della finestra padre dipendono dal tipo, dallo stile e dallo stato corrente del pulsante. Di seguito sono riportati i codici di notifica dei pulsanti che un'applicazione deve monitorare ed elaborare.



| Codice di notifica                                                        | Descrizione                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | Il mouse ha immesso o lasciato l'area client di un pulsante. |
| [BN \_ SU CUI È STATO FATTO CLIC](bn-clicked.md)                                            | L'utente ha fatto clic su un pulsante.                             |
| [BN \_ DBLCLK](bn-dblclk.md) o [BN \_ DOUBLECLICKED](bn-doubleclicked.md) | L'utente ha fatto doppio clic su un pulsante.                      |
| [BN \_ DISABLE](bn-disable.md)                                            | Un pulsante è disabilitato.                                  |
| [BN \_ PUSH](bn-pushed.md) o [BN \_ HILITE](bn-hilite.md)               | L'utente ha premuto un pulsante.                              |
| [BN \_ KILLFOCUS](bn-killfocus.md)                                        | Il pulsante ha perso lo stato attivo della tastiera.                    |
| [DISEGNO \_ BN](bn-paint.md)                                                | Il pulsante deve essere dipinta.                          |
| [BN \_ SETFOCUS](bn-setfocus.md)                                          | Il pulsante ha acquisito lo stato attivo della tastiera.                  |
| [BN \_ UNPUSHED](bn-unpushed.md) o [BN \_ UNHILITE](bn-unhilite.md)       | Il pulsante non viene più premuto.                        |



 

Un pulsante invia i codici di notifica [BN \_ DISABLE,](bn-disable.md) [BN \_ PUSHED,](bn-pushed.md) [BN \_ KILLFOCUS,](bn-killfocus.md) [BN \_ PAINT,](bn-paint.md) [BN \_ SETFOCUS](bn-setfocus.md)e [BN \_ UNPUSHED](bn-unpushed.md) solo se ha lo stile [**BS \_ NOTIFY.**](button-styles.md) [BN \_ I codici di notifica DBLCLK](bn-dblclk.md) vengono inviati automaticamente per i pulsanti [**BS \_ USERBUTTON**](button-styles.md), [**BS \_ RADIOBUTTON**](button-styles.md)e [**BS \_ OWNERDRAW.**](button-styles.md) Gli altri tipi di pulsante inviano \_ BN DBLCLK solo se hanno lo **stile BS \_ NOTIFY.** Tutti i pulsanti inviano il [codice di notifica BN \_ CLICKED](bn-clicked.md) indipendentemente dai relativi stili di pulsante.

Per i pulsanti automatici, il sistema modifica lo stato di push e disegna il pulsante. In questo caso, l'applicazione elabora in genere solo i codici di notifica [BN \_ CLICKED](bn-clicked.md) e [BN \_ DBLCLK.](bn-dblclk.md) Per i pulsanti non automatici, l'applicazione in genere risponde al codice di notifica inviando un messaggio per modificare lo stato del pulsante. Per informazioni sull'invio di messaggi ai pulsanti, vedere [Invio di messaggi ai pulsanti](#sending-messages-to-buttons).

Quando l'utente seleziona un pulsante disegnato dal proprietario, il pulsante invia alla finestra padre un messaggio [**WM \_ DRAWITEM**](wm-drawitem.md) contenente l'identificatore del controllo da disegnare e le informazioni sulle relative dimensioni e stato.

## <a name="button-color-messages"></a>Messaggi a colori dei pulsanti

Il sistema fornisce valori di colore predefiniti per i pulsanti. Un'applicazione può recuperare i valori predefiniti per questi colori chiamando la [**funzione GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) o impostando i valori chiamando la [**funzione SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) La tabella seguente mostra i valori predefiniti del colore del pulsante.



| Valore               | Colore dell'elemento                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| COLORE \_ BTNFACE      | Visi dei pulsanti.                                                                                                              |
| COLORE \_ BTNHIGHLIGHT | Area di evidenziazione (bordi superiore e sinistro) di un pulsante.                                                                       |
| COLORE \_ BTNSHADOW    | Area ombreggiata (i bordi inferiore e destro) di un pulsante.                                                                      |
| COLORE \_ BTNTEXT      | Testo normale (non ingrato) nei pulsanti.                                                                                       |
| COLOR \_ GRAYTEXT     | Testo disabilitato (grigio) nei pulsanti. Questo colore è impostato su 0 se il driver di visualizzazione corrente non supporta un colore grigio a tinta unita. |
| FINESTRA \_ A COLORI       | Sfondi della finestra.                                                                                                        |
| WINDOWFRAME \_ A COLORI  | Riquadri della finestra.                                                                                                             |
| FINESTRA \_ A COLORITESTO   | Testo nelle finestre.                                                                                                           |



 

Tuttavia, la [**chiamata a SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) influisce su tutte le applicazioni, pertanto non è consigliabile chiamare questa funzione per personalizzare i pulsanti per l'applicazione.

Il sistema invia un [**messaggio WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) alla finestra padre di un pulsante prima di disegnare un pulsante. Questo messaggio contiene un handle per il contesto di dispositivo del pulsante e un handle per la finestra figlio. La finestra padre può usare questi handle per modificare i colori del testo e dello sfondo del pulsante. Tuttavia, solo i pulsanti disegnati dal proprietario rispondono alla finestra padre che elabora il messaggio.

## <a name="button-default-message-processing"></a>Elaborazione dei messaggi predefinita del pulsante

La routine della finestra per la classe predefinita della finestra di controllo pulsante esegue l'elaborazione predefinita per tutti i messaggi che la procedura di controllo pulsante non elabora. Quando la routine del controllo pulsante restituisce **FALSE** per qualsiasi messaggio, la routine predefinita della finestra controlla i messaggi ed esegue le azioni predefinite elencate nella tabella seguente.



<table>
<colgroup>
<col  />
<col  />
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
<td>Invia al pulsante un <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> e un <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>messaggio WM_LBUTTONUP</strong></a> e invia alla finestra padre un <a href="bn-clicked.md">codice BN_CLICKED</a> notifica.</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Restituisce lo stato di controllo del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Restituisce un handle per la bitmap o l'icona associata al pulsante o <strong>NULL</strong> se il pulsante non dispone di bitmap o icona.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Restituisce lo stato del controllo corrente, lo stato di push e lo stato attivo del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Imposta lo stato del controllo per tutti gli stili dei pulsanti di opzione e delle caselle di controllo. Se il <em>parametro wParam</em> è maggiore di zero per i pulsanti di opzione, al pulsante viene assegnato <a href="/windows/desktop/winmsg/window-styles"><strong>lo WS_TABSTOP</strong></a> predefinito.</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Associa la bitmap o l'handle di icona specificato al pulsante e restituisce un handle alla bitmap o all'icona precedente.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Imposta lo stato di push del pulsante. Per i pulsanti disegnati dal proprietario, <a href="wm-drawitem.md"><strong>viene WM_DRAWITEM</strong></a> messaggio di errore alla finestra padre se lo stato del pulsante è stato modificato.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Imposta lo stile del pulsante. Se la parola più bassa del <em>parametro lParam</em> è <strong>TRUE,</strong>il pulsante viene ridisegnato.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Seleziona una casella di controllo o una casella di controllo automatica quando l'utente preme il tasto più (+) o uguale (=). Deseleziona una casella di controllo o una casella di controllo automatica quando l'utente preme il tasto meno (-).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Disegna il pulsante.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Cancella lo sfondo per i pulsanti disegnati dal proprietario. Gli sfondi di altri pulsanti vengono cancellati come parte dell'elaborazione WM_PAINT <a href="/windows/desktop/gdi/wm-paint"><strong>e</strong></a> <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> controllo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Restituisce valori che indicano il tipo di input elaborato dalla routine del pulsante predefinita, come illustrato nella tabella seguente. 
<table>
<thead>
<tr class="header">
<th>Stile del pulsante</th>
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

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Restituisce un handle per il tipo di carattere corrente.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Preme il pulsante se l'utente preme la BARRA SPAZIATRICE.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse per tutti i casi ad eccezione del tasto TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Rimuove il rettangolo di attivazione da un pulsante. Per i pulsanti di push e i pulsanti di push predefiniti, il rettangolo di attivazione viene invalidato. Se il pulsante ha mouse capture, l'acquisizione viene rilasciata, il pulsante non viene selezionato e viene rimosso qualsiasi stato di push.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Invia un <a href="bn-dblclk.md">BN_DBLCLK</a> di notifica alla finestra padre per i pulsanti di opzione e i pulsanti disegnati dal proprietario. Per gli altri pulsanti, un doppio clic viene elaborato come <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> messaggio.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Evidenzia il pulsante se la posizione del cursore del mouse si trova all'interno del rettangolo client del pulsante.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse se il pulsante ha il mouse capture.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Esegue la stessa azione di <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, se il pulsante ha mouse capture. In caso contrario, non viene eseguita alcuna azione.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Converte <a href="button-styles.md"><strong>qualsiasi BS_OWNERDRAW</strong></a> in un <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> pulsante.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Restituisce HTTRANSPARENT, se il controllo pulsante è una casella di gruppo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Disegna il pulsante in base allo stile e allo stato corrente.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Disegna un rettangolo di attivazione sul pulsante che riceve lo stato attivo. Per i pulsanti di opzione e i pulsanti di opzione automatici, alla finestra padre viene inviato <a href="bn-clicked.md">un BN_CLICKED</a> di notifica.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Imposta un nuovo tipo di carattere e, facoltativamente, aggiorna la finestra.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Imposta il testo del pulsante. Nel caso di una casella di gruppo, il messaggio disegna sul testo preesistente prima di ridisegnare la casella di gruppo con il nuovo testo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Rilascia l'acquisizione del mouse per tutti i casi ad eccezione del tasto TAB.</td>
</tr>
</tbody>
</table>



 

La routine di finestra predefinita passa tutti gli altri messaggi alla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di controllo](control-messages.md)
</dt> </dl>

 

 
