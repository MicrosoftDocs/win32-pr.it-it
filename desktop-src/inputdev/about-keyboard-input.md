---
title: Informazioni sull'input da tastiera
description: In questo argomento viene illustrato l'input da tastiera.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- input dell'utente, input da tastiera
- acquisizione dell'input dell'utente, input da tastiera
- input da tastiera
- stato attivo della tastiera
- messaggi di tasti
- messaggi di tipo carattere
- sequenze di tasti di sistema
- sequenze di tasti non di sistema
- messaggi di tipo carattere non di sistema
- chiavi inutilizzate
- messaggi di tipo carattere non recapitabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ad481bad6756bb374b98a5510bdc26f1cded6a
ms.sourcegitcommit: ac62be2f60f757f61ea647a95c168c9841ffabac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104560045"
---
# <a name="about-keyboard-input"></a>Informazioni sull'input da tastiera

Le applicazioni devono accettare l'input dell'utente dalla tastiera e dal mouse. Un'applicazione riceve l'input da tastiera sotto forma di messaggi inviati alle relative finestre.

Questa sezione contiene gli argomenti seguenti:

-   [Modello di input da tastiera](#keyboard-input-model)
-   [Messa a fuoco e attivazione della tastiera](#keyboard-focus-and-activation)
-   [Messaggi di tasti](#keystroke-messages)
    -   [Sequenze di tasti di sistema e non di sistema](#system-and-nonsystem-keystrokes)
    -   [Codici di chiave virtuale descritti](#virtual-key-codes-described)
    -   [Flag messaggi di sequenza di tasti](#keystroke-message-flags)
-   [Messaggi di tipo carattere](#character-messages)
    -   [Messaggi di tipo carattere non di sistema](#nonsystem-character-messages)
    -   [Messaggi di tipo carattere non recapitabili](#dead-character-messages)
-   [Stato chiave](#key-status)
-   [Traslazione di tasti e caratteri](#keystroke-and-character-translations)
-   [Supporto per i tasti di scelta rapida](#hot-key-support)
-   [Tasti di scelta rapida per l'esplorazione e altre funzioni](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulazione dell'input](#simulating-input)
-   [Lingue, impostazioni locali e layout di tastiera](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modello di input da tastiera

Il sistema fornisce il supporto della tastiera indipendente dal dispositivo per le applicazioni installando un driver di dispositivo da tastiera appropriato per la tastiera corrente. Il sistema fornisce supporto della tastiera indipendente dal linguaggio utilizzando il layout di tastiera specifico del linguaggio attualmente selezionato dall'utente o dall'applicazione. Il driver del dispositivo da tastiera riceve i codici di analisi dalla tastiera, che vengono inviati al layout della tastiera in cui vengono tradotti in messaggi e inviati alle finestre appropriate nell'applicazione.

Assegnato a ogni chiave su una tastiera è un valore univoco denominato *codice di analisi*, un identificatore dipendente dal dispositivo per la chiave sulla tastiera. Una tastiera genera due codici di analisi quando l'utente digita una chiave, una quando l'utente preme il tasto e l'altra quando l'utente rilascia il tasto.

Il driver di dispositivo della tastiera interpreta un codice di analisi e lo converte (ne esegue il mapping) a un *codice di chiave virtuale*, un valore indipendente dal dispositivo definito dal sistema che identifica lo scopo di una chiave. Dopo la conversione di un codice di analisi, il layout di tastiera crea un messaggio che include il codice di analisi, il codice della chiave virtuale e altre informazioni sulla sequenza di tasti, quindi inserisce il messaggio nella coda di messaggi di sistema. Il sistema rimuove il messaggio dalla coda di messaggi di sistema e lo inserisce nella coda di messaggi del thread appropriato. Infine, il ciclo di messaggi del thread rimuove il messaggio e lo passa alla routine della finestra appropriata per l'elaborazione. Nella figura seguente viene illustrato il modello di input da tastiera.

![modello di elaborazione input da tastiera](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Messa a fuoco e attivazione della tastiera

Il sistema invia i messaggi della tastiera alla coda di messaggi del thread in primo piano che ha creato la finestra con lo stato attivo. Lo *stato attivo della tastiera* è una proprietà temporanea di una finestra. Il sistema condivide la tastiera tra tutte le finestre sullo schermo spostando lo stato attivo della tastiera, alla direzione dell'utente, da una finestra all'altra. La finestra con lo stato attivo della tastiera riceve (dalla coda di messaggi del thread che lo ha creato) tutti i messaggi della tastiera fino a quando lo stato attivo non cambia in un'altra finestra.

Un thread può chiamare la funzione [**GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) per determinare quale delle sue finestre, se presente, dispone attualmente dello stato attivo della tastiera. Un thread può assegnare lo stato attivo alla tastiera a una delle finestre chiamando la funzione [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) . Quando lo stato attivo passa da una finestra a un'altra, il sistema invia un messaggio [**WM \_ KILLFOCUS**](wm-killfocus.md) alla finestra che ha perso lo stato attivo e quindi Invia un messaggio di [**\_ SetFocus di WM**](wm-setfocus.md) alla finestra che ha ottenuto lo stato attivo.

Il concetto di stato attivo della tastiera è correlato a quello della finestra attiva. La *finestra attiva* è la finestra di primo livello attualmente utilizzata dall'utente. La finestra con lo stato attivo della tastiera è la finestra attiva o una finestra figlio della finestra attiva. Per consentire all'utente di identificare la finestra attiva, il sistema la inserisce nella parte superiore del z order e ne evidenzia la barra del titolo, se ne è presente uno, e il bordo.

Per attivare una finestra di primo livello, è possibile fare clic su di essa, selezionarla utilizzando la combinazione di tasti ALT + TAB o ALT + ESC oppure selezionarla dall'Elenco attività. Un thread può attivare una finestra di primo livello tramite la funzione [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) . Può determinare se una finestra di primo livello creata è attiva tramite la funzione [**GetActiveWindow**](/windows/win32/api/winuser/nf-winuser-getactivewindow) .

Quando una finestra viene disattivata e un'altra attivata, il sistema invia il messaggio di [**\_ attivazione WM**](wm-activate.md) . La parola più bassa del parametro *wParam* è zero se la finestra viene disattivata e diversa da zero se viene attivata. Quando la routine della finestra predefinita riceve il messaggio di **\_ attivazione di WM** , imposta lo stato attivo della tastiera sulla finestra attiva.

Per impedire che gli eventi di input della tastiera e del mouse raggiungano le applicazioni, usare [**BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Si noti che la funzione **BlockInput** non interferisce con la tabella di stato di input della tastiera asincrona. Ciò significa che la chiamata della funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) mentre l'input è bloccato modificherà la tabella di stato di input della tastiera asincrona.

## <a name="keystroke-messages"></a>Messaggi di tasti

Premendo un tasto, viene inserito un messaggio [**WM \_ KeyDown**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) nella coda dei messaggi del thread collegata alla finestra con lo stato attivo della tastiera. Se si rilascia una chiave, un messaggio [**WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP**](wm-syskeyup.md) verrà inserito nella coda.

I messaggi Key-up e Key-Down si verificano in genere nelle coppie, ma se l'utente dispone di una chiave abbastanza lunga per avviare la funzionalità di ripetizione automatica della tastiera, il sistema genera un numero di messaggi [**WM \_ KeyDown**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) in una riga. Genera quindi un singolo messaggio [**WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP**](wm-syskeyup.md) quando l'utente rilascia la chiave.

Questa sezione contiene gli argomenti seguenti:

-   [Sequenze di tasti di sistema e non di sistema](#system-and-nonsystem-keystrokes)
-   [Codici di chiave virtuale descritti](#virtual-key-codes-described)
-   [Flag messaggi di sequenza di tasti](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Sequenze di tasti di sistema e non di sistema

Il sistema distingue tra le sequenze di tasti di sistema e le sequenze di tasti non di sistema. Le sequenze di tasti di sistema producono messaggi di tasti di sistema, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md). Le sequenze di tasti non di sistema producono messaggi di sequenza di tasti non di sistema, [**WM \_ KeyDown**](wm-keydown.md) e [**WM \_ KEYUP**](wm-keyup.md).

Se la routine della finestra deve elaborare un messaggio di sequenza di tasti di sistema, assicurarsi che dopo l'elaborazione del messaggio la routine la passi alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . In caso contrario, tutte le operazioni di sistema che coinvolgono il tasto ALT verranno disabilitate ogni volta che la finestra ha lo stato attivo. Ovvero, l'utente non sarà in grado di accedere al menu di sistema o ai menu della finestra oppure utilizzare la combinazione di tasti ALT + ESC o ALT + TAB per attivare un'altra finestra.

I messaggi di tasti di sistema vengono utilizzati principalmente dal sistema anziché da un'applicazione. Il sistema li usa per fornire l'interfaccia della tastiera predefinita ai menu e per consentire all'utente di controllare quale finestra è attiva. I messaggi di sequenza di tasti di sistema vengono generati quando l'utente digita una chiave in combinazione con il tasto ALT oppure quando l'utente digita e nessuna finestra ha lo stato attivo, ad esempio quando l'applicazione attiva è ridotta a icona. In questo caso, i messaggi vengono inseriti nella coda di messaggi collegata alla finestra attiva.

I messaggi di tasti non di sistema sono utilizzabili dalle finestre delle applicazioni; la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non esegue alcuna operazione. Una routine della finestra può rimuovere tutti i messaggi di tasto non di sistema che non sono necessari.

### <a name="virtual-key-codes-described"></a>Virtual-Key codici descritti

Il parametro **wParam** di un messaggio di sequenza di tasti contiene il codice della chiave virtuale della chiave che è stata premuta o rilasciata. Una routine della finestra elabora o Ignora un messaggio di sequenza di tasti, a seconda del valore del codice della chiave virtuale.

Una routine di finestra tipica elabora solo un piccolo subset dei messaggi di tasti che riceve e ignora il resto. Una routine della finestra, ad esempio, potrebbe elaborare solo i messaggi della sequenza di tasti di [**WM \_ KeyDown**](wm-keydown.md) e solo quelli che contengono codici di chiave virtuale per le chiavi di spostamento del cursore, i tasti MAIUSC (detti anche chiavi di controllo) e i tasti funzione. Una normale routine della finestra non elabora i messaggi di sequenza di tasti da chiavi di caratteri. USA invece la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) per convertire il messaggio in messaggi di tipo carattere. Per ulteriori informazioni sui messaggi **TranslateMessage** e character, vedere [messaggi](#character-messages)di tipo carattere.

### <a name="keystroke-message-flags"></a>Flag messaggi di sequenza di tasti

Il parametro **lParam** di un messaggio di sequenza di tasti contiene informazioni aggiuntive sulla sequenza di tasti che ha generato il messaggio. Queste informazioni includono il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato della chiave precedente e il flag di stato di transizione. Nella figura seguente vengono illustrati i percorsi di questi flag e valori nel parametro **lParam** .

![percorsi dei flag e dei valori nel parametro lParam di un messaggio di sequenza di tasti](images/csinp-02.png)

Un'applicazione può usare i valori seguenti per modificare i flag di sequenza di tasti.



| Valore            | Descrizione                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **\_ALTDOWN KF**  | Modifica il flag del tasto ALT, che indica se il tasto ALT è premuto.     |
| **\_DLGMODE KF**  | Modifica il flag della modalità della finestra di dialogo, che indica se una finestra di dialogo è attiva. |
| **KF \_ esteso** | Modifica il flag di chiave estesa.                                                |
| **\_MENUMODE KF** | Modifica il flag della modalità menu, che indica se un menu è attivo.         |
| **\_ripetizione KF**   | Modifica il flag di stato della chiave precedente.                                          |
| **KF \_ attivo**       | Modifica il flag di stato della transizione.                                            |



 

### <a name="repeat-count"></a>Ripeti conteggio

È possibile controllare il numero di ripetizioni per determinare se un messaggio di sequenza di tasti rappresenta più di una sequenza di tasti. Il numero viene incrementato quando la tastiera genera messaggi [**WM \_ KeyDown**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) più velocemente di quanto possa essere elaborata da un'applicazione. Questo problema si verifica spesso quando l'utente dispone di una chiave abbastanza lungo per avviare la funzionalità di ripetizione automatica della tastiera. Anziché riempire la coda di messaggi di sistema con i messaggi di chiave inattivi risultanti, il sistema combina i messaggi in un singolo messaggio di chiave e incrementa il numero di ripetizioni. Il rilascio di una chiave non può avviare la funzionalità di ripetizione automatica, quindi il numero di ripetizioni per i messaggi [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md) è sempre impostato su 1.

### <a name="scan-code"></a>Analizza codice

Il codice di analisi è il valore che l'hardware della tastiera genera quando l'utente preme un tasto. Si tratta di un valore dipendente dal dispositivo che identifica il tasto premuto anziché il carattere rappresentato dalla chiave. Un'applicazione ignora in genere i codici di analisi. USA invece i codici a chiave virtuale indipendenti dal dispositivo per interpretare i messaggi di sequenza di tasti.

### <a name="extended-key-flag"></a>Flag di Extended-Key

Il flag Extended-Key indica se il messaggio di sequenza di tasti ha avuto origine da uno dei tasti aggiuntivi della tastiera avanzata. Le chiavi estese sono costituite dai tasti ALT e CTRL sul lato destro della tastiera; i tasti INS, CANC, HOME, END, PGSU, PGGIÙ e frecce nei cluster a sinistra del tastierino numerico; tasto BLOC NUM; tasto di interruzione (CTRL + pausa); chiave Stamp di stampa. e la divisione (/) e immettere le chiavi nel tastierino numerico. Il flag di chiave estesa viene impostato se la chiave è una chiave estesa.

### <a name="context-code"></a>Codice contesto

Il codice di contesto indica se il tasto ALT è inattivo quando è stato generato il messaggio di sequenza di tasti. Il codice è 1 se il tasto ALT è premuto e 0 se è stato attivo.

### <a name="previous-key-state-flag"></a>Flag di Key-State precedente

Il flag di stato di chiave precedente indica se la chiave che ha generato il messaggio di sequenza di tasti era in precedenza in alto o in basso. È 1 se la chiave si trovava in precedenza e 0 se la chiave era in precedenza attiva. È possibile utilizzare questo flag per identificare i messaggi di sequenza di tasti generati dalla funzionalità di ripetizione automatica della tastiera. Questo flag è impostato su 1 per i messaggi di sequenza di tasti [**WM \_ KeyDown**](wm-keydown.md) e [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) generati dalla funzionalità di ripetizione automatica. È sempre impostato su 1 per i messaggi [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md) .

### <a name="transition-state-flag"></a>Flag di Transition-State

Il flag di stato di transizione indica se la pressione di un tasto o il rilascio di una chiave ha generato il messaggio di sequenza di tasti. Questo flag è sempre impostato su 0 per i messaggi [**WM \_ KeyDown**](wm-keydown.md) e [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) . è sempre impostato su 1 per i messaggi [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md) .

## <a name="character-messages"></a>Messaggi di tipo carattere

I messaggi di tastiera forniscono numerose informazioni sulle sequenze di tasti, ma non forniscono codici carattere per le sequenze di tasti carattere. Per recuperare i codici carattere, un'applicazione deve includere la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) nel ciclo di messaggi del thread. **TranslateMessage** passa un messaggio [**WM \_ KeyDown**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) al layout della tastiera. Il layout esamina il codice della chiave virtuale del messaggio e, se corrisponde a un tasto carattere, fornisce il codice carattere equivalente (tenendo conto dello stato dei tasti MAIUSC e CAPS LOCK). Genera quindi un messaggio di tipo carattere che include il codice carattere e inserisce il messaggio nella parte superiore della coda di messaggi. L'iterazione successiva del ciclo di messaggi rimuove il messaggio di carattere dalla coda e invia il messaggio alla routine della finestra appropriata.

Questa sezione contiene gli argomenti seguenti:

-   [Messaggi di tipo carattere non di sistema](#nonsystem-character-messages)
-   [Messaggi di tipo carattere non recapitabili](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Messaggi di tipo carattere non di sistema

Una procedura finestra può ricevere i seguenti messaggi di tipo carattere: [**WM \_ char**](wm-char.md), [**WM \_ DEADCHAR**](wm-deadchar.md), [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar), [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)e [**WM \_ UNICHAR**](wm-unichar.md). La funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera un messaggio **WM \_ char** o **WM \_ DEADCHAR** quando elabora un messaggio di [**WM \_ KeyDown**](wm-keydown.md) . Analogamente, genera un messaggio **WM \_ SYSCHAR** o **WM \_ SYSDEADCHAR** quando elabora un messaggio [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) .

Un'applicazione che elabora l'input da tastiera Ignora in genere tutti i messaggi a eccezione di [**WM \_ char**](wm-char.md) e [**WM \_ UNICHAR**](wm-unichar.md) , passando altri messaggi alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Si noti che **WM \_ char** usa UTF (Unicode Transformation Format) a 16 bit mentre **WM \_ unichar** usa UTF-32. Il sistema usa i messaggi [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) e [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) per implementare i tasti di scelta del menu.

Il parametro **wParam** di tutti i messaggi di tipo carattere contiene il codice carattere del tasto carattere premuto. Il valore del codice carattere dipende dalla classe della finestra della finestra che riceve il messaggio. Se la versione Unicode della funzione [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) è stata usata per registrare la classe della finestra, il sistema fornisce caratteri Unicode a tutte le finestre di tale classe. In caso contrario, il sistema fornisce codici carattere ASCII. Per ulteriori informazioni, vedere [Unicode e set di caratteri](/windows/desktop/Intl/unicode-and-character-sets).

Il contenuto del parametro **lParam** di un messaggio di tipo carattere è identico al contenuto del parametro **lParam** del messaggio di chiave inattivo tradotto per produrre il messaggio del carattere. Per informazioni, vedere [flag dei messaggi di sequenza di tasti](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Messaggi di Dead-Character

Alcune tastiere non in lingua inglese contengono tasti di tipo carattere che non dovrebbero produrre caratteri da soli. Vengono invece utilizzati per aggiungere segni diacritici al carattere prodotto dalla sequenza di tasti successiva. Queste chiavi sono denominate *chiavi* inutilizzate. Il tasto circonflesso in una tastiera tedesca è un esempio di chiave non attiva. Per immettere il carattere costituito da una "o" con un accento circonflesso, un utente tedesco digita la chiave circonflesso seguita dalla chiave "o". La finestra con lo stato attivo della tastiera riceve la seguente sequenza di messaggi:

1.  [**KeyDown di WM \_**](wm-keydown.md)
2.  [**\_DEADCHAR WM**](wm-deadchar.md)
3.  [**KEYUP di WM \_**](wm-keyup.md)
4.  [**KeyDown di WM \_**](wm-keydown.md)
5.  [**\_carattere WM**](wm-char.md)
6.  [**KEYUP di WM \_**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera il messaggio [**WM \_ DEADCHAR**](wm-deadchar.md) quando elabora il messaggio di [**WM \_ KeyDown**](wm-keydown.md) da una chiave non recapitabile. Anche se il parametro *wParam* del messaggio **WM \_ DEADCHAR** contiene il codice carattere dei segni diacritici per la chiave non recapitabile, un'applicazione in genere ignora il messaggio. Al contrario, elabora il messaggio [**WM \_ char**](wm-char.md) generato dalla sequenza di tasti successiva. Il parametro *wParam* del messaggio **WM \_ char** contiene il codice carattere della lettera con i segni diacritici. Se la sequenza di tasti successiva genera un carattere che non può essere combinato con un segno diacritici, il sistema genera due messaggi **WM \_ char** . Il parametro *wParam* del primo contiene il codice carattere dei segni diacritici; il parametro *wParam* della seconda contiene il codice carattere della chiave del carattere successiva.

La funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera il messaggio [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) quando elabora il messaggio [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) da una chiave non elaborata del sistema, ovvero una chiave inattiva che viene premuta in combinazione con il tasto ALT. Un'applicazione in genere ignora il messaggio **WM \_ SYSDEADCHAR** .

## <a name="key-status"></a>Stato chiave

Durante l'elaborazione di un messaggio della tastiera, è possibile che un'applicazione debba determinare lo stato di un'altra chiave oltre a quella che ha generato il messaggio corrente. Ad esempio, un'applicazione di elaborazione di testo che consente all'utente di premere MAIUSC + fine per selezionare un blocco di testo deve controllare lo stato del tasto MAIUSC ogni volta che viene ricevuto un messaggio di sequenza di tasti dal tasto fine. L'applicazione può utilizzare la funzione [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) per determinare lo stato di una chiave virtuale nel momento in cui è stato generato il messaggio corrente. può usare la funzione [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) per recuperare lo stato corrente di una chiave virtuale.

Il layout della tastiera mantiene un elenco di nomi. Il nome di una chiave che produce un singolo carattere corrisponde al carattere prodotto dalla chiave. Il nome di un tasto non carattere, ad esempio TAB e invio, viene archiviato come stringa di caratteri. Un'applicazione può recuperare il nome di qualsiasi chiave dal driver di dispositivo chiamando la funzione [**GetKeyNameText**](/windows/win32/api/winuser/nf-winuser-getkeynametexta) .

## <a name="keystroke-and-character-translations"></a>Traslazione di tasti e caratteri

Il sistema include diverse funzioni per scopi specifici che convertono i codici di analisi, i codici di caratteri e i codici chiave virtuale forniti da vari messaggi di tasti. Queste funzioni includono [**MapVirtualKey**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya), [**toascii**](/windows/win32/api/winuser/nf-winuser-toascii), [**tounicode**](/windows/win32/api/winuser/nf-winuser-tounicode)e [**VkKeyScan**](/windows/win32/api/winuser/nf-winuser-vkkeyscana).

Microsoft Rich Edit 3,0 supporta inoltre l' [IME HexToUnicode](/windows/desktop/Intl/hextounicode-ime), che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida. Ciò significa che quando Microsoft Rich Edit 3,0 viene incorporato in un'applicazione, l'applicazione erediterà le funzionalità di HexToUnicode IME.

## <a name="hot-key-support"></a>Supporto Hot-Key

Un *tasto di scelta* è una combinazione di tasti che genera un messaggio di [**\_ scelta rapida WM**](wm-hotkey.md) , un messaggio che il sistema posiziona nella parte superiore della coda di messaggi di un thread, ignorando tutti i messaggi esistenti nella coda. Le applicazioni utilizzano tasti di scelta rapida per ottenere input da tastiera ad alta priorità da parte dell'utente. Ad esempio, definendo un tasto di scelta costituito dalla combinazione di tasti CTRL + C, un'applicazione può consentire all'utente di annullare un'operazione di lunga durata.

Per definire un tasto di scelta, un'applicazione chiama la funzione [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) , specificando la combinazione di chiavi che genera il messaggio di [**\_ scelta rapida WM**](wm-hotkey.md) , l'handle della finestra per ricevere il messaggio e l'identificatore del tasto di scelta. Quando l'utente preme il tasto di scelta, un messaggio di **\_ scelta rapida WM** viene inserito nella coda di messaggi del thread che ha creato la finestra. Il parametro *wParam* del messaggio contiene l'identificatore del tasto di scelta. L'applicazione può definire più tasti di scelta rapida per un thread, ma ogni tasto di scelta nel thread deve avere un identificatore univoco. Prima di terminare l'applicazione, è necessario utilizzare la funzione [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) per eliminare il tasto di scelta.

Le applicazioni possono utilizzare un controllo tasto di scelta rapida per facilitare la scelta di un tasto di scelta rapida da parte dell'utente. I controlli tasto di scelta vengono in genere utilizzati per definire un tasto di scelta rapida che attiva una finestra; non usano le funzioni [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) e [**UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) . Al contrario, un'applicazione che utilizza un controllo tasto di scelta in genere invia il messaggio di errore WM per impostare il tasto di scelta. [**\_**](wm-sethotkey.md) Ogni volta che l'utente preme il tasto di scelta, il sistema invia un messaggio [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) che specifica il tasto di \_ scelta rapida SC. Per ulteriori informazioni sui controlli tasto di scelta, vedere l'argomento relativo all'utilizzo dei controlli chiave attiva in [controlli chiave](../controls/hot-key-controls.md)attiva.

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Tasti di scelta rapida per l'esplorazione e altre funzioni

Windows fornisce il supporto per le tastiere con chiavi speciali per funzioni del browser, funzioni multimediali, avvio delle applicazioni e risparmio energia. Il [**\_ APPCOMMAND di WM**](wm-appcommand.md) supporta i tasti di scelta rapida aggiuntivi. Inoltre, la funzione [**ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) viene modificata per supportare i tasti di scelta rapida aggiuntivi.

È improbabile che una finestra figlio in un'applicazione componente possa implementare direttamente i comandi per questi tasti di tastiera aggiuntivi. Quindi, quando viene premuto uno di questi tasti, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invierà un messaggio [**WM \_ APPCOMMAND**](wm-appcommand.md) a una finestra. **DefWindowProc** creerà anche il messaggio **WM \_ APPCOMMAND** nella finestra padre. Questa operazione è simile al modo in cui i menu di scelta rapida vengono richiamati con il pulsante destro del mouse, ovvero **DefWindowProc** Invia un messaggio [**WM \_ ContextMenu**](/windows/desktop/menurc/wm-contextmenu) al pulsante destro del mouse e lo bolle nell'elemento padre. Inoltre, se **DefWindowProc** riceve un messaggio **WM \_ APPCOMMAND** per una finestra di primo livello, chiamerà un hook della shell con il codice **HSHELL \_ APPCOMMAND**.

Windows supporta inoltre Microsoft IntelliMouse Explorer, che è un mouse con cinque pulsanti. I due pulsanti aggiuntivi supportano la navigazione del browser avanti e indietro. Per ulteriori informazioni, vedere [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulazione dell'input

Per simulare una serie ininterrotta di eventi di input utente, usare la funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) . La funzione accetta tre parametri. Il primo parametro, *cInputs*, indica il numero di eventi di input che verranno simulati. Il secondo parametro, *rgInputs*, è una matrice di strutture di [**input**](/windows/win32/api/winuser/ns-winuser-input) , ognuna delle quali descrive un tipo di evento di input e informazioni aggiuntive su tale evento. L'ultimo parametro, *cbSize*, accetta la dimensione, in byte, della struttura di **input** .

La funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) funziona inserendo una serie di eventi di input simulati nel flusso di input di un dispositivo. L'effetto è simile alla chiamata ripetuta dell' [**\_ evento keybd**](/windows/win32/api/winuser/nf-winuser-keybd_event) o della funzione di [**\_ evento del mouse**](/windows/win32/api/winuser/nf-winuser-mouse_event) , ad eccezione del fatto che il sistema garantisce che non si intermingno altri eventi di input con gli eventi simulati. Al termine della chiamata, il valore restituito indica il numero di eventi di input riprodotti correttamente. Se questo valore è zero, l'input è stato bloccato.

La funzione [**SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) non reimposta lo stato corrente della tastiera. Pertanto, se l'utente dispone di tasti premuti quando si chiama questa funzione, potrebbero interferire con gli eventi generati da questa funzione. Se si è interessati a possibili interferenze, controllare lo stato della tastiera con la funzione [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) e correggerlo in caso di necessità.

## <a name="languages-locales-and-keyboard-layouts"></a>Lingue, impostazioni locali e layout di tastiera

Un *linguaggio* è un linguaggio naturale, ad esempio inglese, francese e giapponese. Una *lingua* secondaria è una variante di un linguaggio naturale che viene pronunciata in un'area geografica specifica, ad esempio le sottolingue inglesi pronunciate nel Regno Unito e il Stati Uniti. Le applicazioni utilizzano valori, denominati [identificatori di lingua](/windows/desktop/Intl/language-identifiers), per identificare in modo univoco lingue e sottolingue.

Le applicazioni utilizzano in genere *impostazioni locali* per impostare la lingua in cui vengono elaborati l'input e l'output. L'impostazione delle impostazioni locali per la tastiera, ad esempio, influiscono sui valori di carattere generati dalla tastiera. L'impostazione delle impostazioni locali per la visualizzazione o la stampante influiscono sui glifi visualizzati o stampati. Le applicazioni impostano le impostazioni locali per una tastiera caricando e utilizzando i layout di tastiera. Le impostazioni locali per una visualizzazione o una stampante vengono impostate selezionando un tipo di carattere che supporta le impostazioni locali specificate.

Un layout di tastiera non solo specifica la posizione fisica delle chiavi sulla tastiera, ma determina anche i valori di carattere generati premendo tali tasti. Ogni layout identifica la lingua di input corrente e determina i valori di carattere generati da quali chiavi e combinazioni di chiavi.

Ogni layout della tastiera ha un handle corrispondente che identifica il layout e la lingua. La parola bassa dell'handle è un identificatore di lingua. La parola alta è un handle di dispositivo, che specifica il layout fisico o è zero, che indica un layout fisico predefinito. L'utente può associare qualsiasi lingua di input a un layout fisico. Ad esempio, un utente di lingua inglese che lavora molto occasionalmente in francese può impostare la lingua di input della tastiera su francese senza modificare il layout fisico della tastiera. Ciò significa che l'utente può immettere il testo in francese usando il layout inglese noto.

Generalmente, non è previsto che le applicazioni modifichino direttamente le lingue di input. Al contrario, l'utente configura le combinazioni di lingua e layout, quindi passa tra loro. Quando l'utente fa clic su testo contrassegnato con una lingua diversa, l'applicazione chiama la funzione [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) per attivare il layout predefinito dell'utente per tale lingua. Se l'utente modifica il testo in una lingua non presente nell'elenco attivo, l'applicazione può chiamare la funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) con la lingua per ottenere un layout basato su tale lingua.

La funzione [**ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) imposta la lingua di input per l'attività corrente. Il parametro *HKL* può essere l'handle per il layout di tastiera o un identificatore di lingua con estensione zero. È possibile ottenere gli handle di layout della tastiera dalla funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) o [**GetKeyboardLayoutList**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) . Per selezionare la tastiera successiva o precedente, è anche possibile usare i valori **HKL \_ Next** e **HKL \_ Prev** .

La funzione [**GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) Recupera il nome del layout di tastiera attivo per il thread chiamante. Se un'applicazione crea il layout attivo mediante la funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) , **GetKeyboardLayoutName** recupera la stessa stringa utilizzata per creare il layout. In caso contrario, la stringa corrisponde all'identificatore di lingua principale corrispondente alle impostazioni locali del layout attivo. Ciò significa che la funzione potrebbe non necessariamente distinguere tra layout diversi con lo stesso linguaggio primario, pertanto non può restituire informazioni specifiche sulla lingua di input. La funzione [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) , tuttavia, può essere utilizzata per determinare la lingua di input.

La funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) carica un layout di tastiera e rende disponibile il layout per l'utente. Le applicazioni possono rendere il layout immediatamente attivo per il thread corrente usando il valore di **\_ attivazione di KLF** . Un'applicazione può usare il valore di **\_ riordino KLF** per riordinare i layout senza specificare anche il valore di **\_ attivazione di KLF** . Quando si caricano i layout di tastiera, le applicazioni devono sempre usare il valore **KLF \_ Sostituisci \_ OK** per assicurarsi che sia selezionata la preferenza dell'utente.

Per il supporto multilingue, la funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) fornisce i flag **KLF \_ REPLACELANG** e **KLF \_ NOTELLSHELL** . Il flag **KLF \_ REPLACELANG** indirizza la funzione per sostituire un layout di tastiera esistente senza modificare la lingua. Il tentativo di sostituire un layout esistente con lo stesso identificatore di lingua ma senza specificare **KLF \_ REPLACELANG** è un errore. Il flag **KLF \_ NOTELLSHELL** impedisce alla funzione di notificare la shell quando viene aggiunto o sostituito un layout di tastiera. Questa operazione è utile per le applicazioni che aggiungono più layout in una serie di chiamate consecutive. Questo flag deve essere usato in tutte le chiamate tranne l'ultima.

La funzione [**UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) è limitata perché non è in grado di scaricare la lingua di input predefinita del sistema. Ciò garantisce che l'utente abbia sempre un layout disponibile per immettere il testo usando lo stesso set di caratteri usato dalla shell e file system.

 

 
