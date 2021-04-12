---
title: Informazioni sui menu
description: In questo argomento vengono illustrati i menu.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- risorse, menu
- menu, informazioni
- sottomenu
- barre dei menu
- menu di primo livello
- scelta rapida (menu)
- menu a discesa
- menu, di primo livello
- menu, popup
- menu, elenco a discesa
- nomi di menu
- menu, collegamento
- menu, finestra
- menu, sistema
- menu, controllo
- menu di scelta rapida
- Menu Finestra
- Menu di sistema
- Menu di controllo
- identificatori della Guida
- handle di menu
- voci di menu
- elementi di comando
- identificatori di voci di menu
- posizione voce menu
- selezione delle voci di menu
- cancellazione di voci di menu
- menu creati dal proprietario
- menu, proprietario disegnato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5d42eb42aaaaa16eef0b5b118adcfe0f91156e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398921"
---
# <a name="about-menus"></a>Informazioni sui menu

Un *menu* è un elenco di elementi che specificano opzioni o gruppi di opzioni (un sottomenu) per un'applicazione. Se si fa clic su una voce di menu, viene aperto un sottomenu o l'applicazione esegue un comando. In questa sezione vengono fornite informazioni sui seguenti argomenti:

-   [Barre dei menu e menu](#menu-bars-and-menus)
    -   [Menu di scelta rapida](#shortcut-menus)
    -   [Menu finestra](#the-window-menu)
    -   [Identificatore della Guida](#help-identifier)
-   [Accesso da tastiera a menu](#keyboard-access-to-menus)
    -   [Interfaccia della tastiera standard](#standard-keyboard-interface)
    -   [Chiavi di accesso ai menu](#menu-access-keys)
    -   [Tasti di scelta rapida del menu](#menu-shortcut-keys)
-   [Creazione menu](#menu-creation)
    -   [Risorse modello di menu](#menu-template-resources)
    -   [Modello di menu in memoria](#menu-template-in-memory)
    -   [Handle di menu](#menu-handles)
    -   [Funzioni di creazione menu](#menu-creation-functions)
    -   [Visualizzazione menu](#menu-display)
    -   [Menu della classe finestra](#window-class-menus)
-   [Voci di menu](#menu-items)
    -   [Elementi di comando ed elementi che aprono sottomenu](#command-items-and-items-that-open-submenus)
    -   [Identificatore voce di menu](#menu-item-identifier)
    -   [Posizione voce menu](#menu-item-position)
    -   [Accesso alle voci di menu a livello di codice](#accessing-menu-items-programmatically)
    -   [Voci di menu predefinite](#default-menu-items)
    -   [Voci di menu selezionate e cancellate](#selected-and-clear-menu-items)
    -   [Voci di menu abilitate, in grigio e disabilitate](#enabled-grayed-and-disabled-menu-items)
    -   [Voci di menu evidenziate](#highlighted-menu-items)
    -   [Voci di menu create dal proprietario](#owner-drawn-menu-items)
    -   [Separatori di voci di menu e interruzioni di riga](#menu-item-separators-and-line-breaks)
-   [Messaggi utilizzati con i menu](#messages-used-with-menus)
-   [Distruzione di menu](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Barre dei menu e menu

Un menu viene disposto in una gerarchia. Al livello superiore della gerarchia è presente la *barra dei menu*; che contiene un elenco di *menu* che a loro volta possono contenere *sottomenu*. Una barra dei menu viene talvolta chiamata *menu di primo livello* e i menu e i sottomenu sono noti anche come menu a *comparsa*.

Una voce di menu può eseguire un comando o aprire un sottomenu. Un elemento che esegue un comando è denominato elemento di *comando* o *comando*.

Un elemento nella barra dei menu apre quasi sempre un menu. Le barre dei menu contengono raramente elementi di comando. Un menu aperto dalla barra dei menu scende dalla barra dei menu e viene talvolta definito menu a *discesa*. Quando viene visualizzato un menu a discesa, questo viene collegato alla barra dei menu. Una voce di menu sulla barra dei menu che apre un menu a discesa viene anche denominata *nome del menu*.

I nomi dei menu in una barra dei menu rappresentano le categorie principali di comandi forniti da un'applicazione. Selezionando un nome di menu dalla barra dei menu viene in genere aperto un menu le cui voci di menu corrispondono ai comandi di una categoria. Una barra dei menu, ad esempio, potrebbe contenere un nome di menu **file** che, quando viene selezionato dall'utente, attiva un menu con voci di menu, ad esempio **nuovo**, **Apri** e **Salva**. Per ottenere informazioni su una barra dei menu, chiamare [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Solo una finestra a comparsa o sovrapposta può contenere una barra dei menu; una finestra figlio non può contenere uno. Se la finestra dispone di una barra del titolo, il sistema posiziona la barra dei menu immediatamente sotto di essa. Una barra dei menu è sempre visibile. Tuttavia, un sottomenu non è visibile, fino a quando l'utente non seleziona una voce di menu che la attiva. Per ulteriori informazioni sulle finestre sovrapposte e popup, vedere [tipi di finestra](/windows/desktop/winmsg/window-features).

Ogni menu deve avere una finestra proprietaria. Il sistema invia messaggi alla finestra proprietaria di un menu quando l'utente seleziona il menu o sceglie una voce dal menu.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Menu di scelta rapida](#shortcut-menus)
-   [Menu finestra](#the-window-menu)
-   [Identificatore della Guida](#help-identifier)

### <a name="shortcut-menus"></a>Menu di scelta rapida

Il sistema fornisce anche *menu di scelta rapida*. Un menu di scelta rapida non è collegato alla barra dei menu; può essere visualizzata in qualsiasi punto dello schermo. Un'applicazione in genere associa un menu di scelta rapida con una parte di una finestra, ad esempio l'area client, o con un oggetto specifico, ad esempio un'icona. Per questo motivo, questi menu sono denominati anche *menu di scelta rapida*.

Un menu di scelta rapida rimane nascosto fino a quando non viene attivato dall'utente, generalmente facendo clic con il pulsante destro del mouse su una selezione, una barra degli strumenti o un pulsante della barra delle applicazioni Il menu viene in genere visualizzato nella posizione del punto di inserimento o del cursore del mouse.

### <a name="the-window-menu"></a>Menu finestra

Il menu **finestra** (noto anche come menu di **sistema** o menu di **controllo** ) è un menu a comparsa definito e gestito quasi esclusivamente dal sistema operativo. L'utente può aprire il menu della finestra facendo clic sull'icona dell'applicazione sulla barra del titolo oppure facendo clic con il pulsante destro del mouse in un punto qualsiasi della barra del titolo.

Il menu **finestra** fornisce un set standard di voci di menu che l'utente può scegliere di modificare le dimensioni o la posizione di una finestra o chiudere l'applicazione. È possibile aggiungere, eliminare e modificare elementi nel menu finestra, ma la maggior parte delle applicazioni usa semplicemente il set standard di voci di menu. Una finestra sovrapposta, popup o figlio può avere un menu finestra. Non è frequente che una finestra sovrapposta o popup non includa un menu finestra.

Quando l'utente sceglie un comando dal menu **finestra** , il sistema invia un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) alla finestra proprietaria del menu. Nella maggior parte delle applicazioni, la routine della finestra non elabora i messaggi dal menu finestra. Al contrario, passa semplicemente i messaggi alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita del sistema del messaggio. Se un'applicazione aggiunge un comando al menu della finestra, la routine della finestra deve elaborare il comando.

Un'applicazione può utilizzare la funzione [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) per creare una copia del menu predefinito della finestra da modificare. Qualsiasi finestra che non utilizza la funzione **GetSystemMenu** per eseguire la propria copia del menu finestra riceve il menu della finestra standard.

### <a name="help-identifier"></a>Identificatore della Guida

Associato a ogni barra dei menu, menu, sottomenu e menu di scelta rapida è un identificatore della guida. Se l'utente preme il tasto F1 mentre il menu è attivo, questo valore viene inviato alla finestra proprietaria come parte di un messaggio [**della \_ Guida WM**](../shell/wm-help.md) .

## <a name="keyboard-access-to-menus"></a>Accesso da tastiera a menu

Il sistema fornisce un'interfaccia della tastiera standard per i menu. È possibile migliorare questa interfaccia fornendo chiavi di accesso mnemonico e tasti di scelta rapida per le voci di menu.

Negli argomenti seguenti vengono descritti l'interfaccia della tastiera standard, le chiavi di accesso e i tasti di scelta rapida:

-   [Interfaccia della tastiera standard](#standard-keyboard-interface)
-   [Chiavi di accesso ai menu](#menu-access-keys)
-   [Tasti di scelta rapida del menu](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interfaccia della tastiera standard

Il sistema è progettato per funzionare con o senza un mouse o un altro dispositivo di puntamento. Poiché il sistema fornisce un'interfaccia della tastiera standard, l'utente può utilizzare la tastiera per selezionare le voci di menu. Questa interfaccia della tastiera non richiede codice speciale. Un'applicazione riceve un messaggio di comando indipendentemente dal fatto che l'utente selezioni una voce di menu tramite la tastiera o con il mouse. L'interfaccia della tastiera standard elabora le seguenti sequenze di tasti.



| Combinazioni di tasti              | Azione                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Carattere alfabetico | Seleziona la prima voce di menu con il carattere specificato come chiave di accesso. Se l'elemento selezionato richiama un menu, viene visualizzato il menu e il primo elemento viene evidenziato. In caso contrario, viene scelta la voce di menu.                            |
| ALT                    | Consente di abilitare o disabilitare la modalità barra dei menu.                                                                                                                                                                                                     |
| ALT+BARRA SPAZIATRICE           | Consente di visualizzare il menu finestra.                                                                                                                                                                                                                |
| INVIO                  | Attiva un menu e seleziona la prima voce di menu se a un elemento è associato un menu. In caso contrario, questa sequenza di tasti sceglie l'elemento come se l'utente avesse rilasciato il pulsante del mouse mentre l'elemento è stato selezionato.                              |
| ESC                    | Esce dalla modalità menu.                                                                                                                                                                                                                         |
| FRECCIA SINISTRA             | Passa alla voce di menu di primo livello precedente. Le voci di menu di primo livello includono i nomi dei menu e il menu finestra. Se l'elemento selezionato si trova in un menu, viene selezionata la colonna precedente nel menu o è selezionata la voce di menu di primo livello precedente. |
| FRECCIA DESTRA            | Funziona come il tasto freccia sinistra, ad eccezione della direzione opposta. Nei menu questa sequenza di tasti viene spostata in un altro colonna; Quando l'elemento attualmente selezionato si trova nella colonna all'estrema destra, viene selezionato il menu successivo.                              |
| FRECCE verso l'alto o verso il basso      | Attiva un menu quando viene premuto in un nome di menu. Quando viene premuto in un menu, la sequenza di tasti freccia su Seleziona l'elemento precedente; la sequenza di tasti freccia giù seleziona l'elemento successivo.                                                                  |



 

### <a name="menu-access-keys"></a>Chiavi di accesso ai menu

L'interfaccia della tastiera standard per i menu può essere migliorata aggiungendo chiavi di accesso (mnemonico) alle voci di menu. Una chiave di accesso è una lettera sottolineata nel testo di una voce di menu. Quando un menu è attivo, l'utente può selezionare una voce di menu premendo il tasto corrispondente alla lettera sottolineata dell'elemento. L'utente rende attiva la barra dei menu premendo il tasto ALT per evidenziare il primo elemento sulla barra dei menu. Un menu è attivo quando viene visualizzato.

Per creare una chiave di accesso per una voce di menu, precedere qualsiasi carattere nella stringa di testo dell'elemento con una e commerciale. Ad esempio, la stringa di testo "&Move" fa in modo che il sistema sottolineare la lettera "M".

### <a name="menu-shortcut-keys"></a>Tasti di scelta rapida del menu

Oltre a disporre di una chiave di accesso, a una voce di menu può essere associato un tasto di scelta rapida. Un tasto di scelta rapida è diverso da un tasto di scelta, perché non è necessario che il menu sia attivo perché il tasto di scelta rapida funzioni. Inoltre, una chiave di accesso è *sempre* associata a una voce di menu, mentre un tasto di scelta rapida è in *genere* , ma non deve essere, associato a una voce di menu.

Il testo che identifica il tasto di scelta rapida viene aggiunto alla stringa di testo della voce di menu. Il testo del collegamento viene visualizzato a destra del nome della voce di menu, dopo una barra rovesciata e un carattere di tabulazione ( \\ t). Ad esempio, "&Close \\ tAlt + F4" rappresenta un comando Close con la combinazione di tasti ALT + F4 come tasto di scelta rapida e con la lettera "C" come chiave di accesso. Per ulteriori informazioni, vedere [tasti](keyboard-accelerators.md)di scelta rapida.

## <a name="menu-creation"></a>Creazione menu

È possibile creare un menu usando un modello di menu o funzioni di creazione di menu. I modelli di menu vengono in genere definiti come risorse. Menu: è possibile caricare le risorse del modello in modo esplicito o assegnato come menu predefinito per una classe di finestra. È anche possibile creare risorse del modello di menu in modo dinamico in memoria.

Gli argomenti seguenti descrivono in dettaglio la creazione di menu:

-   [Risorse modello di menu](#menu-template-resources)
-   [Modello di menu in memoria](#menu-template-in-memory)
-   [Handle di menu](#menu-handles)
-   [Funzioni di creazione menu](#menu-creation-functions)
-   [Visualizzazione menu](#menu-display)
-   [Menu della classe finestra](#window-class-menus)

### <a name="menu-template-resources"></a>Risorse modello di menu

La maggior parte delle applicazioni crea menu usando le risorse del modello di menu. Un *modello di menu* definisce un menu che include gli elementi nella barra dei menu e in tutti i menu. Per informazioni sulla creazione di una risorsa modello di menu, vedere la documentazione inclusa con gli strumenti di sviluppo.

Dopo aver creato una risorsa del modello di menu e averla aggiunta al file eseguibile dell'applicazione (exe), è possibile usare la funzione [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) per caricare la risorsa in memoria. Questa funzione restituisce un handle per il menu, che è quindi possibile assegnare a una finestra utilizzando la funzione [**semenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . È possibile assegnare un menu a qualsiasi finestra che non sia una finestra figlio.

L'implementazione di menu come risorse rende più semplice la localizzazione di un'applicazione per l'uso in più paesi/aree geografiche. È necessario localizzare solo il file di definizione delle risorse per ogni lingua, non per il codice sorgente dell'applicazione.

### <a name="menu-template-in-memory"></a>Modello di menu in memoria

È possibile creare un menu da un modello di menu compilato in memoria in fase di esecuzione. Ad esempio, un'applicazione che consente a un utente di personalizzare il menu potrebbe creare un modello di menu in memoria in base alle preferenze dell'utente. L'applicazione può quindi salvare il modello in un file o nel registro di sistema per un uso futuro. Per creare un menu da un modello in memoria, usare la funzione [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Per le descrizioni dei formati dei modelli di menu, vedere [risorse del modello di menu](#menu-template-resources).

Un modello di menu standard è costituito da una struttura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguita da una o più strutture [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

Un modello di menu esteso è costituito da una struttura di [**\_ \_ intestazione del modello menuex**](menuex-template-header.md) seguita da una o più strutture di [**\_ \_ elementi del modello menuex**](menuex-template-item.md) .

### <a name="menu-handles"></a>Handle di menu

Il sistema genera un handle univoco per ogni menu. Un *handle di menu* è un valore del tipo **HMENU** . Un'applicazione deve specificare un handle di menu in molte delle funzioni di menu. Si riceve un handle per una barra dei menu quando si crea il menu o si carica una risorsa di menu.

Per recuperare un handle per la barra dei menu per un menu che è stato creato o caricato, usare la funzione [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu) . Per recuperare un handle per il sottomenu associato a una voce di menu, usare la funzione [**getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) . Per recuperare un handle a un menu finestra, utilizzare la funzione [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) .

### <a name="menu-creation-functions"></a>Funzioni di creazione menu

Utilizzando le funzioni di creazione dei menu, è possibile creare menu in fase di esecuzione o aggiungere voci di menu a menu esistenti. È possibile usare la funzione [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) per creare una barra dei menu vuota e la funzione [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) per creare un menu vuoto. È possibile salvare alcune informazioni sulle impostazioni per un menu usando la struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Per ottenere o recuperare le impostazioni di un menu, usare [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) o [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo). Per aggiungere elementi a un menu, utilizzare la funzione [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . Le funzioni [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) e [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) meno recenti sono ancora supportate, ma è necessario usare **InsertMenuItem** per le nuove applicazioni.

### <a name="menu-display"></a>Visualizzazione menu

Dopo che un menu è stato caricato o creato, deve essere assegnato a una finestra prima che il sistema possa visualizzarlo. È possibile assegnare un menu definendo un menu classe. Per altre informazioni, vedere [menu della classe Window](#window-class-menus). È anche possibile assegnare un menu a una finestra specificando un handle per il menu come parametro *HMENU* della funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oppure chiamando la funzione [**semenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) .

Per visualizzare un menu di scelta rapida, utilizzare la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . I menu di scelta rapida, detti anche menu a comparsa mobile o menu di scelta rapida, vengono in genere visualizzati quando il messaggio [**WM \_ ContextMenu**](wm-contextmenu.md) viene elaborato.

È possibile assegnare un menu a qualsiasi finestra che non sia una finestra figlio.

La funzione [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) precedente è ancora supportata, ma le nuove applicazioni devono usare la funzione [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .

### <a name="window-class-menus"></a>Menu della classe finestra

Quando si registra una classe della finestra, è possibile specificare un menu predefinito, denominato *menu classe* . A tale scopo, assegnare il nome della risorsa del modello di menu al membro **lpszMenuName** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) usata per registrare la classe.

Per impostazione predefinita, a ogni finestra viene assegnato il menu della classe per la relativa classe della finestra, pertanto non è necessario caricare in modo esplicito il menu e assegnarlo a ogni finestra. È possibile eseguire l'override del menu della classe specificando un handle di menu diverso in una chiamata alla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . È anche possibile modificare il menu di una finestra dopo averla creata tramite la funzione [**semenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Per altre informazioni, vedere [classi di finestra](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Voci di menu

Negli argomenti seguenti viene illustrato il funzionamento del sistema quando l'utente sceglie una voce di menu e i modi in cui un'applicazione può controllare l'aspetto e la funzionalità di un elemento:

-   [Elementi di comando ed elementi che aprono sottomenu](#command-items-and-items-that-open-submenus)
-   [Identificatore voce di menu](#menu-item-identifier)
-   [Posizione voce menu](#menu-item-position)
-   [Accesso alle voci di menu a livello di codice](#accessing-menu-items-programmatically)
-   [Voci di menu predefinite](#default-menu-items)
-   [Voci di menu selezionate e cancellate](#selected-and-clear-menu-items)
-   [Voci di menu abilitate, in grigio e disabilitate](#enabled-grayed-and-disabled-menu-items)
-   [Voci di menu evidenziate](#highlighted-menu-items)
-   [Voci di menu create dal proprietario](#owner-drawn-menu-items)
-   [Separatori di voci di menu e interruzioni di riga](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Elementi di comando ed elementi che aprono sottomenu

Quando l'utente sceglie un elemento di comando, il sistema invia un messaggio di comando alla finestra che possiede il menu. Se l'elemento di comando si trova nel menu finestra, il sistema invia il messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) . In caso contrario, invia il messaggio del [**\_ comando WM**](wm-command.md) .

Associato a ogni voce di menu che apre un sottomenu è un handle per il sottomenu corrispondente. Quando l'utente punta a tale elemento, il sistema apre il sottomenu. Nessun messaggio di comando inviato alla finestra proprietaria. Tuttavia, il sistema invia un messaggio [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) alla finestra proprietaria prima di visualizzare il sottomenu. È possibile ottenere un handle per il sottomenu associato a un elemento usando la funzione [**getsottomenù**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Una barra dei menu contiene in genere i nomi di menu, ma può contenere anche elementi di comando. Un sottomenu contiene in genere gli elementi del comando, ma può contenere anche elementi che aprono i sottomenu annidati. Aggiungendo tali elementi ai sottomenu, è possibile annidare i menu a qualsiasi profondità. Per fornire un segnale visivo per l'utente, il sistema visualizza automaticamente una piccola freccia a destra del testo di una voce di menu che apre un sottomenu.

### <a name="menu-item-identifier"></a>Identificatore Menu-Item

Associato a ogni voce di menu è un intero univoco definito dall'applicazione, denominato *identificatore voce di menu*. Quando l'utente sceglie un elemento di comando da un menu, il sistema invia l'identificatore dell'elemento alla finestra proprietaria come parte di un messaggio di [**\_ comando WM**](wm-command.md) . La routine della finestra esamina l'identificatore per determinare l'origine del messaggio ed elabora il messaggio di conseguenza. Inoltre, è possibile specificare una voce di menu usando il relativo identificatore quando si chiamano le funzioni di menu; ad esempio, per abilitare o disabilitare una voce di menu.

Le voci di menu che aprono sottomenu hanno identificatori esattamente come gli elementi di comando. Tuttavia, il sistema non invia un messaggio di comando quando tale elemento viene selezionato da un menu. Al contrario, il sistema apre il sottomenu associato alla voce di menu.

Per recuperare l'identificatore della voce di menu in una posizione specificata, utilizzare la funzione [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) o [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

### <a name="menu-item-position"></a>Posizione Menu-Item

Oltre a disporre di un identificatore univoco, ogni voce di menu in una barra dei menu o un menu ha un valore di posizione univoco. L'elemento più a sinistra in una barra dei menu o l'elemento superiore di un menu ha la posizione zero. Il valore di posizione viene incrementato per le voci di menu successive. Il sistema assegna un valore di posizione a tutti gli elementi in un menu, inclusi i separatori. Nella figura seguente vengono mostrati i valori di posizione degli elementi in una barra dei menu e in un menu.

![barra dei menu e menu](images/csemn-01.png)

Quando si chiama una funzione di menu che modifica o recupera informazioni su una voce di menu specifica, è possibile specificare l'elemento utilizzando il relativo identificatore o la relativa posizione. Per ulteriori informazioni, vedere la sezione successiva.

### <a name="accessing-menu-items-programmatically"></a>Accesso alle voci di menu a livello di codice

La maggior parte delle funzioni di menu consente di specificare una voce di menu in base alla posizione o al comando. Alcune funzioni usano i flag **MF \_ BYPOSITION** e **MF \_ BYCOMMAND** per indicare l'algoritmo di ricerca, mentre altri hanno un parametro *fByPosition* esplicito. Se si specifica la voce di menu in base alla posizione, il numero dell'elemento è un indice in base zero nel menu. Se si specifica la voce di menu per comando, nel menu e nei relativi sottomenu viene cercata una voce il cui identificatore di menu è uguale al numero di elemento specificato. Se più di un elemento nella gerarchia dei menu corrisponde al numero di elemento, non è specificato quello utilizzato. Se i menu contengono identificatori di menu duplicati, è consigliabile usare operazioni di menu basate sulla posizione per evitare questa ambiguità.

### <a name="default-menu-items"></a>Voci di menu predefinite

Un sottomenu può contenere una voce di menu predefinita. Quando l'utente apre un sottomenu facendo doppio clic, il sistema invia un messaggio di comando alla finestra proprietaria del menu e chiude il menu come se fosse stato scelto l'elemento di comando predefinito. Se non è presente alcun elemento del comando predefinito, il sottomenu rimane aperto. Per recuperare e impostare l'elemento predefinito per un sottomenu, usare le funzioni [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) e [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem) .

### <a name="selected-and-clear-menu-items"></a>Voci di menu selezionate e cancellate

Una voce di menu può essere selezionata o deselezionata. Il sistema Visualizza una bitmap accanto alle voci di menu selezionate per indicare lo stato selezionato. Il sistema non visualizza una bitmap accanto a Cancella elementi, a meno che non sia specificata una bitmap "Clear" definita dall'applicazione. È possibile selezionare solo voci di menu in un menu; non è possibile selezionare elementi in una barra dei menu.

Le applicazioni in genere controllano o cancellano una voce di menu per indicare se è attiva un'opzione. Si supponga, ad esempio, che un'applicazione disponga di una barra degli strumenti che l'utente può visualizzare o nascondere utilizzando un comando della **barra degli strumenti** in un menu. Quando la barra degli strumenti è nascosta, la voce di menu della **barra degli strumenti** è deselezionata. Quando l'utente sceglie il comando, l'applicazione controlla la voce di menu e Mostra la barra degli strumenti.

Un attributo di segno di spunta controlla se è selezionata una voce di menu. È possibile impostare l'attributo del segno di spunta di una voce di menu tramite la funzione [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) . È possibile utilizzare la funzione [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) per determinare se una voce di menu è attualmente selezionata o deselezionata.

Anziché [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) e [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate), è possibile usare le funzioni [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) per recuperare e impostare lo stato di selezione di una voce di menu.

In alcuni casi, un gruppo di voci di menu corrisponde a un set di opzioni che si escludono a vicenda. In questo caso, è possibile indicare l'opzione selezionata utilizzando una voce di menu di opzione selezionata (analogamente a un controllo pulsante di opzione). Gli elementi radio selezionati vengono visualizzati con una bitmap Bullet anziché con una bitmap di segno di spunta. Per controllare una voce di menu e impostarla come voce di Radio, usare la funzione [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem) .

Per impostazione predefinita, il sistema Visualizza un segno di spunta o una bitmap Bullet accanto a voci di menu selezionate e nessuna bitmap accanto a voci di menu deselezionate. È tuttavia possibile usare la funzione [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) per associare le bitmap selezionate e cancellate dall'applicazione a una voce di menu. Il sistema usa quindi le bitmap specificate per indicare lo stato selezionato o cancellato della voce di menu.

Le bitmap definite dall'applicazione associate a una voce di menu devono avere le stesse dimensioni della bitmap del segno di spunta predefinito, le cui dimensioni possono variare a seconda della risoluzione dello schermo. Per recuperare le dimensioni corrette, utilizzare la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . È possibile creare più risorse bitmap per diverse risoluzioni dello schermo; creare una risorsa bitmap e ridimensionarla, se necessario; in alternativa, creare una bitmap in fase di esecuzione e creare un'immagine al suo interno. Le bitmap possono essere di tipo monocromatico o colore. Tuttavia, poiché le voci di menu vengono invertite quando evidenziato, l'aspetto di determinate bitmap di colore invertite potrebbe essere indesiderato. Per ulteriori informazioni, vedere [bitmap](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Voci di menu abilitate, in grigio e disabilitate

Una voce di menu può essere abilitata, visualizzata in grigio o disabilitata. Per impostazione predefinita, una voce di menu è abilitata. Quando l'utente sceglie una voce di menu abilitata, il sistema invia un messaggio di comando alla finestra proprietaria o Visualizza il sottomenu corrispondente, a seconda del tipo di voce di menu.

Quando le voci di menu non sono disponibili per l'utente, devono essere visualizzate in grigio o disabilitate. Non è possibile scegliere voci di menu in grigio e disabilitate. Un elemento disabilitato è simile a un elemento attivato. Quando l'utente fa clic su un elemento disabilitato, l'elemento non è selezionato e non viene eseguita alcuna operazione. Gli elementi disabilitati possono essere utili, ad esempio, in un'esercitazione che presenta un menu che sembra attivo ma non lo è.

Un'applicazione Disabilita una voce di menu non disponibile per fornire all'utente un segnale visivo che non è disponibile un comando. È possibile utilizzare un elemento disattivato quando un'azione non è appropriata. ad esempio, è possibile utilizzare il comando **stampa** nel menu **file** quando il sistema non dispone di una stampante installata.

La funzione [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) Abilita, Disabilita o Disabilita una voce di menu. Per determinare se una voce di menu è abilitata, in grigio o disabilitata, utilizzare la funzione [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) .

Anziché [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa), è anche possibile usare la funzione [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) per determinare se una voce di menu è abilitata, in grigio o disabilitata.

### <a name="highlighted-menu-items"></a>Voci di menu evidenziate

Il sistema evidenzia automaticamente le voci di menu nei menu quando vengono selezionate dall'utente. Tuttavia, l'evidenziazione può essere aggiunta o rimossa in modo esplicito da un nome di menu sulla barra dei menu tramite la funzione [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) . Questa funzione non ha effetto sulle voci di menu nei menu. Quando **HiliteMenuItem** viene usato per evidenziare un nome di menu, tuttavia, il nome sembra essere selezionato. Se l'utente preme il tasto invio, l'elemento evidenziato non viene selezionato. Questa funzionalità può essere utile, ad esempio, in un'applicazione di training che illustra l'uso dei menu.

### <a name="owner-drawn-menu-items"></a>Voci di menu Owner-Drawn

Un'applicazione è in grado di controllare completamente l'aspetto di una voce di menu utilizzando un *elemento creato dal proprietario*. Gli elementi creati dal proprietario richiedono che un'applicazione assuma la responsabilità totale del disegno degli stati selezionati (evidenziati), selezionati e cancellati. Se, ad esempio, un'applicazione ha fornito un menu del tipo di carattere, può creare ogni voce di menu usando il tipo di carattere corrispondente. l'elemento per Roman viene disegnato con Roman, l'elemento per Italic viene disegnato in corsivo e così via. Per ulteriori informazioni, vedere [creazione di Owner-Drawn voci di menu](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Separatori di voci di menu e interruzioni di riga

Il sistema fornisce un tipo speciale di voce di menu, denominato *separatore*, che viene visualizzato come linea orizzontale. È possibile utilizzare un separatore per dividere un menu in gruppi di elementi correlati. Non è possibile usare un separatore in una barra dei menu e l'utente non può selezionare un separatore.

Quando una barra dei menu contiene più nomi di menu che si adattano a una sola riga, il sistema esegue il wrapping della barra dei menu suddividendo automaticamente in due o più righe. È possibile fare in modo che un'interruzioni di riga venga eseguita in corrispondenza di un elemento specifico in una barra dei menu assegnando il flag di tipo **\_ MENUBREAK di MFT** all'elemento. Il sistema posiziona l'elemento e tutti gli elementi successivi in una nuova riga.

Quando un menu contiene più elementi di quelli che rientrano in una colonna, il menu viene troncato. È possibile fare in modo che un'interruzioni di colonna venga eseguita in corrispondenza di un elemento specifico in un menu assegnando il flag di tipo **MFT \_ MENUBREAK** all'elemento o utilizzando l'opzione MENUBREAK nell'istruzione [MenuItem](/windows/desktop/menurc/menuitem-statement) . Il sistema posiziona l'elemento e tutti gli elementi successivi in una nuova colonna. Il flag di tipo **MFT \_ MENUBARBREAK** ha lo stesso effetto, ad eccezione del fatto che viene visualizzata una linea verticale tra la nuova colonna e la vecchia.

Se si usano le funzioni [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) per assegnare le interruzioni di riga, è necessario assegnare i flag di tipo **MF \_ MENUBREAK** o **MF \_ MENUBARBREAK**.

## <a name="messages-used-with-menus"></a>Messaggi utilizzati con i menu

L'attività correlata al menu segnala il sistema inviando messaggi alla routine della finestra che possiede il menu. Il sistema invia una serie di messaggi quando l'utente seleziona elementi sulla barra dei menu o fa clic con il pulsante destro del mouse per visualizzare un menu di scelta rapida.

Quando l'utente attiva un elemento nella barra dei menu, la finestra proprietaria riceve prima di tutto un messaggio [**WM \_ SYSCOMMAND**](wm-syscommand.md) . Questo messaggio include un flag che indica se l'utente ha attivato il menu usando la tastiera ( \_ menu SC) o il mouse (SC \_ MOUSEMENU). Per ulteriori informazioni, vedere [accesso da tastiera a menu](#keyboard-access-to-menus).

Successivamente, prima di visualizzare i menu, il sistema invia il messaggio [**WM \_ INITMENU**](wm-initmenu.md) alla routine della finestra in modo che un'applicazione possa modificare i menu prima che l'utente li visualizzi. Il sistema invia il **messaggio \_ INITMENU WM** solo una volta per ogni attivazione di menu.

Quando l'utente punta a una voce di menu che apre un sottomenu, il sistema invia la finestra proprietaria al messaggio [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) prima di visualizzare il sottomenu. Questo messaggio fornisce all'applicazione la possibilità di modificare il sottomenu prima che venga visualizzato.

Ogni volta che l'utente sposta l'evidenziazione da un elemento a un altro, il sistema invia un messaggio [**WM \_ MENUSELECT**](wm-menuselect.md) alla procedura della finestra proprietaria del menu. Questo messaggio identifica la voce di menu attualmente selezionata. Molte applicazioni forniscono un'area informazioni nella parte inferiore delle finestre principali e utilizzano questo messaggio per visualizzare informazioni aggiuntive sulla voce di menu selezionata.

Quando l'utente sceglie un elemento di comando da un menu, il sistema invia un messaggio di [**\_ comando WM**](wm-command.md) alla routine della finestra. La parola più bassa del parametro *wParam* del messaggio del **\_ comando WM** contiene l'identificatore dell'elemento scelto. La routine della finestra deve esaminare l'identificatore ed elaborare di conseguenza il messaggio.

È possibile salvare le informazioni per un menu usando la struttura [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) . Se il menu è definito con un **MENUINFO**. valore **dwStyle** di MNS \_ NOTIFYBYPOS, il sistema invia il comando [**WM \_ MENUCOMMAND**](wm-menucommand.md) anziché [**il \_ comando WM**](wm-command.md) quando viene selezionato un elemento. Questo consente di accedere alle informazioni nella struttura **MENUINFO** e fornisce anche l'indice dell'elemento selezionato direttamente.

Non tutti i menu sono accessibili tramite la barra dei menu di una finestra. Molte applicazioni visualizzano i menu di scelta rapida quando l'utente fa clic con il pulsante destro del mouse in una posizione specifica. Tali applicazioni devono elaborare il messaggio [**WM \_ ContextMenu**](wm-contextmenu.md) e visualizzare un menu di scelta rapida, se appropriato. Se un'applicazione non visualizza un menu di scelta rapida, deve passare il messaggio **WM \_ ContextMenu** alla funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

Il messaggio [**WM \_ MENURBUTTONUP**](wm-menurbuttonup.md) viene inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova in una voce di menu. Questo messaggio viene fornito in modo che le applicazioni possano visualizzare un menu di scelta rapida o sensibile al contesto per una voce di menu.

Ci sono alcuni messaggi che coinvolgono solo i menu con trascinamento della selezione. Il [**\_ MENUGETOBJECT WM**](wm-menugetobject.md) viene inviato al proprietario di un menu di trascinamento della selezione quando il cursore del mouse entra in una voce di menu o passa dal centro di un elemento alla parte superiore o inferiore di un elemento. Il messaggio [**WM \_ MENUDRAG**](wm-menudrag.md) viene inviato quando l'utente trascina effettivamente una voce di menu.

Quando un menu a discesa o un sottomenu è stato eliminato definitivamente, il sistema invia un messaggio [**WM \_ UNINITMENUPOPUP**](wm-uninitmenupopup.md) .

## <a name="menu-destruction"></a>Distruzione di menu

Se un menu viene assegnato a una finestra e tale finestra viene distrutta, il sistema distrugge automaticamente il menu e i relativi sottomenu, liberando il punto di controllo del menu e la memoria occupata dal menu. Il sistema non elimina automaticamente un menu non assegnato a una finestra. Un'applicazione deve eliminare il menu non assegnato chiamando la funzione [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) . In caso contrario, il menu continua a esistere in memoria anche dopo la chiusura dell'applicazione. Per terminare il menu attivo del thread chiamante, usare [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Se una piattaforma non supporta **EndMenu**, inviare il proprietario del menu attivo a [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) Message.

 

 