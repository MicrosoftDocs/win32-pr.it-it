---
title: Informazioni sui controlli barra degli strumenti
description: Una barra degli strumenti è un controllo che contiene uno o più pulsanti.
ms.assetid: b5a00a81-8d23-4844-8b0a-776e7cceced8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f615da972f14bb88c4915504c089dd6b40d9aca
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424151"
---
# <a name="about-toolbar-controls"></a>Informazioni sui controlli barra degli strumenti

Una barra degli strumenti è un controllo che contiene uno o più pulsanti. Ogni pulsante, quando viene selezionato da un utente, invia un messaggio di comando alla finestra padre. In genere, i pulsanti in una barra degli strumenti corrispondono agli elementi nel menu dell'applicazione e forniscono all'utente un ulteriore modo più diretto di accedere ai controlli di un'applicazione.

Lo screenshot seguente mostra una finestra che contiene una barra degli strumenti semplice per le operazioni sui file. L'applicazione ha abilitato gli stili di visualizzazione. Il pulsante Salva è "hot" perché il cursore era posizionato su di esso quando è stata ripresa la schermata. L'aspetto effettivo del controllo varia a seconda del sistema operativo e del tema selezionato dall'utente.

![screenshot di una finestra con una barra degli strumenti a tre pulsanti; un pulsante è a caldo](images/tb-withstyles.png)

La schermata seguente mostra lo stesso controllo in un'applicazione compilata senza gli stili di visualizzazione abilitati.

![Screenshot di una finestra senza stili di visualizzazione: nessuno dei pulsanti ha un aspetto caldo](images/tb-wostyles.png)

Negli argomenti seguenti vengono illustrate le funzionalità da considerare durante la pianificazione di una barra degli strumenti. Per informazioni specifiche sull'implementazione e sul codice di esempio, vedere [Uso dei controlli barra degli strumenti](using-toolbar-controls.md).

-   [Specifica delle dimensioni e della posizione della barra degli strumenti](#specifying-toolbar-size-and-position)
-   [Barre degli strumenti trasparenti](#transparent-toolbars)
-   [Barre degli strumenti in stile elenco](#list-style-toolbars)
-   [Definizione delle immagini dei pulsanti](#defining-button-images)
    -   [Definizione di immagini pulsante tramite bitmap](#defining-button-images-by-using-bitmaps)
    -   [Definizione di immagini pulsante tramite elenchi di immagini](#defining-button-images-by-using-image-lists)
-   [Definizione del testo per i pulsanti](#defining-text-for-buttons)
-   [Aggiunta di pulsanti della barra degli strumenti](#adding-toolbar-buttons)
    -   [Stili dei pulsanti della barra degli strumenti](#toolbar-button-styles)
    -   [Stati dei pulsanti della barra degli strumenti](#toolbar-button-states)
    -   [Identificatore del comando](#command-identifier)
    -   [Dimensioni e posizione dei pulsanti](#button-size-and-position)
-   [Abilitazione della personalizzazione](#enabling-customization)
-   [Abilitazione del rilevamento a caldo](#enabling-hot-tracking)

## <a name="specifying-toolbar-size-and-position"></a>Specifica delle dimensioni e della posizione della barra degli strumenti

Se si crea una barra degli strumenti usando [**CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex)la funzione consente di specificare in pixel l'altezza e la larghezza della barra degli strumenti.

> [!Note]  
> Non [**è consigliabile usare CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) perché non supporta nuove funzionalità delle barre degli strumenti, inclusi gli elenchi di immagini. Per altre informazioni sulla creazione di barre degli strumenti, vedere [Uso dei controlli barra degli strumenti.](using-toolbar-controls.md)

 

La [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non dispone di parametri per specificare le dimensioni della barra degli strumenti. La routine della finestra della barra degli strumenti imposta automaticamente le dimensioni e la posizione della finestra della barra degli strumenti. L'altezza è basata sull'altezza dei pulsanti nella barra degli strumenti. La larghezza corrisponde alla larghezza dell'area client della finestra padre. Per modificare le impostazioni delle dimensioni automatiche, inviare un [**messaggio \_ SETBUTTONSIZE da TB.**](tb-setbuttonsize.md) Gli stili di controllo comuni [**CCS \_ TOP**](common-control-styles.md) e [**CCS \_ BOTTOM**](common-control-styles.md) determinano se la barra degli strumenti è posizionata lungo la parte superiore o inferiore dell'area client. Per impostazione predefinita, una barra degli strumenti ha **lo stile \_ CCS TOP.**

Inoltre, la routine della finestra della barra degli strumenti regola automaticamente le dimensioni della barra degli strumenti ogni volta che riceve un messaggio [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size) o [**TB \_ AUTOSIZE.**](tb-autosize.md) Un'applicazione deve inviare uno di questi messaggi ogni volta che le dimensioni della finestra padre cambiano o dopo l'invio di un messaggio che richiede la modifica delle dimensioni della barra degli strumenti, ad esempio un messaggio [**\_ TB SETBUTTONSIZE.**](tb-setbuttonsize.md)

I comportamenti di ridimensionamento e posizionamento predefiniti della barra degli strumenti possono essere disattivati impostando gli stili di controllo comuni [**CCS \_ NORESIZE**](common-control-styles.md) e [**\_ CCS NOPARENTALIGN.**](common-control-styles.md) I controlli barra degli strumenti ospitati dai controlli rebar devono impostare questi stili perché il controllo rebar ridimensiona e posiziona la barra degli strumenti.

## <a name="transparent-toolbars"></a>Barre degli strumenti trasparenti

I controlli barra degli strumenti supportano un aspetto trasparente che consente la visualizzazione dell'area client sotto la barra degli strumenti. Esistono due tipi di barre degli strumenti trasparenti, una con pulsanti flat e una con pulsanti tridimensionali. Se si vuole che l'applicazione corrisponda all'interfaccia di Windows, usare la barra degli strumenti in stile trasparente semplice.

Lo screenshot seguente mostra i due tipi di barre degli strumenti trasparenti, non usando gli stili di visualizzazione.

![Screenshot di due finestre con stili diversi delle barre degli strumenti, ma entrambe le barre degli strumenti sono trasparenti](images/toolbartrans.jpg)

Lo screenshot seguente mostra una barra degli strumenti trasparente come potrebbe essere visualizzata in Windows Vista, con gli stili di visualizzazione abilitati. Il colore di sfondo della finestra di dialogo è stato modificato per rendere la trasparenza più ovvia.

![Screenshot di una finestra in Windows Vista con una barra degli strumenti trasparente](images/tb-transparent.png)

Per creare una barra degli strumenti trasparente, è necessario aggiungere [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ TRANSPARENT**](toolbar-control-and-button-styles.md) al parametro di stile della finestra [**di CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Se non si vuole che venga visualizzata una riga per indicare la parte inferiore della barra degli strumenti, non usare lo stile della finestra [**WS \_ BORDER.**](/windows/desktop/winmsg/window-styles)

> [!Note]  
> Quando si usano gli stili di visualizzazione, le barre degli strumenti possono essere flat per impostazione predefinita.

 

## <a name="list-style-toolbars"></a>Barre degli strumenti in stile elenco

I pulsanti della barra degli strumenti consentono di visualizzare sia testo che bitmap. I pulsanti di una barra degli strumenti creata con lo stile [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) posizionano il testo a destra della bitmap anziché sotto di essa.

Lo screenshot seguente mostra una barra degli strumenti con lo stile elenco.

![Screenshot di una barra degli strumenti con testo a destra di ogni icona](images/tb-liststyle.png)

È possibile usare lo stile della barra degli strumenti [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) in combinazione con lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) per creare una barra degli strumenti con pulsanti flat.

## <a name="defining-button-images"></a>Definizione delle immagini dei pulsanti

Esistono due modi per specificare le immagini per i pulsanti: per bitmap o per elenchi di immagini. Un'applicazione deve scegliere il metodo da usare. Non può usare entrambi i metodi con lo stesso controllo barra degli strumenti. Si noti che [**la funzione CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) usa il metodo bitmap. Le applicazioni che vogliono usare il metodo dell'elenco di immagini devono usare la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare il controllo barra degli strumenti.

### <a name="defining-button-images-by-using-bitmaps"></a>Definizione di immagini di pulsanti tramite bitmap

Ogni pulsante in una barra degli strumenti può includere un'immagine bitmap. Una barra degli strumenti usa un elenco interno per archiviare le informazioni necessarie per disegnare le immagini. Quando si chiama la [**funzione CreateToolbarEx,**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) si specifica una bitmap monocromatica o a colori che contiene le immagini iniziali e la barra degli strumenti aggiunge le informazioni all'elenco interno di immagini. È possibile aggiungere altre immagini in un secondo momento usando il [**\_ messaggio ADDBITMAP da TB.**](tb-addbitmap.md)

Ogni immagine ha un indice in base zero. La prima immagine aggiunta all'elenco interno ha un indice 0, la seconda immagine ha un indice 1 e così via. [**TB \_ ADDBITMAP aggiunge**](tb-addbitmap.md) immagini alla fine dell'elenco e restituisce l'indice della prima nuova immagine aggiunta. Per associare l'immagine a un pulsante, è necessario inviare un messaggio [**\_ ADDBUTTONS DA TB**](tb-addbuttons.md) e specificare l'indice dell'immagine dopo aver aggiunto bitmap all'elenco di immagini interno.

Windows presuppone che tutte le immagini bitmap di una barra degli strumenti siano delle stesse dimensioni. È possibile specificare le dimensioni quando si crea la barra degli strumenti usando [**CreateToolbarEx.**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) Se si usa la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra degli strumenti, le dimensioni delle immagini vengono impostate su dimensioni predefinite di 16 per 15 pixel. È possibile usare il messaggio [**\_ TB SETBITMAPSIZE**](tb-setbitmapsize.md) per modificare le dimensioni delle immagini bitmap, ma è necessario farlo prima di aggiungere immagini all'elenco interno.

### <a name="defining-button-images-by-using-image-lists"></a>Definizione di immagini pulsante tramite elenchi di immagini

È anche possibile archiviare le immagini dei pulsanti in un set [di elenchi di immagini.](image-lists.md) Un elenco di immagini è una raccolta di immagini delle stesse dimensioni, ognuna delle quali può essere indicata dal relativo indice. Gli elenchi di immagini vengono usati per gestire grandi set di icone o bitmap. È possibile usare fino a tre diversi elenchi di immagini per visualizzare i pulsanti in vari stati, come illustrato nella tabella seguente.



|  State        |  Descrizione                                                                                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Normale   | Pulsanti nello stato predefinito.                                                                                                                                                              |
| Accesso frequente      | Pulsanti sotto il puntatore o premuti. Gli elementi di tipo hot sono supportati solo nei controlli barra degli strumenti con [**stile TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md) |
| Disabled | Pulsanti disabilitati.                                                                                                                                                                   |



 

Dopo l'eliminazione della barra degli strumenti, le applicazioni devono liberare tutti gli elenchi di immagini creati.

## <a name="defining-text-for-buttons"></a>Definizione del testo per i pulsanti

Ogni pulsante può visualizzare una stringa oltre a o invece di un'immagine. Una barra degli strumenti mantiene un elenco interno che contiene tutte le stringhe disponibili per i pulsanti della barra degli strumenti. Per aggiungere stringhe all'elenco interno, usare il messaggio [**\_ TB ADDSTRING,**](tb-addstring.md) specificando l'indirizzo del buffer contenente le stringhe da aggiungere. Ogni stringa deve essere con terminazione Null e l'ultima stringa deve essere terminata con due caratteri Null.

Ogni stringa ha un indice in base zero. La prima stringa aggiunta all'elenco interno di stringhe ha un indice 0, la seconda ha un indice 1 e così via. [**TB \_ ADDSTRING**](tb-addstring.md) aggiunge stringhe alla fine dell'elenco e restituisce l'indice della prima nuova stringa. Usare l'indice di una stringa per associare la stringa a un pulsante.

[**L'uso \_ di TB ADDSTRING**](tb-addstring.md) non è l'unico modo per aggiungere stringhe a una barra degli strumenti. È possibile visualizzare una stringa in un pulsante passando un puntatore di stringa nel membro **iString** della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) passato a [**TB \_ ADDBUTTONS.**](tb-addbuttons.md) È anche possibile usare [**TB \_ SETBUTTONINFO per**](tb-setbuttoninfo.md) assegnare testo a un pulsante della barra degli strumenti.

## <a name="adding-toolbar-buttons"></a>Aggiunta di pulsanti della barra degli strumenti

Se si usa la funzione [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) per creare una barra degli strumenti, è possibile aggiungere pulsanti alla barra degli strumenti compilando una matrice di strutture [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) e specificando l'indirizzo della matrice nella chiamata di funzione. Tuttavia, la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) non ha un parametro per passare una **struttura TBBUTTON.** **CreateWindowEx crea** una barra degli strumenti vuota che si riempie inviando un messaggio [**\_ ADDBUTTONS DA TB,**](tb-addbuttons.md) specificando l'indirizzo di una **struttura TBBUTTON.**

Dopo aver creato una barra degli strumenti, è possibile aggiungere pulsanti inviando un messaggio [**\_ INSERTBUTTON**](tb-insertbutton.md) o [**\_ TB ADDBUTTONS.**](tb-addbuttons.md) Ogni pulsante è descritto da una struttura [**TBBUTTON,**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che definisce gli attributi del pulsante, inclusi gli indici della stringa e della bitmap, nonché lo stile, lo stato, l'identificatore del comando e il valore a 32 bit definito dall'applicazione.

> [!Note]  
> Se si usa la [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra degli strumenti, è necessario inviare il messaggio [**\_ BUTTONSTRUCTSIZE TB**](tb-buttonstructsize.md) prima di aggiungere eventuali pulsanti. Il messaggio passa la dimensione della struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) alla barra degli strumenti.

 

### <a name="toolbar-button-styles"></a>Stili dei pulsanti della barra degli strumenti

Lo stile di un pulsante determina come viene visualizzato il pulsante e come risponde all'input dell'utente. Ad esempio, lo [**stile PULSANTE \_ BTNS**](toolbar-control-and-button-styles.md) crea un pulsante della barra degli strumenti che si comporta come un pulsante di comando standard. Un pulsante con lo stile [**CHECK BTNS \_**](toolbar-control-and-button-styles.md) è simile a un pulsante push standard, ad eccezione del fatto che alterna gli stati premuto e non premuto ogni volta che l'utente fa clic su di esso.

È possibile creare gruppi di pulsanti della barra degli strumenti che fungono da pulsanti di opzione usando lo stile [**BTNS \_ GROUP**](toolbar-control-and-button-styles.md) o [**BTNS \_ CHECKGROUP.**](toolbar-control-and-button-styles.md) In questo modo un pulsante rimane premuto finché l'utente non sceglie un altro pulsante nel gruppo. Un gruppo è definito come una raccolta contigua di pulsanti, tutti con lo stile **BTNS \_ GROUP** **o BTNS \_ CHECKGROUP.**

Lo [**stile \_ SEP BTNS**](toolbar-control-and-button-styles.md) crea un piccolo spazio tra i pulsanti o disegna un'etch tra i pulsanti sulle barre degli strumenti flat. Un pulsante con lo **stile \_ BTNS SEP** non riceve l'input dell'utente.

La versione 5.80 dei controlli comuni ha introdotto alcuni nuovi stili dei pulsanti della barra degli strumenti e rinominato alcuni degli stili precedenti. Tutti i flag di stile dei pulsanti iniziano ora con BTNS \_ XXX anziché con TBSTYLE \_ XXX. Per un elenco e una descrizione degli stili dei pulsanti, vedere Controllo barra degli [strumenti e Stili dei pulsanti](toolbar-control-and-button-styles.md).

### <a name="toolbar-button-states"></a>Stati dei pulsanti della barra degli strumenti

Ogni pulsante in una barra degli strumenti ha uno stato. La barra degli strumenti aggiorna lo stato di un pulsante per riflettere le azioni dell'utente, ad esempio facendo clic sul pulsante. Lo stato indica se il pulsante è attualmente premuto o meno, abilitato o disabilitato, nascosto o visibile. Anche se un'applicazione imposta lo stato iniziale di un pulsante quando aggiunge il pulsante alla barra degli strumenti, può modificare e recuperare lo stato inviando messaggi [**\_ TB GETSTATE**](tb-getstate.md) e [**TB \_ SETSTATE**](tb-setstate.md) alla barra degli strumenti. Per un elenco degli stati dei pulsanti della barra degli strumenti, vedere [Stati della barra degli strumenti](toolbar-button-states.md).

### <a name="command-identifier"></a>Identificatore del comando

A ogni pulsante è associato un identificatore di comando definito dall'applicazione. Gli identificatori dei pulsanti sono in genere definiti in un file di intestazione dell'applicazione. Ad esempio, un pulsante Incolla può essere definito come:


```
#define ID_PASTE 100
```



Quando l'utente seleziona un pulsante, la barra degli strumenti invia alla finestra padre un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) o [**WM \_ NOTIFY**](wm-notify.md) che include l'identificatore del comando del pulsante. La finestra padre esamina l'identificatore del comando ed esegue il comando associato al pulsante. Per informazioni su quando i controlli inviano messaggi **WM \_ COMMAND** e quando inviano **WM \_ NOTIFY,** vedere la sezione Osservazioni della [**documentazione di WM \_ NOTIFY.**](wm-notify.md)

### <a name="button-size-and-position"></a>Dimensioni e posizione dei pulsanti

Una barra degli strumenti tiene traccia dei pulsanti assegnando a ogni pulsante un indice di posizione. L'indice è in base zero. ciò significa che il pulsante più a sinistra ha un indice 0, il pulsante successivo a destra ha un indice 1 e così via. Un'applicazione deve specificare l'indice di un pulsante durante l'invio di messaggi per recuperare informazioni sul pulsante o per impostare gli attributi del pulsante.

Una barra degli strumenti aggiorna gli indici di posizione quando i pulsanti vengono inseriti e rimossi. Un'applicazione può recuperare l'indice della posizione corrente di un pulsante usando il [**\_ messaggio COMMANDTOINDEX TB.**](tb-commandtoindex.md) Il messaggio specifica l'identificatore di comando di un pulsante e la finestra della barra degli strumenti usa l'identificatore per individuare il pulsante e restituirne l'indice di posizione.

Tutti i pulsanti in una barra degli strumenti hanno le stesse dimensioni. La [**funzione CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex) richiede di impostare le dimensioni iniziali dei pulsanti quando si crea la barra degli strumenti. Quando si usa la [**funzione CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) le dimensioni iniziali vengono impostate su dimensioni predefinite di 24 per 22 pixel. È possibile usare il [**messaggio \_ SETBUTTONSIZE tb**](tb-setbuttonsize.md) per modificare le dimensioni del pulsante, ma è necessario farlo prima di aggiungere pulsanti alla barra degli strumenti. Il [**messaggio \_ GETITEMRECT da**](tb-getitemrect.md) TB recupera le dimensioni correnti dei pulsanti.

Quando si aggiunge una stringa più lunga di qualsiasi stringa attualmente presente nella barra degli strumenti, la barra degli strumenti reimposta automaticamente la larghezza dei pulsanti. La larghezza è impostata in modo da contenere la stringa più lunga nella barra degli strumenti.

## <a name="enabling-customization"></a>Abilitazione della personalizzazione

Una barra degli strumenti include funzionalità di personalizzazione incorporate che è possibile rendere disponibili all'utente fornendo alla barra degli strumenti lo stile di controllo [**\_ comune CCS ADJUSTABLE.**](common-control-styles.md) Le funzionalità di personalizzazione consentono all'utente di trascinare un pulsante in una nuova posizione o di rimuovere un pulsante trascinandolo dalla barra degli strumenti. L'utente può anche fare doppio clic sulla barra degli strumenti per visualizzare la finestra di dialogo Personalizza barra degli strumenti, che consente di aggiungere, eliminare e riordinare i pulsanti della barra degli strumenti. Per visualizzare la finestra di dialogo, usare il [**messaggio TB \_ CUSTOMIZE.**](tb-customize.md) Un'applicazione determina se le funzionalità di personalizzazione sono disponibili all'utente e controlla l'ambito in cui l'utente può personalizzare la barra degli strumenti.

Come parte del processo di personalizzazione, le applicazioni spesso devono salvare e ripristinare lo stato di una barra degli strumenti. Ad esempio, molte applicazioni archiviano lo stato della barra degli strumenti prima che l'utente inizi a personalizzare la barra degli strumenti nel caso in cui in un secondo momento l'utente voglia ripristinare lo stato originale della barra degli strumenti. Il controllo barra degli strumenti non mantiene automaticamente un record dello stato di precustomizzazione. L'applicazione deve salvare lo stato della barra degli strumenti per ripristinarlo. Per altre informazioni, vedere Uso [dei controlli barra degli strumenti](using-toolbar-controls.md).

## <a name="enabling-hot-tracking"></a>Abilitazione del rilevamento a caldo

Il rilevamento a caldo significa che quando il puntatore si sposta su un elemento, l'aspetto del pulsante cambia. Quando gli stili di visualizzazione sono abilitati, le barre degli strumenti supportano il rilevamento attivo per impostazione predefinita. In caso contrario, solo i controlli barra degli strumenti creati con lo stile [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) supportano il rilevamento a caldo. È possibile usare altri stili di finestra in combinazione con **TBSTYLE \_ FLAT** per produrre barre degli strumenti che abilitano il rilevamento rapido ma hanno un aspetto diverso da una barra degli strumenti semplice. Per altre informazioni, vedere Uso [dei controlli barra degli strumenti](using-toolbar-controls.md).

 

 