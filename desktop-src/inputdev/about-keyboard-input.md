---
title: Informazioni sull'input da tastiera
description: In questo argomento viene illustrato l'input da tastiera.
ms.assetid: de34727e-e8c7-481d-982d-0e42a02704db
keywords:
- input utente, input da tastiera
- acquisizione dell'input dell'utente, input da tastiera
- input da tastiera
- stato attivo della tastiera
- messaggi di sequenza di tasti
- messaggi di tipo carattere
- sequenze di tasti di sistema
- sequenze di tasti non di sistema
- messaggi di caratteri non di sistema
- chiavi in dead
- messaggi di caratteri non inviati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de85794901be3fef37156bde29520039f85702b
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373197"
---
# <a name="about-keyboard-input"></a>Informazioni sull'input da tastiera

Le applicazioni devono accettare l'input dell'utente dalla tastiera e dal mouse. Un'applicazione riceve l'input da tastiera sotto forma di messaggi inviati alle relative finestre.

Questa sezione contiene gli argomenti seguenti:

-   [Modello di input da tastiera](#keyboard-input-model)
-   [Stato attivo e attivazione della tastiera](#keyboard-focus-and-activation)
-   [Messaggi di pressione dei tasti](#keystroke-messages)
    -   [Sequenze di tasti di sistema e non di sistema](#system-and-nonsystem-keystrokes)
    -   [Descrizione dei codici chiave virtuale](#virtual-key-codes-described)
    -   [Flag di messaggi con sequenza di tasti](#keystroke-message-flags)
-   [Messaggi di tipo carattere](#character-messages)
    -   [Messaggi di tipo carattere non di sistema](#nonsystem-character-messages)
    -   [Messaggi di caratteri non inviati](#dead-character-messages)
-   [Stato chiave](#key-status)
-   [Sequenze di tasti e traduzioni di caratteri](#keystroke-and-character-translations)
-   [Supporto dei tasti di scelta rapida](#hot-key-support)
-   [Tasti da tastiera per l'esplorazione e altre funzioni](#keyboard-keys-for-browsing-and-other-functions)
-   [Simulazione dell'input](#simulating-input)
-   [Lingue, impostazioni locali e layout di tastiera](#languages-locales-and-keyboard-layouts)

## <a name="keyboard-input-model"></a>Modello di input da tastiera

Il sistema fornisce il supporto della tastiera indipendente dal dispositivo per le applicazioni installando un driver di dispositivo da tastiera appropriato per la tastiera corrente. Il sistema fornisce il supporto della tastiera indipendente dalla lingua usando il layout di tastiera specifico della lingua attualmente selezionato dall'utente o dall'applicazione. Il driver di dispositivo della tastiera riceve i codici di scansione dalla tastiera, che vengono inviati al layout di tastiera in cui vengono convertiti in messaggi e inseriti nelle finestre appropriate dell'applicazione.

A ogni tasto di una tastiera viene assegnato un valore univoco denominato codice di digitalizzazione, un identificatore dipendente dal dispositivo per il tasto della tastiera. Una tastiera genera due codici di digitalizzazione quando l'utente preme un tasto, uno quando preme il tasto e un altro quando l'utente rilascia il tasto.

Il driver di dispositivo da tastiera interpreta un codice di scansione e lo converte (ne esegue il mapping) in un codice di tasto virtuale *,* un valore indipendente dal dispositivo definito dal sistema che identifica lo scopo di un tasto. Dopo aver traslato un codice di analisi, il layout di tastiera crea un messaggio che include il codice di analisi, il codice del tasto virtuale e altre informazioni sulla sequenza di tasti, quindi inserisce il messaggio nella coda di messaggi di sistema. Il sistema rimuove il messaggio dalla coda di messaggi di sistema e lo invia alla coda di messaggi del thread appropriato. Infine, il ciclo di messaggi del thread rimuove il messaggio e lo passa alla routine della finestra appropriata per l'elaborazione. La figura seguente illustra il modello di input da tastiera.

![modello di elaborazione dell'input da tastiera](images/csinp-01.png)

## <a name="keyboard-focus-and-activation"></a>Stato attivo e attivazione della tastiera

Il sistema invia i messaggi della tastiera alla coda di messaggi del thread in primo piano che ha creato la finestra con lo stato attivo. Lo *stato attivo della* tastiera è una proprietà temporanea di una finestra. Il sistema condivide la tastiera tra tutte le finestre sullo schermo spostando lo stato attivo della tastiera, in direzione dell'utente, da una finestra a un'altra. La finestra con lo stato attivo riceve (dalla coda di messaggi del thread che lo ha creato) tutti i messaggi della tastiera fino a quando lo stato attivo non viene modificato in un'altra finestra.

Un thread può chiamare la [**funzione GetFocus**](/windows/win32/api/winuser/nf-winuser-getfocus) per determinare quale delle finestre (se presenti) ha attualmente lo stato attivo della tastiera. Un thread può assegnare lo stato attivo della tastiera a una delle relative finestre chiamando la [**funzione SetFocus.**](/windows/win32/api/winuser/nf-winuser-setfocus) Quando lo stato attivo della tastiera cambia da una finestra a un'altra, il sistema invia un messaggio [**\_ KILLFOCUS WM**](wm-killfocus.md) alla finestra che ha perso lo stato attivo e quindi invia un messaggio [**WM \_ SETFOCUS**](wm-setfocus.md) alla finestra che ha raggiunto lo stato attivo.

Il concetto di stato attivo della tastiera è correlato a quello della finestra attiva. La *finestra attiva* è la finestra di primo livello con cui l'utente sta attualmente lavorando. La finestra con lo stato attivo della tastiera è la finestra attiva o una finestra figlio della finestra attiva. Per consentire all'utente di identificare la finestra attiva, il sistema la posiziona nella parte superiore dell'ordine Z ed evidenzia la barra del titolo (se ne ha una) e il bordo.

L'utente può attivare una finestra di primo livello facendo clic su di essa, selezionandola usando la combinazione di tasti ALT+TAB o ALT+ESC o selezionandola dal Elenco attività. Un thread può attivare una finestra di primo livello usando la [**funzione SetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-setactivewindow) Può determinare se una finestra di primo livello creata è attiva usando la [**funzione GetActiveWindow.**](/windows/win32/api/winuser/nf-winuser-getactivewindow)

Quando una finestra viene disattivata e un'altra attivata, il sistema invia il [**messaggio WM \_ ACTIVATE.**](wm-activate.md) La parola più bassa del *parametro wParam* è zero se la finestra viene disattivata e diversa da zero se viene attivata. Quando la routine della finestra predefinita riceve il **messaggio WM \_ ACTIVATE,** imposta lo stato attivo della tastiera sulla finestra attiva.

Per impedire agli eventi di input della tastiera e del mouse di raggiungere le applicazioni, [**usare BlockInput**](/windows/win32/api/winuser/nf-winuser-blockinput). Si noti che la **funzione BlockInput** non interferisce con la tabella asincrona dello stato di input della tastiera. Ciò significa che la chiamata alla [**funzione SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) mentre l'input è bloccato modificherà la tabella asincrona dello stato di input della tastiera.

## <a name="keystroke-messages"></a>Messaggi di pressione dei tasti

Premendo un tasto, un messaggio [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) viene inserito nella coda di messaggi del thread collegata alla finestra con lo stato attivo della tastiera. Il rilascio di una chiave fa [**sì che un messaggio WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP**](wm-syskeyup.md) sia inserito nella coda.

I messaggi di tasti up e key-down in genere si verificano a coppie, ma se l'utente tiene premuto un tasto per un tempo sufficiente per avviare la funzionalità di ripetizione automatica della tastiera, il sistema genera una serie di messaggi [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) in una riga. Genera quindi un singolo messaggio [**WM \_ KEYUP**](wm-keyup.md) o [**WM \_ SYSKEYUP**](wm-syskeyup.md) quando l'utente rilascia la chiave.

Questa sezione contiene gli argomenti seguenti:

-   [Sequenze di tasti di sistema e non di sistema](#system-and-nonsystem-keystrokes)
-   [Descrizione dei codici chiave virtuale](#virtual-key-codes-described)
-   [Flag di messaggi con sequenza di tasti](#keystroke-message-flags)

### <a name="system-and-nonsystem-keystrokes"></a>Sequenze di tasti di sistema e non di sistema

Il sistema distingue tra le sequenze di tasti di sistema e le sequenze di tasti non di sistema. Le sequenze di tasti di sistema producono messaggi di pressione dei tasti di sistema, [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) e [**WM \_ SYSKEYUP.**](wm-syskeyup.md) Le sequenze di tasti non di sistema producono messaggi di sequenza di tasti non di sistema, [**WM \_ KEYDOWN**](wm-keydown.md) e [**WM \_ KEYUP.**](wm-keyup.md)

Se la routine della finestra deve elaborare un messaggio di pressione dei tasti di sistema, assicurarsi che dopo l'elaborazione del messaggio la procedura lo passi alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) In caso contrario, tutte le operazioni di sistema che coinvolgono il tasto ALT verranno disabilitate ogni volta che la finestra ha lo stato attivo. Ciò significa che l'utente non potrà accedere ai menu della finestra o al menu di sistema oppure usare la combinazione di tasti ALT+ESC o ALT+TAB per attivare un'altra finestra.

I messaggi di pressione dei tasti di sistema vengono utilizzati principalmente dal sistema anziché da un'applicazione. Il sistema li usa per fornire l'interfaccia della tastiera predefinita ai menu e per consentire all'utente di controllare quale finestra è attiva. I messaggi di pressione dei tasti di sistema vengono generati quando l'utente digita un tasto in combinazione con ALT o quando l'utente digita e nessuna finestra ha lo stato attivo della tastiera (ad esempio, quando l'applicazione attiva è ridotta a icona). In questo caso, i messaggi vengono inviati alla coda di messaggi associata alla finestra attiva.

I messaggi di pressione dei tasti non di sistema vengono utilizzati dalle finestre dell'applicazione; La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) non esegue alcuna operazione. Una routine di finestra può eliminare tutti i messaggi di sequenza di tasti non di sistema che non sono necessari.

### <a name="virtual-key-codes-described"></a>Virtual-Key descrizione dei codici

Il **parametro wParam** di un messaggio di sequenza di tasti contiene il codice del tasto virtuale del tasto premuto o rilasciato. Una routine della finestra elabora o ignora un messaggio di sequenza di tasti, a seconda del valore del codice del tasto virtuale.

Una routine di finestra tipica elabora solo un piccolo subset dei messaggi di pressione dei tasti ricevuti e ignora il resto. Ad esempio, una routine della finestra potrebbe elaborare solo i messaggi di pressione dei tasti [**WM \_ KEYDOWN**](wm-keydown.md) e solo quelli che contengono codici di tasto virtuale per i tasti di spostamento del cursore, i tasti di direzione (detti anche tasti di controllo) e i tasti funzione. Una routine di finestra tipica non elabora i messaggi relativi alla sequenza di tasti dai tasti di scelta rapida. Usa invece la funzione [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) per convertire il messaggio in messaggi di tipo carattere. Per altre informazioni su **TranslateMessage e** sui messaggi di tipo carattere, vedere [Messaggi di tipo carattere.](#character-messages)

### <a name="keystroke-message-flags"></a>Flag di messaggi con sequenza di tasti

Il **parametro lParam** di un messaggio di sequenza di tasti contiene informazioni aggiuntive sulla sequenza di tasti che ha generato il messaggio. Queste informazioni includono il conteggio delle ripetizioni, il codice di analisi, il flag di chiave estesa, il codice di contesto, il flag di stato della chiave precedente e il flag dello stato di transizione. La figura seguente mostra le posizioni di questi flag e valori nel **parametro lParam.**

![percorsi dei flag e dei valori nel parametro lparam di un messaggio di sequenza di tasti](images/csinp-02.png)

Un'applicazione può usare i valori seguenti per modificare i flag di pressione dei tasti.



| Valore            | Descrizione                                                                       |
|------------------|-----------------------------------------------------------------------------------|
| **KF \_ ALTDOWN**  | Modifica il flag del tasto ALT, che indica se il tasto ALT è premuto.     |
| **KF \_ DLGMODE**  | Modifica il flag della modalità finestra di dialogo, che indica se una finestra di dialogo è attiva. |
| **KF \_ EXTENDED** | Modifica il flag della chiave estesa.                                                |
| **KF \_ MENUMODE** | Modifica il flag della modalità menu, che indica se un menu è attivo.         |
| **KF \_ REPEAT**   | Modifica il flag di stato della chiave precedente.                                          |
| **KF \_ UP**       | Modifica il flag dello stato di transizione.                                            |

Codice di esempio:

```cpp
case WM_KEYDOWN:
case WM_KEYUP:
case WM_SYSKEYDOWN:
case WM_SYSKEYUP:
{
    WORD vkCode = LOWORD(wParam);                                       // virtual-key code

    BYTE scanCode = LOBYTE(HIWORD(lParam));                             // scan code
    BOOL scanCodeE0 = (HIWORD(lParam) & KF_EXTENDED) == KF_EXTENDED;    // extended-key flag, 1 if scancode has 0xE0 prefix

    BOOL upFlag = (HIWORD(lParam) & KF_UP) == KF_UP;                    // transition-state flag, 1 on keyup
    BOOL repeatFlag = (HIWORD(lParam) & KF_REPEAT) == KF_REPEAT;        // previous key-state flag, 1 on autorepeat
    WORD repeatCount = LOWORD(lParam);                                  // repeat count, > 0 if several keydown messages was combined into one message

    BOOL altDownFlag = (HIWORD(lParam) & KF_ALTDOWN) == KF_ALTDOWN;     // ALT key was pressed

    BOOL dlgModeFlag = (HIWORD(lParam) & KF_DLGMODE) == KF_DLGMODE;     // dialog box is active
    BOOL menuModeFlag = (HIWORD(lParam) & KF_MENUMODE) == KF_MENUMODE;  // menu is active
    
    // ...
}
break;
```

### <a name="repeat-count"></a>Ripeti conteggio

È possibile controllare il numero di ripetizioni per determinare se un messaggio di sequenza di tasti rappresenta più di una sequenza di tasti. Il sistema incrementa il conteggio quando la tastiera genera messaggi [**WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) più velocemente di quanto un'applicazione possa elaborarli. Questo errore si verifica spesso quando l'utente tiene premuto un tasto per un tempo sufficiente per avviare la funzionalità di ripetizione automatica della tastiera. Invece di riempire la coda di messaggi di sistema con i messaggi key-down risultanti, il sistema combina i messaggi in un singolo messaggio key down e incrementa il numero di ripetizioni. Il rilascio di una chiave non può avviare la funzionalità di ripetizione automatica, pertanto il numero di ripetizioni per i messaggi [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP**](wm-syskeyup.md) è sempre impostato su 1.

### <a name="scan-code"></a>Codice di analisi

Il codice di analisi è il valore generato dall'hardware della tastiera quando l'utente preme un tasto. Si tratta di un valore dipendente dal dispositivo che identifica il tasto premuto, anziché il carattere rappresentato dal tasto. Un'applicazione in genere ignora i codici di analisi. Usa invece i codici dei tasti virtuali indipendenti dal dispositivo per interpretare i messaggi relativi alle sequenze di tasti.

### <a name="extended-key-flag"></a>Extended-Key flag

Il flag di tasti estesi indica se il messaggio di pressione dei tasti ha avuto origine da uno dei tasti aggiuntivi della tastiera avanzata. I tasti estesi sono costituiti da ALT e CTRL sul lato destro della tastiera; i tasti INS, DEL, HOME, END, PGGIS, PGGIUTO e i tasti di direzione nei cluster a sinistra del tastierino numerico; tasto BLOC NUM; il tasto INTERR (CTRL+PAUSE). il tasto PRINT SCRN; e i tasti di divisione (/) e INVIO nel tastierino numerico. Il flag della chiave estesa viene impostato se la chiave è una chiave estesa.

Se specificato, il codice di analisi è stato preceduto da un byte di prefisso con 0xE0 (224).

### <a name="context-code"></a>Codice di contesto

Il codice di contesto indica se il tasto ALT era premuto quando è stato generato il messaggio di pressione del tasto. Il codice è 1 se il tasto ALT era premuto e 0 se era in alto.

### <a name="previous-key-state-flag"></a>Flag Key-State precedente

Il flag di stato chiave precedente indica se il tasto che ha generato il messaggio di sequenza di tasti era in precedenza verso l'alto o verso il basso. È 1 se in precedenza la chiave era in stato in basso e 0 se la chiave era in precedenza in alto. È possibile usare questo flag per identificare i messaggi di sequenza di tasti generati dalla funzionalità di ripetizione automatica della tastiera. Questo flag è impostato su 1 per i messaggi di sequenza di tasti [**WM \_ KEYDOWN**](wm-keydown.md) e [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) generati dalla funzionalità di ripetizione automatica. È sempre impostato su 1 per i [**messaggi WM \_ KEYUP**](wm-keyup.md) [**e WM \_ SYSKEYUP.**](wm-syskeyup.md)

### <a name="transition-state-flag"></a>Transition-State flag

Il flag transition-state indica se la pressione di un tasto o il rilascio di un tasto ha generato il messaggio di sequenza di tasti. Questo flag è sempre impostato su 0 per i messaggi [**WM \_ KEYDOWN**](wm-keydown.md) e [**WM \_ SYSKEYDOWN.**](wm-syskeydown.md) È sempre impostato su 1 per i messaggi [**WM \_ KEYUP**](wm-keyup.md) e [**WM \_ SYSKEYUP.**](wm-syskeyup.md)

## <a name="character-messages"></a>Messaggi di tipo carattere

I messaggi relativi alle sequenze di tasti forniscono molte informazioni sulle sequenze di tasti, ma non forniscono codici carattere per le sequenze di caratteri. Per recuperare i codici carattere, un'applicazione deve includere la [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) nel ciclo di messaggi del thread. **TranslateMessage** passa un [**messaggio WM \_ KEYDOWN**](wm-keydown.md) o [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) al layout di tastiera. Il layout esamina il codice del tasto virtuale del messaggio e, se corrisponde a un tasto carattere, fornisce l'equivalente del codice carattere (tenendo conto dello stato dei tasti MAIUSC e BLOC MAIUSC). Genera quindi un messaggio di tipo carattere che include il codice carattere e inserisce il messaggio nella parte superiore della coda di messaggi. L'iterazione successiva del ciclo di messaggi rimuove il messaggio di tipo carattere dalla coda e invia il messaggio alla routine della finestra appropriata.

Questa sezione contiene gli argomenti seguenti:

-   [Messaggi di caratteri non di sistema](#nonsystem-character-messages)
-   [Messaggi con caratteri non inviati](#dead-character-messages)

### <a name="nonsystem-character-messages"></a>Messaggi di caratteri non di sistema

Una routine finestra può ricevere i seguenti messaggi di carattere: [**WM \_ CHAR,**](wm-char.md) [**WM \_ DEADCHAR,**](wm-deadchar.md) [**WM \_ SYSCHAR,**](/windows/desktop/menurc/wm-syschar) [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)e [**WM \_ UNICHAR.**](wm-unichar.md) La [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera un **messaggio WM \_ CHAR** o **WM \_ DEADCHAR** quando elabora un [**messaggio WM \_ KEYDOWN.**](wm-keydown.md) Analogamente, genera un messaggio **\_ SYSCHAR o** **\_ SYSDEADCHAR WM** quando elabora un [**messaggio \_ SYSKEYDOWN WM.**](wm-syskeydown.md)

Un'applicazione che elabora l'input da tastiera ignora in genere tutti i messaggi, ad esempio [**WM \_ CHAR**](wm-char.md) e [**WM \_ UNICHAR,**](wm-unichar.md) passando tutti gli altri messaggi alla [**funzione DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Si noti **che WM \_ CHAR** usa il formato di trasformazione Unicode (UTF) a 16 bit, mentre **WM \_ UNICHAR** usa UTF-32. Il sistema usa i [**messaggi WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) e [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) per implementare i comandi di menu.

Il **parametro wParam** di tutti i messaggi di tipo carattere contiene il codice carattere del tasto carattere premuto. Il valore del codice carattere dipende dalla classe finestra della finestra che riceve il messaggio. Se la versione Unicode della [**funzione RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) è stata usata per registrare la classe della finestra, il sistema fornisce caratteri Unicode a tutte le finestre di tale classe. In caso contrario, il sistema fornisce codici di caratteri ASCII. Per altre informazioni, vedere [Unicode e set di caratteri](/windows/desktop/Intl/unicode-and-character-sets).

Il contenuto del **parametro lParam** di un messaggio di tipo carattere è identico al contenuto del **parametro lParam** del messaggio key-down convertito per produrre il messaggio di tipo carattere. Per informazioni, vedere [Flag dei messaggi di sequenza di tasti](#keystroke-message-flags).

### <a name="dead-character-messages"></a>Dead-Character messaggi

Alcune tastiere non in lingua inglese contengono tasti di carattere che non dovrebbero produrre caratteri da soli. Vengono invece usati per aggiungere un diacritico al carattere prodotto dalla sequenza di tasti successiva. Queste chiavi sono denominate *chiavi non disponibili.* Il tasto circonflesso su una tastiera tedesca è un esempio di tasto non attivo. Per immettere il carattere costituito da una "o" con un circonflesso, un utente tedesco digita la chiave circumflex seguita dal tasto "o". La finestra con lo stato attivo della tastiera riceverà la sequenza di messaggi seguente:

1.  [**WM \_ KEYDOWN**](wm-keydown.md)
2.  [**WM \_ DEADCHAR**](wm-deadchar.md)
3.  [**WM \_ KEYUP**](wm-keyup.md)
4.  [**WM \_ KEYDOWN**](wm-keydown.md)
5.  [**WM \_ CHAR**](wm-char.md)
6.  [**WM \_ KEYUP**](wm-keyup.md)

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera il [**messaggio \_ WM DEADCHAR**](wm-deadchar.md) quando elabora il [**messaggio WM \_ KEYDOWN**](wm-keydown.md) da una chiave non elaborata. Anche se il *parametro wParam* del messaggio **WM \_ DEADCHAR** contiene il codice carattere del diacritico per la chiave non trovata, un'applicazione in genere ignora il messaggio. Elabora invece il messaggio [**WM \_ CHAR**](wm-char.md) generato dalla sequenza di tasti successiva. Il *parametro wParam* del **messaggio WM \_ CHAR** contiene il codice carattere della lettera con il diacritico. Se la sequenza di tasti successiva genera un carattere che non può essere combinato con un diacritico, il sistema genera due **messaggi WM \_ CHAR.** Il *parametro wParam* del primo contiene il codice carattere del diacritico. il *parametro wParam* del secondo contiene il codice carattere del tasto carattere successivo.

La [**funzione TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) genera il messaggio [**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md) quando elabora il messaggio [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) da un tasto non funzionante di sistema (un tasto non funzionante premuto in combinazione con alt). Un'applicazione in genere ignora **il messaggio \_ WM SYSDEADCHAR.**

## <a name="key-status"></a>Stato chiave

Durante l'elaborazione di un messaggio da tastiera, un'applicazione potrebbe dover determinare lo stato di un altro tasto oltre a quello che ha generato il messaggio corrente. Ad esempio, un'applicazione di elaborazione di testo che consente all'utente di premere MAIUSC+FINE per selezionare un blocco di testo deve controllare lo stato del tasto MAIUSC ogni volta che riceve un messaggio di pressione del tasto FINE. L'applicazione può usare [**la funzione GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) per determinare lo stato di una chiave virtuale al momento della generazione del messaggio corrente. può usare la [**funzione GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) per recuperare lo stato corrente di una chiave virtuale.

Il layout di tastiera mantiene un elenco di nomi. Il nome di una chiave che produce un singolo carattere è lo stesso del carattere prodotto dalla chiave. Il nome di un tasto non carattere, ad esempio TAB e INVIO, viene archiviato come stringa di caratteri. Un'applicazione può recuperare il nome di qualsiasi chiave dal driver di dispositivo chiamando la [**funzione GetKeyNameText.**](/windows/win32/api/winuser/nf-winuser-getkeynametexta)

## <a name="keystroke-and-character-translations"></a>Combinazione di tasti e conversioni di caratteri

Il sistema include diverse funzioni per scopi speciali che traslano codici di analisi, codici carattere e codici chiave virtuale forniti da vari messaggi di sequenza di tasti. Queste funzioni includono [**MapVirtualKey,**](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya) [**ToAscii,**](/windows/win32/api/winuser/nf-winuser-toascii) [**ToUnicode**](/windows/win32/api/winuser/nf-winuser-tounicode)e [**VkKeyScan.**](/windows/win32/api/winuser/nf-winuser-vkkeyscana)

Microsoft Rich Edit 3.0 supporta anche [l'IME HexToUnicode,](/windows/desktop/Intl/hextounicode-ime)che consente a un utente di eseguire la conversione tra caratteri esadecimali e Unicode usando i tasti di scelta rapida. Ciò significa che quando Microsoft Rich Edit 3.0 viene incorporato in un'applicazione, l'applicazione erediterà le funzionalità dell'IME HexToUnicode.

## <a name="hot-key-support"></a>Hot-Key supporto tecnico

Un *tasto di* scelta rapida è una combinazione di tasti che genera un messaggio WM [**\_ HOTKEY,**](wm-hotkey.md) un messaggio che il sistema inserisce nella parte superiore della coda di messaggi di un thread, ignorando tutti i messaggi esistenti nella coda. Le applicazioni usano i tasti di scelta rapida per ottenere l'input della tastiera ad alta priorità dall'utente. Ad esempio, definendo un tasto di scelta rapida costituito dalla combinazione di tasti CTRL+C, un'applicazione può consentire all'utente di annullare un'operazione di lunga durata.

Per definire un tasto di scelta rapida, un'applicazione chiama la funzione [**RegisterHotKey,**](/windows/win32/api/winuser/nf-winuser-registerhotkey) specificando la combinazione di tasti che genera il messaggio [**WM \_ HOTKEY,**](wm-hotkey.md) l'handle alla finestra per ricevere il messaggio e l'identificatore del tasto di scelta rapida. Quando l'utente preme il tasto di scelta rapida, viene inserito un messaggio **WM \_ HOTKEY** nella coda di messaggi del thread che ha creato la finestra. Il *parametro wParam* del messaggio contiene l'identificatore del tasto di scelta rapida. L'applicazione può definire più tasti di scelta rapida per un thread, ma ogni tasto di scelta nel thread deve avere un identificatore univoco. Prima che l'applicazione termini, deve usare la [**funzione UnregisterHotKey**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) per eliminare il tasto di scelta rapida.

Le applicazioni possono usare un controllo tasto di scelta rapida per semplificare la scelta di un tasto di scelta rapida da parte dell'utente. I controlli tasto di scelta vengono in genere usati per definire un tasto di scelta rapida che attiva una finestra. non usano le [**funzioni RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) [**e UnregisterHotKey.**](/windows/win32/api/winuser/nf-winuser-unregisterhotkey) Al contrario, un'applicazione che usa un controllo tasto di scelta in genere invia il [**messaggio WM \_ SETHOTKEY**](wm-sethotkey.md) per impostare il tasto di scelta rapida. Ogni volta che l'utente preme il tasto di scelta rapida, il sistema invia un [**messaggio \_ SYSCOMMAND WM**](/windows/desktop/menurc/wm-syscommand) specificando SC \_ HOTKEY. Per altre informazioni sui controlli tasto di scelta rapida, vedere "Uso dei controlli tasto di scelta rapida" in [Controlli tasto di scelta rapida](../controls/hot-key-controls.md).

## <a name="keyboard-keys-for-browsing-and-other-functions"></a>Tasti da tastiera per l'esplorazione e altre funzioni

Windows supporto per tastiere con tasti speciali per funzioni del browser, funzioni multimediali, avvio di applicazioni e risparmio energia. [**WM \_ APPCOMMAND**](wm-appcommand.md) supporta i tasti della tastiera aggiuntivi. Inoltre, la [**funzione ShellProc**](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) viene modificata per supportare i tasti aggiuntivi della tastiera.

È improbabile che una finestra figlio in un'applicazione componente sia in grado di implementare direttamente i comandi per questi tasti aggiuntivi della tastiera. Pertanto, quando viene premuto uno di questi tasti, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invierà un [**messaggio WM \_ APPCOMMAND**](wm-appcommand.md) a una finestra. **DefWindowProc inserirà** anche il **messaggio WM \_ APPCOMMAND** nella relativa finestra padre. Questo è simile al modo in cui i menu di scelta rapida vengono richiamati con il pulsante destro del mouse, ovvero **DefWindowProc** invia un messaggio [**WM \_ CONTEXTMENU**](/windows/desktop/menurc/wm-contextmenu) al clic con il pulsante destro del mouse e lo bolla al relativo elemento padre. Inoltre, se **DefWindowProc** riceve un messaggio **WM \_ APPCOMMAND** per una finestra di primo livello, chiamerà un hook della shell con codice **HSHELL \_ APPCOMMAND**.

Windows supporta anche Microsoft IntelliMouse Explorer, ovvero un mouse con cinque pulsanti. I due pulsanti aggiuntivi supportano lo spostamento avanti e indietro nel browser. Per altre informazioni, vedere [XBUTTONs](about-mouse-input.md).

## <a name="simulating-input"></a>Simulazione dell'input

Per simulare una serie ininterrotta di eventi di input utente, usare la [**funzione SendInput.**](/windows/win32/api/winuser/nf-winuser-sendinput) La funzione accetta tre parametri. Il primo parametro, *cInputs*, indica il numero di eventi di input che verranno simulati. Il secondo parametro, *rgInputs*, è una matrice di strutture [**INPUT,**](/windows/win32/api/winuser/ns-winuser-input) ognuna delle quali descrive un tipo di evento di input e informazioni aggiuntive su tale evento. L'ultimo parametro, *cbSize*, accetta le dimensioni della struttura **INPUT,** in byte.

La [**funzione SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) funziona inseriscendo una serie di eventi di input simulati nel flusso di input di un dispositivo. L'effetto è simile alla chiamata ripetuta dell'evento [**keybd \_**](/windows/win32/api/winuser/nf-winuser-keybd_event) o della funzione dell'evento [**mouse, \_**](/windows/win32/api/winuser/nf-winuser-mouse_event) ad eccezione del fatto che il sistema garantisce che nessun altro evento di input si mesci con gli eventi simulati. Al termine della chiamata, il valore restituito indica il numero di eventi di input riprodotti correttamente. Se questo valore è zero, l'input è stato bloccato.

La [**funzione SendInput**](/windows/win32/api/winuser/nf-winuser-sendinput) non reimposta lo stato corrente della tastiera. Pertanto, se l'utente ha tasti premuti quando si chiama questa funzione, potrebbe interferire con gli eventi generati da questa funzione. Se si è interessati a possibili interferenze, controllare lo stato della tastiera con la [**funzione GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate) e correggere in base alle esigenze.

## <a name="languages-locales-and-keyboard-layouts"></a>Lingue, impostazioni locali e layout di tastiera

Una *lingua* è un linguaggio naturale, ad esempio inglese, francese e giapponese. Un *sottolinguaggio* è una variante di un linguaggio naturale parlato in un'area geografica specifica, ad esempio le sottolinguaggi inglesi parlati nel Regno Unito e nel Stati Uniti. Le applicazioni usano valori, [detti identificatori di lingua,](/windows/desktop/Intl/language-identifiers)per identificare in modo univoco lingue e sottolinguaggi.

Le applicazioni usano in *genere le impostazioni* locali per impostare la lingua in cui vengono elaborati l'input e l'output. L'impostazione delle impostazioni locali per la tastiera, ad esempio, influisce sui valori dei caratteri generati dalla tastiera. L'impostazione delle impostazioni locali per lo schermo o la stampante influisce sui glifi visualizzati o stampati. Le applicazioni impostano le impostazioni locali per una tastiera caricando e usando i layout di tastiera. Impostano le impostazioni locali per uno schermo o una stampante selezionando un tipo di carattere che supporti le impostazioni locali specificate.

Un layout di tastiera non solo specifica la posizione fisica dei tasti sulla tastiera, ma determina anche i valori dei caratteri generati premendo tali tasti. Ogni layout identifica la lingua di input corrente e determina i valori dei caratteri generati da quali tasti e combinazioni di tasti.

Ogni layout di tastiera ha un handle corrispondente che identifica il layout e la lingua. La parola bassa dell'handle è un identificatore di lingua. La parola alta è un handle del dispositivo, che specifica il layout fisico, o è zero, che indica un layout fisico predefinito. L'utente può associare qualsiasi lingua di input a un layout fisico. Ad esempio, un utente di lingua inglese che lavora molto occasionalmente in francese può impostare la lingua di input della tastiera sul francese senza modificare il layout fisico della tastiera. Ciò significa che l'utente può immettere testo in francese usando il noto layout inglese.

Le applicazioni in genere non devono modificare direttamente le lingue di input. Al contrario, l'utente configura combinazioni di lingua e layout, quindi passa da una all'altra. Quando l'utente fa clic su un testo contrassegnato con una lingua diversa, l'applicazione chiama la [**funzione ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) per attivare il layout predefinito dell'utente per tale lingua. Se l'utente modifica il testo in una lingua non presente nell'elenco attivo, l'applicazione può chiamare la funzione [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) con la lingua per ottenere un layout basato su tale lingua.

La [**funzione ActivateKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout) imposta la lingua di input per l'attività corrente. Il *parametro hkl* può essere l'handle per il layout di tastiera o un identificatore di lingua con estensione zero. Gli handle di layout di tastiera possono essere ottenuti [**dalla funzione LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) [**o GetKeyboardLayoutList.**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist) I **valori HKL \_ NEXT** e **HKL \_ PREV** possono essere usati anche per selezionare la tastiera successiva o precedente.

La [**funzione GetKeyboardLayoutName**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea) recupera il nome del layout di tastiera attivo per il thread chiamante. Se un'applicazione crea il layout attivo usando la [**funzione LoadKeyboardLayout,**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) **GetKeyboardLayoutName** recupera la stessa stringa usata per creare il layout. In caso contrario, la stringa è l'identificatore di lingua principale corrispondente alle impostazioni locali del layout attivo. Ciò significa che la funzione non può necessariamente distinguere tra layout diversi con la stessa lingua primaria, pertanto non può restituire informazioni specifiche sulla lingua di input. La [**funzione GetKeyboardLayout,**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout) tuttavia, può essere usata per determinare la lingua di input.

La [**funzione LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) carica un layout di tastiera e lo rende disponibile all'utente. Le applicazioni possono rendere il layout immediatamente attivo per il thread corrente usando il **valore KLF \_ ACTIVATE.** Un'applicazione può usare **il valore KLF \_ REORDER** per riordinare i layout senza specificare anche il **valore KLF \_ ACTIVATE.** Le applicazioni devono sempre usare il **valore KLF \_ SUBSTITUTE \_ OK** durante il caricamento dei layout di tastiera per assicurarsi che sia selezionata la preferenza dell'utente, se presente.

Per il supporto multilingue, la [**funzione LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) fornisce i flag **KLF \_ REPLACELANG** e **KLF \_ NOTELLSHELL.** Il flag **KLF \_ REPLACELANG** indica alla funzione di sostituire un layout di tastiera esistente senza modificare la lingua. Il tentativo di sostituire un layout esistente usando lo stesso identificatore di lingua, ma senza specificare **KLF \_ REPLACELANG,** è un errore. Il flag **\_ NOTELLSHELL di KLF** impedisce alla funzione di notificare alla shell quando viene aggiunto o sostituito un layout di tastiera. Ciò è utile per le applicazioni che aggiungono più layout in una serie consecutiva di chiamate. Questo flag deve essere usato in tutte le chiamate, ad esempio l'ultima.

La [**funzione UnloadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout) è limitata in quanto non può scaricare la lingua di input predefinita del sistema. In questo modo si garantisce che l'utente abbia sempre un layout disponibile per l'immissione di testo usando lo stesso set di caratteri usato dalla shell e file system.

 

 
