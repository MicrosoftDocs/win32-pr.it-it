---
description: La guida online può essere costituita da diverse forme, da informazioni concettuali dettagliate a definizioni rapide. In questo argomento sono contenute le sezioni seguenti.
title: Gestione della Guida in linea
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2a3f6034-6ba6-4204-a2e1-59995fbf40fe
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f1c125df135068c2eee37cb33a8a9d2b281b1f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994696"
---
# <a name="handling-online-help"></a>Gestione della Guida in linea

La guida online può essere costituita da diverse forme, da informazioni concettuali dettagliate a definizioni rapide. In questo argomento sono contenute le sezioni seguenti.

-   [Informazioni sulla guida](#about-help)
    -   [Richieste della Guida](#help-requests)
    -   [Guida di visualizzazione e guida di Windows](#help-display-and-windows-help)
-   [Uso della Guida](#using-help)
    -   [Fornire la Guida in una finestra di dialogo](#providing-help-in-a-dialog-box)
    -   [Impostazione dell'aspetto di una finestra della guida secondaria](#setting-the-appearance-of-a-secondary-help-window)

## <a name="about-help"></a>Informazioni sulla guida

Un elemento importante di un'applicazione intuitiva è immediatamente disponibile nella Guida in linea. Windows fornisce funzioni e messaggi che, se utilizzati insieme all'applicazione della Guida di Windows, semplificano l'implementazione della guida online nell'applicazione. In questa panoramica vengono illustrati gli elementi di Windows che supportano la Guida in linea. Viene descritto come utilizzare questi elementi per fornire agli utenti un mezzo per richiedere assistenza e viene illustrato come utilizzare l'applicazione della Guida di Windows per visualizzare la guida.

### <a name="help-requests"></a>Richieste della Guida

La maggior parte delle applicazioni basate su Windows fornisce informazioni della guida online in un'ampia gamma di moduli, dalla Guida concettuale che spiega lo scopo delle funzionalità di un'applicazione alla Guida popup che fornisce definizioni rapide dei singoli elementi nell'interfaccia utente dell'applicazione. Si usano funzioni e messaggi per offrire agli utenti una serie di modi per richiedere l'accesso a queste informazioni. Nelle sezioni seguenti vengono descritte queste richieste della guida.

### <a name="help-menu"></a>Menu Guida

La maggior parte delle applicazioni fornisce l'accesso utente alle informazioni **della guida includendo un menu** ? nella finestra principale. Quando l'utente **Seleziona un elemento da un menu?** , la routine della finestra corrispondente riceve un messaggio di [**\_ comando WM**](../menurc/wm-command.md) che identifica l'elemento selezionato. L'applicazione risponde visualizzando le informazioni della guida appropriate, ad esempio un elenco di argomenti della guida, un indice o un'introduzione all'applicazione.

### <a name="help-from-the-keyboard"></a>Guida dalla tastiera

Windows consente agli utenti di accedere alle informazioni della Guida tramite la tastiera inviando una notifica all'applicazione ogni volta che l'utente preme il tasto F1. Il sistema invia un messaggio della [**\_ Guida WM**](wm-help.md) alla finestra con lo stato attivo quando l'utente preme il tasto. Se la finestra è una finestra figlio, ad esempio un controllo in una finestra di dialogo, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre. Se un menu è attivo quando si preme F1, il sistema invia il messaggio alla finestra associata al menu. L'applicazione risponde visualizzando le informazioni della Guida associate alla finestra, al controllo o al menu con lo stato attivo o attivo. Se, ad esempio, l'utente seleziona un controllo in una finestra di dialogo e preme F1, l'applicazione visualizzerà le informazioni della guida relative a tale controllo.

Il parametro *lParam* della [**\_ Guida WM**](wm-help.md) è un puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) contenente informazioni dettagliate sull'elemento per il quale è richiesta la guida. Usare queste informazioni per determinare l'argomento della guida da visualizzare. La struttura **HELPINFO** include anche le coordinate del cursore del mouse al momento in cui l'utente ha premuto il tasto. È possibile utilizzare queste informazioni per fornire informazioni sulla posizione del cursore del mouse.

### <a name="help-from-the-mouse"></a>Guida dal mouse

Windows fornisce all'utente l'accesso alle informazioni della guida dal mouse inviando una notifica all'applicazione ogni volta che l'utente fa clic con il pulsante destro del mouse o fa clic su una finestra, un controllo o un menu dopo aver fatto clic sul pulsante question (?). L'applicazione risponde visualizzando le informazioni della Guida associate alla finestra, al controllo o al menu specificato.

Il sistema invia un messaggio [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) quando l'utente fa clic con il pulsante destro del mouse. La finestra su cui è stato fatto clic riceve il messaggio. Se la finestra è una finestra figlio, ad esempio un controllo, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) passa il messaggio alla finestra padre. Il messaggio **WM \_ ContextMenu** specifica le coordinate del cursore del mouse. La coordinata x si trova nella parola di basso livello del parametro *lParam* e la coordinata y si trova nella parola più ordinata. Se l'utente ha fatto clic su un controllo, il parametro *wParam* è l'handle per il controllo che ha ricevuto il clic.

Il sistema invia un messaggio della [**\_ Guida WM**](wm-help.md) quando l'utente fa clic su un elemento in una finestra dopo aver fatto clic sul pulsante question (?) che viene visualizzato nella barra del titolo della finestra. È possibile aggiungere un pulsante di domanda a una barra del titolo specificando lo stile **WS \_ ex \_ CONTEXTHELP** nella funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) quando si crea la finestra. Il parametro *lParam* della **\_ Guida WM** è un puntatore a una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) contenente informazioni dettagliate sull'elemento per il quale è richiesta la guida, incluse le coordinate del cursore del mouse al momento in cui l'utente ha fatto clic sul pulsante del mouse.

È consigliabile usare il pulsante domanda solo nelle finestre di dialogo. In passato, le applicazioni hanno fornito l'accesso utente per ottenere informazioni sulla guida relative a una finestra di dialogo, **fornendo un pulsante** ? nella finestra di dialogo. Questo metodo non è più consigliato. In alternativa, usare il pulsante question.

### <a name="help-display-and-windows-help"></a>Guida di visualizzazione e guida di Windows

Quando un'applicazione riceve una richiesta di assistenza, deve visualizzare le informazioni della guida appropriate. Poiché l'applicazione della Guida di Windows fornisce un'interfaccia utente coerente, è consigliabile che le applicazioni usino la Guida di Windows invece di altri metodi. Per indirizzare la Guida di Windows alla visualizzazione di informazioni della guida, un'applicazione utilizza la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , specificando dettagli quali le informazioni da visualizzare e il formato della finestra in cui viene visualizzata. Le sezioni seguenti illustrano come usare **WinHelp** per visualizzare le informazioni della guida.

### <a name="help-files"></a>file della Guida

Per visualizzare le informazioni della guida, è necessario specificare un file della guida quando si chiama la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . Il file della guida deve avere il formato di file della Guida di Windows (con estensione hlp) e uno o più argomenti. Ogni argomento è un'unità distinta di informazioni, ad esempio una descrizione concettuale, un set di istruzioni, un'immagine, una definizione di glossario e così via. Gli argomenti devono essere identificati in modo univoco, in modo che la Guida di Windows possa individuarli ogni volta che vengono richiesti. Internamente, la Guida di Windows utilizza gli identificatori di argomento per individuare gli argomenti, ma le applicazioni utilizzano più spesso identificatori di contesto (valori integer univoci) per specificare gli argomenti da visualizzare. L'autore del file della guida deve eseguire in modo esplicito il mapping degli identificatori di contesto agli identificatori di argomento nella \[ \] sezione della mappa del file di progetto usato per compilare il file della guida.

Quando si specifica un file della guida ma non si specifica un percorso, [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) Cerca il file della guida nella directory della guida o in una directory specificata dalla variabile di ambiente Path. Inoltre, **WinHelp** è in grado di trovare un file della guida il cui nome è elencato nel seguente percorso del registro di sistema:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Help
```

Per sfruttare i vantaggi del registro di sistema, è necessario creare un nome di valore con lo stesso nome del file della guida. Il valore assegnato a tale nome deve corrispondere alla directory in cui risiede il file della guida.

Se [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) non riesce a trovare il file della Guida specificato, viene visualizzata una finestra di dialogo che consente all'utente di specificare il percorso del file della guida. Poiché **WinHelp** Salva le informazioni sul percorso nel registro di sistema, non viene più richiesta la posizione dello stesso file della guida.

Per ulteriori informazioni su come creare e compilare un file della guida, vedere la documentazione fornita con gli strumenti di sviluppo.

### <a name="starting-windows-help"></a>Avvio della Guida di Windows

Nell'esempio seguente viene usata la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per avviare l'applicazione della Guida di Windows e aprire il file della guida nell'argomento relativo al contenuto.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_CONTENTS, 0L);
```



Nell'esempio seguente viene aperto il file della Guida dell'utente, viene eseguita una ricerca nel file per l'argomento associato a una stringa di parole chiave, quindi viene visualizzato l'argomento.


```
HWND hwnd;     // main window handle 
BOOL bResult   // for checking Boolean function result 

bResult = WinHelp(hWnd, "WINNT.HLP", HELP_KEY, (DWORD) "finding topics");
```



### <a name="help-topics-dialog-box"></a>Finestra di dialogo argomenti della Guida

È possibile visualizzare la finestra di dialogo **argomenti della Guida** chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il comando **Help \_ Finder** . La finestra di dialogo **argomenti della Guida** consente all'utente di selezionare gli argomenti da visualizzare visualizzando i titoli degli argomenti, le parole chiave associate agli argomenti oppure le parole e le frasi trovate negli argomenti. In genere, le applicazioni visualizzano questa finestra di dialogo quando l'utente sceglie un comando, ad esempio gli argomenti della guida, dal menu?. Un'applicazione può anche visualizzare questa finestra di dialogo se l'utente preme il tasto quando nessuna finestra, un controllo o un menu specifico nell'applicazione ha lo stato attivo o è attivo.

In passato, le applicazioni usavano il **\_ contenuto della Guida** e i comandi dell' **\_ Indice** della guida con la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per visualizzare l'argomento contenuto e la parola chiave index del file della guida. Questi comandi non sono più consigliati. Usare invece il comando **Help \_ Finder** .

### <a name="information-topics"></a>Argomenti relativi alle informazioni

È possibile visualizzare un argomento specifico chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il comando di \_ contesto della guida e specificando l'identificatore di contesto per l'argomento. Le applicazioni utilizzano in genere il comando di contesto della Guida \_ in risposta alle richieste dell'utente per argomenti contenenti informazioni concettuali o la guida procedurale anziché informazioni su un controllo o un menu specifico. In questi casi, l'utente può continuare a esplorare il file della guida cercando le informazioni correlate prima di tornare all'applicazione.

Il \_ comando di contesto della guida richiama una normale istanza della Guida di Windows, consentendo all'utente di trovare altri argomenti nel file della guida. Viene in genere visualizzata la finestra della guida principale, che include una barra del titolo, un menu di sistema, i pulsanti Riduci a icona e Ingrandisci, un menu principale, una barra di navigazione facoltativa, un bordo di ridimensionamento e un'area client. Il testo dell'argomento selezionato viene visualizzato nell'area client e l'utente può spostarsi nel file della guida usando i collegamenti sensibili o i pulsanti di spostamento nella finestra principale. È inoltre possibile utilizzare la Guida di Windows per visualizzare la Guida in una o più finestre secondarie anziché nella finestra principale.

### <a name="pop-up-topics"></a>Argomenti popup

È possibile visualizzare un argomento popup che contiene informazioni per un controllo o un menu specifico chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) con il \_ comando Guida WM o Guida \_ \_ ContextMenu. Questi comandi visualizzano un argomento in una finestra popup accanto al controllo o al menu corrispondente. Per consentire all'utente di tornare immediatamente a lavorare nell'applicazione, la finestra popup viene distrutta non appena l'utente preme un tasto o fa clic con il pulsante sinistro del mouse.

Usare il comando Help \_ WM \_ Help per elaborare i messaggi della [**\_ Guida WM**](wm-help.md) per le finestre di controllo. Poiché la maggior parte dei controlli passa il messaggio della **\_ Guida WM** alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , il messaggio viene elaborato dalla procedura della finestra di dialogo corrispondente (o dalla procedura della finestra padre). Anziché assegnare un identificatore di contesto specifico, la routine della finestra di dialogo deve passare una matrice di coppie di controlli e di identificatori di contesto a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) insieme all'handle di controllo specificato nel membro **HItemHandle** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) passata con il messaggio della **\_ Guida WM** . La funzione determina l'identificatore del controllo per il quale è stato generato il messaggio della **\_ Guida WM** e utilizza l'identificatore di contesto corrispondente per visualizzare l'argomento appropriato.

Usare il comando HELP \_ ContextMenu quando si elaborano i messaggi di [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) . Poiché la maggior parte dei controlli passa il messaggio **WM \_ ContextMenu** alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , il messaggio viene elaborato dalla routine della finestra di dialogo corrispondente o dalla routine della finestra padre. La procedura specifica una matrice di coppie di controllo e di identificatore di contesto. Specifica inoltre l'handle nel parametro *wParam* quando si chiama [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , in modo che la funzione possa selezionare l'identificatore di contesto appropriato dalla matrice e visualizzare l'argomento appropriato. A differenza del comando della Guida \_ WM \_ , Help \_ ContextMenu Visualizza prima di tutto un comando **What ' s?** in un menu. Se l'utente sceglie il comando, **WinHelp** Visualizza l'argomento. In caso contrario, la richiesta viene annullata.

È anche possibile visualizzare gli argomenti popup usando il \_ comando help CONTEXTPOPUP e specificando un identificatore di contesto dell'argomento. Questo comando è simile al comando del \_ contesto della guida ma richiama l'istanza popup della Guida di Windows usata dalla Guida di \_ WM e dalla Guida di \_ \_ ContextMenu. Le applicazioni possono utilizzare questo comando in risposta ai messaggi della [**\_ Guida di WM**](wm-help.md) per visualizzare la guida per i menu e per le finestre che non sono controlli in una finestra di dialogo. Per usare questo comando in modo più efficace, l'applicazione deve assegnare identificatori di contesto a questi menu e finestre.

È possibile assegnare un identificatore di contesto a qualsiasi finestra o menu nell'applicazione. Quando viene generato un messaggio della [**\_ Guida WM**](wm-help.md) , il sistema include l'identificatore di contesto nella struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) che viene passato alla finestra padre nel messaggio **della \_ Guida WM** . La finestra padre può quindi passare l'identificatore di contesto a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per visualizzare l'argomento della guida richiesto.

Usare la funzione [**SetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setwindowcontexthelpid) per assegnare un identificatore di contesto a una finestra o a un controllo e la funzione [**SetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-setmenucontexthelpid) per assegnare un identificatore di contesto a un menu. È possibile recuperare l'identificatore di contesto per una finestra o un menu usando la funzione [**GetWindowContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getwindowcontexthelpid) o [**GetMenuContextHelpId**](/windows/desktop/api/Winuser/nf-winuser-getmenucontexthelpid) .

### <a name="keyword-searches"></a>Ricerche di parole chiave

È possibile consentire all'utente di trovare e visualizzare gli argomenti assegnando parole chiave agli argomenti del file della guida. Una parola chiave è semplicemente una stringa associata a uno o più argomenti. La Guida di Windows raccoglie tutte le parole chiave in un file della guida, le inserisce in una tabella e le Visualizza nell'elenco indice della finestra di dialogo **argomenti della Guida** . Quando l'utente seleziona una parola chiave, la Guida di Windows Visualizza l'argomento della Guida associato o, se è presente più di un argomento associato alla parola chiave, Visualizza un elenco di argomenti da cui l'utente può scegliere.

In un'applicazione, è possibile usare il \_ tasto Help, la Guida \_ PARTIALKEY o il \_ comando help join con la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per cercare e visualizzare gli argomenti della Guida in base a parole chiave intere o parziali. Si specificano il comando, la parola chiave String, il file della guida e l'handle per la finestra proprietaria. In tutti i casi, se viene rilevata una corrispondenza singola, **WinHelp** Visualizza l'argomento corrispondente. Se viene trovata più di una corrispondenza, la funzione Visualizza la finestra di dialogo Argomenti trovati e l'utente può scegliere quale argomento visualizzare. Se non viene trovata alcuna corrispondenza, **WinHelp** Visualizza l'elenco degli indici (per la chiave della Guida \_ e la Guida \_ PARTIALKEY) o Visualizza un messaggio di errore (per la Guida \_ join).

L'applicazione può cercare più parole chiave in una singola chiamata a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) separando le parole chiave con punti e virgola. La ricerca di più parole chiave non è supportata per i file della Guida creati per Windows versione 3. *x*) consente anche di cercare parole chiave in più file della guida se il file della Guida specificato contiene un file di contenuto (. cnt) che contiene i comandi: index o: link. Con il \_ comando della chiave Help, **WinHelp** Cerca le parole chiave in tutti i file specificati da questi comandi. Con i \_ comandi join e Help \_ PARTIALKEY della guida, la funzione Cerca tutti i file tranne quelli specificati da: comandi di collegamento.

Per impostazione predefinita, la Guida di Windows riconosce solo la tabella delle parole chiave identificata dal carattere a nota K nel file di origine della guida. È possibile indirizzare la Guida di Windows alla creazione di tabelle di parole chiave aggiuntive aggiungendo un carattere a piè di pagina diverso da K, con la definizione della parola chiave, nel file di origine della guida. (Il carattere A piè di pagina A, tuttavia, è riservato). Quando si compila il file della guida, è necessario definire le tabelle di parole chiave aggiuntive usando le istruzioni JOIN nella \[ \] sezione Opzioni del file di progetto.

Un'applicazione può usare il \_ comando help SetIndex con la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) per indirizzare la Guida di Windows alla visualizzazione di una tabella di parole chiave diversa da K nell'elenco degli indici. Per indirizzare la Guida di Windows alla ricerca di una parola chiave in una tabella di parole chiave alternativa, un'applicazione può usare il \_ comando help join. È possibile specificare la parola chiave e la tabella delle parole chiave in una struttura [**MULTIKEYHELP**](/windows/win32/api/winuser/ns-winuser-multikeyhelpa) , che viene passata a **WinHelp**.

Quando in [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) viene visualizzato un argomento, questo viene visualizzato nella finestra specificata dalla nota ">" per l'argomento, nella finestra specificata dal comando: base nel file di contenuto o nella finestra principale. Se la finestra principale è già aperta a un file della Guida diverso quando si chiama **WinHelp**, la funzione nasconde la finestra principale durante la ricerca. In questo caso, l'annullamento di entrambe le finestre di dialogo **argomenti trovati** e **argomenti della Guida** chiude la finestra principale.

### <a name="secondary-help-windows"></a>Finestre della guida secondaria

La finestra principale dell'applicazione della Guida di Windows è detta finestra principale. La Guida di Windows consente inoltre di visualizzare gli argomenti della Guida in una finestra secondaria. A differenza della finestra della guida principale, una finestra secondaria non contiene una barra dei menu. È possibile includere una barra di navigazione in una finestra secondaria ed è possibile aggiungere pulsanti alla barra. È inoltre possibile scegliere di impostare automaticamente la Guida di Windows per regolare l'altezza della finestra secondaria in modo da includere l'argomento.

È necessario definire le finestre secondarie \[ nella \] sezione Windows del file di progetto della guida, specificando il nome e, facoltativamente, le dimensioni iniziali e la posizione di ogni finestra. È possibile indirizzare l'applicazione della Guida di Windows per visualizzare un argomento in una finestra secondaria aggiungendo una parentesi uncinata (>) e il nome definito per la finestra secondaria al nome del file della guida. La stringa risultante viene quindi passata alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

Un'applicazione può modificare le dimensioni e la posizione di una finestra primaria o secondaria specificando l'indirizzo di una struttura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) e il \_ comando help SETWINPOS in una chiamata a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). **HELPWININFO** specifica il nome della finestra e le nuove dimensioni e posizione.

### <a name="training-card-help"></a>Guida alla scheda di formazione

Utilizzando la guida alla scheda di training, un'applicazione può visualizzare una sequenza di istruzioni per guidare l'utente nei passaggi di un'attività. Una scheda di training è costituita in genere da testo che illustra un particolare passaggio e i pulsanti associati alle macro TCard, che consentono all'utente di indicare all'applicazione cosa fare successivamente. Le schede di training possono essere visualizzate solo nelle finestre secondarie e non devono contenere collegamenti sensibili ad altri argomenti del file della guida.

Un'applicazione avvia l'istanza della scheda di training della Guida di Windows chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e specificando il \_ comando help TCARD in combinazione con un altro comando, ad esempio il contesto della Guida \_ . Successivamente, quando l'utente fa clic su un pulsante nella scheda di training, fa clic su un punto attivo assegnato alla macro TCard o chiude la scheda di training, Windows Help invia una notifica all'applicazione inviando un messaggio [**WM \_ TCard**](wm-tcard.md) . Il parametro *wParam* identifica il pulsante o l'azione dell'utente e il parametro *lParam* contiene dati aggiuntivi, il cui significato dipende dal valore di *wParam*.

### <a name="canceling-help"></a>Annullamento della Guida

La Guida di Windows richiede che un'applicazione annulli esplicitamente la Guida in modo da poter liberare le risorse usate per tenere traccia dell'applicazione e dei relativi file della guida. L'applicazione può eseguire questa operazione in qualsiasi momento chiamando la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) e specificando il \_ comando help Quit. Si noti che questa operazione non è valida per l'istanza popup della Guida di Windows. Un'applicazione non deve tentare di chiudere un'istanza popup.

Se un'applicazione ha effettuato chiamate a [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), è necessario annullare la guida prima di chiudere la finestra principale (ad esempio, in risposta al messaggio WM \_ Destroy nella procedura della finestra principale). Per annullare la guida, un'applicazione deve chiamare **WinHelp** solo una volta, indipendentemente dal numero di file della Guida aperti. La Guida di Windows rimane in esecuzione fino a quando non viene annullata la guida.

Per chiudere l'istanza della scheda di training della Guida di Windows, è necessario specificare sia la Guida \_ TCARD che la Guida \_ Quit quando si chiama [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa). Non è necessario che un'applicazione annulli l'istanza della carta di formazione della Guida di Windows se l'utente annulla prima l'operazione. La Guida di Windows notifica a un'applicazione quando l'utente annulla l'istanza della carta di training inviando il messaggio [**WM \_ TCARD**](wm-tcard.md) con il parametro *wParam* impostato su IDCLOSE.

## <a name="using-help"></a>Uso della Guida

In questa sezione viene illustrato come fornire la Guida sensibile al contesto per una finestra di dialogo e come impostare l'aspetto di una finestra della guida secondaria.

-   [Fornire la Guida in una finestra di dialogo](#providing-help-in-a-dialog-box)
-   [Impostazione dell'aspetto di una finestra della guida secondaria](#setting-the-appearance-of-a-secondary-help-window)

### <a name="providing-help-in-a-dialog-box"></a>Fornire la Guida in una finestra di dialogo

Per fornire la Guida sensibile al contesto in una finestra di dialogo, è necessario creare una matrice costituita da coppie di valori **DWORD** . Il primo valore in ogni coppia è l'identificatore di un controllo nella finestra di dialogo e il secondo è l'identificatore di contesto dell'argomento della Guida per il controllo. La matrice deve contenere una coppia di identificatori per ogni controllo nella finestra di dialogo.

La routine della finestra di dialogo deve elaborare i messaggi della [**\_ Guida WM**](wm-help.md) e del [**\_ ContextMenu di WM**](../menurc/wm-contextmenu.md) . La procedura della finestra di dialogo riceve la **\_ Guida di WM** quando l'utente preme il tasto e il file di conferma di **WM \_** quando l'utente fa clic con il pulsante destro del mouse.

Il parametro *lParam* della [**\_ Guida di WM**](wm-help.md) contiene l'indirizzo di una struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) . Il membro **hItemHandle** della struttura identifica il controllo per il quale l'utente ha richiesto la guida. È necessario passare questo handle alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) insieme al \_ comando Guida WM \_ , il nome del file della guida e un puntatore alla matrice di identificatori. La funzione **WinHelp** Cerca nella matrice l'identificatore di controllo del controllo specificato e quindi recupera l'identificatore di contesto della Guida corrispondente. Successivamente, la funzione passa l'identificatore di contesto della Guida alla guida di Windows, che trova l'argomento corrispondente e lo Visualizza in una finestra popup. Se il controllo ha un identificatore pari a-1, il sistema cerca il controllo successivo che rappresenta una tabulazione, quindi usa il relativo identificatore per trovare l'identificatore di contesto della guida. Per questo motivo, è importante inserire testo statico prima dei controlli in un file di risorse.

Quando si chiama la funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) , l'elaborazione di [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md) è simile all'elaborazione della [**\_ Guida di WM**](wm-help.md) con queste due eccezioni:

-   Il parametro *wParam* viene passato da [**WM \_ ContextMenu**](../menurc/wm-contextmenu.md), che è l'handle per il controllo che ha inviato il messaggio.
-   Specificare il comando **Help \_ ContextMenu** anziché la Guida **di \_ WM \_**.

Il comando **Help \_ ContextMenu** fa sì che la Guida di Windows visualizzi un menu prima di visualizzare l'argomento della guida. Il menu è definito dal sistema. Consente all'utente di visualizzare la guida per il controllo o di visualizzare la finestra di dialogo **argomenti della Guida** .

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



### <a name="setting-the-appearance-of-a-secondary-help-window"></a>Impostazione dell'aspetto di una finestra della guida secondaria

Un'applicazione può impostare le dimensioni, la posizione e visualizzare lo stato di una finestra della guida secondaria passando il \_ comando help SETWINPOS e l'indirizzo di una struttura [**HELPWININFO**](/windows/win32/api/winuser/ns-winuser-helpwininfoa) alla funzione [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) . I membri di **HELPWININFO** specificano il nome della finestra da modificare e le nuove dimensioni, la posizione e lo stato di visualizzazione della finestra.

Nell'esempio seguente viene impostato l'aspetto di una finestra secondaria denominata "WND \_ menu". Il nome deve essere definito nella \[ sezione Windows \] del file di progetto della guida.


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



 

 
