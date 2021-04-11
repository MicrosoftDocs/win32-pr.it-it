---
description: In questo argomento vengono descritti gli elementi di programmazione utilizzati dalle applicazioni per creare e utilizzare Windows; gestire le relazioni tra le finestre; e le finestre di ridimensionamento, spostamento e visualizzazione.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Informazioni su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2df510deea689d70bd1ebf5e59cafc92b0389d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231586"
---
# <a name="about-windows"></a>Informazioni su Windows

In questo argomento vengono descritti gli elementi di programmazione utilizzati dalle applicazioni per creare e utilizzare Windows; gestire le relazioni tra le finestre; e le finestre di ridimensionamento, spostamento e visualizzazione.

La panoramica include gli argomenti seguenti.

-   [Finestra del desktop](#desktop-window)
-   [Finestre delle applicazioni](#application-windows)
    -   [Area client](#client-area)
    -   [Area non client](#nonclient-area)
-   [Controlli e finestre di dialogo](#controls-and-dialog-boxes)
-   [Attributi finestra](#window-attributes)
    -   [Nome della classe](#class-name)
    -   [Nome della finestra](#window-name)
    -   [Stile finestra](#window-style)
    -   [Stile finestra estesa](#extended-window-style)
    -   [Position](#position)
    -   [Dimensioni](#size)
    -   [Handle della finestra padre o proprietario](#parent-or-owner-window-handle)
    -   [Handle di menu o identificatore Child-Window](#menu-handle-or-child-window-identifier)
    -   [Handle dell'istanza dell'applicazione](#application-instance-handle)
    -   [Dati di creazione](#creation-data)
    -   [Handle finestra](#window-handle)
-   [Creazione finestra](#creation-data)
    -   [Creazione della finestra principale](#main-window-creation)
    -   [Messaggi di creazione finestra](#window-creation-messages)
    -   [Applicazioni multithread](#multithread-applications)

## <a name="desktop-window"></a>Finestra del desktop

Quando si avvia il sistema, viene creata automaticamente la finestra desktop. La *finestra del desktop* è una finestra definita dal sistema che dipinge lo sfondo dello schermo e funge da base per tutte le finestre visualizzate da tutte le applicazioni.

La finestra del desktop usa una bitmap per disegnare lo sfondo dello schermo. Il modello creato dalla bitmap è denominato sfondo del *Desktop*. Per impostazione predefinita, la finestra del desktop usa la bitmap da un file con estensione bmp specificato nel registro di sistema come sfondo del desktop.

La funzione [**GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) restituisce un handle per la finestra desktop.

Un'applicazione di configurazione di sistema, ad esempio un elemento del pannello di controllo, modifica lo sfondo del desktop usando la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il parametro *WAction* impostato su **SPI \_ SETDESKWALLPAPER** e il parametro *lpvParam* che specifica un nome di file bitmap. **SystemParametersInfo** carica quindi la bitmap dal file specificato, usa la bitmap per disegnare lo sfondo dello schermo e immette il nuovo nome del file nel registro di sistema.

## <a name="application-windows"></a>Finestre delle applicazioni

Ogni applicazione grafica basata su Windows crea almeno una finestra, denominata *finestra principale*, che funge da interfaccia primaria tra l'utente e l'applicazione. La maggior parte delle applicazioni crea anche altre finestre, direttamente o indirettamente, per eseguire attività correlate alla finestra principale. Ogni finestra svolge una parte della visualizzazione dell'output e della ricezione dell'input da parte dell'utente.

Quando si avvia un'applicazione, il sistema associa anche un pulsante della barra delle applicazioni all'applicazione. Il *pulsante della barra delle applicazioni* contiene l'icona e il titolo del programma. Quando l'applicazione è attiva, il pulsante della relativa barra delle applicazioni viene visualizzato nello stato push.

Una finestra dell'applicazione include elementi quali una barra del titolo, una barra dei menu, il menu della finestra (precedentemente noto come menu di sistema), il pulsante Riduci a icona, il pulsante Ingrandisci, il pulsante Ripristina, il pulsante Chiudi, un bordo di ridimensionamento, un'area client, una barra di scorrimento orizzontale e una barra di scorrimento verticale. La finestra principale di un'applicazione include in genere tutti questi componenti. Nella figura seguente vengono illustrati questi componenti in una tipica finestra principale.

![finestra tipica](images/cswin-02.png)

### <a name="client-area"></a>Area client

L' *area client* è la parte di una finestra in cui l'applicazione Visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop Visualizza la pagina corrente di un documento nell'area client. L'applicazione deve fornire una funzione, denominata routine della finestra, per elaborare l'input nella finestra e visualizzare l'output nell'area client. Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

### <a name="nonclient-area"></a>Area non client

La barra del titolo, la barra dei menu, il menu finestra, i pulsanti Riduci a icona e Ingrandisci, il bordo di ridimensionamento e le barre di scorrimento vengono definiti collettivamente come *area non client* della finestra. Il sistema gestisce la maggior parte degli aspetti dell'area non client; l'aspetto e il comportamento dell'area client vengono gestiti dall'applicazione.

La *barra del titolo* Visualizza un'icona e una riga di testo definite dall'applicazione; in genere, il testo specifica il nome dell'applicazione o indica lo scopo della finestra. Un'applicazione specifica l'icona e il testo quando si crea la finestra. La barra del titolo consente inoltre all'utente di spostare la finestra utilizzando un mouse o un altro dispositivo di puntamento.

La maggior parte delle applicazioni include una *barra dei menu* che elenca i comandi supportati dall'applicazione. Gli elementi nella barra dei menu rappresentano le categorie principali di comandi. Facendo clic su un elemento nella barra dei menu viene in genere aperto un menu popup i cui elementi corrispondono alle attività di una determinata categoria. Facendo clic su un comando, l'utente indirizza l'applicazione per eseguire un'attività.

Il *menu finestra* viene creato e gestito dal sistema. Contiene un set di voci di menu standard che, quando viene scelto dall'utente, imposta le dimensioni o la posizione di una finestra, chiude l'applicazione o esegue attività. Per ulteriori informazioni, vedere [menu](/windows/desktop/menurc/menus).

I pulsanti nell'angolo superiore destro influiscono sulle dimensioni e sulla posizione della finestra. Quando si fa clic sul *pulsante Ingrandisci*, il sistema ingrandisce la finestra fino alla dimensione dello schermo e posiziona la finestra, in modo da coprire l'intero desktop, meno la barra delle applicazioni. Allo stesso tempo, il sistema sostituisce il pulsante Ingrandisci con il pulsante Ripristina. Quando si fa clic sul *pulsante Ripristina*, il sistema ripristina le dimensioni e la posizione precedenti della finestra. Quando si fa clic sul pulsante *Riduci a icona*, il sistema riduce la finestra alla dimensione del pulsante della barra delle applicazioni, posiziona la finestra sul pulsante della barra delle applicazioni e visualizza il pulsante della barra delle applicazioni nello stato normale. Per ripristinare le dimensioni e la posizione precedenti dell'applicazione, fare clic sul pulsante della relativa barra delle applicazioni. Quando si fa clic sul *pulsante Chiudi*, l'applicazione viene chiusa.

Il *bordo di ridimensionamento* è un'area intorno al perimetro della finestra che consente all'utente di ridimensionare la finestra usando un mouse o un altro dispositivo di puntamento.

La *barra* di scorrimento orizzontale e la *barra di scorrimento verticale* convertono il mouse o l'input da tastiera in valori utilizzati da un'applicazione per spostare il contenuto dell'area client orizzontalmente o verticalmente. Ad esempio, un'applicazione per l'elaborazione di testi che visualizza un documento di lunga durata in genere fornisce una barra di scorrimento verticale per consentire all'utente di eseguire la pagina verso l'alto e verso il basso nel documento.

## <a name="controls-and-dialog-boxes"></a>Controlli e finestre di dialogo

Un'applicazione può creare diversi tipi di finestre oltre alla finestra principale, inclusi i controlli e le finestre di dialogo.

Un *controllo* è una finestra usata da un'applicazione per ottenere informazioni specifiche dall'utente, ad esempio il nome di un file da aprire o la dimensione del punto desiderata di una selezione di testo. Inoltre, le applicazioni utilizzano i controlli per ottenere le informazioni necessarie per controllare una particolare funzionalità di un'applicazione. Ad esempio, un'applicazione di elaborazione di testo in genere fornisce un controllo che consente all'utente di attivare e disattivare il ritorno a capo automatico. Per ulteriori informazioni, vedere [controlli Windows](/windows/desktop/Controls/window-controls).

I controlli vengono sempre utilizzati insieme a un'altra finestra, in genere una finestra di dialogo. Una finestra di *dialogo* è una finestra che contiene uno o più controlli. Un'applicazione usa una finestra di dialogo per richiedere all'utente l'input necessario per completare un comando. Ad esempio, un'applicazione che include un comando per aprire un file Visualizza una finestra di dialogo che include i controlli in cui l'utente specifica un percorso e un nome file. In genere, le finestre di dialogo non utilizzano lo stesso set di componenti della finestra della finestra principale. La maggior parte dispone di una barra del titolo, di un menu finestra, di un bordo (senza dimensioni) e di un'area client, ma in genere non dispongono di una barra dei menu, di Riduci a icona e Ingrandisci pulsanti o barre di scorrimento. Per ulteriori informazioni, vedere [finestre di dialogo](/windows/desktop/dlgbox/dialog-boxes).

Una finestra di *messaggio* è una finestra di dialogo speciale in cui viene visualizzata una nota, un'attenzione o un avviso per l'utente. Una finestra di messaggio può ad esempio informare l'utente di un problema riscontrato dall'applicazione durante l'esecuzione di un'attività. Per altre informazioni, vedere [finestre di messaggio](/windows/desktop/dlgbox/about-dialog-boxes).

## <a name="window-attributes"></a>Attributi finestra

Quando si crea una finestra, un'applicazione deve fornire le informazioni seguenti. (Ad eccezione dell'handle della [finestra](#window-handle), che la funzione di creazione restituisce per identificare in modo univoco la nuova finestra).

-   [Nome della classe](#class-name)
-   [Nome della finestra](#window-name)
-   [Stile finestra](#window-style)
-   [Stile finestra estesa](#extended-window-style)
-   [Position](#position)
-   [Dimensioni](#size)
-   [Handle della finestra padre o proprietario](#parent-or-owner-window-handle)
-   [Handle di menu o identificatore Child-Window](#menu-handle-or-child-window-identifier)
-   [Handle dell'istanza dell'applicazione](#application-instance-handle)
-   [Dati di creazione](#creation-data)
-   [Handle finestra](#window-handle)

Questi attributi della finestra sono descritti nelle sezioni seguenti.

### <a name="class-name"></a>Nome della classe

Ogni finestra appartiene a una classe di finestra. Un'applicazione deve registrare una classe della finestra prima di creare qualsiasi finestra di tale classe. La *classe Window* definisce la maggior parte degli aspetti dell'aspetto e del comportamento di una finestra. Il componente principale di una classe di finestra è la *routine della finestra*, una funzione che riceve ed elabora tutte le richieste di input e inviate alla finestra. Il sistema fornisce l'input e le richieste sotto forma di *messaggi*. Per ulteriori informazioni, vedere [classi della finestra](window-classes.md), [procedure di finestra](window-procedures.md)e [messaggi e code di messaggi](messages-and-message-queues.md).

### <a name="window-name"></a>Nome della finestra

Un *nome di finestra* è una stringa di testo che identifica una finestra per l'utente. Una finestra principale, una finestra di dialogo o una finestra di messaggio Visualizza in genere il nome della finestra nella relativa barra del titolo, se presente. Un controllo può visualizzare il nome della finestra, a seconda della classe del controllo. Ad esempio, i pulsanti, i controlli di modifica e i controlli statici visualizzano i nomi delle finestre all'interno del rettangolo occupato dal controllo. Tuttavia, i controlli, ad esempio caselle di riepilogo e caselle combinate, non visualizzano i rispettivi nomi di finestra.

Per modificare il nome della finestra dopo la creazione di una finestra, utilizzare la funzione [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Questa funzione usa le funzioni [**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) per recuperare la stringa del nome di finestra corrente dalla finestra.

### <a name="window-style"></a>Stile della finestra

Ogni finestra ha uno o più stili di finestra. Uno stile della finestra è una costante denominata che definisce un aspetto dell'aspetto e del comportamento della finestra non specificato dalla classe della finestra. In genere, un'applicazione imposta gli stili della finestra durante la creazione di finestre. Può inoltre impostare gli stili dopo la creazione di una finestra tramite la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Il sistema e, in qualche misura, la routine della finestra per la classe interpretano gli stili della finestra.

Alcuni stili di finestra si applicano a tutte le finestre, ma la maggior parte si applica a Windows di classi di finestra specifiche. Gli stili della finestra generale sono rappresentati da costanti che iniziano con il \_ prefisso WS; possono essere combinate con l'operatore OR per formare tipi diversi di finestre, incluse le finestre principali, le finestre di dialogo e le finestre figlio. Gli stili della finestra specifici della classe definiscono l'aspetto e il comportamento delle finestre appartenenti alle classi di controlli predefinite. La classe **ScrollBar** , ad esempio, specifica un controllo barra di scorrimento, ma gli stili [**SBS \_ orizzontalmente**](../controls/scroll-bar-control-styles.md) e **SBS \_ Vert** determinano se viene creato un controllo barra di scorrimento orizzontale o verticale.

Per gli elenchi di stili che possono essere usati da Windows, vedere gli argomenti seguenti:

-   [**Stili finestra**](window-styles.md)
-   [Stili dei pulsanti](../controls/button-styles.md)
-   [Stili casella combinata](../controls/combo-box-styles.md)
-   [Modificare gli stili del controllo](../controls/edit-control-styles.md)
-   [Stili casella di riepilogo](../controls/list-box-styles.md)
-   [Stili del controllo Rich Edit](../controls/rich-edit-control-styles.md)
-   [Stili del controllo barra di scorrimento](../controls/scroll-bar-control-styles.md)
-   [Stili del controllo statico](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Stile finestra estesa

Ogni finestra può facoltativamente avere uno o più stili finestra estesi. Uno *stile di finestra esteso* è una costante denominata che definisce un aspetto dell'aspetto e del comportamento della finestra che non viene specificato dalla classe Window o dagli altri stili della finestra. In genere, un'applicazione imposta gli stili della finestra estesa durante la creazione di finestre. Può inoltre impostare gli stili dopo la creazione di una finestra tramite la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) .

Per ulteriori informazioni, vedere [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa).

### <a name="position"></a>Posizione

La posizione di una finestra è definita come le coordinate dell'angolo superiore sinistro. Queste coordinate, talvolta denominate coordinate della finestra, sono sempre relative all'angolo superiore sinistro dello schermo oppure, per una finestra figlio, nell'angolo superiore sinistro dell'area client della finestra padre. Ad esempio, una finestra di primo livello con le coordinate (10, 10) viene posizionata 10 pixel a destra dell'angolo superiore sinistro dello schermo e 10 pixel per difetto. Una finestra figlio con le coordinate (10, 10) viene posizionata 10 pixel a destra dell'angolo superiore sinistro dell'area client della finestra padre e 10 pixel per difetto.

La funzione [**WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) recupera un handle per la finestra che occupa un particolare punto sullo schermo. Analogamente, le funzioni [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) e [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) recuperano un handle per la finestra figlio che occupa un particolare punto nell'area client della finestra padre. Sebbene **ChildWindowFromPointEx** possa ignorare le finestre figlio invisibili, disabilitate e trasparenti, **ChildWindowFromPoint** non può.

### <a name="size"></a>Dimensione

Le dimensioni di una finestra (larghezza e altezza) sono specificate in pixel. Una finestra può avere larghezza o altezza zero. Se un'applicazione imposta la larghezza e l'altezza di una finestra su zero, le dimensioni del sistema vengono impostate sulle dimensioni minime predefinite della finestra. Per individuare le dimensioni minime predefinite della finestra, un'applicazione utilizza la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con i flag **SM \_ CXMIN** e **SM \_ CYMIN** .

Per un'applicazione potrebbe essere necessario creare una finestra con un'area client di una determinata dimensione. Le funzioni [**AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) e [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) calcolano la dimensione richiesta di una finestra in base alle dimensioni desiderate dell'area client. L'applicazione può passare i valori di dimensione risultanti alla funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

Un'applicazione può ridimensionare una finestra in modo che sia molto grande; Tuttavia, non deve ridimensionare una finestra in modo che sia maggiore dello schermo. Prima di impostare le dimensioni di una finestra, l'applicazione deve controllare la larghezza e l'altezza dello schermo usando [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con i flag **SM \_ CXSCREEN** e **SM \_ CYSCREEN** .

### <a name="parent-or-owner-window-handle"></a>Handle della finestra padre o proprietario

Una finestra può avere una finestra padre. Una finestra con un elemento padre viene chiamata *finestra figlio*. La *finestra padre* fornisce il sistema di coordinate usato per il posizionamento di una finestra figlio. La presenza di una finestra padre influiscono sugli aspetti dell'aspetto di una finestra; ad esempio, una finestra figlio viene ritagliata in modo che nessuna parte della finestra figlio possa apparire all'esterno dei bordi della finestra padre.

Una finestra priva di padre o il cui padre è la finestra del desktop è detta finestra di *primo livello*. Un'applicazione può usare la funzione [**EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) per ottenere un handle per ogni finestra di primo livello sullo schermo. **EnumWindows** passa l'handle a ogni finestra di primo livello, a sua volta, a una funzione di callback definita dall'applicazione, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Una finestra di primo livello può essere proprietaria o essere di proprietà di un'altra finestra. Una *finestra di proprietà* viene sempre visualizzata davanti alla finestra proprietaria, viene nascosta quando la finestra proprietaria è ridotta a icona e viene distrutta quando la finestra proprietaria viene distrutta. Per ulteriori informazioni, vedere [finestre di proprietà](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Handle di menu o identificatore Child-Window

Una finestra figlio può avere un identificatore di *finestra figlio* , un valore univoco definito dall'applicazione associato alla finestra figlio. Gli identificatori della finestra figlio sono particolarmente utili nelle applicazioni che creano più finestre figlio. Quando si crea una finestra figlio, un'applicazione specifica l'identificatore della finestra figlio. Dopo aver creato la finestra, l'applicazione può modificare l'identificatore della finestra usando la funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) oppure può recuperare l'identificatore tramite la funzione [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) .

Ogni finestra, ad eccezione di una finestra figlio, può disporre di un menu. Un'applicazione può includere un menu fornendo un handle di menu quando si registra la classe della finestra o quando si crea la finestra.

### <a name="application-instance-handle"></a>Handle dell'istanza dell'applicazione

A ogni applicazione è associato un handle di istanza. Il sistema fornisce l'handle dell'istanza a un'applicazione all'avvio dell'applicazione. Poiché può eseguire più copie della stessa applicazione, il sistema utilizza internamente gli handle di istanza per distinguere un'istanza di un'applicazione da un'altra. L'applicazione deve specificare l'handle di istanza in molte finestre diverse, incluse quelle che creano Windows.

### <a name="creation-data"></a>Dati di creazione

A ogni finestra è possibile associare dati di creazione definiti dall'applicazione. Quando la finestra viene creata per la prima volta, il sistema passa un puntatore ai dati nella procedura della finestra creata. La routine della finestra usa i dati per inizializzare le variabili definite dall'applicazione.

### <a name="window-handle"></a>Handle finestra

Dopo la creazione di una finestra, la funzione di creazione restituisce un *handle di finestra* che identifica in modo univoco la finestra. Un handle di finestra ha il tipo di dati **HWND** . un'applicazione deve usare questo tipo quando dichiara una variabile che include un handle di finestra. Un'applicazione utilizza questo handle in altre funzioni per indirizzare le azioni alla finestra.

Un'applicazione può utilizzare la funzione [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) per individuare se nel sistema è presente una finestra con il nome della classe o il nome della finestra specificato. Se tale finestra esiste, **FindWindow** restituisce un handle per la finestra. Per limitare la ricerca alle finestre figlio di una particolare applicazione, usare la funzione [**FindWindowEx**](/windows/win32/api/winuser/nf-winuser-findwindowexa) .

La funzione [**unwindow**](/windows/win32/api/winuser/nf-winuser-iswindow) determina se un handle di finestra identifica una finestra valida esistente. Sono presenti costanti speciali che possono sostituire un handle di finestra in determinate funzioni. Ad esempio, un'applicazione può utilizzare **la \_ trasmissione HWND** nelle funzioni [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) o il **\_ Desktop HWND** nella funzione [**MapWindowPoints**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints) .

## <a name="window-creation"></a>Creazione finestra

Per creare finestre dell'applicazione, usare la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . È necessario fornire le informazioni necessarie per definire gli attributi della finestra. **CreateWindowEx** ha un parametro, *DwExStyle*, che **CreateWindow** non ha; in caso contrario, le funzioni sono identiche. Infatti, **CreateWindow** chiama semplicemente **CreateWindowEx** con il parametro *dwExStyle* impostato su zero. Per questo motivo, il resto di questa panoramica si riferisce solo a **CreateWindowEx**.

Questa sezione contiene i seguenti argomenti:

-   [Creazione della finestra principale](#main-window-creation)
-   [Messaggi di creazione finestra](#window-creation-messages)
-   [Applicazioni multithread](#multithread-applications)

> [!Note]  
> Sono disponibili funzioni aggiuntive per la creazione di finestre per scopi specifici, ad esempio finestre di dialogo e finestre di messaggio. Per ulteriori informazioni, vedere [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)e [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Creazione della finestra principale

Ogni applicazione basata su Windows deve avere [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) come funzione del punto di ingresso. **WinMain** esegue una serie di attività, tra cui la registrazione della classe della finestra principale e la creazione della finestra principale. **WinMain** registra la classe della finestra principale chiamando la funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) e crea la finestra principale chiamando la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

La funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) può anche limitare l'applicazione a una singola istanza. Creare un mutex denominato usando la funzione [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) . Se [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un errore, esiste **\_ \_ già** un'altra istanza dell'applicazione (ha creato il mutex) ed è necessario uscire da **WinMain**.

Il sistema non visualizza automaticamente la finestra principale dopo la creazione. un'applicazione deve invece usare la funzione [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) per visualizzare la finestra principale. Dopo la creazione della finestra principale, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) dell'applicazione chiama **ShowWindow**, passando due parametri: un handle alla finestra principale e un flag che specifica se la finestra principale deve essere ridotta a icona o ingrandita quando viene visualizzata per la prima volta. In genere, il flag può essere impostato su una qualsiasi delle costanti che iniziano con il \_ prefisso SW. Tuttavia, quando **ShowWindow** viene chiamato per visualizzare la finestra principale dell'applicazione, il flag deve essere impostato su **SW \_ SHOWDEFAULT**. Questo flag indica al sistema di visualizzare la finestra come indicato dal programma che ha avviato l'applicazione.

Se una classe di finestra è stata registrata con la versione Unicode di [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa), la finestra riceve solo i messaggi Unicode. Per determinare se una finestra utilizza o meno il set di caratteri Unicode, chiamare [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Messaggi di Window-Creation

Quando si crea una finestra, il sistema invia messaggi alla routine della finestra per la finestra. Il sistema invia il [**messaggio \_ NCCREATE di WM**](wm-nccreate.md) dopo aver creato l'area non client della finestra e il messaggio [**WM \_ create**](wm-create.md) dopo la creazione dell'area client. La routine della finestra riceve entrambi i messaggi prima che la finestra venga visualizzata dal sistema. Entrambi i messaggi includono un puntatore a una struttura [**struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) contenente tutte le informazioni specificate nella funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . In genere, la routine della finestra esegue le attività di inizializzazione alla ricezione di questi messaggi.

Quando si crea una finestra figlio, il sistema invia il messaggio [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) alla finestra padre dopo aver inviato i messaggi [**WM \_ NCCREATE**](wm-nccreate.md) e [**WM \_ create**](wm-create.md) . Invia anche altri messaggi durante la creazione di una finestra. Il numero e l'ordine di questi messaggi dipendono dalla classe e dallo stile della finestra e dalla funzione utilizzata per creare la finestra. Questi messaggi vengono descritti in altri argomenti di questo file della guida.

### <a name="multithread-applications"></a>Applicazioni multithread

Un'applicazione basata su Windows può disporre di più thread di esecuzione e ogni thread può creare finestre. Il thread che crea una finestra deve contenere il codice per la relativa routine della finestra.

Un'applicazione può usare la funzione [**EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) per enumerare le finestre create da un thread specifico. Questa funzione passa l'handle a ogni finestra del thread, a sua volta, a una funzione di callback definita dall'applicazione, [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

La funzione [**GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) restituisce l'identificatore del thread che ha creato una particolare finestra.

Per impostare lo stato di visualizzazione di una finestra creata da un altro thread, usare la funzione [**ShowWindowAsync**](/windows/win32/api/winuser/nf-winuser-showwindowasync) .

 

 
