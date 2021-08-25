---
title: Operazioni di modifica del testo del controllo
description: Il sistema elabora automaticamente tutte le operazioni di testo avviate dall'utente e invia una notifica all'applicazione al termine delle operazioni.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8698fbd38241a0e5c3f40e69f7ab401fc22e3982e2bc70001733bc71daf49689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826371"
---
# <a name="edit-control-text-operations"></a>Operazioni di modifica del testo del controllo

Il sistema elabora automaticamente tutte le operazioni di testo avviate dall'utente e invia una notifica all'applicazione al termine delle operazioni.

Negli argomenti seguenti vengono illustrate le operazioni di testo avviate dall'utente e la risposta dell'applicazione:

-   [Selezione di un controllo di modifica](#selecting-an-edit-control)
-   [Impostazione e recupero di testo](#setting-and-retrieving-text)
-   [Selezione del testo](#selecting-text)
-   [Sostituzione di testo](#replacing-text)
-   [Modifica del tipo di carattere utilizzato da un controllo di modifica](#changing-the-font-used-by-an-edit-control)
-   [Operazioni Taglia Copia Incolla e Cancella](#cut-copy-paste-and-clear-operations)
-   [Modifica del testo](#modifying-text)
-   [Limitazione del testo immesso dall'utente](#limiting-user-entered-text)
-   [Operazioni su caratteri e righe](#character-and-line-operations)
-   [Scorrimento del testo in un controllo di modifica](#scrolling-text-in-an-edit-control)
-   [Impostazione di tabulazioni e margini](#setting-tab-stops-and-margins)
-   [Nascondere l'input dell'utente](#concealing-user-input)
-   [Uso di numeri interi](#using-integers)
-   [Annullamento delle operazioni di testo](#undoing-text-operations)
-   [Gestione del ritorno a capo e delle interruzioni di riga](#handling-wordwrap-and-line-breaks)
-   [Recupero di punti e caratteri](#retrieving-points-and-characters)
-   [Completamento automatico delle stringhe](#autocompletion-of-strings)
-   [Script complesso nei controlli di modifica](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Selezione di un controllo di modifica

L'utente può selezionare un controllo di modifica facendo clic su di esso con il mouse o premendo TAB per spostarsi su di esso. Il metodo tabbing fa parte di un'interfaccia della tastiera predefinita fornita dal sistema. Per una descrizione completa di questa interfaccia, vedere [Finestre di dialogo](/windows/desktop/dlgbox/dialog-boxes). Quando l'utente seleziona un controllo di modifica, il sistema assegna al controllo lo stato attivo della tastiera (vedere "Stato attivo e attivazione della tastiera" in Informazioni [sull'input](/windows/desktop/inputdev/about-keyboard-input)da tastiera) ed evidenzia il testo usando il video inverso.

## <a name="setting-and-retrieving-text"></a>Impostazione e recupero di testo

Un'applicazione può impostare il testo di un controllo di modifica usando la [**funzione SetWindowText,**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) [**la funzione SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) o inviando al controllo un [**messaggio WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)

Per recuperare tutto il testo da un controllo di modifica, usare prima di tutto la [**funzione GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) o il messaggio [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) per determinare le dimensioni del buffer necessarie per contenere il testo. Recuperare quindi il testo usando la [**funzione GetWindowText,**](/windows/desktop/DevNotes/-getwindowtext) [**la funzione GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) o il [**messaggio WM \_ GETTEXT.**](/windows/desktop/winmsg/wm-gettext)

## <a name="selecting-text"></a>Selezione del testo

Dopo aver selezionato un controllo di modifica, l'utente può selezionare il testo nel controllo usando il mouse o la tastiera. Un'applicazione può recuperare le posizioni dei caratteri iniziale e finale della selezione corrente in un controllo di modifica inviando al controllo un [**messaggio \_ EM GETSEL.**](em-getsel.md) Il valore restituito per la posizione finale è maggiore di uno rispetto all'ultimo carattere nella selezione, ovvero la posizione del primo carattere dopo l'ultimo carattere selezionato.

Un'applicazione può anche selezionare il testo in un controllo di modifica inviando al controllo un messaggio [**EM \_ SETSEL**](em-setsel.md) con gli indici dei caratteri iniziale e finale per la selezione. Ad esempio, l'applicazione può usare **EM \_ SETSEL** con [**EM \_ REPLACESEL**](em-replacesel.md) per eliminare testo da un controllo di modifica.

Questi tre messaggi si applicano sia ai controlli di modifica a riga singola che a più righe.

## <a name="replacing-text"></a>Sostituzione del testo

Un'applicazione può sostituire il testo selezionato in un controllo di modifica inviando al controllo un [**messaggio EM \_ REPLACESEL**](em-replacesel.md) con un puntatore al testo sostitutivo. Se non è presente alcuna selezione corrente, **EM \_ REPLACESEL** inserisce il testo di sostituzione nel punto di inserimento. L'applicazione può ricevere un [codice di notifica EN \_ ERRSPACE](en-errspace.md) se il testo sostitutivo supera la memoria disponibile. Questo messaggio si applica ai controlli di modifica a riga singola e a più righe.

Un'applicazione può [**usare EM \_ REPLACESEL**](em-replacesel.md) per sostituire parte del testo di un controllo di modifica o la [**funzione SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) per sostituirlo.

## <a name="changing-the-font-used-by-an-edit-control"></a>Modifica del tipo di carattere utilizzato da un controllo di modifica

Un'applicazione può modificare il tipo di carattere utilizzato da un controllo di modifica inviando il [**messaggio WM \_ SETFONT.**](/windows/desktop/winmsg/wm-setfont) La maggior parte delle applicazioni lo fa durante l'elaborazione [**del messaggio WM \_ INITDIALOG.**](/windows/desktop/dlgbox/wm-initdialog) La modifica del tipo di carattere non modifica le dimensioni del controllo di modifica. È possibile che le applicazioni che inviano il messaggio **WM \_ SETFONT** devono recuperare le metriche dei caratteri per il testo e ricalcolare le dimensioni del controllo di modifica. Per altre informazioni sui tipi di carattere e sulle metriche dei tipi di carattere, vedere [Tipi di carattere e testo](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Operazioni Taglia Copia Incolla e Cancella

Sono disponibili quattro messaggi per spostare il testo tra un controllo di modifica e gli Appunti. Il [**messaggio WM \_ COPY**](/windows/desktop/dataxchg/wm-copy) copia la selezione corrente (se presente) da un controllo di modifica negli Appunti senza eliminarla dal controllo di modifica. Il [**messaggio WM \_ CUT**](/windows/desktop/dataxchg/wm-cut) elimina la selezione corrente (se presente) nel controllo di modifica e copia il testo eliminato negli Appunti. Il [**messaggio WM \_ CLEAR**](/windows/desktop/dataxchg/wm-clear) elimina la selezione corrente (se presente) da un controllo di modifica, ma non la copia negli Appunti (a meno che l'utente non premuti il tasto MAIUSC). Il [**messaggio WM \_ PASTE**](/windows/desktop/dataxchg/wm-paste) copia il testo dagli Appunti in un controllo di modifica nel punto di inserimento. Questi quattro messaggi si applicano sia ai controlli di modifica a riga singola che a più righe.

Microsoft Windows NT 4.0 e versioni successive: un controllo di modifica include un menu di scelta rapida predefinito che semplifica lo spostamento del testo tra il controllo di modifica e gli Appunti. Il menu di scelta rapida viene visualizzato quando l'utente fa clic con il pulsante destro del mouse sul controllo. I comandi nel menu di scelta rapida includono **Annulla,** **Taglia**, **Copia** **,** Incolla , **Elimina** e **Seleziona tutto**.

## <a name="modifying-text"></a>Modifica del testo

L'utente può selezionare, eliminare o spostare testo in un controllo di modifica. Il sistema mantiene un flag interno per ogni controllo di modifica che indica se il contenuto del controllo è stato modificato. Il sistema cancella questo flag quando crea il controllo e imposta il flag ogni volta che il testo nel controllo viene modificato. Un'applicazione può recuperare il flag di modifica inviando al controllo [**un messaggio EM \_ GETMODIFY.**](em-getmodify.md) L'applicazione può quindi impostare o cancellare il flag di modifica inviando al controllo un [**messaggio EM \_ SETMODIFY.**](em-setmodify.md) Questi messaggi si applicano sia ai controlli di modifica a riga singola che a più righe.

## <a name="limiting-user-entered-text"></a>Limitazione del testo immesso dall'utente

Il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è 32 KB. Un'applicazione può modificare il limite predefinito inviando al controllo [**un messaggio EM \_ SETLIMITTEXT.**](em-setlimittext.md) Questo messaggio imposta un limite rigido al numero di byte che l'utente può immettere in un controllo di modifica, ma non influisce sul testo già presente nel controllo quando il messaggio è stato inviato né sul testo copiato nel controllo dalla funzione [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) o dal messaggio [**WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext) Si supponga, ad esempio, che l'applicazione usi la funzione **SetDlgItemText** per inserire 500 byte in un controllo di modifica e che l'utente immissione di 500 byte (totale 1.000 byte). Se l'applicazione invia quindi un messaggio **EM \_ SETLIMITTEXT** che limita il testo immesso dall'utente a 300 byte, i 1.000 byte già presenti nel controllo di modifica rimangono presenti e l'utente non può aggiungere altro testo. Se invece l'applicazione invia un messaggio **EM \_ SETLIMITTEXT** che limita il testo immesso dall'utente a 1.300 byte, i 1.000 byte rimangono, ma l'utente può aggiungere altri 300 byte.

Quando l'utente raggiunge il limite di caratteri di un controllo di modifica, il sistema invia all'applicazione un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) contenente un codice di notifica [EN \_ MAXTEXT.](en-maxtext.md) Questo codice di notifica non indica che la memoria è stata esaurita, ma che è stato raggiunto il limite per il testo immesso dall'utente. l'utente non può immettere altro testo. Per modificare questo limite, un'applicazione deve inviare al controllo un nuovo [**messaggio EM \_ SETLIMITTEXT**](em-setlimittext.md) con un limite superiore.

Come esempio dell'uso di [**EM \_ SETLIMITTEXT**](em-setlimittext.md) ed [EN \_ MAXTEXT,](en-maxtext.md)si supponga che l'applicazione deve limitare l'utente a non più di quattro caratteri in un controllo di modifica. L'applicazione **userebbe EM \_ SETLIMITTEXT** per specificare un limite di quattro caratteri. Se l'utente tentava di immettere un quinto carattere, il sistema inviava un codice di notifica EN \_ MAXTEXT all'applicazione.

## <a name="character-and-line-operations"></a>Operazioni su caratteri e righe

Esistono diversi messaggi che restituiscono informazioni sui caratteri e sulle righe in un controllo di modifica. La maggior parte dei messaggi restituisce un indice, in genere un numero in base zero, per fare riferimento a un carattere o a una riga. Ad esempio, in un controllo di modifica a riga singola che contiene n caratteri, l'indice di riga è zero e i caratteri vengono indicizzati da zero a n-1. In un controllo di modifica su più righe che contiene righe m e n caratteri, le righe vengono indicizzate da zero a m-1 e i caratteri vengono indicizzati da zero a n-1. Si noti che l'indicizzazione dei caratteri ignora le interruzioni di riga.

Un'applicazione può determinare il numero di caratteri in un controllo di modifica inviando il [**messaggio WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) al controllo di modifica. Questo messaggio restituisce la lunghezza, in caratteri (senza il carattere null di terminazione), del testo in un controllo di modifica a riga singola o su più righe. Il [**messaggio EM \_ LINELENGTH**](em-linelength.md) restituisce la lunghezza, in caratteri, di una riga specificata dall'indice dei caratteri di un carattere nella riga. La lunghezza restituita non include caratteri selezionati. Un'applicazione può usare questi messaggi in un controllo di modifica a riga singola o su più righe.

Il messaggio [**EM \_ GETFIRSTVISIBLELINE**](em-getfirstvisibleline.md) restituisce l'indice in base zero della riga visibile superiore in un controllo di modifica su più righe o l'indice in base zero del primo carattere visibile in un controllo di modifica a riga singola. Un'applicazione può copiare una riga da un controllo di modifica in un buffer inviando il [**messaggio \_ EM GETLINE**](em-getline.md) al controllo di modifica. La riga viene specificata dall'indice di riga e la prima parola del buffer ricevente contiene il numero massimo di byte da copiare nel buffer. Il valore restituito è il numero di byte copiati. Questo messaggio può essere usato anche in un controllo di modifica a riga singola o su più righe.

Sono disponibili messaggi univoci per restituire le informazioni su una riga in un controllo di modifica su più righe. Il [**messaggio EM \_ GETLINECOUNT**](em-getlinecount.md) restituisce il numero di righe in un controllo di modifica. Il [**messaggio EM \_ LINEFROMCHAR**](em-linefromchar.md) restituisce l'indice della riga contenente un indice di caratteri specificato. Il [**messaggio EM \_ LINEINDEX**](em-lineindex.md) restituisce l'indice del primo carattere in una riga specificata.

## <a name="scrolling-text-in-an-edit-control"></a>Scorrimento del testo in un controllo di modifica

Per implementare lo scorrimento in un controllo di modifica, è possibile usare gli stili di scorrimento automatico descritti [in](about-edit-controls.md)Modifica tipi di controllo e stili oppure è possibile aggiungere in modo esplicito barre di scorrimento al controllo di modifica. Per aggiungere una barra di scorrimento orizzontale, usare lo stile WS HSCROLL. Per aggiungere una barra di scorrimento verticale, usare lo stile \_ [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Un controllo di modifica con barre di scorrimento elabora i propri messaggi della barra di scorrimento. Per informazioni dettagliate sull'aggiunta di barre di scorrimento ai controlli di modifica, vedere [Barre di scorrimento](scroll-bars.md).

Il sistema fornisce tre messaggi che un'applicazione può inviare a un controllo di modifica con barre di scorrimento. Il [**messaggio EM \_ LINESCROLL**](em-linescroll.md) può scorrere un controllo di modifica su più righe sia verticalmente che orizzontalmente. Il *parametro lParam* specifica il numero di righe da scorrere verticalmente a partire dalla riga corrente e il *parametro wParam* specifica il numero di caratteri da scorrere orizzontalmente, a partire dal carattere corrente. Il controllo di modifica non riconosce i messaggi di scorrimento orizzontale se ha lo stile [**ES \_ CENTER**](edit-control-styles.md) o [**ES \_ RIGHT.**](edit-control-styles.md) Il **messaggio EM \_ LINESCROLL** si applica solo ai controlli di modifica su più righe.

Il [**messaggio EM \_ SCROLL**](em-scroll.md) scorre verticalmente un controllo di modifica su più righe. Il *parametro wParam* specifica l'azione di scorrimento. Il **messaggio EM \_ SCROLL** si applica solo ai controlli di modifica su più righe. **EM \_ SCROLL** ha lo stesso effetto del [**messaggio WM \_ VSCROLL.**](wm-vscroll.md)

Il [**messaggio EM \_ SCROLLCARET**](em-scrollcaret.md) scorre il punto di accesso alla visualizzazione in un controllo di modifica.

## <a name="setting-tab-stops-and-margins"></a>Impostazione di tabulazioni e margini

Un'applicazione può impostare tabulazioni in un controllo di modifica su più righe usando il [**messaggio EM \_ SETTABSTOPS.**](em-settabstops.md) L'impostazione predefinita per una tabulazione è otto caratteri. Quando un'applicazione aggiunge testo al controllo di modifica, i caratteri di tabulazione nel testo generano automaticamente spazio fino alla tabulazione successiva. Il **messaggio EM \_ SETTABSTOPS** non fa sì che il sistema ridisegni automaticamente il testo. A tale scopo, un'applicazione può chiamare la [**funzione InvalidateRect.**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) Il **messaggio EM \_ SETTABSTOPS** si applica solo ai controlli di modifica su più righe.

Un'applicazione può impostare la larghezza dei margini sinistro e destro per un controllo di modifica usando il messaggio [**EM \_ SETMARGINS.**](em-setmargins.md) Dopo aver inviato questo messaggio, il sistema ridisegna il controllo di modifica per riflettere le nuove impostazioni del margine. Un'applicazione può recuperare la larghezza del margine sinistro o destro inviando il [**messaggio EM \_ GETMARGINS.**](em-getmargins.md) Per impostazione predefinita, i margini del controllo di modifica sono impostati sufficientemente larghi per contenere la sporgenza orizzontale del carattere più grande (larghezze ABC negative) per il tipo di carattere corrente usato nel controllo di modifica.

## <a name="concealing-user-input"></a>Nascondere l'input dell'utente

Un'applicazione può usare un carattere password in un controllo di modifica per nascondere l'input dell'utente. Quando un carattere password è impostato, viene visualizzato al posto di ogni carattere tipiato dall'utente. Quando viene rimosso un carattere della password, il controllo visualizza i caratteri che l'utente digitare. Se l'applicazione crea un controllo di modifica a riga singola usando lo stile [**ES \_ PASSWORD**](edit-control-styles.md), il carattere della password predefinito è un asterisco ( \* ). Un'applicazione può usare il messaggio [**EM \_ SETPASSWORDCHAR**](em-setpasswordchar.md) per rimuovere o definire un carattere di password diverso e il messaggio [**EM \_ GETPASSWORDCHAR**](em-getpasswordchar.md) per recuperare il carattere della password corrente. Questi messaggi si applicano solo ai controlli di modifica a riga singola.

## <a name="using-integers"></a>Uso di numeri interi

Esistono due funzioni di conversione di interi per i controlli di modifica progettati per contenere solo numeri. La [**funzione SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) crea la rappresentazione di stringa di un intero specificato (con segno o senza segno) e invia la stringa a un controllo di modifica. **SetDlgItemInt non** restituisce alcun valore. La [**funzione GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) crea un intero (con o senza segno) dalla relativa rappresentazione di stringa in un controllo di modifica. **GetDlgItemInt** restituisce il numero intero (o un valore di errore).

## <a name="undoing-text-operations"></a>Annullamento delle operazioni di testo

Ogni controllo di modifica mantiene un flag di annullamento che indica se un'applicazione può annullare o annullare l'operazione più recente sul controllo di modifica , ad esempio annullando un'eliminazione di testo. Il controllo di modifica imposta il flag di annullamento per indicare che l'operazione può essere annullata e la reimposta per indicare che l'operazione non può essere annullata. Un'applicazione può determinare l'impostazione del flag di annullamento inviando al controllo un [**messaggio EM \_ CANUNDO.**](em-canundo.md)

Un'applicazione può annullare l'operazione più recente inviando al controllo un [**messaggio EM \_ UNDO.**](em-undo.md) Un'operazione può essere annullata a condizione che non si verifichi prima un'altra operazione di controllo di modifica. Ad esempio, l'utente può eliminare il testo, sostituire il testo (annullare l'eliminazione) e quindi eliminare nuovamente il testo (annullare la sostituzione). Il **messaggio EM \_ UNDO** si applica ai controlli di modifica a riga singola e a più righe e funziona sempre per i controlli di modifica a riga singola.

Un'applicazione può reimpostare il flag di annullamento di un controllo di modifica inviando al controllo un [**messaggio EM \_ EMPTYUNDOBUFFER.**](em-emptyundobuffer.md) Il sistema reimposta automaticamente il flag di annullamento ogni volta che un controllo di modifica riceve un [**messaggio EM \_ SETHANDLE**](em-sethandle.md) o [**WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext) La [**funzione SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) invia un **messaggio WM \_ SETTEXT.**

## <a name="handling-wordwrap-and-line-breaks"></a>Gestione del ritorno a capo e delle interruzioni di riga

Un'applicazione può usare funzioni wordwrap con controlli di modifica su più righe per individuare la parola o il frammento di parola di cui eseguire il wrapping alla riga successiva. Usando la funzione wordwrap predefinita fornita dal sistema, le righe terminano sempre in corrispondenza degli spazi tra le parole. Un'applicazione può specificare la propria funzione Wordwrap specificando una funzione [*Wordwrap EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) e inviando al controllo di modifica un messaggio [**EM \_ SETWORDBREAKPROC.**](em-setwordbreakproc.md) Un'applicazione può recuperare l'indirizzo della funzione Wordwrap corrente inviando al controllo un [**messaggio EM \_ GETWORDBREAKPROC.**](em-getwordbreakproc.md)

Un'applicazione può indirizzare un controllo di modifica su più righe per aggiungere o rimuovere automaticamente un carattere di interruzione di riga soft (due ritorni a capo e un avanzamento riga) alla fine delle righe di testo con ritorno a capo. Un'applicazione può attivare o disattivare questa funzionalità inviando al controllo di modifica un [**messaggio \_ EM FMTLINES.**](em-fmtlines.md) Questo messaggio si applica solo ai controlli di modifica su più righe e non influisce su una riga che termina con un'interruzione di riga (un ritorno a capo e un avanzamento riga immessi dall'utente). Anche nei controlli di modifica su più righe, un'applicazione può specificare lo stile [**ES \_ WANTRETURN**](edit-control-styles.md) per richiedere al sistema di inserire un ritorno a capo quando l'utente preme il tasto INVIO nel controllo di modifica.

## <a name="retrieving-points-and-characters"></a>Recupero di punti e caratteri

Per determinare il carattere più vicino a un punto specificato nell'area client di un controllo di modifica, inviare il messaggio [**EM \_ CHARFROMPOS**](em-charfrompos.md) al controllo. Il messaggio restituisce l'indice dei caratteri e l'indice di riga del carattere più vicino al punto. Analogamente, è possibile recuperare le coordinate dell'area client di un carattere specificato inviando il [**messaggio EM \_ POSFROMCHAR.**](em-posfromchar.md) Il messaggio restituisce le coordinate x e y dell'angolo superiore sinistro del carattere specificato.

## <a name="autocompletion-of-strings"></a>Completamento automatico delle stringhe

Il completamento automatico espande le stringhe immesse parzialmente in un controllo di modifica in stringhe complete. Ad esempio, quando un utente inizia a immettere un URL nel controllo di modifica Indirizzo incorporato nella barra degli strumenti di Windows Internet Explorer, il completamento automatico espande la stringa in uno o più URL completi coerenti con la stringa parziale esistente. Una stringa di URL parziale, ad esempio "mic", potrebbe essere espansa in " https://www.microsoft.com " o https://www.microsoft.com/windows " ". Il completamento automatico viene in genere usato con i controlli di modifica o con i controlli con un controllo di modifica incorporato.

Per altre informazioni, vedere la documentazione [**dell'interfaccia IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) e [**IAutoComplete2.**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2)

## <a name="complex-script-in-edit-controls"></a>Script complesso nei controlli di modifica

Uno *script complesso* è un linguaggio il cui formato stampato non è strutturato in modo semplice. Ad esempio, uno script complesso può consentire il rendering bidirezionale, la modellazione contestuale dei glifi o la combinazione di caratteri. I controlli di modifica standard sono stati estesi per supportare testo multilingue e script complessi. Ciò include non solo l'input e la visualizzazione, ma anche lo spostamento corretto del cursore sui cluster di caratteri (ad esempio, nello script Tailandese e Devanagari).

Un'applicazione ben scritta riceve questo supporto automaticamente, senza modifiche. Anche in questo caso, è consigliabile aggiungere il supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra. In questo caso, attivare o disattivare i flag di stile estesi della finestra del controllo di modifica per controllare questi attributi, come illustrato nell'esempio seguente.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Dopo aver impostato **il valore lAlign,** abilitare la nuova visualizzazione impostando lo stile esteso della finestra di controllo di modifica come indicato di seguito.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe è un altro set di funzioni che forniscono un controllo fine per l'elaborazione di script complessi. Per altre informazioni, vedere [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 