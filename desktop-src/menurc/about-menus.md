---
title: Informazioni sui menu
description: Questo argomento illustra i menu.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- risorse, menu
- menu, informazioni
- Sottomenu
- barre dei menu
- menu di primo livello
- scelta rapida (menu)
- menu a discesa
- menu, livello superiore
- menu, popup
- menu, elenco a discesa
- nomi dei menu
- menu, collegamento
- menu, finestra
- menu, sistema
- menu, controllo
- menu di scelta rapida
- Menu Finestra
- Menu di sistema
- Menu Di controllo
- identificatori della Guida
- handle di menu
- voci di menu
- elementi di comando
- identificatori di voci di menu
- posizione della voce di menu
- selezione di voci di menu
- cancellazione di voci di menu
- menu disegnati dal proprietario
- menu, proprietario disegnato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d35ddf55ad31ed27cc12c6adffa5517e0081db6d70b4d01d3b88780a8797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034494"
---
# <a name="about-menus"></a>Informazioni sui menu

Un *menu* è un elenco di elementi che specificano opzioni o gruppi di opzioni (un sottomenu) per un'applicazione. Se si fa clic su una voce di menu, viene aperto un sottomenu o l'applicazione eseguirà un comando. In questa sezione vengono fornite informazioni sugli argomenti seguenti:

-   [Barre dei menu e menu](#menu-bars-and-menus)
    -   [Menu di scelta rapida](#shortcut-menus)
    -   [Menu finestra](#the-window-menu)
    -   [Identificatore della Guida](#help-identifier)
-   [Accesso tramite tastiera ai menu](#keyboard-access-to-menus)
    -   [Interfaccia della tastiera standard](#standard-keyboard-interface)
    -   [Tasti di scelta dei menu](#menu-access-keys)
    -   [Tasti di scelta rapida del menu](#menu-shortcut-keys)
-   [Creazione di menu](#menu-creation)
    -   [Risorse del modello di menu](#menu-template-resources)
    -   [Modello di menu in memoria](#menu-template-in-memory)
    -   [Quadratini di ridimensionamento dei menu](#menu-handles)
    -   [Funzioni di creazione dei menu](#menu-creation-functions)
    -   [Visualizzazione menu](#menu-display)
    -   [Menu della classe Window](#window-class-menus)
-   [Voci di menu](#menu-items)
    -   [Elementi ed elementi di comando che aprono sottomenu](#command-items-and-items-that-open-submenus)
    -   [Identificatore voce di menu](#menu-item-identifier)
    -   [Posizione voce di menu](#menu-item-position)
    -   [Accesso alle voci di menu a livello di codice](#accessing-menu-items-programmatically)
    -   [Voci di menu predefinite](#default-menu-items)
    -   [Voci di menu selezionate e cancellabili](#selected-and-clear-menu-items)
    -   [Voci di menu abilitate, in grigio e disabilitate](#enabled-grayed-and-disabled-menu-items)
    -   [Voci di menu evidenziate](#highlighted-menu-items)
    -   [Voci di menu disegnate dal proprietario](#owner-drawn-menu-items)
    -   [Separatori di voci di menu e interruzioni di riga](#menu-item-separators-and-line-breaks)
-   [Messaggi usati con i menu](#messages-used-with-menus)
-   [Distruzione dei menu](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Barre dei menu e menu

Un menu è organizzato in una gerarchia. Al livello superiore della gerarchia è disponibile la *barra dei menu*. che contiene un elenco *di menu*, che a sua volta possono contenere *sottomenu*. Una barra dei menu viene talvolta definita *menu* di primo livello e i menu e i sottomenu sono noti anche come *menu popup.*

Una voce di menu può eseguire un comando o aprire un sottomenu. Un elemento che esegue un comando è detto elemento *di comando* o *comando*.

Un elemento nella barra dei menu apre quasi sempre un menu. Le barre dei menu contengono raramente voci di comando. Un menu aperto dalla barra dei menu viene visualizzato a discesa dalla barra dei menu e viene talvolta definito *menu a discesa.* Quando viene visualizzato, un menu a discesa viene collegato alla barra dei menu. Una voce di menu sulla barra dei menu che apre un menu a discesa è detta *anche nome di menu*.

I nomi dei menu in una barra dei menu rappresentano le categorie principali di comandi forniti da un'applicazione. La selezione di un nome di menu dalla barra dei menu in genere apre un menu le cui voci di menu corrispondono ai comandi di una categoria. Ad esempio, una barra dei menu potrebbe contenere un nome di menu **File** che, quando viene selezionato dall'utente, attiva un menu con voci di menu quali **Nuovo** **,** Apri e **Salva**. Per ottenere informazioni su una barra dei menu, chiamare [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Solo una finestra sovrapposta o popup può contenere una barra dei menu. una finestra figlio non può contenere una finestra. Se la finestra ha una barra del titolo, il sistema posiziona la barra dei menu appena sotto di essa. Una barra dei menu è sempre visibile. Un sottomenu non è tuttavia visibile finché l'utente non seleziona una voce di menu che lo attiva. Per altre informazioni sulle finestre sovrapposte e popup, vedere [Tipi di finestra](/windows/desktop/winmsg/window-features).

Ogni menu deve avere una finestra proprietaria. Il sistema invia messaggi alla finestra proprietaria di un menu quando l'utente seleziona il menu o sceglie una voce dal menu.

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Menu di scelta rapida](#shortcut-menus)
-   [Menu finestra](#the-window-menu)
-   [Identificatore della Guida](#help-identifier)

### <a name="shortcut-menus"></a>Menu di scelta rapida

Il sistema fornisce anche *menu di scelta rapida.* Un menu di scelta rapida non è collegato alla barra dei menu. può essere visualizzata in qualsiasi punto dello schermo. Un'applicazione associa in genere un menu di scelta rapida a una parte di una finestra, ad esempio l'area client, o a un oggetto specifico, ad esempio un'icona. Per questo motivo, questi menu sono chiamati anche *menu di scelta rapida.*

Un menu di scelta rapida rimane nascosto fino a quando l'utente non lo attiva, in genere facendo clic con il pulsante destro del mouse su una selezione, una barra degli strumenti o un pulsante della barra delle applicazioni. Il menu viene in genere visualizzato in corrispondenza della posizione del cursore del cursore del mouse o del cursore del mouse.

### <a name="the-window-menu"></a>Menu finestra

Il  menu Finestra (noto anche come **menu** Sistema o **Menu** di controllo) è un menu a comparsa definito e gestito quasi esclusivamente dal sistema operativo. L'utente può aprire il menu della finestra facendo clic sull'icona dell'applicazione sulla barra del titolo o facendo clic con il pulsante destro del mouse in un punto qualsiasi della barra del titolo.

Il menu **Finestra** fornisce un set standard di voci di menu che l'utente può scegliere di modificare le dimensioni o la posizione di una finestra o chiudere l'applicazione. Le voci del menu della finestra possono essere aggiunte, eliminate e modificate, ma la maggior parte delle applicazioni usa semplicemente il set standard di voci di menu. Una finestra sovrapposta, popup o figlio può avere un menu finestra. Non è insolito che una finestra sovrapposta o popup non includa un menu finestra.

Quando l'utente sceglie un comando dal menu **Finestra,** il sistema invia un messaggio [**\_ SYSCOMMAND WM**](wm-syscommand.md) alla finestra proprietaria del menu. Nella maggior parte delle applicazioni, la routine della finestra non elabora i messaggi dal menu della finestra. Al contrario, passa semplicemente i messaggi alla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita del messaggio. Se un'applicazione aggiunge un comando al menu della finestra, la routine della finestra deve elaborare il comando.

Un'applicazione può usare [**la funzione GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) per creare una copia del menu della finestra predefinita da modificare. Qualsiasi finestra che non usa la **funzione GetSystemMenu** per creare una propria copia del menu della finestra riceve il menu della finestra standard.

### <a name="help-identifier"></a>Identificatore della Guida

Associato a ogni barra dei menu, menu, sottomenu e menu di scelta rapida è un identificatore della Guida. Se l'utente preme il tasto F1 mentre il menu è attivo, questo valore viene inviato alla finestra proprietaria come parte di un [**messaggio WM \_ HELP.**](../shell/wm-help.md)

## <a name="keyboard-access-to-menus"></a>Accesso tramite tastiera ai menu

Il sistema fornisce un'interfaccia da tastiera standard per i menu. È possibile migliorare questa interfaccia fornendo tasti di scelta rapida mnemoici e tasti di scelta rapida per le voci di menu.

Gli argomenti seguenti descrivono l'interfaccia della tastiera standard, i tasti di scelta rapida e i tasti di scelta rapida:

-   [Interfaccia della tastiera standard](#standard-keyboard-interface)
-   [Tasti di scelta dei menu](#menu-access-keys)
-   [Tasti di scelta rapida del menu](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interfaccia della tastiera standard

Il sistema è progettato per funzionare con o senza un mouse o un altro dispositivo di puntamento. Poiché il sistema fornisce un'interfaccia da tastiera standard, l'utente può usare la tastiera per selezionare le voci di menu. Questa interfaccia della tastiera non richiede codice speciale. Un'applicazione riceve un messaggio di comando se l'utente seleziona una voce di menu tramite la tastiera o tramite un mouse. L'interfaccia della tastiera standard elabora le sequenze di tasti seguenti.



| Combinazioni di tasti              | Azione                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Carattere alfabetico | Seleziona la prima voce di menu con il carattere specificato come tasto di scelta. Se l'elemento selezionato richiama un menu, viene visualizzato il menu e viene evidenziato il primo elemento. In caso contrario, viene scelta la voce di menu.                            |
| ALT                    | Attiva e disattiva la modalità barra dei menu.                                                                                                                                                                                                     |
| ALT+BARRA SPAZIATRICE           | Visualizza il menu della finestra.                                                                                                                                                                                                                |
| INVIO                  | Attiva un menu e seleziona la prima voce di menu se a una voce è associato un menu. In caso contrario, questa sequenza di tasti sceglie l'elemento come se l'utente rilascia il pulsante del mouse mentre l'elemento è stato selezionato.                              |
| ESC                    | Esce dalla modalità menu.                                                                                                                                                                                                                         |
| FRECCIA SINISTRA             | Scorre la voce di menu di primo livello precedente. Le voci di menu di primo livello includono i nomi dei menu e il menu della finestra. Se la voce selezionata si trova in un menu, viene selezionata la colonna precedente del menu o la voce di menu di primo livello precedente. |
| FRECCIA DESTRA            | Funziona come il tasto FRECCIA SINISTRA, tranne nella direzione opposta. Nei menu questa sequenza di tasti viene spostata in avanti di una colonna. quando l'elemento attualmente selezionato si trova nella colonna all'estrema destra, viene selezionato il menu successivo.                              |
| FRECCE SU o FRECCIA GIÙ      | Attiva un menu quando viene premuto in un nome di menu. Quando viene premuto in un menu, la combinazione di tasti FRECCIA SU seleziona l'elemento precedente. la combinazione di tasti FRECCIA GIÙ seleziona l'elemento successivo.                                                                  |



 

### <a name="menu-access-keys"></a>Tasti di scelta dei menu

L'interfaccia della tastiera standard per i menu può essere migliorata aggiungendo tasti di scelta (tasti di scelta) alle voci di menu. Un tasto di scelta è una lettera sottolineata nel testo di una voce di menu. Quando un menu è attivo, l'utente può selezionare una voce di menu premendo il tasto corrispondente alla lettera sottolineata dell'elemento. L'utente rende attiva la barra dei menu premendo ALT per evidenziare la prima voce della barra dei menu. Un menu è attivo quando viene visualizzato.

Per creare un tasto di scelta per una voce di menu, far precedere qualsiasi carattere nella stringa di testo dell'elemento con una e commerciale. Ad esempio, la stringa di testo "&Move" fa sì che il sistema sottolinei la lettera "M".

### <a name="menu-shortcut-keys"></a>Tasti di scelta rapida del menu

Oltre a disporre di un tasto di scelta, a una voce di menu può essere associato un tasto di scelta rapida. Un tasto di scelta rapida è diverso da un tasto di scelta, perché il menu non deve essere attivo per il funzionamento del tasto di scelta rapida. Inoltre, un tasto  di scelta è sempre associato a una voce di menu, mentre un tasto di scelta rapida è in genere *(ma* non deve essere) associato a una voce di menu.

Il testo che identifica il tasto di scelta rapida viene aggiunto alla stringa di testo della voce di menu. Il testo del collegamento viene visualizzato a destra del nome della voce di menu, dopo una barra rovesciata e un carattere di tabulazione \\ (t). Ad esempio, "&Chiudi tAlt+F4" rappresenta un comando Chiudi con la combinazione di tasti ALT+F4 come tasto di scelta rapida e con la lettera "C" come tasto di \\ scelta. Per altre informazioni, vedere [Tasti di scelta rapida.](keyboard-accelerators.md)

## <a name="menu-creation"></a>Creazione di menu

È possibile creare un menu usando un modello di menu o funzioni di creazione di menu. I modelli di menu sono in genere definiti come risorse. Le risorse del modello di menu possono essere caricate in modo esplicito o assegnate come menu predefinito per una classe finestra. È anche possibile creare risorse modello di menu in modo dinamico in memoria.

Gli argomenti seguenti descrivono in dettaglio la creazione di menu:

-   [Risorse del modello di menu](#menu-template-resources)
-   [Modello di menu in memoria](#menu-template-in-memory)
-   [Quadratini di ridimensionamento dei menu](#menu-handles)
-   [Funzioni di creazione dei menu](#menu-creation-functions)
-   [Visualizzazione menu](#menu-display)
-   [Menu della classe Window](#window-class-menus)

### <a name="menu-template-resources"></a>Risorse del modello di menu

La maggior parte delle applicazioni crea menu usando risorse modello di menu. Un *modello di menu* definisce un menu, incluse le voci nella barra dei menu e tutti i menu. Per informazioni sulla creazione di una risorsa modello di menu, vedere la documentazione inclusa con gli strumenti di sviluppo.

Dopo aver creato una risorsa modello di menu e aggiunta al file eseguibile (.exe) dell'applicazione, è possibile usare la funzione [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) per caricare la risorsa in memoria. Questa funzione restituisce un handle al menu, che è quindi possibile assegnare a una finestra usando la [**funzione SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu) È possibile assegnare un menu a qualsiasi finestra che non sia una finestra figlio.

L'implementazione di menu come risorse semplifica la localizzazione di un'applicazione per l'uso in più paesi/aree geografiche. Solo il file di definizione delle risorse deve essere localizzato per ogni lingua, non per il codice sorgente dell'applicazione.

### <a name="menu-template-in-memory"></a>Modello di menu in memoria

È possibile creare un menu da un modello di menu compilato in memoria in fase di esecuzione. Ad esempio, un'applicazione che consente a un utente di personalizzare il proprio menu potrebbe creare un modello di menu in memoria in base alle preferenze dell'utente. L'applicazione potrebbe quindi salvare il modello in un file o nel Registro di sistema per un uso futuro. Per creare un menu da un modello in memoria, usare la [**funzione LoadMenuIndirect.**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) Per le descrizioni dei formati dei modelli di menu, vedere [Risorse del modello di menu](#menu-template-resources).

Un modello di menu standard è costituito da [**una struttura MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguita da una o più [**strutture MENUITEMTEMPLATE.**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)

Un modello di menu esteso è costituito da [**una struttura MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) seguita da una o più [**strutture MENUEX TEMPLATE \_ \_ ITEM.**](menuex-template-item.md)

### <a name="menu-handles"></a>Quadratini di ridimensionamento dei menu

Il sistema genera un handle univoco per ogni menu. Un *handle di menu* è un valore di tipo **HMENU.** Un'applicazione deve specificare un handle di menu in molte delle funzioni di menu. Si riceve un handle per una barra dei menu quando si crea il menu o si carica una risorsa di menu.

Per recuperare un handle alla barra dei menu per un menu che è stato creato o caricato, usare la [**funzione GetMenu.**](/windows/desktop/api/Winuser/nf-winuser-getmenu) Per recuperare un handle per il sottomenu associato a una voce di menu, usare la [**funzione GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) Per recuperare un handle per un menu di finestra, usare la [**funzione GetSystemMenu.**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)

### <a name="menu-creation-functions"></a>Funzioni di creazione dei menu

Usando le funzioni di creazione dei menu, è possibile creare menu in fase di esecuzione o aggiungere voci di menu ai menu esistenti. È possibile usare la [**funzione CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) per creare una barra dei menu vuota e la [**funzione CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) per creare un menu vuoto. È possibile salvare determinate informazioni sulle impostazioni per un menu usando la [**struttura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Per ottenere o recuperare le impostazioni di un menu, usare [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) o [**SetMenuInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) Per aggiungere elementi a un menu, usare la [**funzione InsertMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) Le funzioni [**AppendMenu e**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu precedenti**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) sono ancora supportate, ma **InsertMenuItem** deve essere usato per le nuove applicazioni.

### <a name="menu-display"></a>Visualizzazione menu

Dopo che un menu è stato caricato o creato, deve essere assegnato a una finestra prima che il sistema possa visualizzarlo. È possibile assegnare un menu definendo un menu di classe. Per altre informazioni, vedere [Menu di classe finestra.](#window-class-menus) Puoi anche assegnare un menu a una finestra specificando un handle per il menu come parametro *hMenu* della funzione [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oppure chiamando la [**funzione SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu)

Per visualizzare un menu di scelta rapida, [**usare la funzione TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) I menu di scelta rapida, detti anche menu a comparsa mobili o menu di scelta rapida, vengono in genere visualizzati quando viene elaborato il messaggio [**WM \_ CONTEXTMENU.**](wm-contextmenu.md)

È possibile assegnare un menu a qualsiasi finestra che non sia una finestra figlio.

La funzione [**TrackPopupMenu precedente**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) è ancora supportata, ma le nuove applicazioni devono usare la [**funzione TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)

### <a name="window-class-menus"></a>Menu della classe Window

È possibile specificare un menu predefinito, denominato *menu di classe,* quando si registra una classe di finestra. A tale scopo, assegnare il nome della risorsa modello di menu al membro **lpszMenuName** della [**struttura WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) usata per registrare la classe.

Per impostazione predefinita, a ogni finestra viene assegnato il menu della classe per la relativa classe di finestra, quindi non è necessario caricare il menu in modo esplicito e assegnarlo a ogni finestra. È possibile eseguire l'override del menu della classe specificando un handle di menu diverso in una chiamata alla [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) È anche possibile modificare il menu di una finestra dopo la creazione usando la [**funzione SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu) Per altre informazioni, vedere [Classi window.](/windows/desktop/winmsg/window-classes)

## <a name="menu-items"></a>Voci di menu

Gli argomenti seguenti illustrano le operazioni che il sistema esegue quando l'utente sceglie una voce di menu e i modi in cui un'applicazione può controllare l'aspetto e le funzionalità di un elemento:

-   [Elementi di comando ed elementi che aprono sottomenu](#command-items-and-items-that-open-submenus)
-   [Identificatore voce di menu](#menu-item-identifier)
-   [Posizione voce di menu](#menu-item-position)
-   [Accesso alle voci di menu a livello di codice](#accessing-menu-items-programmatically)
-   [Voci di menu predefinite](#default-menu-items)
-   [Voci di menu selezionate e cancellabili](#selected-and-clear-menu-items)
-   [Voci di menu Abilitata, Disattivata e Disabilitata](#enabled-grayed-and-disabled-menu-items)
-   [Voci di menu evidenziate](#highlighted-menu-items)
-   [Voci di menu disegnate dal proprietario](#owner-drawn-menu-items)
-   [Separatori di voci di menu e interruzioni di riga](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Elementi di comando ed elementi che aprono sottomenu

Quando l'utente sceglie un elemento di comando, il sistema invia un messaggio di comando alla finestra proprietaria del menu. Se l'elemento di comando si trova nel menu della finestra, il sistema invia il [**messaggio \_ SYSCOMMAND WM.**](wm-syscommand.md) In caso contrario, invia il [**messaggio WM \_ COMMAND.**](wm-command.md)

Associato a ogni voce di menu che apre un sottomenu è un handle per il sottomenu corrispondente. Quando l'utente punta a un elemento di questo tipo, il sistema apre il sottomenu. Nessun messaggio di comando viene inviato alla finestra del proprietario. Tuttavia, il sistema invia un [**messaggio \_ WM INITMENUPOPUP**](wm-initmenupopup.md) alla finestra proprietaria prima di visualizzare il sottomenu. È possibile ottenere un handle per il sottomenu associato a un elemento usando la [**funzione GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) o [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Una barra dei menu contiene in genere nomi di menu, ma può anche contenere voci di comando. Un sottomenu contiene in genere elementi di comando, ma può anche contenere elementi che aprono sottomenu annidati. Aggiungendo tali elementi ai sottomenu, è possibile annidare i menu a qualsiasi profondità. Per fornire un segnale visivo all'utente, il sistema visualizza automaticamente una piccola freccia a destra del testo di una voce di menu che apre un sottomenu.

### <a name="menu-item-identifier"></a>Menu-Item identificatore

Associato a ogni voce di menu è un intero univoco definito dall'applicazione, denominato identificatore *di voce di menu*. Quando l'utente sceglie una voce di comando da un menu, il sistema invia l'identificatore dell'elemento alla finestra proprietaria come parte di un [**messaggio WM \_ COMMAND.**](wm-command.md) La routine della finestra esamina l'identificatore per determinare l'origine del messaggio ed elabora il messaggio di conseguenza. Inoltre, è possibile specificare una voce di menu usando il relativo identificatore quando si chiamano le funzioni di menu. ad esempio per abilitare o disabilitare una voce di menu.

Le voci di menu che aprono sottomenu hanno identificatori esattamente come le voci di comando. Tuttavia, il sistema non invia un messaggio di comando quando tale elemento viene selezionato da un menu. Il sistema apre invece il sottomenu associato alla voce di menu.

Per recuperare l'identificatore della voce di menu in una posizione specificata, usare la [**funzione GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) [**o GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

### <a name="menu-item-position"></a>Menu-Item posizione

Oltre ad avere un identificatore univoco, ogni voce di menu in una barra dei menu o in un menu ha un valore di posizione univoco. L'elemento più a sinistra in una barra dei menu o l'elemento superiore in un menu ha la posizione zero. Il valore della posizione viene incrementato per le voci di menu successive. Il sistema assegna un valore di posizione a tutte le voci di un menu, inclusi i separatori. La figura seguente mostra i valori di posizione delle voci in una barra dei menu e in un menu.

![barra dei menu e menu](images/csemn-01.png)

Quando si chiama una funzione di menu che modifica o recupera informazioni su una voce di menu specifica, è possibile specificare la voce usando il relativo identificatore o la relativa posizione. Per ulteriori informazioni, vedere la sezione successiva.

### <a name="accessing-menu-items-programmatically"></a>Accesso alle voci di menu a livello di codice

La maggior parte delle funzioni di menu consente di specificare una voce di menu in base alla posizione o al comando. Alcune funzioni usano i **flag MF \_ BYPOSITION** e **MF \_ BYCOMMAND** per indicare l'algoritmo di ricerca, mentre altre hanno un parametro *fByPosition* esplicito. Se si specifica la voce di menu in base alla posizione, il numero di voce è un indice in base zero nel menu. Se si specifica la voce di menu in base al comando, nel menu e nei relativi sottomenu viene cercata una voce il cui identificatore di menu è uguale al numero specificato. Se più di una voce nella gerarchia di menu corrisponde al numero di elemento, non viene specificato quale elemento viene usato. Se i menu contengono identificatori di menu duplicati, è consigliabile usare operazioni di menu basate sulla posizione per evitare questa ambiguità.

### <a name="default-menu-items"></a>Voci di menu predefinite

Un sottomenu può contenere una voce di menu predefinita. Quando l'utente apre un sottomenu facendo doppio clic, il sistema invia un messaggio di comando alla finestra proprietaria del menu e chiude il menu come se fosse stata scelta la voce di comando predefinita. Se non è presente alcun elemento di comando predefinito, il sottomenu rimane aperto. Per recuperare e impostare l'elemento predefinito per un sottomenu, usare le [**funzioni GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) [**e SetMenuDefaultItem.**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)

### <a name="selected-and-clear-menu-items"></a>Voci di menu selezionate e cancellabili

Una voce di menu può essere selezionata o deselezionata. Il sistema visualizza una bitmap accanto alle voci di menu selezionate per indicarne lo stato selezionato. Il sistema non visualizza una bitmap accanto a cancella gli elementi, a meno che non venga specificata una bitmap "cancella" definita dall'applicazione. È possibile selezionare solo voci di menu in un menu. Non è possibile selezionare gli elementi in una barra dei menu.

Le applicazioni in genere controllano o deselezionano una voce di menu per indicare se un'opzione è attiva. Si supponga, ad esempio, che un'applicazione abbia una barra degli strumenti che l'utente può visualizzare o nascondere usando un comando **Barra** degli strumenti in un menu. Quando la barra degli strumenti è nascosta, la **voce di** menu Barra degli strumenti è deselezionata. Quando l'utente sceglie il comando, l'applicazione controlla la voce di menu e mostra la barra degli strumenti.

Un attributo con segno di spunta controlla se è selezionata una voce di menu. È possibile impostare l'attributo del segno di spunta di una voce di menu usando la [**funzione CheckMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) È possibile usare la [**funzione GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) per determinare se una voce di menu è attualmente selezionata o deselezionata.

Invece di [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) e [**GetMenuState,**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)puoi usare le funzioni [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) per recuperare e impostare lo stato di controllo di una voce di menu.

In alcuni casi, un gruppo di voci di menu corrisponde a un set di opzioni che si escludono a vicenda. In questo caso, è possibile indicare l'opzione selezionata usando una voce di menu di opzione selezionata (analoga a un controllo pulsante di opzione). Gli elementi di opzione selezionati vengono visualizzati con una bitmap punto elenco anziché con un segno di spunta. Per controllare una voce di menu e impostarla come voce di opzione, usare la [**funzione CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

Per impostazione predefinita, il sistema visualizza un segno di spunta o una bitmap punto elenco accanto alle voci di menu selezionate e nessuna bitmap accanto alle voci di menu deselezionate. È tuttavia possibile usare la [**funzione SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) per associare bitmap selezionate e cancellate definite dall'applicazione a una voce di menu. Il sistema usa quindi le bitmap specificate per indicare lo stato selezionato o cancellato della voce di menu.

Le bitmap definite dall'applicazione associate a una voce di menu devono avere le stesse dimensioni della bitmap del segno di spunta predefinita, le cui dimensioni possono variare a seconda della risoluzione dello schermo. Per recuperare le dimensioni corrette, usare la [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) È possibile creare più risorse bitmap per diverse risoluzioni dello schermo. creare una risorsa bitmap e ridimensionarla, se necessario; oppure creare una bitmap in fase di esecuzione e disegnarne un'immagine. Le bitmap possono essere monocroma o a colori. Tuttavia, poiché le voci di menu vengono invertiti quando sono evidenziate, l'aspetto di determinate bitmap a colori invertiti potrebbe non essere desiderato. Per altre informazioni, vedere [Bitmap .](/windows/desktop/gdi/bitmaps)

### <a name="enabled-grayed-and-disabled-menu-items"></a>Voci di menu abilitate, in grigio e disabilitate

Una voce di menu può essere abilitata, disabilitata o disabilitata. Per impostazione predefinita, è abilitata una voce di menu. Quando l'utente sceglie una voce di menu abilitata, il sistema invia un messaggio di comando alla finestra proprietaria o visualizza il sottomenu corrispondente, a seconda del tipo di voce di menu.

Quando le voci di menu non sono disponibili per l'utente, devono essere disabilitate o disabilitate. Non è possibile scegliere voci di menu disabilitate e disabilitate. Un elemento disabilitato è simile a un elemento abilitato. Quando l'utente fa clic su un elemento disabilitato, l'elemento non viene selezionato e non accade nulla. Gli elementi disabilitati possono essere utili, ad esempio, in un'esercitazione che presenta un menu che sembra attivo ma non lo è.

Un'applicazione grigio una voce di menu non disponibile per fornire un segnale visivo all'utente che un comando non è disponibile. È possibile usare un elemento in grigio quando un'azione non  è appropriata(ad esempio, è possibile usare il comando Stampa nel menu **File** quando nel sistema non è installata una stampante).

La [**funzione EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) abilita, grigio o disabilita una voce di menu. Per determinare se una voce di menu è abilitata, disabilitata o disabilitata, usare la [**funzione GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Anziché [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa), è anche possibile usare la [**funzione GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) per determinare se una voce di menu è abilitata, disabilitata o disabilitata.

### <a name="highlighted-menu-items"></a>Voci di menu evidenziate

Il sistema evidenzia automaticamente le voci di menu nei menu quando l'utente le seleziona. Tuttavia, l'evidenziazione può essere aggiunta o rimossa in modo esplicito da un nome di menu sulla barra dei menu usando la [**funzione HiliteMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) Questa funzione non ha alcun effetto sulle voci di menu nei menu. Quando **hiliteMenuItem viene** usato per evidenziare un nome di menu, tuttavia, il nome sembra essere selezionato solo. Se l'utente preme INVIO, l'elemento evidenziato non viene scelto. Questa funzionalità può essere utile, ad esempio, in un'applicazione di training che illustra l'uso dei menu.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn di menu

Un'applicazione può controllare completamente l'aspetto di una voce di menu usando una *voce disegnata dal proprietario.* Gli elementi disegnati dal proprietario richiedono che un'applicazione si prenda la responsabilità totale per disegnare gli stati selezionati (evidenziati), selezionati e cancellati. Ad esempio, se un'applicazione ha fornito un menu del tipo di carattere, può disegnare ogni voce di menu usando il tipo di carattere corrispondente. l'elemento per Roman verrebbe disegnato con il carattere roman, l'elemento per il corsivo verrebbe disegnato in corsivo e così via. Per altre informazioni, vedere [Creazione di Owner-Drawn di menu.](using-menus.md)

### <a name="menu-item-separators-and-line-breaks"></a>Separatori di voci di menu e interruzioni di riga

Il sistema fornisce un tipo speciale di voce di menu, denominata *separatore*, che viene visualizzata come linea orizzontale. È possibile usare un separatore per dividere un menu in gruppi di elementi correlati. Non è possibile usare un separatore in una barra dei menu e l'utente non può selezionare un separatore.

Quando una barra dei menu contiene più nomi di menu di quelli contenuti in una riga, il sistema esegue il wrapping della barra dei menu suddividendo automaticamente la barra in due o più righe. È possibile fare in modo che un'interruzione di riga si verifichi in corrispondenza di una voce specifica di una barra dei menu assegnando il flag di tipo **\_ MENUBREAK MFT** all'elemento. Il sistema inserisce l'elemento e tutti gli elementi successivi in una nuova riga.

Quando un menu contiene più voci di quelle contenute in una colonna, il menu verrà troncato. È possibile fare in modo che un'interruzione di colonna si verifichi in corrispondenza di una voce specifica di un menu assegnando il flag di tipo **MFT \_ MENUBREAK** alla voce o usando l'opzione MENUBREAK [nell'istruzione MENUITEM.](/windows/desktop/menurc/menuitem-statement) Il sistema inserisce tale elemento e tutti gli elementi successivi in una nuova colonna. Il flag **di tipo \_ MFT MENUBARBREAK** ha lo stesso effetto, ad eccezione del fatto che viene visualizzata una linea verticale tra la nuova colonna e quella precedente.

Se si usano le funzioni [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)o [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) per assegnare interruzioni di riga, è necessario assegnare i flag di tipo **MF \_ MENUBREAK** o **MF \_ MENUBARBREAK**.

## <a name="messages-used-with-menus"></a>Messaggi usati con i menu

Il sistema segnala l'attività correlata al menu inviando messaggi alla routine della finestra proprietaria del menu. Il sistema invia una serie di messaggi quando l'utente seleziona elementi sulla barra dei menu o fa clic sul pulsante destro del mouse per visualizzare un menu di scelta rapida.

Quando l'utente attiva un elemento sulla barra dei menu, la finestra proprietaria riceve prima un [**messaggio \_ SYSCOMMAND WM.**](wm-syscommand.md) Questo messaggio include un flag che indica se l'utente ha attivato il menu usando la tastiera (SC \_ KEYMENU) o il mouse (SC \_ MOUSEMENU). Per altre informazioni, vedere [Accesso tramite tastiera ai menu](#keyboard-access-to-menus).

Successivamente, prima di visualizzare i menu, il sistema invia il messaggio [**WM \_ INITMENU**](wm-initmenu.md) alla routine della finestra in modo che un'applicazione possa modificare i menu prima che l'utente li veda. Il sistema invia il messaggio **WM \_ INITMENU** una sola volta per ogni attivazione del menu.

Quando l'utente punta a una voce di menu che apre un sottomenu, il sistema invia alla finestra proprietaria il messaggio [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) prima di visualizzare il sottomenu. Questo messaggio offre all'applicazione la possibilità di modificare il sottomenu prima che venga visualizzato.

Ogni volta che l'utente sposta l'evidenziazione da un elemento a un altro, il sistema invia un messaggio [**WM \_ MENUSELECT**](wm-menuselect.md) alla procedura della finestra della finestra proprietaria del menu. Questo messaggio identifica la voce di menu attualmente selezionata. Molte applicazioni forniscono un'area di informazioni nella parte inferiore delle finestre principali e usano questo messaggio per visualizzare informazioni aggiuntive sulla voce di menu selezionata.

Quando l'utente sceglie una voce di comando da un menu, il sistema invia un [**messaggio WM \_ COMMAND**](wm-command.md) alla routine della finestra. La parola di ordine basso del parametro *wParam* del messaggio **WM \_ COMMAND** contiene l'identificatore dell'elemento scelto. La routine della finestra deve esaminare l'identificatore ed elaborare il messaggio di conseguenza.

È possibile salvare le informazioni per un menu usando la [**struttura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Se il menu è definito con **menuINFO**. **dwStyle valore** di MNS \_ NOTIFYBYPOS, il sistema invia [**WM \_ MENUCOMMAND**](wm-menucommand.md) anziché [**WM \_ COMMAND**](wm-command.md) quando viene selezionato un elemento. Ciò consente di accedere alle informazioni nella **struttura MENUINFO** e fornisce direttamente l'indice dell'elemento selezionato.

Non tutti i menu sono accessibili tramite la barra dei menu di una finestra. Molte applicazioni visualizzano i menu di scelta rapida quando l'utente fa clic con il pulsante destro del mouse in una posizione specifica. Tali applicazioni devono elaborare il [**messaggio WM \_ CONTEXTMENU**](wm-contextmenu.md) e visualizzare un menu di scelta rapida, se appropriato. Se un'applicazione non visualizza un menu di scelta rapida, deve passare il **messaggio WM \_ CONTEXTMENU** alla [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) per l'elaborazione predefinita.

Il [**messaggio WM \_ MENURBUTTONUP**](wm-menurbuttonup.md) viene inviato quando l'utente rilascia il pulsante destro del mouse mentre il cursore si trova su una voce di menu. Questo messaggio viene fornito in modo che le applicazioni possano visualizzare un menu di scelta rapida o sensibile al contesto per una voce di menu.

Esistono alcuni messaggi che coinvolgono solo menu di trascinamento della selezione. [**WM \_ MENUGETOBJECT**](wm-menugetobject.md) viene inviato al proprietario di un menu di trascinamento della selezione quando il cursore del mouse entra in una voce di menu o si sposta dal centro di una voce alla parte superiore o inferiore di una voce. Il [**messaggio WM \_ MENUDRAG**](wm-menudrag.md) viene inviato quando l'utente trascina effettivamente una voce di menu.

Quando un menu a discesa o un sottomenu è stato eliminato, il sistema invia un messaggio [**WM \_ UNINITMENUPOPUP.**](wm-uninitmenupopup.md)

## <a name="menu-destruction"></a>Distruzione dei menu

Se un menu viene assegnato a una finestra e tale finestra viene distrutta, il sistema elimina automaticamente il menu e i relativi sottomenu, liberando l'handle del menu e la memoria occupata dal menu. Il sistema non elimina automaticamente un menu non assegnato a una finestra. Un'applicazione deve eliminare il menu non assegnato chiamando la [**funzione DestroyMenu.**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) In caso contrario, il menu continua a esistere in memoria anche dopo la chiusura dell'applicazione. Per terminare il menu attivo del thread chiamante, usare [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Se una piattaforma non supporta **EndMenu,** inviare al proprietario del menu attivo un [**messaggio WM \_ CANCELMODE.**](/windows/desktop/winmsg/wm-cancelmode)

 

 