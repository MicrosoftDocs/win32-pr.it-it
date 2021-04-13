---
title: Implementazione di una visualizzazione cartelle
description: Windows Shell fornisce un'implementazione predefinita della visualizzazione cartelle, colloquialmente noto come DefView, in modo che sia possibile evitare la maggior parte delle operazioni di implementazione dell'estensione dello spazio dei nomi.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- oggetto visualizzazione cartella
- IShellView
- IShellBrowser, oggetti visualizzazione cartella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/11/2020
ms.locfileid: "104399869"
---
# <a name="implementing-a-folder-view"></a>Implementazione di una visualizzazione cartelle

Windows Shell fornisce un'implementazione predefinita della visualizzazione cartelle, colloquialmente noto come DefView, in modo che sia possibile evitare la maggior parte delle operazioni di implementazione dell'estensione dello spazio dei nomi. Poiché alcune funzionalità di visualizzazione non possono essere realizzate tramite visualizzazioni personalizzate, è spesso consigliabile usare l'oggetto visualizzazione cartella di sistema predefinito al posto di una visualizzazione personalizzata. Per ulteriori informazioni, vedere [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). Nella parte restante di questo argomento viene illustrata l'implementazione di una visualizzazione cartella personalizzata che non supporta le funzionalità di visualizzazione più recenti.

A differenza della visualizzazione albero, Esplora risorse non gestisce il contenuto di una visualizzazione cartelle. La finestra visualizzazione cartelle ospita invece una finestra figlio fornita dall'oggetto Folder. L'oggetto Folder è responsabile della creazione di un oggetto visualizzazione cartella per visualizzare il contenuto della cartella nella finestra figlio.

La chiave per implementare un oggetto visualizzazione cartella è l'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Questa interfaccia viene utilizzata da Esplora risorse per comunicare con l'oggetto visualizzazione cartella. Prima di visualizzare una visualizzazione cartelle, Esplora risorse chiama il metodo [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) dell'oggetto Folder con *riid* impostato su IID \_ IShellView. Creare un oggetto visualizzazione cartelle e restituire l'interfaccia **IShellView** . L'oggetto visualizzazione cartelle deve quindi creare una finestra figlio della finestra visualizzazione cartelle e utilizzare la finestra figlio per visualizzare le informazioni relative al contenuto della cartella.

Oltre a controllare la modalità di visualizzazione dei dati, le estensioni possono anche personalizzare una serie di funzionalità di Esplora risorse. Ad esempio, un'estensione può aggiungere elementi alla barra degli strumenti o alla barra dei menu o visualizzare informazioni sulla barra di stato.

-   [Oggetto visualizzazione cartella](#the-folder-view-object)
-   [Inizializzazione dell'oggetto visualizzazione cartella](#initializing-the-folder-view-object)
-   [Visualizzazione della visualizzazione cartelle](#displaying-the-folder-view)
-   [Implementazione di IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [Aggiorna](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [Uso di IShellBrowser per comunicare con Esplora risorse](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Modifica della barra dei menu di Esplora risorse](#modifying-the-windows-explorer-menu-bar)
    -   [Modifica della barra degli strumenti di Esplora risorse](#modifying-the-windows-explorer-toolbar)
    -   [Modifica della barra di stato di Esplora risorse](#modifying-the-windows-explorer-status-bar)
    -   [Archiviazione di informazioni specifiche della visualizzazione](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>Oggetto visualizzazione cartella

Un oggetto visualizzazione cartella è un oggetto Component Object Model (COM) che espone un'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Questo oggetto è responsabile di:

-   Creazione di una finestra figlio della finestra visualizzazione cartelle e relativa utilizzo per visualizzare il contenuto della cartella.
-   Gestione della comunicazione con Esplora risorse.
-   Aggiunta di comandi specifici per la cartella alla barra dei menu e della barra degli strumenti di Esplora risorse e gestione di tali comandi quando sono selezionati.
-   Gestione dell'interazione utente con la finestra visualizzazione cartelle, ad esempio la visualizzazione di menu di scelta rapida o la gestione delle operazioni di trascinamento della selezione.

In questo documento vengono illustrati i primi tre argomenti. Poiché l'interazione dell'utente con la visualizzazione cartelle avviene all'interno della finestra figlio, l'oggetto visualizzazione cartella è responsabile della relativa gestione come per qualsiasi altra finestra.

Esplora risorse richiede un oggetto visualizzazione cartelle chiamando [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) dell'oggetto Folder con *riid* impostato su IID \_ IShellView. La procedura per la creazione di una visualizzazione cartella è la seguente:

1.  L'oggetto Folder Crea una nuova istanza dell'oggetto visualizzazione cartella e restituisce un puntatore alla relativa interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) .
2.  Esplora risorse Inizializza l'oggetto visualizzazione cartelle chiamando il metodo [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Creare una finestra figlio della finestra visualizzazione cartelle e restituire il relativo handle a Esplora risorse.
3.  L'oggetto visualizzazione cartelle utilizza l'interfaccia [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) di Esplora risorse per personalizzare la barra degli strumenti di Esplora risorse, la barra dei menu e la barra di stato.
4.  Nell'oggetto visualizzazione cartella viene visualizzato il contenuto della cartella nella finestra figlio.
5.  L'oggetto visualizzazione cartella gestisce l'interazione dell'utente con la visualizzazione cartelle e qualsiasi barra degli strumenti o barra dei menu specifica della cartella.

## <a name="initializing-the-folder-view-object"></a>Inizializzazione dell'oggetto visualizzazione cartella

Esplora risorse Inizializza l'oggetto visualizzazione cartelle chiamando il metodo [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . I parametri del metodo forniscono all'oggetto visualizzazione cartelle le informazioni necessarie per creare la finestra figlio che verrà usata per visualizzare il contenuto della cartella:

-   Puntatore all'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) dell'oggetto visualizzazione della cartella precedente. Questo parametro può essere impostato su **null**.
-   Struttura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) che contiene le impostazioni della visualizzazione della cartella precedente.
-   Puntatore all'interfaccia [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) di Esplora risorse.
-   Struttura [Rect](/previous-versions//ms536136(v=vs.85)) con le dimensioni della finestra di visualizzazione cartelle.

Il metodo [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) viene chiamato prima che l'oggetto visualizzazione della cartella precedente venga eliminato definitivamente. Il puntatore all'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) consente quindi di comunicare con l'oggetto visualizzazione cartella precedente. Questa interfaccia è particolarmente utile se la cartella precedente apparteneva all'estensione e usava lo stesso schema di visualizzazione. In tal caso, è possibile comunicare con l'oggetto visualizzazione cartella precedente a scopo di questo tipo, come lo scambio di impostazioni private.

Un modo semplice per determinare se il puntatore [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) appartiene all'estensione consiste nel fare in modo che tutti gli oggetti visualizzazione cartella espongano un'interfaccia privata. Chiamare [IShellView:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per richiedere l'interfaccia privata ed esaminare il valore restituito per determinare se l'oggetto visualizzazione cartella è uno dei propri. È quindi possibile usare un metodo privato su tale interfaccia per scambiare informazioni.

La struttura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) contiene le impostazioni di visualizzazione della visualizzazione cartella precedente. L'impostazione principale è la modalità di visualizzazione: icona grande, icona piccola, elenco o dettagli. È inoltre disponibile un flag che contiene le impostazioni di un'ampia gamma di opzioni di visualizzazione, ad esempio se la visualizzazione deve essere allineata a sinistra. La visualizzazione della cartella deve seguire queste impostazioni nella misura massima consentita per offrire agli utenti un'esperienza coerente mentre passano da una cartella all'altra. È consigliabile archiviare questa struttura e aggiornarla in caso di modifica delle impostazioni. Esplora risorse chiama [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) per ottenere il valore più recente di questa struttura prima di aprire la visualizzazione cartella successiva.

L'interfaccia [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) viene esposta da Esplora risorse. Questa interfaccia è complementare a [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) e consente a un oggetto visualizzazione cartella di comunicare con Esplora risorse. Non esiste un altro modo per recuperare questo puntatore di interfaccia, quindi l'oggetto visualizzazione cartelle deve archiviarlo per un uso successivo. In particolare, sarà necessario chiamare [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) per recuperare la finestra di visualizzazione della cartella padre che si userà per creare la finestra figlio. Si noti che il metodo IShellBrowser:: GetWindow non è incluso nella documentazione di **IShellBrowser** perché viene ereditato da [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow). Dopo l'archiviazione del puntatore a interfaccia, ricordarsi di chiamare [IShellBrowser:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) per incrementare il conteggio dei riferimenti dell'interfaccia. Quando l'interfaccia non è più necessaria, chiamare [IShellBrowser:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

Per creare la finestra figlio:

1.  Esaminare le strutture [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) e [Rect](/previous-versions//ms536136(v=vs.85)) .
2.  Se necessario, ottenere le impostazioni private dall'oggetto visualizzazione cartella precedente.
3.  Chiamare [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) per recuperare la finestra di visualizzazione della cartella padre.
4.  Creare un elemento figlio della finestra di visualizzazione cartelle ottenuta nel passaggio precedente e restituirlo a Esplora risorse.

## <a name="displaying-the-folder-view"></a>Visualizzazione della visualizzazione cartelle

Dopo aver creato la finestra figlio e averla restituita a Esplora risorse, è possibile visualizzare il contenuto della cartella. In genere, le estensioni visualizzano le informazioni con la finestra figlio che ospita un [controllo visualizzazione elenco](../controls/list-view-control-reference.md) o un **controllo WebBrowser**. Il controllo visualizzazione elenco consente di replicare la [visualizzazione classica](web-view.md)di Esplora risorse. Il controllo WebBrowser consente di usare un documento DHTML (Dynamic HTML) per visualizzare le informazioni, molto simile alla visualizzazione Web di Esplora risorse. Per ulteriori informazioni, fare riferimento alla documentazione di tali controlli.

La finestra di visualizzazione cartelle esiste sempre, anche se non ha lo stato attivo. È pertanto necessario mantenere tre stati per la finestra figlio:

-   Attivato con lo stato attivo. La visualizzazione cartelle è stata creata e ha lo stato attivo. Impostare la barra dei menu o gli elementi della barra degli strumenti appropriati per uno stato attivo.
-   Attivato senza lo stato attivo. La visualizzazione cartelle è stata creata ed è attiva, ma non ha lo stato attivo. Imposta la barra dei menu o gli elementi della barra degli strumenti appropriati per uno stato non attivo. Omettere tutti gli elementi che si applicano alla selezione di elementi nella visualizzazione cartelle.
-   Disattivato. La visualizzazione cartelle sta per essere eliminata definitivamente. Rimuovere tutte le voci di menu specifiche della cartella.

Esplora risorse invia una notifica all'oggetto visualizzazione cartella quando lo stato della finestra viene modificato chiamando [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate). A sua volta, l'oggetto visualizzazione cartelle deve notificare a Esplora risorse quando un utente attiva la finestra di visualizzazione cartelle chiamando [**IShellBrowser:: OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive). Per ulteriori informazioni su questa interfaccia, vedere [utilizzo di IShellBrowser per comunicare con Esplora risorse](#using-ishellbrowser-to-communicate-with-windows-explorer).

Mentre la visualizzazione cartella è attiva, è necessario elaborare tutti i messaggi di Windows, ad esempio le [ \_ dimensioni WM](../winmsg/wm-size.md), che appartengono alla finestra figlio. La routine della finestra riceverà anche i messaggi di [ \_ comando WM](../menurc/wm-command.md) per tutti gli elementi aggiunti alla barra dei menu o alla barra degli strumenti di Esplora risorse.

Dopo aver creato la visualizzazione cartelle, Esplora risorse chiama l'interfaccia [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) dell'oggetto visualizzazione cartella per passare un'ampia gamma di informazioni. L'oggetto deve modificare la visualizzazione di conseguenza. Quando la visualizzazione cartelle sta per essere distrutta, Esplora risorse invia una notifica all'oggetto visualizzazione cartelle chiamando il metodo [**IShellView::D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) .

## <a name="implementing-ishellview"></a>Implementazione di IShellView

Dopo che l'oggetto Folder è stato creato, Esplora risorse chiama diversi metodi [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) per richiedere informazioni o notificare all'oggetto una modifica nello stato di Esplora risorse. In questa sezione viene descritto come implementare tali metodi **IShellView** . I metodi rimanenti vengono utilizzati per scopi più specializzati, ad esempio la finestra di dialogo Apri file comune. Per informazioni dettagliate, vedere la documentazione di **IShellView** .

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

Quando un utente seleziona **Opzioni cartella** dal menu **strumenti** di Esplora risorse, viene visualizzata una finestra delle proprietà che consente all'utente di modificare le opzioni della cartella. Esplora risorse chiama il metodo [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) dell'oggetto visualizzazione cartella per consentire l'aggiunta di una pagina a questa finestra delle proprietà.

Esplora risorse passa un puntatore a una funzione di callback [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) nel parametro *lpfn* di [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Chiamare [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) per creare la pagina e quindi chiamare il AddPropSheetPageProc per aggiungerlo alla finestra delle proprietà. Per ulteriori informazioni sulla gestione delle finestre delle proprietà, vedere [finestre delle proprietà](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>GetCurrentInfo

Quando l'utente passa da una cartella a un'altra, Esplora risorse tenta di mantenere una visualizzazione di cartella simile. Se, ad esempio, nella visualizzazione cartella precedente sono state visualizzate icone grandi, sarà necessario anche il successivo. Quando Esplora risorse chiama [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) per inizializzare l'oggetto visualizzazione cartella, il metodo riceve una struttura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Questa struttura contiene informazioni che consentono di rendere la visualizzazione della cartella coerente con la visualizzazione della cartella precedente.

Per garantire che la visualizzazione successiva sia coerente con la visualizzazione corrente, archiviare la struttura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Se la vista viene modificata, ad esempio dalle icone grandi a piccole, aggiornare la struttura di conseguenza. Prima di cambiare le viste, Esplora risorse chiamerà [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) per richiedere i valori **FOLDERSETTINGS** correnti per passarli all'oggetto visualizzazione cartella successiva.

### <a name="refresh"></a>Aggiorna

L'utente può assicurarsi che la visualizzazione cartelle rifletta lo stato corrente della cartella selezionando **Aggiorna** dal menu **Visualizza** o premendo F5. Quando l'utente esegue questa operazione, Esplora risorse chiama il metodo [**IShellView:: Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) . L'oggetto visualizzazione cartella dovrebbe aggiornare immediatamente la visualizzazione delle cartelle.

### <a name="saveviewstate"></a>SaveViewState

Esplora risorse chiama il metodo [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) per richiedere all'oggetto visualizzazione cartella di salvare lo stato di visualizzazione. Sarà quindi possibile recuperare lo stato la volta successiva che la cartella viene visualizzata. Il modo migliore per salvare uno stato di visualizzazione consiste nel chiamare il metodo [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) . Questo metodo restituisce un'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) che può essere utilizzata dall'oggetto visualizzazione cartella per salvarne lo stato. Quando si crea un'altra visualizzazione di cartelle, è possibile chiamare lo stesso metodo **IShellBrowser:: GetViewStateStream** per ottenere un puntatore IStream che consente di leggere le impostazioni salvate dalle visualizzazioni di cartelle precedenti.

### <a name="translateacelerator"></a>TranslateAcelerator

Quando l'utente preme un tasto di scelta rapida, Esplora risorse passa il messaggio all'oggetto visualizzazione cartella chiamando [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator). Restituisce \_ false per fare in modo che Esplora risorse elabori il messaggio. Se il messaggio è stato elaborato dall'oggetto visualizzazione cartella, restituire S \_ OK.

Quando la finestra visualizzazione cartelle ha lo stato attivo, Esplora risorse chiama [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) prima di elaborare il messaggio. Poiché la maggior parte dei messaggi è in genere associata alla barra dei menu o ai comandi della barra degli strumenti di Esplora risorse, l'oggetto visualizzazione cartella deve normalmente restituire S \_ false. Esplora risorse può quindi elaborare il messaggio normalmente. Restituire S \_ OK solo se il messaggio è specifico della cartella e non si desidera che Esplora risorse esegua ulteriori elaborazioni. Se la visualizzazione cartelle non ha lo stato attivo, Esplora risorse elabora innanzitutto il messaggio. Chiama [**IShellBrowser:: TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) solo se non gestisce il messaggio.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Uso di IShellBrowser per comunicare con Esplora risorse

L'interfaccia [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) viene utilizzata dall'oggetto visualizzazione cartelle per comunicare con Esplora risorse per diversi scopi, tra cui:

-   [Modifica della barra dei menu di Esplora risorse](#modifying-the-windows-explorer-menu-bar)
-   [Modifica della barra degli strumenti di Esplora risorse](#modifying-the-windows-explorer-toolbar)
-   [Modifica della barra di stato di Esplora risorse](#modifying-the-windows-explorer-status-bar)
-   [Archiviazione di informazioni specifiche della visualizzazione](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Modifica della barra dei menu di Esplora risorse

La barra dei menu di Esplora risorse consente all'utente di avviare un'ampia gamma di comandi. Per impostazione predefinita, la barra dei menu supporta solo i comandi specifici di Esplora risorse. I messaggi [di \_ comando WM](../menurc/wm-command.md) correlati vengono elaborati da Esplora risorse e non vengono passati all'oggetto visualizzazione cartella. Tuttavia, è possibile modificare la barra dei menu in modo da includere una o più voci di menu specifiche della cartella con [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser). Esplora risorse passa i \_ messaggi di comando WM associati di tali elementi alla routine della finestra dell'oggetto cartella per l'elaborazione. È anche possibile rimuovere o disabilitare i comandi standard che non si applicano all'applicazione.

In genere, gli oggetti di visualizzazione cartelle modificano la barra dei menu prima che la visualizzazione della cartella venga visualizzata. Devono restituire la barra dei menu allo stato originale quando la visualizzazione cartelle viene distrutta. Potrebbe anche essere necessario modificare la barra dei menu ogni volta che la visualizzazione cartella acquisisce o perde lo stato attivo.

Poiché Esplora risorse chiama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) ogni volta che lo stato della finestra visualizzazione cartella viene modificato, la modifica della barra dei menu viene in genere inclusa nell'implementazione del metodo. La procedura di base per modificare la barra dei menu di Esplora risorse è la seguente:

1.  Chiamare [CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) per creare un handle di menu.
2.  Passare l'handle del menu a Esplora risorse chiamando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb). Esplora risorse compilerà le informazioni di menu.
3.  Modificare il menu in base alle esigenze.
4.  Chiamare [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) per fare in modo che Esplora risorse visualizzi la barra dei menu modificata.

In Esplora risorse sono presenti sei menu popup sulla barra dei menu. Come per tutti i contenitori OLE, il menu Esplora risorse è diviso in sei gruppi: file, modifica, contenitore, oggetto, finestra e guida. Nella tabella seguente sono elencati i menu a comparsa di Esplora risorse e il gruppo associato, insieme agli ID menu.



| Menu a comparsa | ID                     | Group     |
|-------------|------------------------|-----------|
| File        | \_file di menu FCIDM \_      | File      |
| Modifica        | \_modifica menu \_ FCIDM      | File      |
| Visualizzazione        | \_visualizzazione del menu FCIDM \_      | Contenitore |
| Preferiti   | FCIDM \_ menu \_ Preferiti | Contenitore |
| Strumenti       | \_strumenti di menu FCIDM \_     | Contenitore |
| Help        | \_Guida del menu FCIDM \_      | Finestra    |



 

Quando si passa l'handle di menu a Esplora risorse chiamando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb), è necessario passare anche un puntatore a una struttura [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) i cui membri sono stati inizializzati su zero.

Quando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) restituisce, Esplora risorse avrà aggiunto le voci di menu. È quindi possibile usare l'handle di menu restituito con le funzioni di menu standard di Windows, ad esempio [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) , per:

-   Consente di aggiungere elementi ai menu a comparsa di Esplora risorse.
-   Modificare o eliminare gli elementi esistenti nei menu a comparsa di Esplora risorse.
-   Aggiungere nuovi menu popup.

Usare gli ID elencati nella tabella per identificare i vari menu a comparsa di Esplora risorse di Windows.

> [!Note]  
> Per evitare conflitti con gli ID dei comandi di Esplora risorse, gli ID di tutte le voci di menu aggiunte devono essere compresi tra FCIDM \_ SHVIEWFIRST e FCIDM \_ SHVIEWLAST. Questi due valori sono definiti in Shlobj. h.

 

Una volta completata la modifica del menu, chiamare [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in modo che Esplora risorse visualizzi la nuova barra dei menu.

Dopo la visualizzazione iniziale della visualizzazione cartelle, Esplora risorse chiama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) ogni volta che la visualizzazione cartella acquisisce o perde lo stato attivo. Se sono presenti voci di menu sensibili allo stato della visualizzazione cartelle, è necessario modificare il menu di conseguenza, ogni volta che lo stato cambia. Ad esempio, è possibile disporre di una voce di menu che agisce su un elemento nella visualizzazione cartelle selezionata dall'utente. È necessario disabilitare o rimuovere questa voce di menu quando la visualizzazione cartelle perde lo stato attivo.

Quando Esplora risorse chiama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) per indicare che la visualizzazione cartelle viene disattivata, ripristinare lo stato originale della barra dei menu chiamando [**IShellBrowser:: RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb).

### <a name="modifying-the-windows-explorer-toolbar"></a>Modifica della barra degli strumenti di Esplora risorse

Oltre a modificare la barra dei menu di Esplora risorse, è anche possibile aggiungere pulsanti alla barra degli strumenti. Come per la barra dei menu, la modifica della barra degli strumenti è in genere inclusa nell'implementazione di [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) . La procedura per aggiungere pulsanti alla barra degli strumenti di Esplora risorse è la seguente:

1.  Aggiungere la bitmap del pulsante all'elenco immagini della barra degli strumenti.
2.  Definire la stringa di testo del pulsante.
3.  Aggiungere il pulsante alla barra degli strumenti.

Per aggiungere una bitmap all'elenco di immagini di una barra degli strumenti, inviare la barra degli strumenti un messaggio [TB \_ ADDBITMAP](../controls/tb-addbitmap.md) chiamando [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg). Per specificare il controllo Toolbar, impostare il parametro *ID* del metodo sulla **\_ barra degli strumenti FCW**. Impostare *wParam* sul numero di immagini dei pulsanti nella bitmap e *lParam* sull'indirizzo di una struttura [TBADDBITMAP](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) . L'indice dell'immagine viene restituito nel parametro *Pret* .

Esistono due modi per definire una stringa per il pulsante:

-   Assegnare la stringa **al membro della** struttura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) del pulsante.
-   Chiamare [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) per inviare il controllo Toolbar a un messaggio [TB \_ ADDSTRING](../controls/tb-addstring.md) . Il parametro *wParam* deve essere impostato su zero e il parametro *lParam* sulla stringa. L'indice della stringa viene restituito nel parametro *Pret* .

Per aggiungere il pulsante alla barra degli strumenti, compilare una struttura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) e passarla a [**IShellBrowser:: SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Come nel menu, l'ID del comando deve essere compreso tra FCIDM \_ SHVIEWFIRST e FCIDM \_ SHVIEWLAST. La barra degli strumenti aggiungerà quindi il pulsante a destra dei pulsanti esistenti.

Il frammento di codice seguente, ad esempio, aggiunge un pulsante standard alla barra degli strumenti di Esplora risorse con l'ID del comando IDB \_ .


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



Per ulteriori informazioni su come gestire i controlli della barra degli strumenti, vedere [controlli della barra](../controls/toolbar-control-reference.md)degli strumenti.

### <a name="modifying-the-windows-explorer-status-bar"></a>Modifica della barra di stato di Esplora risorse

È possibile utilizzare la barra di stato di Esplora risorse per visualizzare una serie di informazioni utili. Esistono due modi per usare la barra di stato:

-   Usare [**IShellBrowser:: SetStatusTextSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) per visualizzare una stringa di testo sulla barra di stato.
-   Inviare i messaggi direttamente al controllo barra di stato con [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

Il primo metodo è semplice ma sufficiente per molti scopi. Per maggiore flessibilità, è possibile inviare messaggi direttamente al controllo barra di stato chiamando [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) con il parametro *ID* impostato **\_ sullo stato FCW**. Per ulteriori informazioni sui controlli barra di stato, vedere [barre di stato](../controls/status-bars.md).

### <a name="storing-view-specific-information"></a>Archiviazione di informazioni specifiche della visualizzazione

Quando una visualizzazione sta per essere distrutta, è spesso utile archiviare informazioni quali lo stato o le impostazioni della vista. Esplora risorse richiede di eseguire questa attività chiamando [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate). Il modo migliore per salvare le informazioni specifiche della visualizzazione consiste nel chiamare [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream). Questo metodo fornisce un'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) che è possibile usare per archiviare le informazioni. È possibile utilizzare qualsiasi formato dati appropriato.

 

 
