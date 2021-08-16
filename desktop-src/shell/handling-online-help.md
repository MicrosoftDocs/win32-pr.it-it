---
description: La Guida online può essere disponibile in diversi formati, da informazioni concettuali dettagliate a definizioni rapide. In questo argomento sono contenute le sezioni seguenti.
title: Gestione della Guida online
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: caf576d723b27e1c81bb715ea04743740930b5bb257f03eb3ca0a9ab697affd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223683"
---
# <a name="handling-online-help"></a>Gestione della Guida online

La Guida online può essere disponibile in diversi formati, da informazioni concettuali dettagliate a definizioni rapide. In questo argomento sono contenute le sezioni seguenti.

-   [Informazioni sulla Guida](#about-help)
    -   [Richieste di assistenza](#help-requests)
    -   [Help Display and Windows Help](#help-display-and-windows-help)
-   [Uso della Guida](#using-help)
    -   [Informazioni della Guida in una finestra di dialogo](#providing-help-in-a-dialog-box)
    -   [Impostazione dell'aspetto di una finestra della Guida secondaria](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Informazioni sulla Guida

Un elemento importante di un'applicazione facile da usare è immediatamente disponibile nella Guida online. Windows fornisce funzioni e messaggi che, se usati in combinazione con l'applicazione della Guida di Windows, semplificano l'implementazione della Guida online nell'applicazione. In questa panoramica vengono illustrati gli elementi di Windows che supportano la Guida online. Viene descritto come usare questi elementi per offrire agli utenti un mezzo per richiedere assistenza e come usare l'applicazione Windows per visualizzare la Guida.

### <a name="help-requests"></a>Richieste di assistenza

La maggior parte delle applicazioni basate su Windows fornisce informazioni della Guida online in un'ampia gamma di moduli, dalla guida concettuale che illustra lo scopo delle funzionalità di un'applicazione alla Guida popup che fornisce definizioni rapide di singoli elementi nell'interfaccia utente dell'applicazione. Le funzioni e i messaggi vengono utilizzati per offrire agli utenti un'ampia gamma di modi per richiedere l'accesso a queste informazioni. Le sezioni seguenti descrivono queste richieste di assistenza.

### <a name="help-menu"></a>Menu Guida

La maggior parte delle applicazioni consente all'utente di accedere alle informazioni della Guida includendo **un** menu ? nella finestra principale. Quando l'utente seleziona un elemento da un **menu** ? , la routine della finestra corrispondente riceve un messaggio [**WM \_ COMMAND**](../menurc/wm-command.md) che identifica l'elemento selezionato. L'applicazione risponde visualizzando le informazioni della Guida appropriate, ad esempio un elenco di argomenti della Guida, un indice o un'introduzione all'applicazione.

### <a name="help-from-the-keyboard"></a>Guida dalla tastiera

Windows consente all'utente di accedere alle informazioni della Guida dalla tastiera inviando una notifica all'applicazione ogni volta che l'utente preme il tasto F1. Il sistema invia un [**messaggio WM \_ HELP**](wm-help.md) alla finestra con lo stato attivo quando l'utente preme il tasto. Se la finestra è una finestra figlio, ad esempio un controllo in una finestra di dialogo, la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre. Se un menu è attivo quando si preme F1, il sistema invia il messaggio alla finestra associata al menu. L'applicazione risponde visualizzando le informazioni della Guida associate alla finestra, al controllo o al menu con lo stato attivo o attivo. Ad esempio, se l'utente seleziona un controllo in una finestra di dialogo e preme F1, l'applicazione visualizza le informazioni della Guida per tale controllo.

Il *parametro lParam* di [**WM HELP \_ è**](wm-help.md) un puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che contiene informazioni dettagliate sull'elemento per cui è richiesta la Guida. Usare queste informazioni per determinare l'argomento della Guida da visualizzare. La **struttura HELPINFO** include anche le coordinate del cursore del mouse nel momento in cui l'utente ha premuto il tasto. È possibile utilizzare queste informazioni per fornire informazioni della Guida in base alla posizione del cursore del mouse.

### <a name="help-from-the-mouse"></a>Guida del mouse

Windows consente all'utente di accedere alle informazioni della Guida dal mouse inviando una notifica all'applicazione ogni volta che l'utente fa clic con il pulsante destro del mouse o fa clic su una finestra, un controllo o un menu dopo aver fatto clic sul pulsante Domanda (?). L'applicazione risponde visualizzando le informazioni della Guida associate alla finestra, al controllo o al menu specificato.

Il sistema invia un [**messaggio WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) quando l'utente fa clic con il pulsante destro del mouse. La finestra su cui è stato fatto clic riceve il messaggio. Se la finestra è una finestra figlio, ad esempio un controllo , la [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre. Il **messaggio WM \_ CONTEXTMENU** specifica le coordinate del cursore del mouse. La coordinata x è nella parola di ordine basso del parametro *lParam* e la coordinata y si trova nella parola di ordine superiore. Se l'utente ha fatto clic su un controllo, il *parametro wParam* è l'handle per il controllo che ha ricevuto il clic.

Il sistema invia un [**messaggio della \_**](wm-help.md) Guida WM quando l'utente fa clic su un elemento in una finestra dopo aver fatto clic sul pulsante Domanda (?) visualizzato nella barra del titolo della finestra. È possibile aggiungere un pulsante Domanda a una barra del titolo specificando lo stile **WS \_ EX \_ CONTEXTHELP** nella [**funzione CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) durante la creazione della finestra. Il *parametro lParam* di **WM \_ HELP** è un puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che contiene informazioni dettagliate sull'elemento per cui è richiesta la Guida, incluse le coordinate del cursore del mouse nel momento in cui l'utente ha fatto clic sul pulsante del mouse.

Il pulsante Domanda è consigliato solo nelle finestre di dialogo. In passato, le applicazioni hanno fornito all'utente l'accesso alle informazioni della Guida su una finestra di dialogo fornendo un pulsante ? nella finestra di dialogo.  Questo metodo non è più consigliato. Usare invece il pulsante Domanda.

### <a name="help-display-and-windows-help"></a>Help Display and Windows Help

Quando un'applicazione riceve una richiesta di assistenza, deve visualizzare le informazioni della Guida appropriate. Poiché l Windows'applicazione Della Guida fornisce un'interfaccia utente coerente, è consigliabile che le applicazioni usino Windows Guida anziché altri metodi. Per indicare Windows Guida per visualizzare le informazioni della Guida, un'applicazione usa la funzione [**WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) specificando dettagli quali le informazioni da visualizzare e il form della finestra in cui visualizzarle. Le sezioni seguenti illustrano come usare **WinHelp per** visualizzare informazioni della Guida.

### <a name="help-files"></a>file della Guida

Per visualizzare le informazioni della Guida, è necessario specificare un file della Guida quando si chiama la [**funzione WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Il file della Guida deve avere il Windows file della Guida (con estensione hlp) e uno o più argomenti. Ogni argomento è un'unità distinta di informazioni, ad esempio una descrizione concettuale, un set di istruzioni, un'immagine, una definizione di glossario e così via. Gli argomenti devono essere identificati in modo univoco in modo Windows guida possa individuarli ogni volta che vengono richiesti. Internamente, Windows guida usa gli identificatori di argomento per individuare gli argomenti, ma le applicazioni usano spesso identificatori di contesto (valori interi univoci) per specificare gli argomenti da visualizzare. L'autore del file della Guida deve eseguire in modo esplicito il mapping degli identificatori di contesto agli identificatori di argomento nella sezione MAP del file di progetto usato \[ \] per compilare il file della Guida.

Quando si specifica un file della Guida ma non si specifica un percorso, [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) cerca il file della Guida nella directory della Guida o in una directory specificata dalla variabile di ambiente PATH. WinHelp può anche **trovare** un file della Guida il cui nome è elencato nel percorso del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Per sfruttare i vantaggi del Registro di sistema, è necessario creare un nome di valore con lo stesso nome del file della Guida. Il valore assegnato a tale nome deve essere la directory in cui si trova il file della Guida.

Se [**WinHelp non**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) riesce a trovare il file della Guida specificato, viene visualizzata una finestra di dialogo che consente all'utente di specificare il percorso del file della Guida. Poiché **WinHelp** salva le informazioni sul percorso nel Registro di sistema, non chiede di nuovo il percorso dello stesso file della Guida.

Per altre informazioni su come creare e compilare un file della Guida, vedere la documentazione fornita con gli strumenti di sviluppo.

### <a name="starting-windows-help"></a>Avvio Windows Guida

L'esempio seguente usa [**la funzione WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per avviare l'applicazione Windows e aprire il file della Guida nel relativo argomento Contenuto.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



Nell'esempio seguente viene aperto il file della Guida dell'utente, viene eseguita una ricerca nel file dell'argomento associato a una stringa di parola chiave e quindi viene visualizzato l'argomento.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Argomenti della Guida - finestra di dialogo

È possibile visualizzare la **finestra di dialogo** Argomenti della Guida chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il **comando HELP \_ FINDER.** La **finestra di dialogo** Argomenti della Guida consente all'utente di selezionare gli argomenti da visualizzare visualizzando i titoli degli argomenti, le parole chiave associate agli argomenti o le parole e le frasi presenti negli argomenti. Le applicazioni visualizzano in genere questa finestra di dialogo quando l'utente sceglie un comando, ad esempio Argomenti della Guida, dal menu ? . Un'applicazione può visualizzare questa finestra di dialogo anche se l'utente preme il tasto quando nessuna finestra, controllo o menu specifico nell'applicazione ha lo stato attivo o è attivo.

In passato, le applicazioni usava i comandi **HELP \_ CONTENTS** e **HELP \_ INDEX** con la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per visualizzare l'argomento Contents e l'indice delle parole chiave del file della Guida. Questi comandi non sono più consigliati. In alternativa, usare il **comando HELP \_ FINDER.**

### <a name="information-topics"></a>Argomenti in cui vengono fornite informazioni

È possibile visualizzare un argomento specifico chiamando la [**funzione WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il comando HELP CONTEXT e specificando \_ l'identificatore di contesto per l'argomento. Le applicazioni usano in genere il comando HELP CONTEXT in risposta alle richieste dell'utente relative ad argomenti contenenti informazioni concettuali o informazioni procedurali anziché informazioni su un controllo o un \_ menu specifico. In questi casi, l'utente può continuare a esplorare il file della Guida alla ricerca di informazioni correlate prima di tornare all'applicazione.

Il comando HELP CONTEXT richiama un'istanza regolare di Windows guida, consentendo all'utente di trovare \_ altri argomenti nel file della Guida. Visualizza in genere la finestra principale della Guida, che include una barra del titolo, un menu di sistema, pulsanti di riduzione a icona e ingrandimento, un menu principale, una barra di spostamento facoltativa, un bordo di ridimensionamento e un'area client. Il testo dell'argomento selezionato viene visualizzato nell'area client e l'utente può spostarsi nel file della Guida usando collegamenti rapidi o pulsanti di spostamento nella finestra principale. L'istanza normale Windows guida può essere usata anche per visualizzare la Guida in una o più finestre secondarie anziché nella finestra principale.

### <a name="pop-up-topics"></a>Argomenti popup

È possibile visualizzare un argomento popup contenente informazioni per un controllo o un menu specifico chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il comando HELP WM HELP o \_ HELP \_ \_ CONTEXTMENU. Questi comandi visualizzano un argomento in una finestra popup accanto al controllo o al menu corrispondente. Per consentire all'utente di tornare immediatamente al lavoro nell'applicazione, la finestra popup viene distrutta non appena l'utente preme un tasto o fa clic sul pulsante sinistro del mouse.

Usare il comando HELP \_ WM \_ HELP durante l'elaborazione [**dei messaggi DELLA \_ GUIDA WM**](wm-help.md) per le finestre di controllo. Poiché la maggior parte dei controlli passa il messaggio **WM \_ HELP** alla funzione [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) la routine della finestra di dialogo corrispondente (o routine della finestra padre) elabora questo messaggio. Invece di fornire un identificatore di contesto specifico, la routine della finestra di dialogo deve passare una matrice di coppie di identificatori di controllo e di contesto a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) insieme all'handle di controllo specificato nel membro **hItemHandle** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) passata con il messaggio **WM \_ HELP.** La funzione determina l'identificatore del controllo per il quale è stato generato il messaggio **WM \_ HELP** e usa l'identificatore di contesto corrispondente per visualizzare l'argomento appropriato.

Usare il comando HELP \_ CONTEXTMENU durante l'elaborazione [**dei messaggi WM \_ CONTEXTMENU.**](../menurc/wm-contextmenu.md) Poiché la maggior parte dei controlli passa il messaggio **WM \_ CONTEXTMENU** alla funzione [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) la routine della finestra di dialogo corrispondente (o routine della finestra padre) elabora questo messaggio. La routine specifica una matrice di coppie di identificatori di controllo e contesto. specifica anche l'handle nel *parametro wParam* quando si chiama [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) in modo che la funzione possa selezionare l'identificatore di contesto appropriato dalla matrice e visualizzare l'argomento appropriato. A differenza del comando HELP WM HELP, HELP CONTEXTMENU visualizza innanzitutto un comando \_ \_ \_ **What's This?** in un menu. Se l'utente sceglie il comando, **WinHelp visualizza** l'argomento. In caso contrario, la richiesta viene annullata.

È anche possibile visualizzare gli argomenti popup usando il comando HELP CONTEXTPOPUP e specificando un identificatore di \_ contesto dell'argomento. Questo comando è simile al comando HELP CONTEXT, ma richiama l'istanza popup di Windows Help usata da \_ HELP WM HELP e HELP \_ \_ \_ CONTEXTMENU. Le applicazioni possono usare questo comando in risposta ai [**messaggi WM \_ HELP**](wm-help.md) per visualizzare la Guida per i menu e per le finestre che non sono controlli in una finestra di dialogo. Per usare questo comando in modo più efficace, l'applicazione deve assegnare identificatori di contesto a questi menu e finestre.

È possibile assegnare un identificatore di contesto a qualsiasi finestra o menu nell'applicazione. Quando viene generato un messaggio [**WM \_ HELP,**](wm-help.md) il sistema include l'identificatore di contesto nella [**struttura HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che viene passato alla finestra padre nel **messaggio WM \_ HELP.** La finestra padre può quindi passare l'identificatore di contesto [**a WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per visualizzare l'argomento della Guida richiesto.

Usare la [**funzione SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) per assegnare un identificatore di contesto a una finestra o a un controllo e la [**funzione SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) per assegnare un identificatore di contesto a un menu. È possibile recuperare l'identificatore di contesto per una finestra o un menu usando la [**funzione GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) o [**GetMenuContextHelpId.**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid)

### <a name="keyword-searches"></a>Ricerche di parole chiave

È possibile abilitare l'utente per trovare e visualizzare gli argomenti assegnando parole chiave agli argomenti nel file della Guida. Una parola chiave è semplicemente una stringa associata a uno o più argomenti. Windows La Guida raccoglie tutte le parole chiave in un file della Guida, le inserisce in una tabella e le visualizza nell'elenco Indice della finestra **di dialogo** Argomenti della Guida. Quando l'utente seleziona una parola chiave, nella Guida di Windows viene visualizzato l'argomento della Guida associato oppure, se alla parola chiave è associato più di un argomento, viene visualizzato un elenco di argomenti tra cui l'utente può scegliere.

In un'applicazione è possibile usare il comando HELP KEY, HELP PARTIALKEY o HELP MULTIKEY con la funzione WinHelp per cercare e visualizzare argomenti della Guida in base a parole chiave intere \_ \_ o \_ parziali. [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Specificare il comando, la stringa della parola chiave, il file della Guida e l'handle per la finestra del proprietario. In tutti i casi, se viene trovata una singola corrispondenza, **WinHelp visualizza** l'argomento corrispondente. Se vengono trovate più corrispondenze, la funzione visualizza la finestra di dialogo Argomenti trovati e l'utente può scegliere quale argomento visualizzare. Se non viene trovata alcuna corrispondenza, **WinHelp** visualizza l'elenco Indice (per HELP KEY e HELP PARTIALKEY) o visualizza un messaggio di errore \_ \_ (per HELP \_ MULTIKEY).

L'applicazione può cercare più parole chiave in una singola chiamata a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) separando le parole chiave con punti e virgola. La ricerca di più parole chiave non è supportata per i file della Guida creati Windows versione 3. *x*) Può anche cercare parole chiave in più file della Guida se il file della Guida specificato include un file contents(.cnt) che contiene i comandi :Index o :Link. Con il comando HELP \_ KEY, **WinHelp** cerca le parole chiave in tutti i file specificati da questi comandi. Con i comandi HELP MULTIKEY e HELP PARTIALKEY, la funzione cerca tutti i file tranne quelli \_ \_ specificati dai comandi :Link.

Per impostazione predefinita, Windows Guida riconosce solo la tabella delle parole chiave identificata dal carattere K nel file di origine della Guida. È possibile indirizzare Windows Guida per creare tabelle di parole chiave aggiuntive aggiungendo un carattere di nota a piè di pagina diverso da K, con la definizione della parola chiave, nel file di origine della Guida. Il carattere A della nota a piè di pagina, tuttavia, è riservato. È necessario definire eventuali tabelle di parole chiave aggiuntive usando istruzioni MULTIKEY nella sezione OPTIONS del file di progetto \[ durante la compilazione del file della \] Guida.

Un'applicazione può usare il comando HELP SETINDEX con la funzione WinHelp per indirizzare Windows Guida per visualizzare una tabella di parole chiave diversa da K nel \_ relativo elenco di indici. [](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Per indirizzare Windows guida alla ricerca di una parola chiave in una tabella di parole chiave alternativa, un'applicazione può usare il comando HELP \_ MULTIKEY. È possibile specificare la parola chiave e la tabella delle parole chiave in [**una struttura MULTIKEYHELP,**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) che viene passata a **WinHelp**.

Quando [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) visualizza un argomento, lo visualizza nella finestra specificata dalla nota a piè di pagina ">" per l'argomento, nella finestra specificata dal comando :Base nel file di contenuto o nella finestra principale. Se la finestra principale è già aperta in un file della Guida diverso quando si chiama **WinHelp,** la funzione nasconde la finestra principale durante la ricerca. In questo caso, l'annullamento  di entrambe le finestre **di** dialogo Argomenti trovati e Argomenti della Guida chiude la finestra principale.

### <a name="secondary-help-windows"></a>Finestre della Guida secondaria

La finestra principale dell'Windows della Guida è denominata finestra primaria. Windows La Guida può anche visualizzare gli argomenti della Guida in una finestra secondaria. A differenza della finestra principale della Guida, una finestra secondaria non contiene una barra dei menu. È possibile includere una barra di spostamento in una finestra secondaria ed è possibile aggiungere pulsanti alla barra. È anche possibile scegliere di fare in modo che Windows La Guida regola automaticamente l'altezza della finestra secondaria per adattare l'argomento.

È necessario definire le finestre secondarie nella sezione WINDOWS del file di progetto della Guida, specificando il nome e, facoltativamente, le dimensioni iniziali e \[ la posizione di ogni \] finestra. È possibile indirizzare l'applicazione guida Windows per visualizzare un argomento in una finestra secondaria aggiungendo una parentesi angolare (>) e il nome definito per la finestra secondaria al nome del file della Guida. La stringa risultante viene quindi passata alla [**funzione WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)

Un'applicazione può modificare le dimensioni e la posizione di una finestra primaria o secondaria specificando l'indirizzo di una struttura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) e il comando HELP SETWINPOS in una chiamata \_ a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO** specifica il nome della finestra e le nuove dimensioni e posizione.

### <a name="training-card-help"></a>Guida della scheda di training

Usando la guida della scheda di training, un'applicazione può visualizzare una sequenza di istruzioni per guidare l'utente nei passaggi di un'attività. Una scheda di training è in genere costituita da testo che illustra un passaggio specifico e pulsanti associati alle macro TCard, che consentono all'utente di indicare all'applicazione cosa fare successivamente. Le schede di training possono essere visualizzate solo nelle finestre secondarie e non devono contenere collegamenti rapidi ad altri argomenti nel file della Guida.

Un'applicazione avvia l'istanza della scheda di training della Guida di Windows chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e specificando il comando HELP TCARD in combinazione con un altro comando, ad esempio \_ HELP \_ CONTEXT. Successivamente, quando l'utente fa clic su un pulsante nella scheda di training, fa clic su un'area sensibile assegnata alla macro TCard o chiude la scheda di training, Windows Help notifica all'applicazione inviando un messaggio [**WM \_ TCARD.**](wm-tcard.md) Il *parametro wParam* identifica il pulsante o l'azione utente e il *parametro lParam* contiene dati aggiuntivi, il cui significato dipende dal valore *di wParam*.

### <a name="canceling-help"></a>Annullamento della Guida

Windows La Guida richiede a un'applicazione di annullare in modo esplicito la Guida in modo che possa liberare tutte le risorse usate per tenere traccia dell'applicazione e dei relativi file della Guida. L'applicazione può eseguire questa operazione in qualsiasi momento chiamando la [**funzione WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e specificando il comando HELP \_ QUIT. Si noti che questo non è vero per l'istanza popup di Windows Guida. Un'applicazione non deve tentare di chiudere un'istanza popup.

Se un'applicazione ha effettuato chiamate a [**WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa)deve annullare la Guida prima di chiudere la finestra principale, ad esempio in risposta al messaggio WM DESTROY nella procedura della finestra \_ principale. Un'applicazione deve chiamare **WinHelp** una sola volta per annullare la Guida, indipendentemente dal numero di file della Guida aperti. Windows La Guida rimane in esecuzione fino a quando tutte le applicazioni o le DLL non hanno annullato la Guida.

Per chiudere l'istanza della scheda di training Windows Help, è necessario specificare entrambi i comandi HELP TCARD e \_ HELP QUIT quando si chiama \_ [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Un'applicazione non deve annullare l'istanza della scheda di training Windows Guida se l'utente la annulla per prima. Windows Invia una notifica a un'applicazione quando l'utente annulla l'istanza della scheda di training inviando il messaggio [**WM \_ TCARD**](wm-tcard.md) con il *parametro wParam* impostato su IDCLOSE.

## <a name="using-help"></a>Uso della Guida

Questa sezione illustra come fornire la Guida sensibile al contesto per una finestra di dialogo e come impostare l'aspetto di una finestra della Guida secondaria.

-   [Informazioni della Guida in una finestra di dialogo](#providing-help-in-a-dialog-box)
-   [Impostazione dell'aspetto di una finestra della Guida secondaria](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Informazioni della Guida in una finestra di dialogo

Per fornire la Guida sensibile al contesto in una finestra di dialogo, è necessario creare una matrice costituita da coppie **di valori DWORD.** Il primo valore in ogni coppia è l'identificatore di un controllo nella finestra di dialogo e il secondo è l'identificatore di contesto dell'argomento della Guida per il controllo. La matrice deve contenere una coppia di identificatori per ogni controllo nella finestra di dialogo.

La routine della finestra di dialogo deve elaborare [**i messaggi WM \_ HELP**](wm-help.md) e [**WM \_ CONTEXTMENU.**](../menurc/wm-contextmenu.md) La procedura della finestra di dialogo riceve **WM \_ HELP** quando l'utente preme il tasto e **WM \_ CONTEXTMENU** quando l'utente fa clic con il pulsante destro del mouse.

Il *parametro lParam* di [**WM \_ HELP**](wm-help.md) contiene l'indirizzo di [**una struttura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo) Il **membro hItemHandle** di questa struttura identifica il controllo per cui l'utente ha richiesto assistenza. È necessario passare questo handle alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) insieme al comando HELP WM HELP, al nome del file della Guida e a un puntatore alla \_ matrice di \_ identificatori. La **funzione WinHelp** cerca l'identificatore di controllo del controllo specificato nella matrice e quindi recupera l'identificatore di contesto della Guida corrispondente. La funzione passa quindi l'identificatore del contesto della Guida Windows Guida, che trova l'argomento corrispondente e lo visualizza in una finestra popup. Se il controllo ha un identificatore -1, il sistema cerca il controllo successivo che è una tabulazione e quindi usa il relativo identificatore per trovare l'identificatore del contesto della Guida. Per questo motivo, è importante inserire testo statico prima dei controlli in un file di risorse.

Quando si chiama la [**funzione WinHelp,**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) l'elaborazione [**di WM \_ CONTEXTMENU**](../menurc/wm-contextmenu.md) è simile all'elaborazione [**di WM \_ HELP**](wm-help.md) con queste due eccezioni:

-   Il parametro *wParam* viene passato da [**WM \_ CONTEXTMENU,**](../menurc/wm-contextmenu.md)ovvero l'handle al controllo che ha inviato il messaggio.
-   Specificare il **comando HELP \_ CONTEXTMENU** anziché **HELP WM \_ \_ HELP**.

Il **comando HELP \_ CONTEXTMENU** fa sì Windows guida di visualizzare un menu prima di visualizzare l'argomento della Guida. Il menu è definito dal sistema. Consente all'utente di visualizzare la Guida per il controllo o la finestra di dialogo **Argomenti** della Guida.

Nell'esempio seguente viene illustrato come implementare la Guida sensibile al contesto in una finestra di dialogo.


```
LRESULT CALLBACK EditDlgProc(HWND hwndDlg, UINT uMsg, 
                             WPARAM wParam, LPARAM lParam) 
{ 
    // Create an array of control identifiers and context identifiers. 
    static DWORD aIds[ ] = 
    { 
        ID_SAVE,   IDH_SAVE, 
        ID_DELETE, IDH_DELETE, 
        ID_COPY,   IDH_COPY, 
        ID_PASTE,  IDH_PASTE, 
        0,0 
    }; 

    switch (uMsg) 
    { 
        case WM_HELP: 
            WinHelp(((LPHELPINFO)lParam)->hItemHandle, "helpfile.hlp", 
                    HELP_WM_HELP, (DWORD)(LPSTR)aIds); 
            break; 

        case WM_CONTEXTMENU: 
            WinHelp((HWND)wParam, "helpfile.hlp", HELP_CONTEXTMENU, 
                    (DWORD)(LPVOID)aIds); 
            break; 
        
        // Process other messages here. 
    } 
    return FALSE; 
}
```



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Impostazione dell'aspetto di una finestra della Guida secondaria

Un'applicazione può impostare le dimensioni, la posizione e lo stato di visualizzazione di una finestra della Guida secondaria passando il comando HELP SETWINPOS e l'indirizzo di una struttura \_ [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) alla [**funzione WinHelp.**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) I membri di **HELPWININFO** specificano il nome della finestra da modificare e le nuove dimensioni, posizione e stato di visualizzazione della finestra.

Nell'esempio seguente viene impostato l'aspetto di una finestra secondaria denominata "wnd \_ menu". Il nome deve essere definito nella sezione \[ WINDOWS del file di progetto della \] Guida.


```
BOOL DoWindowSize(VOID) 
{ 
    HANDLE hhwi; 
    LPHELPWININFO lphwi; 
    WORD wSize; 
    char *szWndName = "wnd_menu"; 
    size_t NameLength;      // Does not include the terminating null character
    HRESULT hr
    BOOL retval;

    hr = StringCbLengthA(szWndName, STRSAFE_MAX_CCH, &NameLength);
    
    if (SUCCEEDED(hr))
    {
        // Add 1 to account for the name string's terminating null character.
        NameLength++;
        
        // The HELPWININFO structure contains a minimal TCHAR array of size [2] 
        // that is used for the window name. Since sizeof(HELPWININFO) 
        // includes those two TCHARS, they must be subtracted from the 
        // total when adding the actual string length to calculate the  
        // size of the structure. 
        wSize = sizeof(HELPWININFO) - 2 + NameLength; 
    }
    else
        // Something's amiss with the string.
        return FALSE;
        
    hhwi  = GlobalAlloc(GHND, wSize); 
    lphwi = (LPHELPWININFO)GlobalLock(hhwi); 

    lphwi->wStructSize = wSize; 
    lphwi->x    = 256;      // horizontal position 
    lphwi->y    = 256;      // vertical position 
    lphwi->dx   = 767;      // width 
    lphwi->dy   = 512;      // height 
    lphwi->wMax = SW_SHOW;  // show the window 
    
    // secondary window
    hr = StringCbCopyA(lphwi->rgchMember, sizeof(lphwi->rgchMember), szWndName);
    
    if (SUCCEEDED(hr))
    {
        WinHelp(hwnd, "myhelp.hlp", HELP_SETWINPOS, (DWORD)lphwi); 
     
        GlobalUnlock(hhwi); 
        GlobalFree(hhwi); 

        return TRUE; 
    }
    else
        // There was a problem copying the window name.
        return FALSE;
}
```



 

 
