---
description: A ogni classe finestra è associata una routine di finestra condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e ne controlla pertanto il comportamento e l'aspetto.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Informazioni sulle classi finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcb46d862bf5b9249bb4f13b111ac10c441c3e687dd3fb1784f355c40d14b72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932331"
---
# <a name="about-window-classes"></a>Informazioni sulle classi finestra

A ogni classe finestra è associata una routine di finestra condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e ne controlla pertanto il comportamento e l'aspetto. Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

Un processo deve registrare una classe finestra prima di poter creare una finestra di tale classe. La registrazione di una classe finestra associa una routine della finestra, gli stili di classe e altri attributi di classe a un nome di classe. Quando un processo specifica un nome di classe nella [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) il sistema crea una finestra con la routine della finestra, gli stili e altri attributi associati a tale nome di classe.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Tipi di classi finestra](#types-of-window-classes)
    -   [Classi di sistema](#system-classes)
    -   [Classi globali dell'applicazione](#application-global-classes)
    -   [Classi locali dell'applicazione](#application-local-classes)
-   [Individuazione di una classe window da parte del sistema](#how-the-system-locates-a-window-class)
-   [Registrazione di una classe Window](#registering-a-window-class)
-   [Elementi di una classe Window](#elements-of-a-window-class)
    -   [Nome della classe](#class-name)
    -   [Indirizzo della procedura della finestra](#window-procedure-address)
    -   [Handle istanza](#instance-handle)
    -   [Cursore di classe](#class-cursor)
    -   [Icone delle classi](#class-icons)
    -   [Pennello di sfondo della classe](#class-background-brush)
    -   [Menu Classe](#class-menu)
    -   [Stili classe](#class-styles)
    -   [Memoria aggiuntiva della classe](#extra-class-memory)
    -   [Memoria della finestra aggiuntiva](#extra-window-memory)

## <a name="types-of-window-classes"></a>Tipi di classi finestra

Esistono tre tipi di classi finestra:

-   [Classi di sistema](#system-classes)
-   [Classi globali dell'applicazione](#application-global-classes)
-   [Classi locali dell'applicazione](#application-local-classes)

Questi tipi differiscono per ambito e in quando e come vengono registrati ed distrutti.

### <a name="system-classes"></a>Classi di sistema

Una classe di sistema è una classe finestra registrata dal sistema. Molte classi di sistema sono disponibili per tutti i processi, mentre altre vengono usate solo internamente dal sistema. Poiché il sistema registra queste classi, un processo non può eliminarle.

Il sistema registra le classi di sistema per un processo la prima volta che uno dei relativi thread chiama una funzione User o Windows Graphics Device Interface (GDI).

Ogni applicazione riceve la propria copia delle classi di sistema. Tutte le applicazioni basate Windows a 16 bit nella stessa classe di sistema di condivisione VDM, esattamente come nelle applicazioni a 16 bit Windows.

Nella tabella seguente vengono descritte le classi di sistema disponibili per l'uso da parte di tutti i processi.



| Classe     | Descrizione                         |
|-----------|-------------------------------------|
| Button    | Classe per un pulsante.             |
| ComboBox  | Classe per una casella combinata.          |
| Modifica      | Classe per un controllo di modifica.      |
| ListBox   | Classe per una casella di riepilogo.           |
| Mdiclient | Classe per una finestra client MDI. |
| ScrollBar | Classe per una barra di scorrimento.         |
| Statica    | Classe per un controllo statico.     |



 

Nella tabella seguente vengono descritte le classi di sistema disponibili solo per l'uso da parte del sistema. Sono elencati qui per motivi di completezza.



| Classe      | Descrizione                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Classe per la casella di riepilogo contenuta in una casella combinata.                   |
| DDEMLEvent | Classe per gli eventi Dynamic Data Exchange Management Library (DDEML). |
| Message    | Classe per una finestra di solo messaggio.                                   |
| \#32768    | Classe per un menu.                                                  |
| \#32769    | Classe per la finestra del desktop.                                      |
| \#32770    | Classe per una finestra di dialogo.                                            |
| \#32771    | Classe per la finestra di cambio attività.                                  |
| \#32772    | Classe per i titoli delle icone.                                             |



 

### <a name="application-global-classes"></a>Classi globali dell'applicazione

Una [classe globale dell'applicazione](#application-global-classes) è una classe finestra registrata da un eseguibile o da una DLL disponibile per tutti gli altri moduli nel processo. Ad esempio, il .dll può chiamare la funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) per registrare una classe finestra che definisce un controllo personalizzato come classe globale dell'applicazione in modo che un processo che carica il .dll possa creare istanze del controllo personalizzato.

Per creare una classe che può essere usata in ogni processo, creare la classe window in un .dll e caricare il .dll in ogni processo. Per caricare il .dll in ogni processo, aggiungerne il nome al **valore APPInit \_ DLL nella** chiave del Registro di sistema seguente:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Ogni volta che un processo viene avviato, il sistema carica il .dll specificato nel contesto del processo appena avviato prima di chiamare la relativa funzione del punto di ingresso. Il .dll deve registrare la classe durante la procedura di inizializzazione e deve specificare lo **stile CS \_ GLOBALCLASS.** Per altre informazioni, vedere [Stili di classe](#class-styles).

Per rimuovere una classe globale dell'applicazione e liberare l'archiviazione associata, usare la [**funzione UnregisterClass.**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)

### <a name="application-local-classes"></a>Classi locali dell'applicazione

Una [classe locale dell'applicazione](#application-local-classes) è qualsiasi classe finestra che un eseguibile o .dll registra per l'utilizzo esclusivo. Anche se è possibile registrare un numero qualsiasi di classi locali, in genere ne viene registrato solo uno. Questa classe di finestra supporta la routine della finestra principale dell'applicazione.

Il sistema elimina una classe locale alla chiusura del modulo che la ha registrata. Un'applicazione può anche usare la [**funzione UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) per rimuovere una classe locale e liberare l'archiviazione associata.

## <a name="how-the-system-locates-a-window-class"></a>Individuazione di una classe window da parte del sistema

Il sistema gestisce un elenco di strutture per ognuno dei tre tipi di classi finestra. Quando un'applicazione chiama la [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) per creare una finestra con una classe specificata, il sistema usa la procedura seguente per individuare la classe.

1.  Cercare nell'elenco delle classi locali dell'applicazione una classe con il nome specificato il cui handle di istanza corrisponde all'handle di istanza del modulo. Diversi moduli possono usare lo stesso nome per registrare le classi locali nello stesso processo.
2.  Se il nome non è presente nell'elenco di classi locali dell'applicazione, cercare nell'elenco delle classi globali dell'applicazione.
3.  Se il nome non è presente nell'elenco delle classi globali dell'applicazione, cercare nell'elenco delle classi di sistema.

Tutte le finestre create dall'applicazione usano questa procedura, incluse le finestre create dal sistema per conto dell'applicazione, ad esempio le finestre di dialogo. È possibile eseguire l'override delle classi di sistema senza influire sulle altre applicazioni. Ciò significa che un'applicazione può registrare una classe locale dell'applicazione con lo stesso nome di una classe di sistema. Questa operazione sostituisce la classe di sistema nel contesto dell'applicazione, ma non impedisce ad altre applicazioni di usare la classe di sistema.

## <a name="registering-a-window-class"></a>Registrazione di una classe window

Una classe finestra definisce gli attributi di una finestra, ad esempio lo stile, l'icona, il cursore, il menu e la routine della finestra. Il primo passaggio per la registrazione di una classe di finestra consiste nel compilare una [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) con le informazioni sulla classe della finestra. Per altre informazioni, vedere [Elementi di una classe Window.](#elements-of-a-window-class) Passare quindi la struttura alla [**funzione RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Per altre informazioni, vedere [Uso delle classi di finestre.](using-window-classes.md)

Per registrare una classe globale dell'applicazione, specificare lo stile CS \_ GLOBALCLASS nel membro **style** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Quando si registra una classe locale dell'applicazione, non specificare lo **stile CS \_ GLOBALCLASS.**

Se si registra la classe della finestra usando la versione ANSI di [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, l'applicazione richiede che il sistema passi i parametri di testo dei messaggi alle finestre della classe creata usando il set di caratteri ANSI. Se si registra la classe usando la versione Unicode di **RegisterClassEx**, **RegisterClassExW**, l'applicazione richiede che il sistema passi i parametri di testo dei messaggi alle finestre della classe creata usando il set di caratteri Unicode. La [**funzione IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) consente alle applicazioni di eseguire query sulla natura di ogni finestra. Per altre informazioni sulle funzioni ANSI e Unicode, vedere [Convenzioni per i prototipi di funzione.](/windows/desktop/Intl/conventions-for-function-prototypes)

L'eseguibile o la DLL che ha registrato la classe è il proprietario della classe . Il sistema determina la proprietà della classe dal membro **hInstance** della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) passato alla [**funzione RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) quando la classe viene registrata. Per le DLL, il **membro hInstance** deve essere l'handle per l.dll istanza.

La classe non viene distrutta quando il .dll proprietario viene scaricato. Pertanto, se il sistema chiama la routine della finestra per una finestra di tale classe, si verifica una violazione di accesso, perché il .dll che contiene la routine della finestra non è più in memoria. Il processo deve eliminare tutte le finestre usando la classe prima che .dll venga scaricato e chiamare la [**funzione UnregisterClass.**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)

## <a name="elements-of-a-window-class"></a>Elementi di una classe Window

Gli elementi di una classe finestra definiscono il comportamento predefinito delle finestre appartenenti alla classe . L'applicazione che registra una classe finestra assegna elementi alla classe impostando i membri appropriati in una struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) e passando la struttura alla [**funzione RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) Le [**funzioni GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) e [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) recuperano informazioni su una determinata classe di finestra. La [**funzione SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) modifica gli elementi di una classe locale o globale già registrata dall'applicazione.

Anche se una classe di finestra completa è costituita da molti elementi, il sistema richiede solo che un'applicazione fornirà un nome di classe, l'indirizzo della routine della finestra e un handle di istanza. Usare gli altri elementi per definire gli attributi predefiniti per le finestre della classe , ad esempio la forma del cursore e il contenuto del menu per la finestra. È necessario inizializzare tutti i membri inutilizzati della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su zero o **NULL.** Gli elementi della classe window sono come illustrato nella tabella seguente.



| Elemento                                               | Scopo                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nome della classe](#class-name)                             | Distingue la classe dalle altre classi registrate.                                                                                                                                                                                        |
| [Indirizzo routine finestra](#window-procedure-address) | Puntatore alla funzione che elabora tutti i messaggi inviati alle finestre nella classe e definisce il comportamento della finestra.                                                                                                                      |
| [Handle istanza](#instance-handle)                   | Identifica l'applicazione o .dll che ha registrato la classe.                                                                                                                                                                                 |
| [Cursore di classe](#class-cursor)                         | Definisce il cursore del mouse visualizzato dal sistema per una finestra della classe .                                                                                                                                                                  |
| [Icone delle classi](#class-icons)                           | Definisce l'icona grande e l'icona piccola.                                                                                                                                                                                                    |
| [Pennello di sfondo della classe](#class-background-brush)     | Definisce il colore e il motivo che riempiono l'area client quando la finestra viene aperta o disegnata.                                                                                                                                                 |
| [Menu Classe](#class-menu)                             | Specifica il menu predefinito per le finestre che non definiscono in modo esplicito un menu.                                                                                                                                                                  |
| [Stili classe](#class-styles)                         | Definisce come aggiornare la finestra dopo lo spostamento o il ridimensionamento, come elaborare i doppio clic del mouse, come allocare spazio per il contesto di dispositivo e altri aspetti della finestra.                                                       |
| [Memoria aggiuntiva per le classi](#extra-class-memory)             | Specifica la quantità di memoria aggiuntiva, in byte, che il sistema deve riservare per la classe . Tutte le finestre nella classe condividono la memoria aggiuntiva e possono usarla per qualsiasi scopo definito dall'applicazione. Il sistema inizializza questa memoria su zero. |
| [Memoria aggiuntiva della finestra](#extra-window-memory)           | Specifica la quantità di memoria aggiuntiva, in byte, che il sistema deve riservare per ogni finestra appartenente alla classe . La memoria aggiuntiva può essere usata per qualsiasi scopo definito dall'applicazione. Il sistema inizializza questa memoria su zero.          |



 

### <a name="class-name"></a>Nome della classe

Ogni classe di finestra richiede un [nome di classe per](#class-name) distinguere una classe da un'altra. Assegnare un nome di classe impostando il membro **lpszClassName** della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sull'indirizzo di una stringa con terminazione Null che specifica il nome. Poiché le classi finestra sono specifiche del processo, i nomi delle classi di finestra devono essere univoci solo all'interno dello stesso processo. Inoltre, poiché i nomi delle classi occupano spazio nella tabella atom privata del sistema, è consigliabile mantenere le stringhe dei nomi di classe il più brevi possibile.

La [**funzione GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) recupera il nome della classe a cui appartiene una determinata finestra.

### <a name="window-procedure-address"></a>Indirizzo routine finestra

Ogni classe necessita di un indirizzo di routine della finestra per definire il punto di ingresso della routine della finestra usata per elaborare tutti i messaggi per le finestre nella classe. Il sistema passa i messaggi alla procedura quando richiede alla finestra di eseguire attività, ad esempio disegnare la propria area client o rispondere all'input dell'utente. Un processo assegna una routine della finestra a una classe copiandone l'indirizzo nel membro **lpfnWndProc** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

### <a name="instance-handle"></a>Handle istanza

Ogni classe di finestra richiede un handle di istanza per identificare l'applicazione o .dll che ha registrato la classe. Il sistema richiede che gli handle di istanza tengano traccia di tutti i moduli. Il sistema assegna un handle a ogni copia di un eseguibile in esecuzione o di .dll.

Il sistema passa un handle di istanza alla funzione del punto di ingresso di ogni eseguibile (vedere [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) e .dll (vedere [**DllMain).**](/windows/desktop/Dlls/dllmain) L'eseguibile .dll assegna questo handle di istanza alla classe copiarlo nel membro **hInstance** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

### <a name="class-cursor"></a>Cursore di classe

Il *cursore* della classe definisce la forma del cursore quando si trova nell'area client di una finestra nella classe . Il sistema imposta automaticamente il cursore sulla forma specificata quando il cursore entra nell'area client della finestra e assicura che manteni tale forma mentre rimane nell'area client. Per assegnare una forma del cursore a una classe finestra, caricare una forma di cursore predefinita usando la funzione [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) e quindi assegnare l'handle di cursore restituito al membro **hCursor** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) In alternativa, specificare una risorsa cursore personalizzata e usare la **funzione LoadCursor** per caricarla dalle risorse dell'applicazione.

Il sistema non richiede un cursore di classe. Se un'applicazione imposta **il membro hCursor** della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **NULL,** non viene definito alcun cursore di classe. Il sistema presuppone che la finestra imposta la forma del cursore ogni volta che il cursore viene spostato nella finestra. Una finestra può impostare la forma del cursore chiamando la [**funzione SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) ogni volta che la finestra riceve il [**messaggio WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove) Per altre informazioni sui cursori, vedere [Cursori](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Icone delle classi

*Un'icona* di classe è un'immagine che il sistema usa per rappresentare una finestra di una classe specifica. Un'applicazione può avere due icone di classe, una grande e una piccola. Il sistema visualizza l'icona della classe di grandi dimensioni di una finestra nella finestra di cambio attività visualizzata quando l'utente preme ALT+TAB e nelle visualizzazioni icone grandi della barra delle applicazioni e di Esplora risorse.  *L'icona piccola della* classe viene visualizzata nella barra del titolo di una finestra e nelle visualizzazioni icona piccola della barra delle applicazioni e di Esplora risorse.

Per assegnare un'icona grande e piccola a una classe finestra, specificare gli handle delle icone nei membri **hIcon** e **hIconSm** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Le dimensioni dell'icona devono essere conformi alle dimensioni necessarie per le icone delle classi grandi e piccole. Per un'icona di classe di grandi dimensioni, è possibile determinare le dimensioni necessarie specificando i valori **\_ SM CXICON** e **SM \_ CYICON** in una chiamata alla [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Per un'icona di classe piccola, specificare **i valori \_ SM CXSMICON** e **SM \_ CYSMICON.** Per informazioni, vedere [Icone.](/windows/desktop/menurc/icons)

Se un'applicazione imposta i membri **hIcon** e **hIconSm** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **NULL,** il sistema usa l'icona dell'applicazione predefinita come icone di classe grande e piccola per la classe della finestra. Se si specifica un'icona di classe di grandi dimensioni ma non una piccola, il sistema crea un'icona di classe piccola basata su quella grande. Tuttavia, se si specifica un'icona di classe piccola ma non grande, il sistema usa l'icona dell'applicazione predefinita come icona della classe grande e l'icona specificata come icona della classe piccola.

È possibile eseguire l'override dell'icona della classe grande o piccola per una determinata finestra usando il [**messaggio \_ WM SETICON.**](wm-seticon.md) È possibile recuperare l'icona della classe grande o piccola corrente usando il [**messaggio \_ WM GETICON.**](wm-geticon.md)

### <a name="class-background-brush"></a>Pennello di sfondo della classe

Un *pennello di sfondo della* classe prepara l'area client di una finestra per il disegno successivo da parte dell'applicazione. Il sistema usa il pennello per riempire l'area client con un colore a tinta unita o un motivo, rimuovendo così tutte le immagini precedenti da tale posizione indipendentemente dal fatto che appartengano o meno alla finestra. Il sistema notifica a una finestra che lo sfondo deve essere dipingeto inviando il messaggio [**\_ WM ERASEBKGND**](wm-erasebkgnd.md) alla finestra. Per altre informazioni, vedere [Pennelli.](/windows/desktop/gdi/brushes)

Per assegnare un pennello di sfondo a una classe, creare un pennello usando le funzioni GDI appropriate e assegnare l'handle del pennello restituito al membro **hbrBackground** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

Anziché creare un pennello, un'applicazione può impostare il membro **hbrBackground** su uno dei valori di colore di sistema standard. Per un elenco dei valori di colore di sistema standard, vedere [**SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors)

Per usare un colore di sistema standard, l'applicazione deve aumentare di uno il valore del colore di sfondo. Ad esempio, **COLOR \_ BACKGROUND** + 1 è il colore di sfondo del sistema. In alternativa, è possibile usare la funzione [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) per recuperare un handle per un pennello che corrisponde a un colore di sistema standard e quindi specificare l'handle nel membro **hbrBackground** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa)

Il sistema non richiede che una classe finestra abbia un pennello di sfondo della classe. Se questo parametro è impostato su **NULL,** la finestra deve disegnare il proprio sfondo ogni volta che riceve il messaggio [**WM \_ ERASEBKGND.**](wm-erasebkgnd.md)

### <a name="class-menu"></a>Menu Classe

Un *menu della* classe definisce il menu predefinito che deve essere usato dalle finestre nella classe se non viene specificato alcun menu esplicito quando vengono create le finestre. Un menu è un elenco di comandi da cui un utente può scegliere le azioni che l'applicazione deve eseguire.

È possibile assegnare un menu a una classe impostando il membro **lpszMenuName** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sull'indirizzo di una stringa con terminazione Null che specifica il nome della risorsa del menu. Si presuppone che il menu sia una risorsa nell'applicazione specificata. Il sistema carica automaticamente il menu quando necessario. Se la risorsa di menu è identificata da un numero intero e non da un nome, l'applicazione può impostare il membro **lpszMenuName** su tale numero intero applicando la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) prima di assegnare il valore.

Il sistema non richiede un menu di classe. Se un'applicazione imposta il membro **lpszMenuName** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **NULL,** le finestre nella classe non hanno barre dei menu. Anche se non viene specificato alcun menu di classe, un'applicazione può comunque definire una barra dei menu per una finestra quando crea la finestra.

Se viene specificato un menu per una classe e viene creata una finestra figlio di tale classe, il menu viene ignorato. Per altre informazioni, vedere [Menu.](/windows/desktop/menurc/menus)

### <a name="class-styles"></a>Stili classe

Gli stili della classe definiscono elementi aggiuntivi della classe della finestra. È possibile combinare due o più stili usando l'operatore OR bit per \| bit ( ). Per assegnare uno stile a una classe finestra, assegnare lo stile al membro **style** della [**struttura WNDCLASSEX.**](/windows/win32/api/winuser/ns-winuser-wndclassexa) Per un elenco di stili di classe, vedere [**Stili delle classi delle finestre.**](window-class-styles.md)

### <a name="classes-and-device-contexts"></a>Classi e contesti di dispositivo

Un *contesto di* dispositivo è un set speciale di valori che le applicazioni usano per disegnare nell'area client delle relative finestre. Il sistema richiede un contesto di dispositivo per ogni finestra sullo schermo, ma offre una certa flessibilità nel modo in cui il sistema archivia e considera tale contesto di dispositivo.

Se non viene specificato in modo esplicito uno stile di contesto di dispositivo, il sistema presuppone che ogni finestra usi un contesto di dispositivo recuperato da un pool di contesti gestiti dal sistema. In questi casi, ogni finestra deve recuperare e inizializzare il contesto di dispositivo prima di disegnarlo e liberarlo dopo il disegno.

Per evitare di recuperare un contesto di dispositivo ogni volta che è necessario disegnare all'interno di una finestra, un'applicazione può specificare lo stile **CS \_ OWNDC** per la classe della finestra. Questo stile di classe indica al sistema di creare un contesto di dispositivo privato, ovvero allocare un contesto di dispositivo univoco per ogni finestra nella classe . L'applicazione deve recuperare il contesto una sola volta e quindi usarlo per tutti i disegnare successivi.

### <a name="extra-class-memory"></a>Memoria aggiuntiva per le classi

Il sistema gestisce [**internamente una struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) per ogni classe di finestra nel sistema. Quando un'applicazione registra una classe di finestra, può indirizzare il sistema ad allocare e aggiungere un numero di byte di memoria aggiuntivi alla fine della **struttura WNDCLASSEX.** Questa memoria è detta *memoria di classe aggiuntiva* ed è condivisa da tutte le finestre appartenenti alla classe . Usare la memoria di classe aggiuntiva per archiviare le informazioni relative alla classe .

Poiché la memoria aggiuntiva viene allocata dall'heap locale del sistema, un'applicazione deve usare la memoria di classe aggiuntiva con parsimonio. La [**funzione RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) ha esito negativo se la quantità di memoria di classe aggiuntiva richiesta è maggiore di 40 byte. Se un'applicazione richiede più di 40 byte, deve allocare la propria memoria e archiviare un puntatore alla memoria nella memoria della classe aggiuntiva.

Le [**funzioni SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) [**e SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copiano un valore nella memoria della classe aggiuntiva. Per recuperare un valore dalla memoria aggiuntiva della classe, usare le [**funzioni GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) [**e GetClassLong.**](/windows/win32/api/winuser/nf-winuser-getclasslonga) Il **membro cbClsExtra** della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) specifica la quantità di memoria di classe aggiuntiva da allocare. Un'applicazione che non usa memoria di classe aggiuntiva deve inizializzare il membro **cbClsExtra** su zero.

### <a name="extra-window-memory"></a>Memoria aggiuntiva della finestra

Il sistema mantiene una struttura di dati interna per ogni finestra. Quando si registra una classe di finestra, un'applicazione può specificare un numero di byte aggiuntivi di memoria, denominato *memoria aggiuntiva della finestra.* Quando si crea una finestra della classe , il sistema alloca e aggiunge la quantità specificata di memoria aggiuntiva della finestra alla fine della struttura della finestra. Un'applicazione può usare questa memoria per archiviare dati specifici della finestra.

Poiché la memoria aggiuntiva viene allocata dall'heap locale del sistema, un'applicazione deve usare la memoria aggiuntiva della finestra con parsimonio. La [**funzione RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) ha esito negativo se la quantità di memoria della finestra aggiuntiva richiesta è maggiore di 40 byte. Se un'applicazione richiede più di 40 byte, deve allocare la propria memoria e archiviare un puntatore alla memoria nella memoria aggiuntiva della finestra.

La [**funzione SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copia un valore nella memoria aggiuntiva. La [**funzione GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) recupera un valore dalla memoria aggiuntiva. Il **membro cbWndExtra** della [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) specifica la quantità di memoria aggiuntiva della finestra da allocare. Un'applicazione che non usa la memoria deve inizializzare **cbWndExtra** su zero.

 

 
