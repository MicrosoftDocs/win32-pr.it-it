---
title: Modificare le operazioni di testo del controllo
description: Il sistema elabora automaticamente tutte le operazioni di testo avviate dall'utente e invia una notifica all'applicazione quando le operazioni vengono completate.
ms.assetid: 9af3a1bc-4c87-4cc9-966d-50742be7c811
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9640616cf70b9a2933ef9d4c3fdb2accbfdcabf0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047423"
---
# <a name="edit-control-text-operations"></a>Modificare le operazioni di testo del controllo

Il sistema elabora automaticamente tutte le operazioni di testo avviate dall'utente e invia una notifica all'applicazione quando le operazioni vengono completate.

Negli argomenti seguenti vengono illustrate le operazioni di testo avviate dall'utente e la risposta dell'applicazione:

-   [Selezione di un controllo di modifica](#selecting-an-edit-control)
-   [Impostazione e recupero di testo](#setting-and-retrieving-text)
-   [Selezione del testo](#selecting-text)
-   [Sostituzione di testo](#replacing-text)
-   [Modifica del tipo di carattere utilizzato da un controllo di modifica](#changing-the-font-used-by-an-edit-control)
-   [Taglia operazioni di copia incolla e cancella](#cut-copy-paste-and-clear-operations)
-   [Modifica di testo](#modifying-text)
-   [Limitazione del testo immesso dall'utente](#limiting-user-entered-text)
-   [Operazioni di tipo carattere e riga](#character-and-line-operations)
-   [Scorrimento del testo in un controllo di modifica](#scrolling-text-in-an-edit-control)
-   [Impostazione di tabulazioni e margini](#setting-tab-stops-and-margins)
-   [Nascondi input utente](#concealing-user-input)
-   [Uso di numeri interi](#using-integers)
-   [Non eseguire operazioni di testo](#undoing-text-operations)
-   [Gestione di WordWrap e interruzioni di riga](#handling-wordwrap-and-line-breaks)
-   [Recupero di punti e caratteri](#retrieving-points-and-characters)
-   [Completamento automatico delle stringhe](#autocompletion-of-strings)
-   [Script complesso nei controlli di modifica](#complex-script-in-edit-controls)

## <a name="selecting-an-edit-control"></a>Selezione di un controllo di modifica

L'utente può selezionare un controllo di modifica facendo clic su di esso con il mouse oppure premendo il tasto TAB per spostarsi su di esso. Il metodo di tabulazione fa parte di un'interfaccia di tastiera predefinita fornita dal sistema. Per una descrizione completa di questa interfaccia, vedere finestre di [dialogo](/windows/desktop/dlgbox/dialog-boxes). Quando l'utente seleziona un controllo di modifica, il sistema fornisce al controllo lo stato attivo per la tastiera (vedere "attivazione e attivazione della tastiera" in [informazioni sull'input da tastiera](/windows/desktop/inputdev/about-keyboard-input)) ed evidenzia il testo usando il video inverso.

## <a name="setting-and-retrieving-text"></a>Impostazione e recupero di testo

Un'applicazione può impostare il testo di un controllo di modifica usando la funzione [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) , la funzione [**SetDlgItemText**](/windows/desktop/DevNotes/-setdlgitemtext) oppure inviando il controllo a un messaggio di [**\_ testo WM**](/windows/desktop/winmsg/wm-settext) .

Per recuperare tutto il testo da un controllo di modifica, usare prima la funzione [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) o il messaggio [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) per determinare le dimensioni del buffer necessarie per contenere il testo. Recuperare quindi il testo usando la funzione [**GetWindowText**](/windows/desktop/DevNotes/-getwindowtext) , la funzione [**GetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-getdlgitemtexta) o il messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) .

## <a name="selecting-text"></a>Selezione del testo

Dopo aver selezionato un controllo di modifica, l'utente può selezionare il testo nel controllo utilizzando il mouse o la tastiera. Un'applicazione può recuperare le posizioni dei caratteri iniziale e finale della selezione corrente in un controllo di modifica inviando al controllo un messaggio [**\_ GETSEL em**](em-getsel.md) . Il valore restituito per la posizione finale è maggiore di uno rispetto all'ultimo carattere della selezione, ovvero la posizione del primo carattere che segue l'ultimo carattere selezionato.

Un'applicazione può anche selezionare il testo in un controllo di modifica inviando il controllo un messaggio [**\_ SETSEL em**](em-setsel.md) con gli indici dei caratteri iniziale e finale per la selezione. Ad esempio, l'applicazione può usare **em \_ SETSEL** con [**em \_ REPLACESEL**](em-replacesel.md) per eliminare il testo da un controllo di modifica.

Questi tre messaggi si applicano ai controlli di modifica a riga singola e a più righe.

## <a name="replacing-text"></a>Sostituzione di testo

Un'applicazione può sostituire il testo selezionato in un controllo di modifica inviando il controllo un messaggio [**\_ REPLACESEL em**](em-replacesel.md) con un puntatore al testo sostitutivo. Se non è presente alcuna selezione corrente, **em \_ REPLACESEL** inserisce il testo di sostituzione in corrispondenza del punto di inserimento. Se il testo di sostituzione supera la memoria disponibile, l'applicazione può ricevere un codice di notifica [en \_ ERRSPACE](en-errspace.md) . Questo messaggio si applica ai controlli di modifica a riga singola e a più righe.

Un'applicazione può usare [**em \_ REPLACESEL**](em-replacesel.md) per sostituire parte del testo di un controllo di modifica o la funzione [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) per sostituirla.

## <a name="changing-the-font-used-by-an-edit-control"></a>Modifica del tipo di carattere utilizzato da un controllo di modifica

Un'applicazione può modificare il tipo di carattere utilizzato da un controllo di modifica inviando il messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) . Questa operazione viene eseguita dalla maggior parte delle applicazioni durante l'elaborazione del messaggio [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . La modifica del tipo di carattere non modifica le dimensioni del controllo di modifica; le applicazioni che inviano il messaggio di **\_ tipo carattere di tipo WM** possono dover recuperare la metrica del tipo di carattere per il testo e ricalcolare le dimensioni del controllo di modifica. Per altre informazioni sui tipi di carattere e sulle metriche dei tipi di carattere, vedere [caratteri e testo](/windows/desktop/gdi/fonts-and-text).

## <a name="cut-copy-paste-and-clear-operations"></a>Taglia operazioni di copia incolla e cancella

Sono disponibili quattro messaggi per lo trasferimento di testo tra un controllo di modifica e gli Appunti. Il messaggio di [**\_ copia WM**](/windows/desktop/dataxchg/wm-copy) copia la selezione corrente, se presente, da un controllo di modifica negli Appunti senza eliminarlo dal controllo di modifica. Il messaggio [**WM \_ Cut**](/windows/desktop/dataxchg/wm-cut) Elimina la selezione corrente (se presente) nel controllo di modifica e copia il testo eliminato negli Appunti. Il messaggio [**WM \_ Clear**](/windows/desktop/dataxchg/wm-clear) Elimina la selezione corrente, se presente, da un controllo di modifica, ma non lo copia negli Appunti, a meno che l'utente non abbia premuto il tasto MAIUSC. Il messaggio [**WM \_ Incolla**](/windows/desktop/dataxchg/wm-paste) copia il testo dagli Appunti in un controllo di modifica nel punto di inserimento. Questi quattro messaggi si applicano ai controlli di modifica a riga singola e a più righe.

Microsoft Windows NT 4,0 e versioni successive: un controllo di modifica include un menu di scelta rapida incorporato che rende più semplice per l'utente spostare il testo tra il controllo di modifica e gli Appunti. Il menu di scelta rapida viene visualizzato quando l'utente fa clic con il pulsante destro del mouse sul controllo. I comandi nel menu di scelta rapida includono le opzioni **Annulla**, **taglia**, **copia**, **Incolla**, **Elimina** e **Seleziona tutto**.

## <a name="modifying-text"></a>Modifica di testo

L'utente può selezionare, eliminare o spostare il testo in un controllo di modifica. Il sistema mantiene un flag interno per ogni controllo di modifica che indica se il contenuto del controllo è stato modificato. Il sistema cancella questo flag quando crea il controllo e imposta il flag ogni volta che il testo nel controllo viene modificato. Un'applicazione può recuperare il flag di modifica inviando al controllo un messaggio [**\_ GetModify em**](em-getmodify.md) . L'applicazione può quindi impostare o deselezionare il flag di modifica inviando il controllo un messaggio di modifica [**em \_**](em-setmodify.md) . Questi messaggi si applicano ai controlli di modifica a riga singola e a più righe.

## <a name="limiting-user-entered-text"></a>Limitazione del testo immesso dall'utente

Il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è 32 KB. Un'applicazione può modificare il limite predefinito inviando il controllo un [**messaggio \_ SETLIMITTEXT em**](em-setlimittext.md) . Questo messaggio consente di impostare un limite rigido per il numero di byte che l'utente può immettere in un controllo di modifica, ma non influiscono sul testo che è già presente nel controllo quando il messaggio è stato inviato, né sul testo copiato nel controllo mediante la funzione [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) o il messaggio di testo [**WM \_**](/windows/desktop/winmsg/wm-settext) . Si supponga, ad esempio, che l'applicazione usi la funzione **SetDlgItemText** per inserire 500 byte in un controllo di modifica e che l'utente immetta anche 500 byte (1.000 byte totali). Se l'applicazione invia quindi un messaggio **em \_ SETLIMITTEXT** che limita il testo immesso dall'utente a 300 byte, i 1.000 byte già presenti nel controllo di modifica rimarranno in tale posizione e l'utente non potrà aggiungere altro testo. D'altra parte, se l'applicazione invia un messaggio **em \_ SETLIMITTEXT** limitando il testo immesso dall'utente a 1.300 byte, i 1.000 byte rimangono, ma l'utente può aggiungere 300 più byte.

Quando l'utente raggiunge il limite di caratteri di un controllo di modifica, il sistema invia all'applicazione un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) contenente un codice di notifica [en \_ MAXTEXT](en-maxtext.md) . Questo codice di notifica non significa che la memoria è stata esaurita, ma che è stato raggiunto il limite per il testo immesso dall'utente. l'utente non può immettere altro testo. Per modificare questo limite, un'applicazione deve inviare al controllo un nuovo [**messaggio \_ SETLIMITTEXT em**](em-setlimittext.md) con un limite superiore.

Come esempio di utilizzo di [**em \_ SETLIMITTEXT**](em-setlimittext.md) e [en \_ MAXTEXT](en-maxtext.md), si supponga che l'applicazione debba limitare l'utente a non più di quattro caratteri in un controllo di modifica. L'applicazione userà **em \_ SETLIMITTEXT** per specificare un limite di quattro caratteri. Se l'utente ha tentato di immettere un quinto carattere, il sistema invierà un \_ codice di notifica en MAXTEXT all'applicazione.

## <a name="character-and-line-operations"></a>Operazioni di tipo carattere e riga

Sono disponibili diversi messaggi che restituiscono informazioni sui caratteri e le righe in un controllo di modifica. La maggior parte dei messaggi restituisce un indice, in genere un numero in base zero, per fare riferimento a un carattere o a una riga. Ad esempio, in un controllo di modifica a riga singola che contiene n caratteri, l'indice di riga è zero e i caratteri sono indicizzati da zero a n-1. In un controllo di modifica su più righe che contiene m righe e n caratteri, le linee vengono indicizzate da zero a m-1 e i caratteri vengono indicizzati da zero a n-1. Si noti che l'indicizzazione di caratteri ignora le interruzioni di riga.

Un'applicazione può determinare il numero di caratteri in un controllo di modifica inviando il messaggio [**WM \_ GETTEXTLENGTH**](/windows/desktop/winmsg/wm-gettextlength) al controllo di modifica. Questo messaggio restituisce la lunghezza, in caratteri, escluso il carattere null di terminazione, del testo in un controllo di modifica a riga singola o su più righe. Il [**messaggio \_ LINELENGTH em**](em-linelength.md) restituisce la lunghezza, in caratteri, di una riga specificata dall'indice dei caratteri di un carattere nella riga. La lunghezza restituita non include alcun carattere selezionato. Un'applicazione può usare questi messaggi in un controllo di modifica a riga singola o su più righe.

Il [**messaggio \_ GETFIRSTVISIBLELINE em**](em-getfirstvisibleline.md) restituisce l'indice in base zero della riga visibile più in alto in un controllo di modifica a più righe o l'indice in base zero del primo carattere visibile in un controllo di modifica a riga singola. Un'applicazione può copiare una riga da un controllo di modifica in un buffer inviando il messaggio [**\_ getline em**](em-getline.md) al controllo di modifica. La riga viene specificata in base all'indice di riga e la prima parola del buffer di ricezione contiene il numero massimo di byte da copiare nel buffer. Il valore restituito è il numero di byte copiati. Questo messaggio può essere usato anche in un controllo di modifica a riga singola o su più righe.

Sono disponibili messaggi univoci per restituire le informazioni su una riga in un controllo di modifica su più righe. Il [**messaggio \_ GETLINECOUNT em**](em-getlinecount.md) restituisce il numero di righe in un controllo di modifica. Il [**messaggio \_ LINEFROMCHAR em**](em-linefromchar.md) restituisce l'indice della riga contenente un indice dei caratteri specificato. Il [**messaggio \_ LINEINDEX em**](em-lineindex.md) restituisce l'indice del primo carattere in una riga specificata.

## <a name="scrolling-text-in-an-edit-control"></a>Scorrimento del testo in un controllo di modifica

Per implementare lo scorrimento in un controllo di modifica, è possibile usare gli stili di scorrimento automatico descritti in [modifica tipi di controllo e stili](about-edit-controls.md)oppure è possibile aggiungere in modo esplicito le barre di scorrimento al controllo di modifica. Per aggiungere una barra di scorrimento orizzontale, utilizzare lo stile WS \_ HSCROLL; per aggiungere una barra di scorrimento verticale, utilizzare lo stile [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles). Un controllo di modifica con barre di scorrimento elabora i propri messaggi della barra di scorrimento. Per informazioni dettagliate sull'aggiunta di barre di scorrimento ai controlli di modifica, vedere [barre di scorrimento](scroll-bars.md).

Il sistema fornisce tre messaggi che un'applicazione può inviare a un controllo di modifica con barre di scorrimento. Il [**messaggio \_ LINESCROLL em**](em-linescroll.md) può scorrere un controllo di modifica su più righe sia verticalmente che orizzontalmente. Il parametro *lParam* specifica il numero di righe da scorrere verticalmente a partire dalla riga corrente e il parametro *wParam* specifica il numero di caratteri da scorrere orizzontalmente, a partire dal carattere corrente. Il controllo di modifica non riconosce i messaggi di scorrimento orizzontale se presenta lo stile [**es \_ Center**](edit-control-styles.md) o [**es \_ right**](edit-control-styles.md) . Il **messaggio \_ LINESCROLL em** si applica solo ai controlli di modifica su più righe.

Il messaggio di [**\_ scorrimento em**](em-scroll.md) scorre verticalmente un controllo di modifica su più righe. Il parametro *wParam* specifica l'azione di scorrimento. Il messaggio di **\_ scorrimento em** si applica solo ai controlli di modifica su più righe. **Em \_ SCROLL** ha lo stesso effetto del messaggio [**WM \_ VSCROLL**](wm-vscroll.md) .

Il [**messaggio \_ SCROLLCARET em**](em-scrollcaret.md) scorre il punto di inserimento nella visualizzazione in un controllo di modifica.

## <a name="setting-tab-stops-and-margins"></a>Impostazione di tabulazioni e margini

Un'applicazione può impostare le tabulazioni in un controllo di modifica su più righe usando il messaggio [**\_ SETTABSTOPS em**](em-settabstops.md) . Il valore predefinito per una tabulazione è di otto caratteri. Quando un'applicazione aggiunge testo al controllo di modifica, i caratteri di tabulazione nel testo generano automaticamente lo spazio fino alla tabulazione successiva. Il **messaggio \_ SETTABSTOPS em** non determina automaticamente il riprogetto del testo da parte del sistema. A tale scopo, un'applicazione può chiamare la funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) . Il **messaggio \_ SETTABSTOPS em** si applica solo ai controlli di modifica su più righe.

Un'applicazione può impostare la larghezza dei margini sinistro e destro per un controllo di modifica tramite il messaggio [**em \_ semargins**](em-setmargins.md) . Dopo l'invio del messaggio, il sistema riestrae il controllo di modifica in modo da riflettere le nuove impostazioni dei margini. Un'applicazione può recuperare la larghezza del margine sinistro o destro inviando il messaggio [**\_ GetMargins em**](em-getmargins.md) . Per impostazione predefinita, i margini del controllo di modifica sono impostati in modo sufficientemente ampio da contenere la sporgenza orizzontale del carattere più grande (larghezze ABC negative) per il tipo di carattere corrente usato nel controllo di modifica.

## <a name="concealing-user-input"></a>Nascondi input utente

Un'applicazione può usare un carattere di password in un controllo di modifica per nascondere l'input dell'utente. Quando viene impostato un carattere di password, viene visualizzato al posto di ogni carattere che l'utente digita. Quando viene rimosso un carattere della password, il controllo Visualizza i caratteri che i tipi di utente. Se l'applicazione crea un controllo di modifica a riga singola usando la [**\_ password**](edit-control-styles.md)di tipo es, il carattere predefinito per la password è un asterisco ( \* ). Un'applicazione può usare il [**messaggio \_ SETPASSWORDCHAR em**](em-setpasswordchar.md) per rimuovere o definire un carattere diverso per la password e il messaggio [**\_ GETPASSWORDCHAR em**](em-getpasswordchar.md) per recuperare il carattere della password corrente. Questi messaggi si applicano solo ai controlli di modifica a riga singola.

## <a name="using-integers"></a>Uso di numeri interi

Sono disponibili due funzioni di conversione integer per i controlli di modifica progettati per contenere solo numeri. La funzione [**SetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-setdlgitemint) crea la rappresentazione di stringa di un intero specificato (con segno o senza segno) e Invia la stringa a un controllo di modifica. **SetDlgItemInt** non restituisce alcun valore. La funzione [**GetDlgItemInt**](/windows/desktop/api/winuser/nf-winuser-getdlgitemint) crea un intero (con segno o senza segno) dalla relativa rappresentazione di stringa in un controllo di modifica. **GetDlgItemInt** restituisce l'intero (o un valore di errore).

## <a name="undoing-text-operations"></a>Non eseguire operazioni di testo

Ogni controllo di modifica gestisce un flag di annullamento che indica se un'applicazione può invertire o annullare l'operazione più recente sul controllo di modifica (ad esempio, annullando un'eliminazione del testo). Il controllo di modifica imposta il flag di annullamento per indicare che l'operazione può essere annullata e reimpostata per indicare che l'operazione non può essere annullata. Un'applicazione può determinare l'impostazione del flag di annullamento inviando il controllo un [**messaggio \_ CANUNDO em**](em-canundo.md) .

Un'applicazione può annullare l'operazione più recente inviando al controllo un messaggio di [**\_ annullamento em**](em-undo.md) . Un'operazione può essere annullata purché non venga eseguita per prima un'altra operazione di modifica del controllo. Ad esempio, l'utente può eliminare il testo, sostituire il testo (annullare l'eliminazione), quindi eliminare nuovamente il testo (annullare la sostituzione). Il messaggio di **\_ annullamento em** si applica ai controlli di modifica a riga singola e a più righe e funziona sempre per i controlli di modifica a riga singola.

Un'applicazione può reimpostare il flag di annullamento di un controllo di modifica inviando al controllo un messaggio [**\_ EMPTYUNDOBUFFER em**](em-emptyundobuffer.md) . Il sistema Reimposta automaticamente il flag di annullamento ogni volta che un controllo di modifica riceve un messaggio [**em \_ filehandle**](em-sethandle.md) o [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) . La funzione [**SetDlgItemText**](/windows/desktop/api/winuser/nf-winuser-setdlgitemtexta) Invia un messaggio di **\_ testo WM** .

## <a name="handling-wordwrap-and-line-breaks"></a>Gestione di WordWrap e interruzioni di riga

Un'applicazione può utilizzare le funzioni WordWrap con i controlli di modifica su più righe per individuare il frammento di parola o di parola di cui è necessario eseguire il wrapped alla riga successiva. Utilizzando la funzione WordWrap predefinita fornita dal sistema, le linee terminano sempre negli spazi tra le parole. Un'applicazione può specificare la propria funzione WordWrap fornendo una funzione WordWrap [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) e inviando il controllo di modifica un [**messaggio \_ SETWORDBREAKPROC em**](em-setwordbreakproc.md) . Un'applicazione può recuperare l'indirizzo della funzione WordWrap corrente inviando al controllo un messaggio [**\_ GETWORDBREAKPROC em**](em-getwordbreakproc.md) .

Un'applicazione può indirizzare un controllo di modifica su più righe per aggiungere o rimuovere un carattere di interruzioni di riga Soft (due ritorni a capo e un avanzamento riga) automaticamente alla fine delle righe di testo incapsulato. Un'applicazione può attivare o disattivare questa funzionalità inviando il controllo modifica un messaggio [**\_ FMTLINES em**](em-fmtlines.md) . Questo messaggio si applica solo ai controlli di modifica su più righe e non influisce su una riga che termina con un'interruzioni di riga rigido (un ritorno a capo e un avanzamento riga immesso dall'utente). Inoltre, nei controlli di modifica su più righe, un'applicazione può specificare lo stile [**es \_ WANTRETURN**](edit-control-styles.md) per richiedere che il sistema inserisca un ritorno a capo quando l'utente preme il tasto invio nel controllo di modifica.

## <a name="retrieving-points-and-characters"></a>Recupero di punti e caratteri

Per determinare il carattere più vicino a un punto specificato nell'area client di un controllo di modifica, inviare il [**messaggio \_ CHARFROMPOS em**](em-charfrompos.md) al controllo. Il messaggio restituisce l'indice dei caratteri e l'indice di riga del carattere più vicino al punto. Analogamente, è possibile recuperare le coordinate dell'area client di un carattere specificato inviando il messaggio [**\_ POSFROMCHAR em**](em-posfromchar.md) . Il messaggio restituisce le coordinate x e y dell'angolo superiore sinistro del carattere specificato.

## <a name="autocompletion-of-strings"></a>Completamento automatico delle stringhe

Il completamento automatico espande le stringhe che sono state immesse parzialmente in un controllo di modifica in stringhe complete. Ad esempio, quando un utente inizia a immettere un URL nel controllo di modifica degli indirizzi incorporato nella barra degli strumenti di Windows Internet Explorer, il completamento automatico espande la stringa in uno o più URL completi coerenti con la stringa parziale esistente. Una stringa URL parziale, ad esempio "MIC", può essere espansa in " https://www.microsoft.com " o " https://www.microsoft.com/windows ". Il completamento automatico viene in genere usato con i controlli di modifica o con controlli che dispongono di un controllo di modifica incorporato.

Per ulteriori informazioni, vedere la documentazione sull'interfaccia [**IAutoComplete**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete) e [**IAutoComplete2**](/windows/desktop/api/shldisp/nn-shldisp-iautocomplete2) .

## <a name="complex-script-in-edit-controls"></a>Script complesso nei controlli di modifica

Uno *script complesso* è un linguaggio il cui formato stampato non è disposto in modo semplice. Uno script complesso, ad esempio, può consentire il rendering bidirezionale, il Shaping contestuale dei glifi o la combinazione di caratteri. I controlli di modifica standard sono stati estesi per supportare testo multilingue e script complessi. Sono inclusi, ad esempio, non solo l'input e la visualizzazione, ma anche lo spostamento corretto del cursore sui cluster di caratteri (ad esempio, nello script Thai e devangat).

Un'applicazione ben scritta riceve questo supporto automaticamente, senza alcuna modifica. Anche in questo caso, è consigliabile aggiungere il supporto per l'ordine di lettura da destra a sinistra e l'allineamento a destra. In questo caso, impostare i flag di stile estesi della finestra del controllo di modifica in modo da controllare questi attributi, come illustrato nell'esempio seguente.


```
// ID_EDITCONTROL is the control ID in the resource file.
HANDLE hWndEdit = GetDlgItem(hDlg, ID_EDITCONTROL);
LONG lAlign = GetWindowLong(hWndEdit, GWL_EXSTYLE) ;

// To toggle alignment
lAlign ^= WS_EX_RIGHT ;

// To toggle reading order
lAlign ^= WS_EX_RTLREADING ;
```



Dopo aver impostato il valore **lAlign** , abilitare la nuova visualizzazione impostando lo stile esteso della finestra di controllo di modifica come indicato di seguito.


```
// This assumes your edit control is in a dialog box. If not, 
// get the edit control handle from another source.

SetWindowLong(hWndEdit, GWL_EXSTYLE, lAlign);
InvalidateRect(hWndEdit, NULL, FALSE);
```



Uniscribe è un altro set di funzioni che fornisce un controllo accurato per l'elaborazione di script complessi. Per ulteriori informazioni, vedere [Uniscribe](/windows/desktop/Intl/uniscribe).

 

 