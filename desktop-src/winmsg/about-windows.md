---
description: In questo argomento vengono descritti gli elementi di programmazione utilizzati dalle applicazioni per creare e utilizzare finestre. gestire le relazioni tra finestre; e dimensioni, spostamento e visualizzazione delle finestre.
ms.assetid: e325f8dc-004f-44a9-9122-3be5e44764d6
title: Informazioni su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b085ed246ef6f13627d678e3ede68fa6349a780a74c0c89ee7cbafb24c501f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849890"
---
# <a name="about-windows"></a>Informazioni su Windows

In questo argomento vengono descritti gli elementi di programmazione utilizzati dalle applicazioni per creare e utilizzare finestre. gestire le relazioni tra finestre; e dimensioni, spostamento e visualizzazione delle finestre.

La panoramica include gli argomenti seguenti.

-   [Finestra desktop](#desktop-window)
-   [Applicazione Windows](#application-windows)
    -   [Client Area](#client-area)
    -   [Area non client](#nonclient-area)
-   [Controlli e finestre di dialogo](#controls-and-dialog-boxes)
-   [Attributi della finestra](#window-attributes)
    -   [Nome della classe](#class-name)
    -   [Nome della finestra](#window-name)
    -   [Stile finestra](#window-style)
    -   [Stile finestra estesa](#extended-window-style)
    -   [Position](#position)
    -   [Dimensioni](#size)
    -   [Handle di finestra padre o proprietario](#parent-or-owner-window-handle)
    -   [Handle di menu o identificatore Child-Window menu](#menu-handle-or-child-window-identifier)
    -   [Handle dell'istanza dell'applicazione](#application-instance-handle)
    -   [Dati di creazione](#creation-data)
    -   [Handle finestra](#window-handle)
-   [Creazione di finestre](#creation-data)
    -   [Creazione della finestra principale](#main-window-creation)
    -   [Messaggi di creazione di finestre](#window-creation-messages)
    -   [Applicazioni multithread](#multithread-applications)

## <a name="desktop-window"></a>Finestra desktop

Quando si avvia il sistema, viene creata automaticamente la finestra del desktop. La *finestra desktop* è una finestra definita dal sistema che disegna lo sfondo dello schermo e funge da base per tutte le finestre visualizzate da tutte le applicazioni.

La finestra desktop usa una bitmap per disegnare lo sfondo dello schermo. Il modello creato dalla bitmap è denominato sfondo *del desktop.* Per impostazione predefinita, la finestra del desktop usa la bitmap di un file .bmp specificato nel Registro di sistema come sfondo del desktop.

La [**funzione GetDesktopWindow**](/windows/win32/api/winuser/nf-winuser-getdesktopwindow) restituisce un handle alla finestra del desktop.

Un'applicazione di configurazione di sistema, ad esempio un elemento Pannello di controllo, modifica lo sfondo del desktop usando la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il parametro *wAction* impostato su **SPI \_ SETDESKWALLPAPER** e il parametro *lpvParam* che specifica un nome di file bitmap. **SystemParametersInfo** carica quindi la bitmap dal file specificato, usa la bitmap per disegnare lo sfondo dello schermo e immette il nuovo nome file nel Registro di sistema.

## <a name="application-windows"></a>Applicazione Windows

Ogni applicazione basata Windows grafica crea almeno una finestra, denominata finestra *principale,* che funge da interfaccia principale tra l'utente e l'applicazione. La maggior parte delle applicazioni crea anche altre finestre, direttamente o indirettamente, per eseguire attività correlate alla finestra principale. Ogni finestra svolge un ruolo nella visualizzazione dell'output e nella ricezione dell'input da parte dell'utente.

Quando si avvia un'applicazione, il sistema associa anche un pulsante della barra delle applicazioni all'applicazione. Il pulsante *della barra delle applicazioni* contiene l'icona e il titolo del programma. Quando l'applicazione è attiva, il pulsante della barra delle applicazioni viene visualizzato nello stato premuto.

Una finestra dell'applicazione include elementi come una barra del titolo, una barra dei menu, il menu della finestra (precedentemente noto come menu di sistema), il pulsante di riduzione a icona, il pulsante di ingrandimento, il pulsante di ripristino, il pulsante di chiusura, un bordo di ridimensionamento, un'area client, una barra di scorrimento orizzontale e una barra di scorrimento verticale. La finestra principale di un'applicazione include in genere tutti questi componenti. La figura seguente mostra questi componenti in una tipica finestra principale.

![finestra tipica](images/cswin-02.png)

### <a name="client-area"></a>Client Area

*L'area client* è la parte di una finestra in cui l'applicazione visualizza l'output, ad esempio testo o grafica. Ad esempio, un'applicazione di pubblicazione desktop visualizza la pagina corrente di un documento nell'area client. L'applicazione deve fornire una funzione, denominata routine della finestra, per elaborare l'input nella finestra e visualizzare l'output nell'area client. Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

### <a name="nonclient-area"></a>Area non client

La barra del titolo, la barra dei menu, il menu della finestra, i pulsanti riduci a icona e ingrandisci, il bordo di ridimensionamento e le barre di scorrimento vengono definiti collettivamente come *l'area non client della finestra.* Il sistema gestisce la maggior parte degli aspetti dell'area non client; l'applicazione gestisce l'aspetto e il comportamento della relativa area client.

La *barra del titolo* visualizza un'icona e una riga di testo definite dall'applicazione. In genere, il testo specifica il nome dell'applicazione o indica lo scopo della finestra. Un'applicazione specifica l'icona e il testo durante la creazione della finestra. La barra del titolo consente inoltre all'utente di spostare la finestra usando il mouse o un altro dispositivo di puntamento.

La maggior parte delle applicazioni *include una barra dei menu* che elenca i comandi supportati dall'applicazione. Gli elementi nella barra dei menu rappresentano le categorie principali di comandi. Facendo clic su una voce nella barra dei menu viene in genere aperto un menu a comparsa le cui voci corrispondono alle attività all'interno di una determinata categoria. Facendo clic su un comando, l'utente indica all'applicazione di eseguire un'attività.

Il *menu della* finestra viene creato e gestito dal sistema. Contiene un set standard di voci di menu che, se scelte dall'utente, impostano le dimensioni o la posizione di una finestra, chiudono l'applicazione o eseguono attività. Per altre informazioni, vedere [Menu.](/windows/desktop/menurc/menus)

I pulsanti nell'angolo superiore destro influiscono sulle dimensioni e sulla posizione della finestra. Quando si fa clic sul pulsante Ingrandisci *,* il sistema ingrandisce la finestra in base alle dimensioni dello schermo e posiziona la finestra, in modo da coprire l'intero desktop, senza la barra delle applicazioni. Allo stesso tempo, il sistema sostituisce il pulsante di ingrandimento con il pulsante di ripristino. Quando si fa clic *sul pulsante di* ripristino , il sistema ripristina le dimensioni e la posizione precedenti della finestra. Quando si fa clic sul pulsante Riduci a icona *,* il sistema riduce la finestra alle dimensioni del pulsante della barra delle applicazioni, posiziona la finestra sul pulsante della barra delle applicazioni e visualizza il pulsante della barra delle applicazioni nello stato normale. Per ripristinare le dimensioni e la posizione precedenti dell'applicazione, fare clic sul relativo pulsante della barra delle applicazioni. Quando si fa clic *sul pulsante Chiudi*, l'applicazione viene chiusa.

Il *bordo di ridimensionamento* è un'area intorno al perimetro della finestra che consente all'utente di ridimensionare la finestra usando un mouse o un altro dispositivo di puntamento.

La barra di  *scorrimento orizzontale* e la barra di scorrimento verticale convertono l'input del mouse o della tastiera in valori utilizzati da un'applicazione per spostare orizzontalmente o verticalmente il contenuto dell'area client. Ad esempio, un'applicazione di elaborazione di testo che visualizza un documento lungo fornisce in genere una barra di scorrimento verticale per consentire all'utente di scorrere il documento verso l'alto o verso il basso.

## <a name="controls-and-dialog-boxes"></a>Controlli e finestre di dialogo

Un'applicazione può creare diversi tipi di finestre oltre alla finestra principale, inclusi i controlli e le finestre di dialogo.

Un *controllo* è una finestra utilizzata da un'applicazione per ottenere informazioni specifiche dall'utente, ad esempio il nome di un file da aprire o le dimensioni in punti desiderate di una selezione di testo. Le applicazioni usano anche i controlli per ottenere le informazioni necessarie per controllare una particolare funzionalità di un'applicazione. Ad esempio, un'applicazione di elaborazione di testo fornisce in genere un controllo per consentire all'utente di attivare e disattivare il ritorno a capo automatico. Per altre informazioni, vedere Windows [controlli](/windows/desktop/Controls/window-controls).

I controlli vengono sempre usati insieme a un'altra finestra, in genere una finestra di dialogo. Una *finestra di dialogo* è una finestra che contiene uno o più controlli. Un'applicazione usa una finestra di dialogo per richiedere all'utente l'input necessario per completare un comando. Ad esempio, un'applicazione che include un comando per aprire un file visualizza una finestra di dialogo che include i controlli in cui l'utente specifica un percorso e un nome file. Le finestre di dialogo in genere non usano lo stesso set di componenti della finestra di una finestra principale. La maggior parte include una barra del titolo, un menu della finestra, un bordo (senza ridimensionamento) e un'area client, ma in genere non dispongono di una barra dei menu, di pulsanti di riduzione a icona e di ingrandimento o di barre di scorrimento. Per altre informazioni, vedere [Finestre di dialogo.](/windows/desktop/dlgbox/dialog-boxes)

Una *finestra di messaggio* è una finestra di dialogo speciale che visualizza una nota, un avviso o un avviso per l'utente. Ad esempio, una finestra di messaggio può informare l'utente di un problema riscontrato dall'applicazione durante l'esecuzione di un'attività. Per altre informazioni, vedere [Finestre di messaggio.](/windows/desktop/dlgbox/about-dialog-boxes)

## <a name="window-attributes"></a>Attributi della finestra

Quando si crea una finestra, un'applicazione deve fornire le informazioni seguenti. Ad eccezione dell'handle di [finestra](#window-handle), che la funzione di creazione restituisce per identificare in modo univoco la nuova finestra.

-   [Nome della classe](#class-name)
-   [Nome della finestra](#window-name)
-   [Stile finestra](#window-style)
-   [Stile finestra estesa](#extended-window-style)
-   [Position](#position)
-   [Dimensioni](#size)
-   [Handle di finestra padre o proprietario](#parent-or-owner-window-handle)
-   [Handle di menu o identificatore Child-Window menu](#menu-handle-or-child-window-identifier)
-   [Handle dell'istanza dell'applicazione](#application-instance-handle)
-   [Dati di creazione](#creation-data)
-   [Handle finestra](#window-handle)

Questi attributi della finestra sono descritti nelle sezioni seguenti.

### <a name="class-name"></a>Nome della classe

Ogni finestra appartiene a una classe finestra. Un'applicazione deve registrare una classe finestra prima di creare le finestre di tale classe. La *classe window* definisce la maggior parte degli aspetti dell'aspetto e del comportamento di una finestra. Il componente principale di una classe finestra è la routine *della* finestra , una funzione che riceve ed elabora tutti gli input e le richieste inviate alla finestra. Il sistema fornisce l'input e le richieste sotto forma di *messaggi*. Per altre informazioni, vedere [Classi finestra](window-classes.md), [Routine finestra](window-procedures.md)e Messaggi e Code [di messaggi](messages-and-message-queues.md).

### <a name="window-name"></a>Nome della finestra

Un *nome di finestra* è una stringa di testo che identifica una finestra per l'utente. Una finestra principale, una finestra di dialogo o una finestra di messaggio visualizza in genere il nome della finestra nella relativa barra del titolo, se presente. Un controllo può visualizzare il nome della finestra, a seconda della classe del controllo. Ad esempio, pulsanti, controlli di modifica e controlli statici visualizzano i nomi delle finestre all'interno del rettangolo occupato dal controllo . Tuttavia, i controlli, ad esempio caselle di riepilogo e caselle combinate, non visualizzano i relativi nomi di finestra.

Per modificare il nome della finestra dopo aver creato una finestra, usare la [**funzione SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) . Questa funzione usa le [**funzioni GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha) e [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) per recuperare la stringa del nome della finestra corrente dalla finestra.

### <a name="window-style"></a>Stile della finestra

Ogni finestra ha uno o più stili di finestra. Uno stile di finestra è una costante denominata che definisce un aspetto dell'aspetto e del comportamento della finestra non specificato dalla classe della finestra. Un'applicazione imposta in genere gli stili delle finestre durante la creazione di finestre. Può anche impostare gli stili dopo aver creato una finestra usando la [**funzione SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

Il sistema e, in una certa misura, la routine della finestra per la classe interpretano gli stili della finestra.

Alcuni stili di finestra si applicano a tutte le finestre, ma la maggior parte si applica alle finestre di classi di finestre specifiche. Gli stili di finestra generali sono rappresentati da costanti che iniziano con il prefisso WS. Possono essere combinati con l'operatore OR per formare diversi tipi di finestre, tra cui finestre principali, finestre di dialogo e finestre \_ figlio. Gli stili di finestra specifici della classe definiscono l'aspetto e il comportamento delle finestre appartenenti alle classi di controllo predefinite. Ad esempio, la classe **SCROLLBAR** specifica un controllo barra di scorrimento, ma gli stili [**SBS \_ HORZ**](../controls/scroll-bar-control-styles.md) e **SBS \_ VERT** determinano se viene creato un controllo barra di scorrimento orizzontale o verticale.

Per gli elenchi di stili che possono essere usati dalle finestre, vedere gli argomenti seguenti:

-   [**Stili finestra**](window-styles.md)
-   [Stili dei pulsanti](../controls/button-styles.md)
-   [Stili delle caselle combinate](../controls/combo-box-styles.md)
-   [Modificare gli stili dei controlli](../controls/edit-control-styles.md)
-   [Stili della casella di riepilogo](../controls/list-box-styles.md)
-   [Stili dei controlli Rich Edit](../controls/rich-edit-control-styles.md)
-   [Stili dei controlli Barra di scorrimento](../controls/scroll-bar-control-styles.md)
-   [Stili dei controlli statici](../controls/static-control-styles.md)

### <a name="extended-window-style"></a>Stile finestra estesa

Ogni finestra può avere facoltativamente uno o più stili di finestra estesi. Uno *stile di finestra esteso* è una costante denominata che definisce un aspetto dell'aspetto e del comportamento della finestra non specificato dalla classe della finestra o dagli altri stili della finestra. Un'applicazione imposta in genere gli stili di finestra estesi durante la creazione di finestre. Può anche impostare gli stili dopo aver creato una finestra usando la [**funzione SetWindowLong.**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)

Per altre informazioni, vedere [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

### <a name="position"></a>Posizione

La posizione di una finestra è definita come coordinate dell'angolo superiore sinistro. Queste coordinate, talvolta denominate coordinate della finestra, sono sempre relative all'angolo superiore sinistro dello schermo o, per una finestra figlio, all'angolo superiore sinistro dell'area client della finestra padre. Ad esempio, una finestra di primo livello con le coordinate (10,10) viene posizionata 10 pixel a destra dell'angolo superiore sinistro dello schermo e 10 pixel verso il basso. Una finestra figlio con le coordinate (10,10) viene posizionata a 10 pixel a destra dell'angolo superiore sinistro dell'area client della finestra padre e 10 pixel verso il basso.

La [**funzione WindowFromPoint**](/windows/win32/api/winuser/nf-winuser-windowfrompoint) recupera un handle per la finestra che occupa un punto specifico sullo schermo. Analogamente, le funzioni [**ChildWindowFromPoint**](/windows/win32/api/winuser/nf-winuser-childwindowfrompoint) e [**ChildWindowFromPointEx**](/windows/win32/api/winuser/nf-winuser-childwindowfrompointex) recuperano un handle per la finestra figlio che occupa un punto specifico nell'area client della finestra padre. Anche **se ChildWindowFromPointEx** può ignorare le finestre figlio invisibili, disabilitate e trasparenti, **ChildWindowFromPoint** non può.

### <a name="size"></a>Dimensione

Le dimensioni di una finestra (larghezza e altezza) sono specificate in pixel. Una finestra può avere larghezza o altezza pari a zero. Se un'applicazione imposta la larghezza e l'altezza di una finestra su zero, il sistema imposta le dimensioni sulla dimensione minima predefinita della finestra. Per individuare le dimensioni minime predefinite della finestra, un'applicazione usa la [**funzione GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con i flag **SM \_ CXMIN** e **SM \_ CYMIN.**

Un'applicazione potrebbe dover creare una finestra con un'area client di dimensioni specifiche. Le [**funzioni AdjustWindowRect**](/windows/win32/api/winuser/nf-winuser-adjustwindowrect) e [**AdjustWindowRectEx**](/windows/win32/api/winuser/nf-winuser-adjustwindowrectex) calcolano le dimensioni richieste di una finestra in base alle dimensioni desiderate dell'area client. L'applicazione può passare i valori delle dimensioni risultanti alla [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

Un'applicazione può ridimensionare una finestra in modo che sia estremamente grande. tuttavia, non deve ridimensionare una finestra in modo che sia più grande dello schermo. Prima di impostare le dimensioni di una finestra, l'applicazione deve controllare la larghezza e l'altezza dello schermo usando [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) con i flag **SM \_ CXSCREEN** e **SM \_ CYSCREEN.**

### <a name="parent-or-owner-window-handle"></a>Handle della finestra padre o proprietario

Una finestra può avere una finestra padre. Una finestra con un elemento padre è denominata *finestra figlio*. La *finestra padre* fornisce il sistema di coordinate utilizzato per il posizionamento di una finestra figlio. La presenza di una finestra padre influisce sugli aspetti dell'aspetto di una finestra; Ad esempio, una finestra figlio viene ritagliata in modo che nessuna parte della finestra figlio possa essere visualizzata all'esterno dei bordi della finestra padre.

Una finestra senza padre o il cui padre è la finestra desktop è denominata *finestra di primo livello.* Un'applicazione può usare [**la funzione EnumWindows**](/windows/win32/api/winuser/nf-winuser-enumwindows) per ottenere un handle per ogni finestra di primo livello sullo schermo. **EnumWindows** passa l'handle a ogni finestra di primo livello, a sua volta, a una funzione di callback definita dall'applicazione, [**EnumWindowsProc**](/previous-versions/windows/desktop/legacy/ms633498(v=vs.85)).

Una finestra di primo livello può essere proprietaria o di proprietà di un'altra finestra. Una *finestra di proprietà* viene sempre visualizzata davanti alla finestra proprietaria, viene nascosta quando la finestra proprietaria è ridotta a icona e viene distrutta quando la finestra proprietaria viene distrutta. Per altre informazioni, vedere [Proprietà Windows](window-features.md#owned-windows).

### <a name="menu-handle-or-child-window-identifier"></a>Handle di menu o identificatore Child-Window menu

Una finestra figlio può avere un *identificatore di finestra* figlio, un valore univoco definito dall'applicazione associato alla finestra figlio. Gli identificatori della finestra figlio sono particolarmente utili nelle applicazioni che creano più finestre figlio. Quando si crea una finestra figlio, un'applicazione specifica l'identificatore della finestra figlio. Dopo aver creato la finestra, l'applicazione può modificare l'identificatore della finestra usando la [**funzione SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) oppure recuperare l'identificatore usando la [**funzione GetWindowLong.**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)

Ogni finestra, ad eccezione di una finestra figlio, può avere un menu. Un'applicazione può includere un menu fornendo un handle di menu durante la registrazione della classe della finestra o durante la creazione della finestra.

### <a name="application-instance-handle"></a>Handle dell'istanza dell'applicazione

A ogni applicazione è associato un handle di istanza. Il sistema fornisce l'handle di istanza a un'applicazione all'avvio dell'applicazione. Poiché può eseguire più copie della stessa applicazione, il sistema usa internamente gli handle di istanza per distinguere un'istanza di un'applicazione da un'altra. L'applicazione deve specificare l'handle dell'istanza in molte finestre diverse, incluse quelle che creano finestre.

### <a name="creation-data"></a>Dati di creazione

A ogni finestra possono essere associati dati di creazione definiti dall'applicazione. Quando la finestra viene creata per la prima volta, il sistema passa un puntatore ai dati alla routine della finestra da creare. La routine della finestra usa i dati per inizializzare le variabili definite dall'applicazione.

### <a name="window-handle"></a>Handle finestra

Dopo aver creato una finestra, la funzione di creazione restituisce un *handle di finestra* che identifica in modo univoco la finestra. Un handle di finestra ha il tipo di dati **HWND.** Un'applicazione deve usare questo tipo quando dichiara una variabile che contiene un handle di finestra. Un'applicazione usa questo handle in altre funzioni per indirizzare le azioni alla finestra.

Un'applicazione può usare la [**funzione FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) per individuare se nel sistema è presente una finestra con il nome di classe o di finestra specificato. Se tale finestra esiste, **FindWindow** restituisce un handle per la finestra. Per limitare la ricerca alle finestre figlio di una determinata applicazione, usare la [**funzione FindWindowEx.**](/windows/win32/api/winuser/nf-winuser-findwindowexa)

La [**funzione IsWindow**](/windows/win32/api/winuser/nf-winuser-iswindow) determina se un handle di finestra identifica una finestra valida ed esistente. Esistono costanti speciali che possono sostituire un handle di finestra in determinate funzioni. Ad esempio, un'applicazione può usare **HWND \_ BROADCAST** nelle funzioni [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) e [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) o **HWND \_ DESKTOP** nella [**funzione MapWindowPoints.**](/windows/desktop/api/winuser/nf-winuser-mapwindowpoints)

## <a name="window-creation"></a>Creazione di finestre

Per creare finestre dell'applicazione, usare [**la funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) È necessario fornire le informazioni necessarie per definire gli attributi della finestra. **CreateWindowEx** ha un *parametro, dwExStyle*, che **CreateWindow** non ha; In caso contrario, le funzioni sono identiche. In realtà, **CreateWindow** chiama **semplicemente CreateWindowEx** con il *parametro dwExStyle* impostato su zero. Per questo motivo, il resto di questa panoramica fa riferimento solo a **CreateWindowEx.**

Questa sezione contiene i seguenti argomenti:

-   [Creazione della finestra principale](#main-window-creation)
-   [Messaggi di creazione della finestra](#window-creation-messages)
-   [Applicazioni multithread](#multithread-applications)

> [!Note]  
> Sono disponibili funzioni aggiuntive per la creazione di finestre per scopi speciali, ad esempio finestre di dialogo e finestre di messaggio. Per altre informazioni, vedere [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa), [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga)e [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).

 

### <a name="main-window-creation"></a>Creazione della finestra principale

Ogni Windows basata su windows deve avere [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) come funzione del punto di ingresso. **WinMain** esegue una serie di attività, tra cui la registrazione della classe della finestra per la finestra principale e la creazione della finestra principale. **WinMain** registra la classe della finestra principale chiamando la [**funzione RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) e crea la finestra principale chiamando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

La [**funzione WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) può anche limitare l'applicazione a una singola istanza. Creare un mutex denominato usando la [**funzione CreateMutex.**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa) Se [**GetLastError restituisce**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **ERROR ALREADY \_ \_ EXISTS**, esiste un'altra istanza dell'applicazione (ha creato il mutex) ed è necessario uscire **da WinMain**.

Dopo la creazione, il sistema non visualizza automaticamente la finestra principale. Un'applicazione deve invece usare la [**funzione ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) per visualizzare la finestra principale. Dopo aver creato la finestra principale, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) dell'applicazione chiama **ShowWindow**, passando due parametri: un handle alla finestra principale e un flag che specifica se la finestra principale deve essere ridotta a icona o ingrandita quando viene visualizzata per la prima volta. In genere, il flag può essere impostato su una delle costanti che iniziano con il prefisso \_ SW. Tuttavia, quando **showWindow** viene chiamato per visualizzare la finestra principale dell'applicazione, il flag deve essere impostato su **SW \_ SHOWDEFAULT**. Questo flag indica al sistema di visualizzare la finestra come indicato dal programma che ha avviato l'applicazione.

Se una classe finestra è stata registrata con la versione Unicode di [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa), la finestra riceve solo messaggi Unicode. Per determinare se una finestra usa o meno il set di caratteri Unicode, chiamare [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode).

### <a name="window-creation-messages"></a>Window-Creation messaggi

Quando si crea una finestra, il sistema invia messaggi alla routine della finestra per la finestra. Il sistema invia il [**messaggio WM \_ NCCREATE**](wm-nccreate.md) dopo aver creato l'area non client della finestra e il messaggio [**WM \_ CREATE**](wm-create.md) dopo la creazione dell'area client. La routine della finestra riceve entrambi i messaggi prima che il sistema visualizzi la finestra. Entrambi i messaggi includono un puntatore a [**una struttura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) che contiene tutte le informazioni specificate nella [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) In genere, la routine della finestra esegue attività di inizializzazione alla ricezione di questi messaggi.

Quando si crea una finestra figlio, il sistema invia il messaggio [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) alla finestra padre dopo l'invio dei messaggi [**WM \_ NCCREATE**](wm-nccreate.md) [**e WM \_ CREATE.**](wm-create.md) Invia anche altri messaggi durante la creazione di una finestra. Il numero e l'ordine di questi messaggi dipendono dalla classe e stile della finestra e dalla funzione usata per creare la finestra. Questi messaggi sono descritti in altri argomenti di questo file della Guida.

### <a name="multithread-applications"></a>Applicazioni multithread

Un Windows'applicazione basata su più thread può avere più thread di esecuzione e ogni thread può creare finestre. Il thread che crea una finestra deve contenere il codice per la routine della finestra.

Un'applicazione può usare [**la funzione EnumThreadWindows**](/windows/win32/api/winuser/nf-winuser-enumthreadwindows) per enumerare le finestre create da un thread specifico. Questa funzione passa l'handle a ogni finestra del thread, a sua volta, a una funzione di callback definita dall'applicazione, [**EnumThreadWndProc**](/previous-versions/windows/desktop/legacy/ms633496(v=vs.85)).

La [**funzione GetWindowThreadProcessId**](/windows/win32/api/winuser/nf-winuser-getwindowthreadprocessid) restituisce l'identificatore del thread che ha creato una determinata finestra.

Per impostare lo stato di visualizzazione di una finestra creata da un altro thread, usare la [**funzione ShowWindowAsync.**](/windows/win32/api/winuser/nf-winuser-showwindowasync)

 

 
