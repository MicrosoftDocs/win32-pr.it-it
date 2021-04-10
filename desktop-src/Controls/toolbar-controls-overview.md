---
title: Informazioni sui controlli Toolbar
description: Una barra degli strumenti è un controllo che contiene uno o più pulsanti.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263d95b13ddee54561cf1b0bb9d003d5d34cdf8d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963481"
---
# <a name="about-toolbar-controls"></a>Informazioni sui controlli Toolbar

Una barra degli strumenti è un controllo che contiene uno o più pulsanti. Ogni pulsante, quando viene fatto clic da un utente, invia un messaggio di comando alla finestra padre. In genere, i pulsanti in una barra degli strumenti corrispondono agli elementi nel menu dell'applicazione e forniscono all'utente un ulteriore modo più diretto di accedere ai controlli di un'applicazione.

Lo screenshot seguente mostra una finestra che contiene una semplice barra degli strumenti per le operazioni sui file. L'applicazione ha abilitato gli stili di visualizzazione. Il pulsante Salva è "Hot" perché il cursore si trovava al passaggio del mouse al momento della cattura dello schermo. L'aspetto effettivo del controllo varia a seconda del sistema operativo e del tema selezionato dall'utente.

![Screenshot di una finestra con una barra degli strumenti a tre pulsanti; un pulsante è attivo](images/tb-withstyles.png)

Lo screenshot seguente mostra lo stesso controllo in un'applicazione compilata senza gli stili visivi abilitati.

![Screenshot di una finestra senza stili di visualizzazione: nessuno dei pulsanti sembra attivo](images/tb-wostyles.png)

Negli argomenti seguenti vengono illustrate le funzionalità da considerare durante la pianificazione di una barra degli strumenti. Per informazioni specifiche sull'implementazione e il codice di esempio, vedere [uso dei controlli della barra degli strumenti](using-toolbar-controls.md).

-   [Impostazione delle dimensioni e della posizione della barra degli strumenti](#specifying-toolbar-size-and-position)
-   [Barre degli strumenti trasparenti](#transparent-toolbars)
-   [Barre degli strumenti di tipo elenco](#list-style-toolbars)
-   [Definizione di immagini di pulsanti](#defining-button-images)
    -   [Definizione delle immagini dei pulsanti tramite bitmap](#defining-button-images-by-using-bitmaps)
    -   [Definizione delle immagini dei pulsanti tramite elenchi di immagini](#defining-button-images-by-using-image-lists)
-   [Definizione del testo per i pulsanti](#defining-text-for-buttons)
-   [Aggiunta di pulsanti della barra degli strumenti](#adding-toolbar-buttons)
    -   [Stili del pulsante della barra degli strumenti](#toolbar-button-styles)
    -   [Stati del pulsante della barra degli strumenti](#toolbar-button-states)
    -   [Identificatore comando](#command-identifier)
    -   [Dimensioni e posizione del pulsante](#button-size-and-position)
-   [Abilitazione della personalizzazione](#enabling-customization)
-   [Abilitazione del rilevamento a caldo](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Impostazione delle dimensioni e della posizione della barra degli strumenti

Se si crea una barra degli strumenti usando [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), la funzione consente di specificare in pixel l'altezza e la larghezza della barra degli strumenti.

> [!Note]  
> L'uso di [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) non è consigliato, in quanto non supporta le nuove funzionalità delle barre degli strumenti, inclusi gli elenchi di immagini. Per ulteriori informazioni sulla creazione di barre degli strumenti, vedere [utilizzo dei controlli della barra degli strumenti](using-toolbar-controls.md).

 

La funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non dispone di parametri per specificare le dimensioni della barra degli strumenti. La routine della finestra della barra degli strumenti imposta automaticamente le dimensioni e la posizione della finestra della barra degli strumenti. L'altezza è basata sull'altezza dei pulsanti nella barra degli strumenti. La larghezza corrisponde alla larghezza dell'area client della finestra padre. Per modificare le impostazioni di ridimensionamento automatico, inviare un messaggio [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) . Gli stili dei controlli comuni in [**\_ alto**](common-control-styles.md) e [**CCS in \_ basso**](common-control-styles.md) di CCS determinano se la barra degli strumenti è posizionata lungo la parte superiore o inferiore dell'area client. Per impostazione predefinita, una barra degli strumenti ha lo stile **\_ principale CCS** .

Inoltre, la routine della finestra della barra degli strumenti regola automaticamente le dimensioni della barra degli strumenti ogni volta che viene ricevuta una [**\_ dimensione WM**](/windows/desktop/winmsg/wm-size) o un messaggio di [**\_ ridimensionamento automatico TB**](tb-autosize.md) . Un'applicazione deve inviare uno di questi messaggi ogni volta che viene modificata la dimensione della finestra padre o dopo l'invio di un messaggio che richiede la regolazione della dimensione della barra degli strumenti, ad esempio un messaggio [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) .

I comportamenti di ridimensionamento e posizionamento predefiniti della barra degli strumenti possono essere disattivati impostando gli stili dei controlli comuni di [**CCS \_ noresize**](common-control-styles.md) e [**CCS \_ NOPARENTALIGN**](common-control-styles.md) . I controlli della barra degli strumenti ospitati dai controlli Rebar devono impostare questi stili perché il controllo Rebar ridimensiona e posiziona la barra degli strumenti.

## <a name="transparent-toolbars"></a>Barre degli strumenti trasparenti

I controlli Toolbar supportano un aspetto trasparente che consente di visualizzare l'area client sotto la barra degli strumenti. Sono disponibili due tipi di barre degli strumenti trasparenti, ovvero i pulsanti flat e quelli con pulsanti tridimensionali. Se si desidera che l'applicazione corrisponda all'interfaccia di Windows, utilizzare la barra degli strumenti dello stile trasparente bidimensionale.

Lo screenshot seguente mostra i due tipi di barre degli strumenti trasparenti, non usando gli stili di visualizzazione.

![Screenshot di due finestre con stili diversi delle barre degli strumenti, ma entrambe le barre degli strumenti sono trasparenti](images/toolbartrans.jpg)

Lo screenshot seguente mostra una barra degli strumenti trasparente come potrebbe apparire in Windows Vista, con gli stili di visualizzazione abilitati. Il colore di sfondo della finestra di dialogo è stato modificato per rendere la trasparenza più ovvia.

![Screenshot di una finestra di Windows Vista con una barra degli strumenti trasparente](images/tb-transparent.png)

Per creare una barra degli strumenti trasparente, è sufficiente aggiungere [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ trasparente**](toolbar-control-and-button-styles.md) al parametro dello stile della finestra di [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Se non si desidera che venga visualizzata una riga per indicare la parte inferiore della barra degli strumenti, non utilizzare lo stile della finestra del [**\_ bordo WS**](/windows/desktop/winmsg/window-styles) .

> [!Note]  
> Quando si utilizzano gli stili di visualizzazione, le barre degli strumenti possono essere flat per impostazione predefinita.

 

## <a name="list-style-toolbars"></a>Barre degli strumenti di tipo elenco

I pulsanti della barra degli strumenti consentono di visualizzare sia testo che bitmap. I pulsanti di una barra degli strumenti creata con lo stile dell' [**\_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) posizionano il testo a destra della bitmap anziché al suo interno.

Lo screenshot seguente mostra una barra degli strumenti con lo stile dell'elenco.

![Screenshot di una barra degli strumenti con testo a destra di ogni icona](images/tb-liststyle.png)

Per creare una barra degli strumenti con pulsanti flat, è possibile utilizzare lo stile della barra degli strumenti [**\_ elenco TBSTYLE**](toolbar-control-and-button-styles.md) in combinazione con lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) .

## <a name="defining-button-images"></a>Definizione di immagini di pulsanti

Esistono due modi per specificare le immagini per i pulsanti, da bitmap o da elenchi di immagini. Un'applicazione deve scegliere il metodo da usare. Non può usare entrambi i metodi con lo stesso controllo Toolbar. Si noti che la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) usa il metodo bitmap. Per creare il controllo Toolbar, le applicazioni che desiderano utilizzare il metodo Image List devono utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) .

### <a name="defining-button-images-by-using-bitmaps"></a>Definizione delle immagini dei pulsanti tramite bitmap

Ogni pulsante di una barra degli strumenti può includere un'immagine bitmap. Una barra degli strumenti usa un elenco interno per archiviare le informazioni necessarie per creare le immagini. Quando si chiama la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) , si specifica una bitmap a colori o monocromia che contiene le immagini iniziali e la barra degli strumenti aggiunge le informazioni all'elenco interno di immagini. È possibile aggiungere altre immagini in un secondo momento usando il messaggio [**TB \_ ADDBITMAP**](tb-addbitmap.md) .

Ogni immagine ha un indice in base zero. La prima immagine aggiunta all'elenco interno ha un indice pari a 0, la seconda immagine ha un indice 1 e così via. [**TB \_ ADDBITMAP**](tb-addbitmap.md) aggiunge immagini alla fine dell'elenco e restituisce l'indice della prima nuova immagine aggiunta. Per associare l'immagine a un pulsante, è necessario inviare un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) e specificare l'indice dell'immagine dopo aver aggiunto le bitmap all'elenco di immagini interno.

Windows presuppone che tutte le immagini bitmap di una barra degli strumenti abbiano le stesse dimensioni. Specificare le dimensioni quando si crea la barra degli strumenti usando [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex). Se si utilizza la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra degli strumenti, le dimensioni delle immagini vengono impostate sulle dimensioni predefinite di 16 per 15 pixel. È possibile utilizzare il messaggio [**TB \_ SETBITMAPSIZE**](tb-setbitmapsize.md) per modificare le dimensioni delle immagini bitmap, ma è necessario eseguire questa operazione prima di aggiungere immagini all'elenco interno.

### <a name="defining-button-images-by-using-image-lists"></a>Definizione delle immagini dei pulsanti tramite elenchi di immagini

È anche possibile archiviare le immagini dei pulsanti in un set di [elenchi di immagini](image-lists.md). Un elenco di immagini è una raccolta di immagini della stessa dimensione, a cui è possibile fare riferimento in base al relativo indice. Gli elenchi di immagini vengono usati per gestire grandi set di icone o bitmap. È possibile utilizzare fino a tre diversi elenchi di immagini per visualizzare i pulsanti in diversi Stati, come illustrato nella tabella seguente.



|          |                                                                                                                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normale   | Pulsanti nello stato predefinito.                                                                                                                                                              |
| Accesso frequente      | Pulsanti sotto il puntatore o premuti. Gli elementi sensibili sono supportati solo nei controlli della barra degli strumenti con stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) . |
| Disabled | Pulsanti disabilitati.                                                                                                                                                                   |



 

Dopo la distruzione della barra degli strumenti, le applicazioni devono liberare tutti gli elenchi di immagini creati.

## <a name="defining-text-for-buttons"></a>Definizione del testo per i pulsanti

Ogni pulsante può visualizzare una stringa oltre a un'immagine o anziché un'immagine. Una barra degli strumenti gestisce un elenco interno contenente tutte le stringhe disponibili per i pulsanti della barra degli strumenti. Per aggiungere stringhe all'elenco interno, è possibile usare il messaggio [**TB \_ ADDSTRING**](tb-addstring.md) , specificando l'indirizzo del buffer contenente le stringhe da aggiungere. Ogni stringa deve avere terminazione null e l'ultima stringa deve terminare con due caratteri null.

Ogni stringa ha un indice in base zero. La prima stringa aggiunta all'elenco interno di stringhe ha un indice pari a 0, la seconda stringa ha un indice 1 e così via. [**TB \_ ADDSTRING**](tb-addstring.md) aggiunge stringhe alla fine dell'elenco e restituisce l'indice della prima nuova stringa. Usare un indice di stringa per associare la stringa a un pulsante.

L'uso di [**TB \_ ADDSTRING**](tb-addstring.md) non è l'unico modo per aggiungere stringhe a una barra degli strumenti. È possibile visualizzare una stringa in un pulsante passando un puntatore di stringa **nel membro della** struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) passato a [**TB \_ ADDBUTTONS**](tb-addbuttons.md). Inoltre, è possibile utilizzare [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md) per assegnare testo a un pulsante della barra degli strumenti.

## <a name="adding-toolbar-buttons"></a>Aggiunta di pulsanti della barra degli strumenti

Se si utilizza la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) per creare una barra degli strumenti, è possibile aggiungere pulsanti alla barra degli strumenti compilando una matrice di strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) e specificando l'indirizzo della matrice nella chiamata di funzione. Tuttavia, la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non dispone di un parametro per il passaggio di una struttura **TBBUTTON** . **CreateWindowEx** crea una barra degli strumenti vuota che si compila inviando un messaggio [**TB \_ ADDBUTTONS**](tb-addbuttons.md) , specificando l'indirizzo di una struttura **TBBUTTON** .

Dopo la creazione di una barra degli strumenti, è possibile aggiungere i pulsanti inviando un messaggio [**TB \_ INSERTBUTTON**](tb-insertbutton.md) o [**TB \_ ADDBUTTONS**](tb-addbuttons.md) . Ogni pulsante è descritto da una struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) , che definisce gli attributi del pulsante, inclusi gli indici della relativa stringa e della bitmap, nonché il relativo stile, lo stato, l'identificatore di comando e il valore a 32 bit definito dall'applicazione.

> [!Note]  
> Se si usa la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra degli strumenti, è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) prima di aggiungere i pulsanti. Il messaggio passa la dimensione della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) alla barra degli strumenti.

 

### <a name="toolbar-button-styles"></a>Stili del pulsante della barra degli strumenti

Lo stile di un pulsante determina come viene visualizzato il pulsante e come risponde all'input dell'utente. Ad esempio, lo stile del [**\_ pulsante BTNS**](toolbar-control-and-button-styles.md) crea un pulsante della barra degli strumenti che si comporta come un pulsante di push standard. Un pulsante con lo stile [**di \_ Verifica BTNS**](toolbar-control-and-button-styles.md) è simile a un pulsante di push standard, ad eccezione del fatto che viene attivato o disattivato ogni volta che l'utente fa clic su di esso.

È possibile creare gruppi di pulsanti della barra degli strumenti che fungono da pulsanti di opzione usando il [**\_ gruppo BTNS**](toolbar-control-and-button-styles.md) o lo stile [**BTNS \_ CHECKGROUP**](toolbar-control-and-button-styles.md) . In questo modo un pulsante rimane premuto fino a quando l'utente non sceglie un altro pulsante nel gruppo. Un gruppo viene definito come raccolta contigua di pulsanti, tutti con lo **stile \_ gruppo BTNS** o **BTNS \_ CHECKGROUP** .

Lo stile [**BTNS \_ Sep**](toolbar-control-and-button-styles.md) crea un piccolo divario tra i pulsanti o disegna un etch tra i pulsanti sulle barre degli strumenti semplici. Un pulsante con lo stile **BTNS \_ Sep** non riceve l'input dell'utente.

Nella versione 5,80 dei controlli comuni sono stati introdotti alcuni nuovi stili di pulsanti della barra degli strumenti e sono stati rinominati alcuni degli stili precedenti. Tutti i flag di stile dei pulsanti iniziano ora con BTNS \_ XXX anziché TBSTYLE \_ xxx. Per un elenco e una discussione sugli stili dei pulsanti, vedere [stili di controllo e di pulsante della barra degli strumenti](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>Stati del pulsante della barra degli strumenti

Ogni pulsante di una barra degli strumenti ha uno stato. La barra degli strumenti Aggiorna lo stato di un pulsante in modo da riflettere le azioni dell'utente, ad esempio facendo clic sul pulsante. Lo stato indica se il pulsante è attualmente premuto o non premuto, abilitato o disabilitato, nascosto o visibile. Anche se un'applicazione imposta lo stato iniziale di un pulsante quando si aggiunge il pulsante alla barra degli strumenti, può modificare e recuperare lo stato inviando i messaggi di stato di [**TB \_ GetState**](tb-getstate.md) e [**TB \_**](tb-setstate.md) alla barra degli strumenti. Per un elenco degli Stati dei pulsanti della barra degli strumenti, vedere [Stati della barra degli strumenti](toolbar-button-states.md).

### <a name="command-identifier"></a>Identificatore comando

A ogni pulsante è associato un identificatore di comando definito dall'applicazione. Gli identificatori di pulsante vengono in genere definiti in un file di intestazione dell'applicazione. Ad esempio, un pulsante Incolla può essere definito come segue:


```
#define ID_PASTE 100
```



Quando l'utente seleziona un pulsante, la barra degli strumenti Invia alla finestra padre un [**\_ comando WM**](/windows/desktop/menurc/wm-command) o un messaggio di [**\_ notifica WM**](wm-notify.md) che include l'identificatore del comando del pulsante. La finestra padre esamina l'identificatore del comando ed esegue il comando associato al pulsante. Per informazioni su quando i controlli inviano i messaggi di **\_ comando WM** e quando inviano una **\_ notifica WM**, vedere la sezione Osservazioni della documentazione di [**WM \_ Notify**](wm-notify.md) .

### <a name="button-size-and-position"></a>Dimensioni e posizione del pulsante

Una barra degli strumenti tiene traccia dei pulsanti assegnando ogni pulsante a un indice di posizione. L'indice è in base zero; ovvero, il pulsante a sinistra ha un indice pari a 0, il pulsante avanti a destra ha un indice 1 e così via. Quando si inviano messaggi per recuperare informazioni sul pulsante o per impostare gli attributi del pulsante, un'applicazione deve specificare l'indice di un pulsante.

Una barra degli strumenti Aggiorna gli indici di posizione durante l'inserimento e la rimozione dei pulsanti. Un'applicazione può recuperare l'indice di posizione corrente di un pulsante usando il messaggio [**TB \_ COMMANDTOINDEX**](tb-commandtoindex.md) . Il messaggio specifica l'identificatore del comando di un pulsante e la finestra della barra degli strumenti usa l'identificatore per individuare il pulsante e restituire il relativo indice di posizione.

Tutti i pulsanti di una barra degli strumenti hanno le stesse dimensioni. Per la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) è necessario impostare la dimensione iniziale dei pulsanti quando si crea la barra degli strumenti. Quando si utilizza la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , le dimensioni iniziali vengono impostate sulle dimensioni predefinite di 24 per 22 pixel. È possibile utilizzare il messaggio [**TB \_ SETBUTTONSIZE**](tb-setbuttonsize.md) per modificare le dimensioni del pulsante, ma è necessario eseguire questa operazione prima di aggiungere pulsanti alla barra degli strumenti. Il messaggio [**TB \_ GETITEMRECT**](tb-getitemrect.md) recupera le dimensioni correnti dei pulsanti.

Quando si aggiunge una stringa più lunga di una stringa che attualmente si trova nella barra degli strumenti, la barra degli strumenti Reimposta automaticamente la larghezza dei pulsanti. La larghezza viene impostata in modo da contenere la stringa più estesa sulla barra degli strumenti.

## <a name="enabling-customization"></a>Abilitazione della personalizzazione

Una barra degli strumenti include funzionalità di personalizzazione predefinite che è possibile rendere disponibili all'utente assegnando alla barra degli strumenti lo stile di controllo comune [**\_ regolabile da CCS**](common-control-styles.md) . Le funzionalità di personalizzazione consentono all'utente di trascinare un pulsante in una nuova posizione o di rimuovere un pulsante trascinandolo dalla barra degli strumenti. L'utente può anche fare doppio clic sulla barra degli strumenti per visualizzare la finestra di dialogo Personalizza barra degli strumenti, che consente di aggiungere, eliminare e riordinare i pulsanti della barra degli strumenti. Per visualizzare la finestra di dialogo, utilizzare il messaggio di [**\_ personalizzazione TB**](tb-customize.md) . Un'applicazione determina se le funzionalità di personalizzazione sono disponibili all'utente e controlla l'ambito in cui l'utente può personalizzare la barra degli strumenti.

Come parte del processo di personalizzazione, le applicazioni devono spesso salvare e ripristinare lo stato di una barra degli strumenti. In molte applicazioni, ad esempio, lo stato della barra degli strumenti viene archiviato prima che l'utente inizi a personalizzare la barra degli strumenti nel caso in cui l'utente voglia ripristinare lo stato originale della barra degli strumenti. Il controllo Toolbar non mantiene automaticamente un record dello stato di prepersonalizzazione. Per eseguire il ripristino, è necessario che l'applicazione salvi lo stato della barra degli strumenti. Per ulteriori informazioni, vedere [utilizzo dei controlli della barra degli strumenti](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Abilitazione del rilevamento a caldo

Il rilevamento a caldo indica che quando il puntatore viene spostato su un elemento, l'aspetto del pulsante cambia. Quando gli stili di visualizzazione sono abilitati, le barre degli strumenti supportano il rilevamento a caldo per impostazione predefinita. In caso contrario, solo i controlli della barra degli strumenti creati con lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) supportano il rilevamento a caldo. È possibile usare altri stili di finestra in combinazione con **TBSTYLE \_ Flat** per produrre barre degli strumenti che consentono il rilevamento a caldo ma hanno un aspetto diverso da una barra degli strumenti piatta. Per ulteriori informazioni, vedere [utilizzo dei controlli della barra degli strumenti](using-toolbar-controls.md).

 

 