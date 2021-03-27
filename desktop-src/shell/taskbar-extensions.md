---
description: Viene illustrata la nuova funzionalità della barra delle applicazioni, tra cui il consolidamento dell'avvio e del cambio, funzionalità avanzate dei pulsanti della barra delle applicazioni, ad esempio l'accesso con un solo clic a documenti e attività specifiche dell'applicazione, controlli di trasporto e notifiche di stato, rappresentazioni di anteprime e destinazioni switch basate su singole schede in un'applicazione a schede e la possibilità di riordinare i
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Estensioni della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df308d8045301b98937eb03af595d2e800921b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884386"
---
# <a name="taskbar-extensions"></a>Estensioni della barra delle applicazioni

A partire da Windows 7, la barra delle applicazioni è stata estesa in modo significativo in base al principio di guida che consente agli utenti di raggiungere il modo più rapido ed efficiente possibile. A tal fine, le finestre dell'applicazione, i file e i comandi che l'utente deve eseguire sono ora centralizzati in un unico pulsante della barra delle applicazioni che consolida le origini dati e i controlli precedentemente dispersi. Un utente può ora trovare attività comuni, file recenti e frequenti, avvisi, notifiche sullo stato di avanzamento e anteprime per singoli documenti o schede in un'unica posizione.

-   [Avvio e cambio unificati](#unified-launching-and-switching)
-   [Jump List](#jump-lists)
-   [Destinazioni](#destinations)
-   [Attività](#tasks)
-   [Personalizzazione delle Jump List](#customizing-jump-lists)
-   [Barre degli strumenti delle anteprime](#thumbnail-toolbars)
-   [Sovrimpressioni icona](#icon-overlays)
-   [Indicatori di stato](#progress-bars)
-   [Deskbands](#deskbands)
-   [Area di notifica](#notification-area)
-   [Anteprima](#thumbnails)
-   [Argomenti correlati](#related-topics)

## <a name="unified-launching-and-switching"></a>Avvio e cambio unificati

Al momento della barra delle applicazioni di Windows 7, avvio veloce non è più una barra degli strumenti separata. I collegamenti dell'utilità di avvio che vengono in genere contenuti in avvio veloce sono ora aggiunti alla barra delle applicazioni, mescolati con i pulsanti per le applicazioni attualmente in esecuzione. Quando un utente avvia un'applicazione da un collegamento di avvio aggiunto, l'icona viene trasformata nel pulsante della barra delle applicazioni dell'applicazione per tutto il tempo in cui l'applicazione è in esecuzione. Quando l'utente chiude l'applicazione, il pulsante viene ripristinato sull'icona. Tuttavia, il collegamento dell'utilità di avvio e il pulsante per l'applicazione in esecuzione sono solo forme diverse del pulsante della barra delle applicazioni di Windows 7.

![barra delle applicazioni di Windows 7](images/taskbar/taskbar.png)

Per impostazione predefinita, per le nuove installazioni viene aggiunto un piccolo set di applicazioni. A parte questo, solo l'utente può aggiungere altre applicazioni; l'aggiunta a livello di codice da un'applicazione non è consentita.

La funzionalità Mostra desktop di avvio veloce è ora posizionata all'estrema destra della barra delle applicazioni. Posizionando il puntatore del mouse su quest'area, tutte le finestre attive diventano trasparenti, mostrando il desktop. Facendo clic sull'area viene eseguita l'azione nota per ridurre al minimo tutte le finestre e passare al desktop.

Mentre l'applicazione è in esecuzione, il pulsante della relativa barra delle applicazioni diventa l'unica posizione per accedere a tutte le funzionalità seguenti, descritte in dettaglio di seguito.

-   [Attività](#tasks): comandi comuni dell'applicazione, presenti anche quando l'applicazione non è in esecuzione.
-   [Destinazioni](#destinations): file a cui si accede di recente e di frequente specifici dell'applicazione.
-   [Anteprime](#thumbnails): commutazione della finestra, incluse le destinazioni dei commutatori per singole schede e documenti.
-   [Barre degli strumenti delle anteprime](#thumbnail-toolbars): controllo delle applicazioni di base dall'anteprima stessa.
-   [Barre](#progress-bars) di stato e [sovrapposizioni di icone](#icon-overlays): notifiche di stato.

Il pulsante della barra delle applicazioni può rappresentare un'utilità di avvio, una singola finestra dell'applicazione o un gruppo. Un identificatore noto come ID modello utente applicazione (AppUserModelID) viene assegnato a ogni gruppo. È possibile specificare un AppUserModelID per eseguire l'override del raggruppamento della barra delle applicazioni standard, che consente a Windows di diventare membri dello stesso gruppo quando potrebbero non essere visualizzati in altro modo. A ogni membro di un gruppo viene assegnata un'anteprima separata nell'icona a comparsa dell'anteprima visualizzata quando il mouse passa sul pulsante della barra delle applicazioni del gruppo. Si noti che il raggruppamento rimane facoltativo.

A partire da Windows 7, i pulsanti della barra delle applicazioni possono ora essere ridisposti dall'utente tramite operazioni di trascinamento della selezione.

> [!Note]  
> La cartella avvio veloce ([* * * * FOLDERID \_ QuickLaunch * *](knownfolderid.md)* *) è ancora disponibile per compatibilità con le versioni precedenti, anche se non è più disponibile un'interfaccia utente di avvio veloce. Tuttavia, le nuove applicazioni non dovrebbero richiedere di aggiungere un'icona per l'avvio veloce durante l'installazione.

 

Per ulteriori informazioni, vedere [ID modello utente applicazione (AppUserModelIDs)](appids.md).

## <a name="jump-lists"></a>Jump List

Un utente in genere avvia un programma con l'intenzione di accedere a un documento o eseguire attività all'interno del programma. L'utente di un programma di gioco potrebbe voler accedere a un gioco salvato o avviarlo come un carattere specifico anziché riavviare un gioco dall'inizio. Per consentire agli utenti di ottenere in modo più efficiente l'obiettivo finale, un elenco di [destinazioni](#destinations) e [attività](#tasks) comuni associate a un'applicazione viene collegato al pulsante della barra delle applicazioni di tale applicazione (oltre alla voce del menu **Start** equivalente). Si tratta della Jump List dell'applicazione. La Jump List è disponibile se il pulsante della barra delle applicazioni si trova in uno stato di avvio (l'applicazione non è in esecuzione) o se rappresenta una o più finestre. Facendo clic con il pulsante destro del mouse sul pulsante della barra delle applicazioni, viene visualizzata la Jump List dell'applicazione, come illustrato nella figura seguente.

![Jump List con categorie bloccate, frequenti e di attività](images/taskbar/jumplist.png)

Per impostazione predefinita, una Jump List standard contiene due categorie: gli elementi recenti e gli elementi aggiunti, anche se nell'interfaccia utente vengono visualizzate solo le categorie con contenuto, nessuna di queste categorie viene visualizzata al primo avvio. Sempre presente è un'icona di avvio dell'applicazione (per avviare più istanze dell'applicazione), un'opzione per aggiungere o Rimuovi l'applicazione dalla barra delle applicazioni e un comando **Chiudi** per tutte le finestre aperte.

## <a name="destinations"></a>Destinazioni

Le categorie **recenti** e **frequenti** sono considerate che contengono destinazioni. Una destinazione, in genere un file, un documento o un URL, è un elemento che può essere modificato, sfogliato, visualizzato e così via. Si pensi a una destinazione come a una cosa invece che a un'azione. In genere, una destinazione è un elemento nello spazio dei nomi della shell, rappresentato da un [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka). Queste parti dell'elenco di destinazione sono analoghe all'elenco di documenti usati di recente (non più visualizzato per impostazione predefinita) **e all'elenco** di applicazioni usate di frequente, ma sono specifici di un'applicazione e quindi più accurate e utili per l'utente. I risultati usati nell'elenco di destinazione vengono calcolati tramite chiamate a [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Si noti che quando l'utente apre un file da Esplora risorse o usa la finestra di dialogo file comune per aprire, salvare o creare un file, viene chiamato automaticamente **funzione SHAddToRecentDocs** , che consente a molte applicazioni di ottenere gli elementi recenti visualizzati nell'elenco di destinazione senza alcuna azione da parte dell'utente.

L'avvio di una destinazione è molto simile all'avvio di un elemento tramite il comando **Apri con** . L'applicazione viene avviata con tale destinazione caricata e pronta per l'utilizzo. Gli elementi nell'elenco di destinazione possono anche essere trascinati dall'elenco a una destinazione di rilascio, ad esempio un messaggio di posta elettronica. Se questi elementi sono centralizzati in un elenco di destinazione, ottiene gli utenti in cui si vuole passare molto più velocemente, ovvero l'obiettivo.

Quando gli elementi vengono visualizzati nella categoria **recente** di un elenco di destinazione (o nella categoria **frequente** o in una [categoria personalizzata](#customizing-jump-lists) come descritto in una sezione successiva), un utente potrebbe voler assicurarsi che l'elemento sia sempre nell'elenco per l'accesso rapido. A tale scopo, può aggiungere l'elemento all'elenco, che aggiunge l'elemento alla categoria **bloccata** . Quando un utente lavora attivamente con una destinazione, lo desidera facilmente e quindi lo aggiunge all'elenco di destinazione dell'applicazione. Al termine dell'operazione, l'utente deve semplicemente riportare l'elemento. Questo controllo utente mantiene l'elenco non ordinato e pertinente.

Un elenco di destinazione può essere considerato come una versione specifica dell'applicazione del menu **Start** . Un elenco di destinazione non è un menu di scelta rapida. È possibile fare clic con il pulsante destro del mouse su ogni elemento in un elenco di destinazione per il proprio menu di scelta rapida.

### <a name="apis"></a>API

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists:: GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**Funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Attività

Un'altra parte predefinita di una Jump List è la categoria **attività** . Mentre una destinazione è un elemento, un'attività è un'azione e in questo caso si tratta di un'azione specifica dell'applicazione. In altre parole, una destinazione è un sostantivo e un'attività è un verbo. In genere, le attività sono elementi [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) con argomenti della riga di comando che indicano funzionalità specifiche che possono essere attivate da un'applicazione. Anche in questo caso, l'idea è centralizzare la maggior parte delle informazioni relative a un'applicazione.

Le applicazioni definiscono le attività in base alle funzionalità del programma e agli elementi chiave che un utente dovrebbe eseguire con loro. Le attività devono essere senza contesto, in quanto non è necessario che l'applicazione sia in esecuzione perché funzionino. Devono essere anche le azioni statisticamente più comuni che un utente normale può eseguire in un'applicazione, ad esempio comporre un messaggio di posta elettronica o aprire il calendario in un programma di posta elettronica, creare un nuovo documento in un elaboratore di testo, avviare un'applicazione in una determinata modalità o avviare uno dei sottocomandi. Un'applicazione non deve ingombrare il menu con funzionalità avanzate non necessarie per gli utenti standard o azioni monouso, ad esempio la registrazione. Non usare le attività per gli elementi promozionali, ad esempio gli aggiornamenti o le offerte speciali.

Si consiglia vivamente che l'elenco attività sia statico. Deve rimanere invariato indipendentemente dallo stato o dallo stato dell'applicazione. Sebbene sia possibile variare l'elenco in modo dinamico, è necessario considerare che questa operazione potrebbe confondere l'utente che non prevede la modifica di tale parte dell'elenco di destinazione.

### <a name="apis"></a>API

-   [**ICustomDestinationList:: AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalizzazione delle Jump List

Un'applicazione può definire le proprie categorie e aggiungerle in aggiunta o al posto delle categorie standard **recenti** e **frequenti** in una Jump List. L'applicazione può controllare le proprie destinazioni in queste categorie personalizzate in base all'architettura dell'applicazione e all'utilizzo previsto. Lo screenshot seguente mostra una Jump List personalizzata con una categoria della cronologia.

![Jump List personalizzato](images/taskbar/customjumplist.png)

Se un'applicazione decide di fornire una categoria personalizzata, l'applicazione assume la responsabilità di popolarla. Il contenuto della categoria deve essere ancora specifico dell'utente e in base alla cronologia degli utenti, alle azioni o a entrambi, ma tramite una categoria personalizzata un'applicazione può determinare cosa si vuole rilevare e cosa si vuole ignorare, probabilmente in base a un'opzione dell'applicazione. Ad esempio, un programma audio potrebbe decidere di includere solo gli album rilasciati di recente e ignorare le singole tracce riprodotte di recente.

Se un utente ha rimosso un elemento dall'elenco, che è sempre un'opzione utente, l'applicazione deve rispettarla. L'applicazione deve inoltre verificare che gli elementi nell'elenco siano validi o che abbiano esito negativo correttamente se sono stati eliminati. È possibile rimuovere a livello di codice singoli elementi o l'intero contenuto dell'elenco.

Il numero massimo di elementi in un elenco di destinazione è determinato dal sistema in base a diversi fattori, ad esempio la risoluzione dello schermo e le dimensioni del carattere. Se non è disponibile spazio sufficiente per tutti gli elementi in tutte le categorie, questi vengono troncati dal basso verso l'alto.

### <a name="apis"></a>API

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barre degli strumenti delle anteprime

Per consentire l'accesso ai comandi chiave di una determinata finestra senza fare in modo che l'utente ripristini o attivi la finestra dell'applicazione, è possibile incorporare un controllo della barra degli strumenti attivo nell'anteprima dell'anteprima della finestra. Ad esempio, Windows Media Player potrebbe offrire controlli standard per il trasporto multimediale, ad esempio Play, pause, mute e stop. L'interfaccia utente Visualizza questa barra degli strumenti direttamente sotto l'anteprima, come illustrato nella figura seguente: non ne copre alcuna parte.

![barra delle applicazioni Anteprima per Windows Media Player, con tre pulsanti: indietro, riproduzione e avanzamento](images/taskbar/thumbbar.png)

Questa barra degli strumenti è semplicemente il noto controllo comune della barra degli strumenti standard. È costituito da un massimo di sette pulsanti. L'ID, l'immagine, la descrizione comando e lo stato di ogni pulsante sono definiti in una struttura, che viene quindi passata alla barra delle applicazioni. L'applicazione può visualizzare, abilitare, disabilitare o nascondere i pulsanti dalla barra degli strumenti dell'anteprima come richiesto dallo stato corrente.

Poiché è disponibile spazio limitato per visualizzare le anteprime e un numero variabile di anteprime da visualizzare, alle applicazioni non viene garantita una determinata dimensione della barra degli strumenti. Se lo spazio è limitato, i pulsanti della barra degli strumenti vengono troncati da destra a sinistra. Pertanto, quando si progetta la barra degli strumenti, è necessario classificare in ordine di priorità i comandi associati ai pulsanti e assicurarsi che il più importante sia il primo e meno probabile che venga eliminato a causa di problemi di spazio.

> [!Note]  
> Quando in un'applicazione viene visualizzata una finestra, il relativo pulsante della barra delle applicazioni viene creato dal sistema. Quando il pulsante è sul posto, la barra delle applicazioni Invia un messaggio **TaskbarButtonCreated** alla finestra. Il valore viene calcolato chiamando [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L ("TaskbarButtonCreated")). Il messaggio deve essere ricevuto dall'applicazione prima di chiamare qualsiasi metodo [**all'ITaskbarList3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3) .

 

### <a name="api"></a>API

-   [**All'ITaskbarList3:: ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**All'ITaskbarList3:: ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**All'ITaskbarList3:: ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Sovrimpressioni icona

Un'applicazione è in grado di comunicare determinate notifiche e lo stato all'utente tramite il pulsante della barra delle applicazioni mediante la visualizzazione di piccole sovrapposizioni sul pulsante. Queste sovrapposizioni sono simili al tipo di sovrapposizione esistente usato per i collegamenti o le notifiche di sicurezza, visualizzato nell'angolo in basso a destra del pulsante. Per visualizzare un'icona di sovrapposizione, è necessario che la barra delle applicazioni si trovi nella modalità icone grandi predefinite, come illustrato nella schermata seguente.

![pulsante della barra delle applicazioni di Windows Messenger con una sovrimpressione per indicare uno stato disponibile](images/taskbar/taskbaroverlay.png)

Le sovrapposizioni di icone vengono utilizzate come una notifica contestuale dello stato e hanno lo scopo di negare la necessità di un'icona di stato dell'area di notifica separata per comunicare tali informazioni all'utente. Ad esempio, il nuovo stato della posta in Microsoft Outlook, attualmente visualizzato nell'area di notifica, ora può essere indicato tramite una sovrapposizione sul pulsante della barra delle applicazioni. Anche in questo caso, è necessario decidere durante il ciclo di sviluppo quale metodo è migliore per l'applicazione. Le icone sovrapposte sono progettate per fornire uno stato importante e di lunga durata o notifiche quali lo stato della rete, lo stato di Messenger o la nuova posta. L'utente non deve presentare sovrapposizioni o animazioni in continua evoluzione.

Poiché una singola sovrapposizione viene sovrapposta sul pulsante della barra delle applicazioni e non sulle singole anteprime della finestra, si tratta di una funzionalità per gruppo anziché per finestra. Le richieste per le icone sovrapposte possono essere ricevute da singole finestre in un gruppo di applicazioni, ma non vengono accodate. L'ultima sovrapposizione ricevuta è la sovrimpressione visualizzata.

### <a name="apis"></a>API

-   [**All'ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Indicatori di stato

È possibile utilizzare un pulsante della barra delle applicazioni per visualizzare un indicatore di stato. Ciò consente a una finestra di fornire all'utente informazioni sullo stato di avanzamento senza che l'utente debba passare alla finestra stessa. L'utente può rimanere produttivo in un'altra applicazione, visualizzando immediatamente lo stato di una o più operazioni che si verificano in altre finestre. È previsto che un indicatore di stato in un pulsante della barra delle applicazioni rifletta un indicatore di stato più dettagliato nella finestra stessa. Questa funzionalità può essere usata per tenere traccia delle copie dei file, dei download, delle installazioni, della masterizzazione multimediale o di qualsiasi operazione che sta per richiedere un certo periodo di tempo. Questa funzionalità non è destinata all'uso con azioni normalmente periferiche, ad esempio il caricamento di una pagina Web o la stampa di un documento. Questo tipo di avanzamento deve continuare a essere visualizzato nella barra di stato di una finestra.

L'indicatore di stato del pulsante della barra delle applicazioni è un'esperienza simile al controllo indicatore di stato noto. Può visualizzare lo stato di avanzamento determinato in base a una percentuale completa dell'operazione o uno stato di avanzamento dello stile di selezione indeterminato per indicare che l'operazione è in corso senza alcuna stima del tempo rimanente. Può inoltre indicare che l'operazione è stata sospesa o si è verificato un errore e richiede l'intervento dell'utente.

### <a name="apis"></a>API

-   [**All'ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**All'ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

Nelle versioni di Windows precedenti a Windows 7, è possibile ottenere un risultato simile alla funzionalità della barra degli strumenti di anteprima tramite una Deskband, una barra degli strumenti ospitata nella barra delle applicazioni. Ad esempio, Windows Media Player possibile ridurre la barra delle applicazioni come un set di controlli di trasporto invece che con un pulsante standard. In Windows 7, è ancora possibile implementare deskbands e le barre degli strumenti delle anteprime non sono destinate a sostituirle tutte. Non tutte le applicazioni si prestano a una barra degli strumenti di anteprima e un'altra soluzione, ad esempio Deskband o un'attività in un elenco di destinazione, potrebbe essere la risposta giusta per l'applicazione. è necessario decidere quale soluzione funziona meglio per l'applicazione come parte del ciclo di sviluppo. Tuttavia, tenere presente che deskbands deve supportare Windows Aero con translucidità ("Glass") abilitato e l'interfaccia [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2) .

### <a name="apis"></a>API

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Area di notifica

Sono state apportate modifiche all'area di notifica che forniscono all'utente un maggiore controllo sulle icone visualizzate sulla barra delle applicazioni. Tutte le icone di notifica sono ora nascoste per impostazione predefinita e non è possibile controllare la visibilità a livello di codice. Solo l'utente può scegliere quali icone di notifica vengono visualizzate sulla barra delle applicazioni. Quando viene visualizzato un fumetto di notifica, l'icona diventa temporaneamente visibile, ma anche un utente può scegliere di inserirli. Una sovrapposizione di icone in un pulsante della barra delle applicazioni diventa pertanto una scelta interessante quando si desidera che l'applicazione comunichi tali informazioni agli utenti.

## <a name="thumbnails"></a>Anteprime

In Windows Vista, il passaggio del mouse sul pulsante della barra delle applicazioni di un'applicazione Visualizza un'anteprima che rappresenta la finestra in esecuzione. Se la barra delle applicazioni ha compresso le finestre dell'applicazione, l'anteprima viene rappresentata in uno stack, ma solo la finestra attiva viene visualizzata nell'anteprima.

In Windows 7, ogni membro di un gruppo viene visualizzato come anteprima separata ed è ora anche una destinazione del cambio. Un'applicazione può definire i relativi elementi figlio, ad esempio le finestre figlio true, i singoli documenti o le schede, e fornire anteprime corrispondenti per ognuna di queste finestre anche quando normalmente non vengono visualizzate nella barra delle applicazioni. Ciò consente agli utenti di passare direttamente alla visualizzazione dell'applicazione desiderata anziché passare all'applicazione e quindi passare alla destinazione. Ad esempio, le applicazioni con interfaccia a documenti multipli (MDI)/Tabbed-Document Interface (TDI) possono avere ogni documento o scheda visualizzato come un'anteprima e una destinazione di commutazione separate quando il mouse passa sul pulsante della barra delle applicazioni di un gruppo.

![tre anteprime della barra delle applicazioni che rappresentano singole schede in Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Come in Windows Vista, è necessario che Aero sia attivo per visualizzare le anteprime.

 

### <a name="api"></a>API

-   [**All'ITaskbarList3:: RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**All'ITaskbarList3:: SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**All'ITaskbarList3:: SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**All'ITaskbarList3:: UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Le rappresentazioni di anteprime per Windows sono normalmente automatiche, ma nei casi in cui il risultato non è ottimale, l'anteprima può essere specificata in modo esplicito. Per impostazione predefinita, solo le finestre di primo livello hanno un'anteprima generata automaticamente e le anteprime per le finestre figlio vengono visualizzate come una rappresentazione generica. Questo può comportare un'esperienza meno di ideale (e addirittura confusa) per l'utente finale. Un'anteprima di destinazione switch specifica per ogni finestra figlio, ad esempio, offre un'esperienza utente molto migliore.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**\_DWMSENDICONICTHUMBNAIL WM**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

È possibile selezionare una particolare area della finestra da usare come anteprima. Questa operazione può essere utile quando un'applicazione sa che i documenti o le schede saranno simili quando vengono visualizzati in base alle dimensioni dell'anteprima. L'applicazione può quindi scegliere di visualizzare solo la parte dell'area client che l'utente può usare per distinguere le anteprime. Tuttavia, posizionando il puntatore del mouse su qualsiasi anteprima, viene visualizzata la finestra completa sottostante, in modo che l'utente possa esaminare rapidamente anche questi elementi.

Se sono presenti più anteprime di quante non possano essere visualizzate, l'anteprima viene ripristinata sull'anteprima legacy o su un'icona standard.

### <a name="api"></a>API

-   [**All'ITaskbarList3:: SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Per aggiungere **pin alla barra delle applicazioni** al menu di scelta rapida di un elemento, che in genere è necessario solo per i tipi di file che includono la voce di [collegamento](./links.md) , viene eseguita registrando il gestore del menu di scelta rapida appropriato. Questo vale anche per il **menu Aggiungi a Start**. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione dei gestori estensioni della shell](reg-shell-exts.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra delle applicazioni](taskbar.md)
</dt> <dt>

[ID modello utente applicazione (AppUserModelIDs)](appids.md)
</dt> <dt>

[Notifiche e area di notifica](notification-area.md)
</dt> </dl>

 

 
