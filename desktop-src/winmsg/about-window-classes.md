---
description: Ogni classe della finestra dispone di una routine della finestra associata condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e quindi ne controlla il comportamento e l'aspetto.
ms.assetid: db79fd4b-6a15-4bf9-a0d9-5f6415f6c75f
title: Informazioni sulle classi finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b683176c3fd7904cf3f89b385ce0fa393b89e9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233327"
---
# <a name="about-window-classes"></a>Informazioni sulle classi finestra

Ogni classe della finestra dispone di una routine della finestra associata condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e quindi ne controlla il comportamento e l'aspetto. Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

Un processo deve registrare una classe della finestra prima di poter creare una finestra di tale classe. La registrazione di una classe di finestra associa una routine della finestra, stili di classe e altri attributi di classe con un nome di classe. Quando un processo specifica un nome di classe nella funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) , il sistema crea una finestra con la routine della finestra, gli stili e altri attributi associati al nome della classe.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Tipi di classi di finestra](#types-of-window-classes)
    -   [Classi di sistema](#system-classes)
    -   [Classi globali dell'applicazione](#application-global-classes)
    -   [Classi locali dell'applicazione](#application-local-classes)
-   [Modalità di individuazione di una classe di finestra da parte del sistema](#how-the-system-locates-a-window-class)
-   [Registrazione di una classe di finestra](#registering-a-window-class)
-   [Elementi di una classe di finestra](#elements-of-a-window-class)
    -   [Nome della classe](#class-name)
    -   [Indirizzo della routine della finestra](#window-procedure-address)
    -   [Handle istanza](#instance-handle)
    -   [Cursore classe](#class-cursor)
    -   [Icone della classe](#class-icons)
    -   [Pennello di sfondo classe](#class-background-brush)
    -   [Menu classe](#class-menu)
    -   [Stili classe](#class-styles)
    -   [Memoria di classe aggiuntiva](#extra-class-memory)
    -   [Memoria finestra aggiuntiva](#extra-window-memory)

## <a name="types-of-window-classes"></a>Tipi di classi di finestra

Sono disponibili tre tipi di classi finestra:

-   [Classi di sistema](#system-classes)
-   [Classi globali dell'applicazione](#application-global-classes)
-   [Classi locali dell'applicazione](#application-local-classes)

Questi tipi sono diversi nell'ambito e in quando e come vengono registrati ed eliminati definitivamente.

### <a name="system-classes"></a>Classi di sistema

Una classe di sistema è una classe di finestra registrata dal sistema. Molte classi di sistema sono disponibili per l'utilizzo da parte di tutti i processi, mentre altre vengono utilizzate solo internamente dal sistema. Poiché il sistema registra queste classi, un processo non può eliminarle.

Il sistema registra le classi di sistema per un processo la prima volta che uno dei thread chiama un utente o una funzione di Windows Graphics Device Interface (GDI).

Ogni applicazione riceve una propria copia delle classi di sistema. Tutte le applicazioni basate su Windows a 16 bit nello stesso VDM condividono le classi di sistema, come avviene in Windows a 16 bit.

Nella tabella seguente vengono descritte le classi di sistema disponibili per l'utilizzo da parte di tutti i processi.



| Classe     | Descrizione                         |
|-----------|-------------------------------------|
| Pulsante    | Classe per un pulsante.             |
| ComboBox  | Classe per una casella combinata.          |
| Modifica      | Classe per un controllo di modifica.      |
| ListBox   | Classe per una casella di riepilogo.           |
| MDIClient | Classe per una finestra client MDI. |
| ScrollBar | Classe per una barra di scorrimento.         |
| Static    | Classe per un controllo statico.     |



 

Nella tabella seguente vengono descritte le classi di sistema disponibili solo per l'utilizzo da parte del sistema. Sono elencate qui per motivi di completezza.



| Classe      | Descrizione                                                            |
|------------|------------------------------------------------------------------------|
| ComboLBox  | Classe per la casella di riepilogo contenuta in una casella combinata.                   |
| DDEMLEvent | Classe per gli eventi della libreria di gestione Dynamic Data Exchange (DDEML). |
| Message    | Classe per una finestra di solo messaggio.                                   |
| \#32768    | Classe per un menu.                                                  |
| \#32769    | Classe per la finestra del desktop.                                      |
| \#32770    | Classe per una finestra di dialogo.                                            |
| \#32771    | Classe per la finestra delle opzioni dell'attività.                                  |
| \#32772    | Classe per i titoli delle icone.                                             |



 

### <a name="application-global-classes"></a>Classi globali dell'applicazione

Una [classe globale dell'applicazione](#application-global-classes) è una classe di finestre registrata da un eseguibile o una dll disponibile per tutti gli altri moduli nel processo. Ad esempio, il file con estensione dll può chiamare la funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) per registrare una classe della finestra che definisce un controllo personalizzato come classe globale dell'applicazione in modo che un processo che carica il file con estensione dll possa creare istanze del controllo personalizzato.

Per creare una classe che può essere usata in ogni processo, creare la classe della finestra in un file con estensione dll e caricare il file con estensione dll in ogni processo. Per caricare il file con estensione dll in ogni processo, aggiungere il relativo nome al valore **\_ DLL AppInit** nella seguente chiave del registro di sistema:

**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Windows**

Ogni volta che un processo viene avviato, il sistema carica il file con estensione dll specificato nel contesto del processo appena avviato prima di chiamare la funzione del punto di ingresso. Il file con estensione dll deve registrare la classe durante la procedura di inizializzazione e deve specificare lo stile **cs \_ GLOBALCLASS** . Per altre informazioni, vedere [stili di classe](#class-styles).

Per rimuovere una classe globale dell'applicazione e liberare lo spazio di archiviazione associato, usare la funzione [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

### <a name="application-local-classes"></a>Classi locali dell'applicazione

Una [classe locale dell'applicazione](#application-local-classes) è qualsiasi classe di finestra registrata da un eseguibile o dll per l'uso esclusivo. Sebbene sia possibile registrare un numero qualsiasi di classi locali, è normale registrarne solo una. Questa classe della finestra supporta la routine della finestra principale dell'applicazione.

Il sistema distrugge una classe locale quando il modulo che lo ha registrato si chiude. Un'applicazione può anche usare la funzione [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) per rimuovere una classe locale e liberare lo spazio di archiviazione associato.

## <a name="how-the-system-locates-a-window-class"></a>Modalità di individuazione di una classe di finestra da parte del sistema

Il sistema gestisce un elenco di strutture per ognuno dei tre tipi di classi di finestra. Quando un'applicazione chiama la funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) per creare una finestra con una classe specificata, il sistema utilizza la procedura seguente per individuare la classe.

1.  Eseguire una ricerca nell'elenco di classi locali dell'applicazione per una classe con il nome specificato il cui handle di istanza corrisponde all'handle dell'istanza del modulo. (Diversi moduli possono usare lo stesso nome per registrare le classi locali nello stesso processo).
2.  Se il nome non è presente nell'elenco classe locale dell'applicazione, cercare nell'elenco delle classi globali dell'applicazione.
3.  Se il nome non è presente nell'elenco classe globale dell'applicazione, cercare nell'elenco delle classi di sistema.

Tutte le finestre create dall'applicazione utilizzano questa procedura, incluse le finestre create dal sistema per conto dell'applicazione, ad esempio le finestre di dialogo. È possibile eseguire l'override delle classi di sistema senza influire sulle altre applicazioni. Ovvero, un'applicazione può registrare una classe locale dell'applicazione con lo stesso nome di una classe di sistema. In questo modo, la classe di sistema viene sostituita nel contesto dell'applicazione, ma non viene impedita l'utilizzo della classe di sistema da parte di altre applicazioni.

## <a name="registering-a-window-class"></a>Registrazione di una classe di finestra

Una classe di finestra definisce gli attributi di una finestra, ad esempio lo stile, l'icona, il cursore, il menu e la routine della finestra. Il primo passaggio per la registrazione di una classe di finestra consiste nel compilare una struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) con le informazioni sulla classe della finestra. Per ulteriori informazioni, vedere [elementi di una classe di finestra](#elements-of-a-window-class). Passare quindi la struttura alla funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Per ulteriori informazioni, vedere [utilizzo di classi di finestra](using-window-classes.md).

Per registrare una classe globale dell'applicazione, specificare lo \_ stile cs GLOBALCLASS nel membro **Style** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Quando si registra una classe locale dell'applicazione, non specificare lo stile **cs \_ GLOBALCLASS** .

Se si registra la classe della finestra usando la versione ANSI di [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa), **RegisterClassExA**, l'applicazione richiede che il sistema passi i parametri di testo dei messaggi alle finestre della classe creata usando il set di caratteri ANSI; Se si registra la classe utilizzando la versione Unicode di **RegisterClassEx**, **RegisterClassExW**, l'applicazione richiede che il sistema passi i parametri di testo dei messaggi alle finestre della classe creata utilizzando il set di caratteri Unicode. La funzione [**IsWindowUnicode**](/windows/win32/api/winuser/nf-winuser-iswindowunicode) consente alle applicazioni di eseguire query sulla natura di ogni finestra. Per altre informazioni sulle funzioni ANSI e Unicode, vedere [convenzioni per i prototipi di funzione](/windows/desktop/Intl/conventions-for-function-prototypes).

Il file eseguibile o la DLL che ha registrato la classe è il proprietario della classe. Il sistema determina la proprietà della classe dal membro **HINSTANCE** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) passata alla funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) quando la classe è registrata. Per le dll, il membro **HINSTANCE** deve essere l'handle per l'istanza. dll.

La classe non viene distrutta quando viene scaricato il file con estensione dll proprietario. Se pertanto il sistema chiama la routine della finestra per una finestra di tale classe, si verificherà una violazione di accesso, perché la DLL contenente la routine della finestra non è più in memoria. Il processo deve eliminare tutte le finestre usando la classe prima che il file con estensione dll venga scaricato e chiami la funzione [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa) .

## <a name="elements-of-a-window-class"></a>Elementi di una classe di finestra

Gli elementi di una classe della finestra definiscono il comportamento predefinito di Windows appartenente alla classe. L'applicazione che registra una classe della finestra Assegna elementi alla classe impostando membri appropriati in una struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) e passando la struttura alla funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . Le funzioni [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) e [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) recuperano informazioni su una determinata classe di finestra. La funzione [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) modifica gli elementi di una classe locale o globale che l'applicazione ha già registrato.

Sebbene una classe di finestra completa sia costituita da molti elementi, il sistema richiede solo che un'applicazione fornisca un nome di classe, l'indirizzo della routine della finestra e un handle di istanza. Usare gli altri elementi per definire gli attributi predefiniti per Windows della classe, ad esempio la forma del cursore e il contenuto del menu per la finestra. È necessario inizializzare tutti i membri non usati della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su zero o **null**. Gli elementi della classe della finestra sono indicati nella tabella seguente.



| Elemento                                               | Scopo                                                                                                                                                                                                                                       |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nome della classe](#class-name)                             | Distingue la classe dalle altre classi registrate.                                                                                                                                                                                        |
| [Indirizzo della routine della finestra](#window-procedure-address) | Puntatore alla funzione che elabora tutti i messaggi inviati a Windows nella classe e definisce il comportamento della finestra.                                                                                                                      |
| [Handle istanza](#instance-handle)                   | Identifica l'applicazione o la dll che ha registrato la classe.                                                                                                                                                                                 |
| [Cursore classe](#class-cursor)                         | Definisce il cursore del mouse visualizzato dal sistema per una finestra della classe.                                                                                                                                                                  |
| [Icone della classe](#class-icons)                           | Definisce l'icona grande e l'icona piccola.                                                                                                                                                                                                    |
| [Pennello di sfondo classe](#class-background-brush)     | Definisce il colore e il modello che riempiono l'area client quando la finestra viene aperta o disegnata.                                                                                                                                                 |
| [Menu classe](#class-menu)                             | Specifica il menu predefinito per Windows che non definiscono in modo esplicito un menu.                                                                                                                                                                  |
| [Stili classe](#class-styles)                         | Definisce la modalità di aggiornamento della finestra dopo lo spostamento o il ridimensionamento, come elaborare i doppio clic del mouse, come allocare spazio per il contesto di dispositivo e altri aspetti della finestra.                                                       |
| [Memoria di classe aggiuntiva](#extra-class-memory)             | Specifica la quantità di memoria aggiuntiva, in byte, che il sistema deve riservare per la classe. Tutte le finestre della classe condividono la memoria aggiuntiva e possono usarla per qualsiasi scopo definito dall'applicazione. Il sistema Inizializza la memoria su zero. |
| [Memoria finestra aggiuntiva](#extra-window-memory)           | Specifica la quantità di memoria aggiuntiva, in byte, che il sistema deve riservare per ogni finestra appartenente alla classe. La memoria aggiuntiva può essere usata per qualsiasi scopo definito dall'applicazione. Il sistema Inizializza la memoria su zero.          |



 

### <a name="class-name"></a>Nome della classe

Ogni classe della finestra necessita di un [nome di classe](#class-name) per distinguere una classe da un'altra. Assegnare un nome di classe impostando il membro **lpszClassName** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) all'indirizzo di una stringa con terminazione null che specifica il nome. Poiché le classi finestra sono specifiche del processo, i nomi delle classi di finestra devono essere univoci solo all'interno dello stesso processo. Inoltre, poiché i nomi delle classi occupano spazio nella tabella Atom privata del sistema, è consigliabile tenere le stringhe del nome di classe il più breve possibile.

La funzione [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname) Recupera il nome della classe a cui appartiene una determinata finestra.

### <a name="window-procedure-address"></a>Indirizzo della routine della finestra

Ogni classe necessita di un indirizzo della routine della finestra per definire il punto di ingresso della routine della finestra usata per elaborare tutti i messaggi per Windows nella classe. Il sistema passa i messaggi alla procedura quando è necessario che la finestra effettui le attività, ad esempio disegnare l'area client o rispondere all'input dell'utente. Un processo assegna una routine della finestra a una classe copiando il relativo indirizzo nel membro **lpfnWndProc** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Per altre informazioni, vedere [Routine della finestra](window-procedures.md).

### <a name="instance-handle"></a>Handle istanza

Ogni classe della finestra richiede un handle di istanza per identificare l'applicazione o la dll che ha registrato la classe. Il sistema richiede gli handle di istanza per tenere traccia di tutti i moduli. Il sistema assegna un handle a ogni copia di un eseguibile o di un file con estensione dll in esecuzione.

Il sistema passa un handle di istanza alla funzione del punto di ingresso di ogni eseguibile (vedere [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)) e dll (vedere [**DllMain**](/windows/desktop/Dlls/dllmain)). Il file eseguibile o dll assegna questo handle di istanza alla classe copiando il file nel membro **HINSTANCE** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

### <a name="class-cursor"></a>Cursore classe

Il *cursore della classe* definisce la forma del cursore quando si trova nell'area client di una finestra della classe. Il sistema imposta automaticamente il cursore sulla forma specificata quando il cursore entra nell'area client della finestra e garantisce che mantenga tale forma mentre rimane nell'area client. Per assegnare una forma di cursore a una classe della finestra, caricare una forma predefinita del cursore utilizzando la funzione [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) e quindi assegnare l'handle del cursore restituito al membro **HCursor** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . In alternativa, specificare una risorsa di cursore personalizzata e usare la funzione **LoadCursor** per caricarla dalle risorse dell'applicazione.

Il sistema non richiede un cursore della classe. Se un'applicazione imposta il membro **hCursor** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **null**, non viene definito alcun cursore di classe. Il sistema presuppone che la finestra Imposta la forma del cursore ogni volta che il cursore si sposta nella finestra. Una finestra può impostare la forma del cursore chiamando la funzione [**secursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) ogni volta che la finestra riceve il messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Per ulteriori informazioni sui cursori, vedere [cursori](/windows/desktop/menurc/cursors).

### <a name="class-icons"></a>Icone della classe

Un' *icona di classe* è un'immagine utilizzata dal sistema per rappresentare una finestra di una classe specifica. Un'applicazione può avere due icone di classe, una grande e una piccola. Il sistema Visualizza l'icona di una *classe di grandi dimensioni* della finestra nella finestra delle opzioni di attività visualizzata quando l'utente preme ALT + TAB e nelle visualizzazioni icone grandi della barra delle applicazioni e in Esplora. L' *icona di classe piccola* viene visualizzata nella barra del titolo di una finestra e nelle visualizzazioni icone piccole della barra delle applicazioni e in Esplora.

Per assegnare un'icona di grandi dimensioni e piccole a una classe della finestra, specificare gli handle delle icone nei membri **HICON** e **HIconSm** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Le dimensioni dell'icona devono essere conformi alle dimensioni obbligatorie per le icone di classe grande e piccola. Per un'icona di classe di grandi dimensioni, è possibile determinare le dimensioni richieste specificando i valori di **SM \_ CXICON** e **SM \_ CYICON** in una chiamata alla funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . Per un'icona di classe piccola specificare i valori di **SM \_ CXSMICON** e **SM \_ CYSMICON** . Per informazioni, vedere [Icone](/windows/desktop/menurc/icons).

Se un'applicazione imposta i membri **HICON** e **HIconSm** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **null**, il sistema usa l'icona dell'applicazione predefinita come icone di classe large e Small per la classe Window. Se si specifica un'icona di classe di grandi dimensioni ma non una piccola, il sistema crea un'icona di classe di piccole dimensioni basata su quella grande. Tuttavia, se si specifica un'icona di una classe di piccole dimensioni ma non una grande, il sistema usa l'icona dell'applicazione predefinita come icona della classe di grandi dimensioni e l'icona specificata come icona della classe di piccole dimensioni.

È possibile eseguire l'override dell'icona di una classe di grandi dimensioni o di piccole dimensioni per una particolare finestra usando il messaggio [**WM \_ seicon**](wm-seticon.md) . È possibile recuperare l'icona della classe di grandi dimensioni o di piccole dimensioni corrente usando il messaggio [**WM \_ GetIcon**](wm-geticon.md) .

### <a name="class-background-brush"></a>Pennello di sfondo classe

Un *pennello* per lo sfondo di una classe prepara l'area client di una finestra per il disegno successivo da parte dell'applicazione. Il sistema usa il pennello per riempire l'area client con un colore o un modello a tinta unita, rimuovendo in tal modo tutte le immagini precedenti da tale posizione, indipendentemente dal fatto che appartengano o meno alla finestra. Il sistema notifica a una finestra che lo sfondo deve essere disegnato inviando il messaggio [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) alla finestra. Per altre informazioni, vedere [pennelli](/windows/desktop/gdi/brushes).

Per assegnare un pennello in background a una classe, creare un pennello utilizzando le funzioni GDI appropriate e assegnare l'handle del pennello restituito al membro **hbrBackground** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

Anziché creare un pennello, un'applicazione può impostare il membro **hbrBackground** su uno dei valori di colore di sistema standard. Per un elenco dei valori di colore di sistema standard, vedere [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors).

Per utilizzare un colore di sistema standard, è necessario che l'applicazione aumenti il valore di colore di sfondo di uno. Ad esempio, **lo \_ sfondo del colore** + 1 è il colore di sfondo del sistema. In alternativa, è possibile usare la funzione [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) per recuperare un handle a un pennello che corrisponde a un colore di sistema standard e quindi specificare l'handle nel membro **HbrBackground** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) .

Il sistema non richiede che una classe di finestra disponga di un pennello per lo sfondo della classe. Se questo parametro è impostato su **null**, la finestra deve disegnare il proprio sfondo ogni volta che viene ricevuto il messaggio [**WM \_ ERASEBKGND**](wm-erasebkgnd.md) .

### <a name="class-menu"></a>Menu classe

Un *menu classe* definisce il menu predefinito che verrà utilizzato dalle finestre della classe se non viene specificato alcun menu esplicito al momento della creazione delle finestre. Un menu è un elenco di comandi da cui un utente può scegliere le azioni da eseguire per l'applicazione.

È possibile assegnare un menu a una classe impostando il membro **lpszMenuName** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) sull'indirizzo di una stringa con terminazione null che specifica il nome della risorsa del menu. Si presuppone che il menu sia una risorsa nell'applicazione specificata. Il sistema carica automaticamente il menu quando è necessario. Se la risorsa di menu è identificata da un numero intero e non da un nome, l'applicazione può impostare il membro **lpszMenuName** su tale integer applicando la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) prima di assegnare il valore.

Il sistema non richiede un menu di classe. Se un'applicazione imposta il membro **lpszMenuName** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) su **null**, per Windows nella classe non sono presenti barre dei menu. Anche se non viene specificato alcun menu di classe, un'applicazione può comunque definire una barra dei menu per una finestra quando crea la finestra.

Se viene specificato un menu per una classe e viene creata una finestra figlio di tale classe, il menu viene ignorato. Per ulteriori informazioni, vedere [menu](/windows/desktop/menurc/menus).

### <a name="class-styles"></a>Stili classe

Gli stili della classe definiscono elementi aggiuntivi della classe Window. È possibile combinare due o più stili utilizzando l'operatore OR bit per bit ( \| ). Per assegnare uno stile a una classe della finestra, assegnare lo stile al membro dello **stile** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) . Per un elenco degli stili delle classi, vedere [**stili della classe Window**](window-class-styles.md).

### <a name="classes-and-device-contexts"></a>Classi e contesti di dispositivo

Un *contesto di dispositivo* è un set speciale di valori usati dalle applicazioni per il disegno nell'area client delle rispettive finestre. Il sistema richiede un contesto di dispositivo per ogni finestra sullo schermo, ma consente una certa flessibilità nel modo in cui il sistema archivia e considera il contesto di dispositivo.

Se non viene specificato in modo esplicito alcuno stile del contesto di dispositivo, il sistema presuppone che ogni finestra usi un contesto di dispositivo recuperato da un pool di contesti gestiti dal sistema. In questi casi, ogni finestra deve recuperare e inizializzare il contesto di dispositivo prima del disegno e liberarlo dopo il disegno.

Per evitare di recuperare un contesto di dispositivo ogni volta che è necessario disegnare all'interno di una finestra, un'applicazione può specificare lo stile **cs \_ OWNDC** per la classe Window. Questo stile di classe indica al sistema di creare un contesto di dispositivo privato, ovvero di allocare un contesto di dispositivo univoco per ogni finestra della classe. L'applicazione deve recuperare il contesto una sola volta e quindi usarlo per tutti i disegni successivi.

### <a name="extra-class-memory"></a>Memoria di classe aggiuntiva

Il sistema mantiene internamente una struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) per ogni classe di finestra nel sistema. Quando un'applicazione registra una classe della finestra, può indicare al sistema di allocare e aggiungere un numero di byte aggiuntivi di memoria alla fine della struttura **WNDCLASSEX** . Questa memoria è detta *memoria aggiuntiva della classe* ed è condivisa da tutte le finestre appartenenti alla classe. Usare la memoria della classe aggiuntiva per archiviare le informazioni relative alla classe.

Poiché la memoria aggiuntiva viene allocata dall'heap locale del sistema, un'applicazione deve usare la memoria di classe aggiuntiva in modo sporadico. La funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) ha esito negativo se la quantità di memoria della classe aggiuntiva richiesta è superiore a 40 byte. Se un'applicazione richiede più di 40 byte, deve allocare la propria memoria e archiviare un puntatore alla memoria nella memoria della classe aggiuntiva.

Le funzioni [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword) e [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) copiano un valore nella memoria della classe aggiuntiva. Per recuperare un valore dalla memoria della classe aggiuntiva, usare le funzioni [**GetClassWord**](/windows/win32/api/winuser/nf-winuser-getclassword) e [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga) . Il membro **cbClsExtra** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) specifica la quantità di memoria di classe aggiuntiva da allocare. Un'applicazione che non utilizza memoria della classe aggiuntiva deve inizializzare il membro **cbClsExtra** su zero.

### <a name="extra-window-memory"></a>Memoria finestra aggiuntiva

Il sistema mantiene una struttura di dati interna per ogni finestra. Quando si registra una classe della finestra, un'applicazione può specificare un numero di byte aggiuntivi di memoria, denominato *memoria finestra aggiuntiva*. Quando si crea una finestra della classe, il sistema alloca e aggiunge la quantità specificata di memoria della finestra aggiuntiva alla fine della struttura della finestra. Un'applicazione può usare questa memoria per archiviare i dati specifici della finestra.

Poiché la memoria aggiuntiva viene allocata dall'heap locale del sistema, un'applicazione deve usare la memoria della finestra aggiuntiva in modo sporadico. La funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) ha esito negativo se la quantità di memoria della finestra aggiuntiva richiesta è maggiore di 40 byte. Se un'applicazione richiede più di 40 byte, deve allocare la propria memoria e archiviare un puntatore alla memoria nella memoria della finestra aggiuntiva.

La funzione [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) copia un valore nella memoria aggiuntiva. La funzione [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) recupera un valore dalla memoria aggiuntiva. Il membro **cbWndExtra** della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) specifica la quantità di memoria della finestra aggiuntiva da allocare. Un'applicazione che non utilizza la memoria deve inizializzare **cbWndExtra** su zero.

 

 
