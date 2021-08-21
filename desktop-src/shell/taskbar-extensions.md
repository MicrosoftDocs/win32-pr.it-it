---
description: Illustra le nuove funzionalità della barra delle applicazioni, tra cui il consolidamento dell'avvio e del cambio, le funzionalità avanzate dei pulsanti della barra delle applicazioni, ad esempio l'accesso con un solo clic a documenti e attività specifiche dell'applicazione, i controlli di trasporto e le notifiche di stato, le rappresentazioni di anteprima e il cambio di destinazioni in base alle singole schede in un'applicazione a schede e la possibilità di riordinare i pulsanti della barra delle applicazioni tramite un'operazione di trascinamento della selezione.
ms.assetid: cbf2b07d-d67c-4755-888c-d40692d13cae
title: Estensioni della barra delle applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92cb8f100da2c7b5173319c25369a0ada7284b2ff5f4adbfe9b519c0ee96485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773751"
---
# <a name="taskbar-extensions"></a>Estensioni della barra delle applicazioni

A Windows 7, la barra delle applicazioni è stata estesa in modo significativo in base al principio guida per consentire agli utenti di passare al più rapidamente ed efficiente possibile. A tale scopo, le finestre, i file e i comandi dell'applicazione che l'utente deve eseguire sono ora centralizzati in un unico pulsante della barra delle applicazioni che consolida le origini di informazioni e i controlli precedentemente sparsi. Un utente può ora trovare attività comuni, file recenti e frequenti, avvisi, notifiche di stato e anteprime per singoli documenti o schede in un'unica posizione.

-   [Avvio e cambio unificati](#unified-launching-and-switching)
-   [Jump List](#jump-lists)
-   [Destinazioni](#destinations)
-   [Attività](#tasks)
-   [Personalizzazione delle jump list](#customizing-jump-lists)
-   [Barre degli strumenti delle anteprime](#thumbnail-toolbars)
-   [Sovrimpressione delle icone](#icon-overlays)
-   [Barre di stato](#progress-bars)
-   [Deskbands](#deskbands)
-   [Area di notifica](#notification-area)
-   [Anteprima](#thumbnails)
-   [Argomenti correlati](#related-topics)

## <a name="unified-launching-and-switching"></a>Avvio e cambio unificati

A Windows 7 barra delle applicazioni, Avvio veloce non è più una barra degli strumenti separata. I tasti di scelta rapida Avvio veloce in genere contenuti nella barra delle applicazioni vengono ora aggiunti alla barra delle applicazioni stessa, insieme ai pulsanti per le applicazioni attualmente in esecuzione. Quando un utente avvia un'applicazione da un collegamento dell'utilità di avvio aggiunto, l'icona si trasforma nel pulsante della barra delle applicazioni dell'applicazione per tutto il tempo in cui l'applicazione è in esecuzione. Quando l'utente chiude l'applicazione, viene ripristinata l'icona del pulsante. Tuttavia, sia il collegamento dell'utilità di avvio che il pulsante per l'applicazione in esecuzione sono solo forme diverse del pulsante della barra Windows 7.

![Barra delle applicazioni di Windows 7](images/taskbar/taskbar.png)

Per impostazione predefinita, per le nuove installazioni viene aggiunto un piccolo set di applicazioni. Oltre a questi, solo l'utente può aggiungere altre applicazioni. L'aggiunta a livello di codice da parte di un'applicazione non è consentita.

La funzionalità Mostra desktop Avvio veloce ora si trova all'estrema destra della barra delle applicazioni. Se si passa il mouse su quest'area, tutte le finestre attive diventano trasparenti, visualizzando il desktop. Facendo clic sull'area viene eseguita l'azione nota di ridurre al minimo tutte le finestre e passare al desktop.

Mentre l'applicazione è in esecuzione, il pulsante della barra delle applicazioni diventa l'unica posizione in cui accedere a tutte le funzionalità seguenti, ognuna illustrata in dettaglio di seguito.

-   [Attività:](#tasks)comandi comuni dell'applicazione, presenti anche quando l'applicazione non è in esecuzione.
-   [Destinazioni:](#destinations)file usati di recente e di frequente specifici dell'applicazione.
-   [Anteprime:](#thumbnails)cambio di finestra, incluse le destinazioni di cambio per singole schede e documenti.
-   [Barre degli strumenti dell'anteprima:](#thumbnail-toolbars)controllo dell'applicazione di base dall'anteprima stessa.
-   [Barre di stato](#progress-bars) e [sovrimpressione delle icone:](#icon-overlays)notifiche di stato.

Il pulsante della barra delle applicazioni può rappresentare un'utilità di avvio, una singola finestra dell'applicazione o un gruppo. A ogni gruppo viene assegnato un identificatore noto come ID modello utente applicazione (AppUserModelID). È possibile specificare un AppUserModelID per eseguire l'override del raggruppamento standard della barra delle applicazioni, che consente alle finestre di diventare membri dello stesso gruppo quando potrebbero non essere altrimenti viste come tali. A ogni membro di un gruppo viene data un'anteprima separata nel riquadro a comparsa dell'anteprima visualizzato quando il puntatore del mouse viene posizionato sul pulsante della barra delle applicazioni del gruppo. Si noti che il raggruppamento stesso rimane facoltativo.

A Windows 7, i pulsanti della barra delle applicazioni possono ora essere ridisposti dall'utente tramite operazioni di trascinamento della selezione.

> [!Note]  
> La cartella Avvio veloce ([****FOLDERID \_ QuickLaunch****](knownfolderid.md)) è ancora disponibile per la compatibilità con le versioni precedenti, anche se non è più disponibile un'interfaccia utente Avvio veloce. Tuttavia, le nuove applicazioni non devono chiedere di aggiungere un'icona a Avvio veloce durante l'installazione.

 

Per altre informazioni, vedere [ID modello utente applicazione (AppUserModelIDs).](appids.md)

## <a name="jump-lists"></a>Jump List

Un utente in genere avvia un programma con l'intenzione di accedere a un documento o di eseguire attività all'interno del programma. L'utente di un programma di gioco potrebbe voler accedere a un gioco salvato o avviarsi come un carattere specifico anziché riavviare un gioco dall'inizio. Per consentire agli utenti di raggiungere in [](#destinations) modo [](#tasks) più efficiente l'obiettivo finale, un elenco di destinazioni e attività comuni associate a un'applicazione viene collegato al pulsante della barra delle applicazioni dell'applicazione (nonché alla voce del menu **Start** equivalente). Questo è il nome dell'Jump List. Il Jump List è disponibile se il pulsante della barra delle applicazioni è in uno stato di avvio (l'applicazione non è in esecuzione) o se rappresenta una o più finestre. Facendo clic con il pulsante destro del mouse sul pulsante della barra delle applicazioni viene visualizzata la Jump List dell'applicazione, come illustrato nella figura seguente.

![jump list con categorie di attività, frequenti e bloccate](images/taskbar/jumplist.png)

Per impostazione predefinita, un Jump List standard contiene due categorie: elementi recenti ed elementi aggiunti, anche se, poiché nell'interfaccia utente vengono visualizzate solo le categorie con contenuto, nessuna di queste categorie viene visualizzata al primo avvio. Sono sempre presenti un'icona di avvio dell'applicazione (per avviare più istanze dell'applicazione), un'opzione per aggiungere o rimuovere l'applicazione dalla barra delle applicazioni e un **comando** Chiudi per tutte le finestre aperte.

## <a name="destinations"></a>Destinazioni

Le **categorie Recenti** e **Frequenti** sono considerate come destinazioni. Una destinazione, in genere un file, un documento o un URL, è un elemento che può essere modificato, esplorato, visualizzato e così via. Si pensi a una destinazione come a una cosa piuttosto che a un'azione. In genere, una destinazione è un elemento nello spazio dei nomi shell, rappresentato da [**un oggetto IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellLink.**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) Queste parti dell'elenco di destinazione sono analoghe all'elenco dei documenti usati di recente del menu **Start** (non più visualizzato per impostazione predefinita) e all'elenco di applicazioni usate di frequente, ma sono specifiche di un'applicazione e pertanto più accurate e utili per l'utente. I risultati usati nell'elenco di destinazione vengono calcolati tramite chiamate [**a SHAddToRecentDocs.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) Si noti che quando l'utente apre un file da Windows Explorer o usa la finestra di dialogo file comune per aprire, salvare o creare un file, **shAddToRecentDocs** viene chiamato automaticamente e in questo modo molte applicazioni visualizzano gli elementi recenti nell'elenco di destinazione senza alcuna azione da parte dell'utente.

L'avvio di una destinazione è molto simile all'avvio di un elemento usando **il comando Apri** con. L'applicazione viene avviata con la destinazione caricata e pronta per l'uso. Gli elementi nell'elenco di destinazione possono anche essere trascinati dall'elenco a una destinazione di rilascio, ad esempio un messaggio di posta elettronica. La centralizzazione di questi elementi in un elenco di destinazione consente agli utenti di passare molto più velocemente, il che è l'obiettivo.

Quando gli elementi vengono visualizzati nella categoria  Recenti di [](#customizing-jump-lists) un elenco di destinazione (o nella categoria Frequente o in una categoria personalizzata come illustrato in una sezione successiva), un utente potrebbe voler assicurarsi che l'elemento sia sempre presente nell'elenco per l'accesso rapido.  A tale scopo, può aggiungere tale elemento all'elenco, che aggiunge l'elemento alla **categoria Pinned (Elementi aggiunti** in blocco). Quando un utente lavora attivamente con una destinazione, vuole che sia facilmente disponibile e quindi la aggiunge all'elenco di destinazione dell'applicazione. Al termine del lavoro dell'utente, l'utente deve semplicemente rimuovere l'elemento. Questo controllo utente mantiene l'elenco non ingombrato e pertinente.

Un elenco di destinazione può essere considerato una versione specifica dell'applicazione del menu **Start.** Un elenco di destinazione non è un menu di scelta rapida. È possibile fare clic con il pulsante destro del mouse su ogni elemento di un elenco di destinazione per il relativo menu di scelta rapida.

### <a name="apis"></a>API

-   [**IApplicationDestinations::RemoveDestination**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removedestination)
-   [**IApplicationDestinations::RemoveAllDestinations**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations)
-   [**IApplicationDocumentLists::GetList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist)
-   [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)

## <a name="tasks"></a>Attività

Un'altra parte predefinita di un Jump List è la **categoria** Attività. Mentre una destinazione è un elemento, un'attività è un'azione e in questo caso è un'azione specifica dell'applicazione. In altre parole, una destinazione è un sostantivo e un'attività è un verbo. In genere, le [**attività sono elementi IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) con argomenti della riga di comando che indicano funzionalità specifiche che possono essere attivate da un'applicazione. Anche in questo caso, l'idea è quella di centralizzare la quantità di informazioni correlate a un'applicazione quanto sia pratica.

Le applicazioni definiscono le attività in base alle funzionalità del programma e alle operazioni chiave che un utente deve eseguire con esse. Le attività devono essere senza contesto, in quanto non è necessario che l'applicazione sia in esecuzione per il loro funzionamento. Devono anche essere le azioni statisticamente più comuni eseguite da un utente normale in un'applicazione, ad esempio comporre un messaggio di posta elettronica o aprire il calendario in un programma di posta elettronica, creare un nuovo documento in un elaboratore di testo, avviare un'applicazione in una determinata modalità o avviare uno dei relativi sottocomandi. Un'applicazione non deve creare confusione nel menu con funzionalità avanzate che gli utenti standard non necessitano di azioni una sola volta, ad esempio la registrazione. Non usare attività per elementi promozionali, ad esempio aggiornamenti o offerte speciali.

È consigliabile che l'elenco attività sia statico. Deve rimanere invariato indipendentemente dallo stato o dallo stato dell'applicazione. Sebbene sia possibile variare l'elenco in modo dinamico, è consigliabile considerare che ciò potrebbe confondere l'utente che non si aspetta che la parte dell'elenco di destinazione cambi.

### <a name="apis"></a>API

-   [**ICustomDestinationList::AddUserTasks**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks)

## <a name="customizing-jump-lists"></a>Personalizzazione delle jump list

Un'applicazione può definire le proprie categorie e aggiungerle in  aggiunta o al posto delle categorie standard **Recenti** e Frequenti in un Jump List. L'applicazione può controllare le proprie destinazioni in tali categorie personalizzate in base all'architettura dell'applicazione e all'uso previsto. Lo screenshot seguente mostra un'Jump List personalizzata con una categoria Cronologia.

![impostazioni jump list](images/taskbar/customjumplist.png)

Se un'applicazione decide di fornire una categoria personalizzata, si assume la responsabilità di popolarla. Il contenuto della categoria deve comunque essere specifico dell'utente e basato su cronologia utente, azioni o entrambi, ma tramite una categoria personalizzata un'applicazione può determinare ciò che vuole rilevare e cosa vuole ignorare, ad esempio in base a un'opzione dell'applicazione. Ad esempio, un programma audio potrebbe scegliere di includere solo gli album riprodotti di recente e ignorare i singoli tracce riprodotti di recente.

Se un utente ha rimosso un elemento dall'elenco, che è sempre un'opzione utente, l'applicazione deve rispettare questa impostazione. L'applicazione deve anche garantire che gli elementi nell'elenco siano validi o che non riescano correttamente se sono stati eliminati. I singoli elementi o l'intero contenuto dell'elenco possono essere rimossi a livello di codice.

Il numero massimo di elementi in un elenco di destinazione è determinato dal sistema in base a diversi fattori, ad esempio la risoluzione dello schermo e le dimensioni del carattere. Se non è disponibile spazio sufficiente per tutti gli elementi in tutte le categorie, vengono troncati dal basso verso l'alto.

### <a name="apis"></a>API

-   [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)
-   [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)
-   [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)

## <a name="thumbnail-toolbars"></a>Barre degli strumenti delle anteprime

Per consentire l'accesso ai comandi chiave di una determinata finestra senza che l'utente ripristini o attivi la finestra dell'applicazione, è possibile incorporare un controllo barra degli strumenti attivo nell'anteprima dell'anteprima della finestra. Ad esempio, Windows Media Player possono offrire controlli di trasporto multimediale standard, ad esempio riproduzione, sospensione, disattivazione dell'audio e arresto. L'interfaccia utente visualizza questa barra degli strumenti direttamente sotto l'anteprima, come illustrato nella figura seguente, e non ne copre alcuna parte.

![barra delle applicazioni dell'anteprima per Windows Media Player, con tre pulsanti: Indietro, Riproduci e Inoltra](images/taskbar/thumbbar.png)

Questa barra degli strumenti è semplicemente il noto controllo comune della barra degli strumenti standard. Ha un massimo di sette pulsanti. L'ID, l'immagine, la descrizione comando e lo stato di ogni pulsante sono definiti in una struttura , che viene quindi passata alla barra delle applicazioni. L'applicazione può mostrare, abilitare, disabilitare o nascondere i pulsanti dalla barra degli strumenti dell'anteprima come richiesto dallo stato corrente.

Poiché lo spazio disponibile per visualizzare le anteprime e un numero variabile di anteprime è limitato, alle applicazioni non è garantita una determinata dimensione della barra degli strumenti. Se lo spazio è limitato, i pulsanti nella barra degli strumenti vengono troncati da destra a sinistra. Pertanto, quando si progetta la barra degli strumenti, è consigliabile assegnare la priorità ai comandi associati ai pulsanti e assicurarsi che i più importanti siano disponibili per primi e che siano meno probabili a causa di problemi di spazio.

> [!Note]  
> Quando un'applicazione visualizza una finestra, il relativo pulsante della barra delle applicazioni viene creato dal sistema. Quando il pulsante è sul posto, la barra delle applicazioni invia un **messaggio TaskbarButtonCreated** alla finestra. Il valore viene calcolato chiamando [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)(L("TaskbarButtonCreated")). Tale messaggio deve essere ricevuto dall'applicazione prima che chiami qualsiasi [**metodo ITaskbarList3.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3)

 

### <a name="api"></a>API

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**ITaskbarList3::ThumbBarUpdateButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)

## <a name="icon-overlays"></a>Sovrimpressione delle icone

Un'applicazione può comunicare determinate notifiche e stato all'utente tramite il relativo pulsante della barra delle applicazioni visualizzando piccole sovrimpressione sul pulsante. Queste sovrimpressione sono simili al tipo di sovrimpressione esistente usato per i collegamenti o le notifiche di sicurezza, visualizzato nell'angolo inferiore destro del pulsante. Per visualizzare un'icona di sovrimpressione, la barra delle applicazioni deve essere in modalità icona grande predefinita, come illustrato nello screenshot seguente.

![Pulsante della barra delle applicazioni di Windows Messenger con sovrimpressione per indicare uno stato disponibile](images/taskbar/taskbaroverlay.png)

Le sovrimpressione delle icone fungono da notifica contestuale dello stato e sono progettate per negare la necessità di un'icona di stato dell'area di notifica separata per comunicare le informazioni all'utente. Ad esempio, il nuovo stato di posta elettronica in Microsoft Outlook, attualmente visualizzato nell'area di notifica, può ora essere indicato tramite una sovrimpressione sul pulsante della barra delle applicazioni. Anche in questo caso, è necessario decidere durante il ciclo di sviluppo quale metodo è più adatto per l'applicazione. Le icone di sovrimpressione hanno lo scopo di fornire importanti notifiche o stati di lunga durata, ad esempio lo stato della rete, lo stato di Messenger o un nuovo messaggio di posta elettronica. All'utente non devono essere presentate sovrimpressione o animazioni in continua evoluzione.

Poiché una singola sovrimpressione è sovrapposta al pulsante della barra delle applicazioni e non alle anteprime delle singole finestre, si tratta di una funzionalità per gruppo anziché per finestra. Le richieste di icone di sovrimpressione possono essere ricevute da singole finestre in un gruppo della barra delle applicazioni, ma non vengono accodato. L'ultima sovrimpressione ricevuta è la sovrimpressione visualizzata.

### <a name="apis"></a>API

-   [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon)

## <a name="progress-bars"></a>Barre di stato

Un pulsante della barra delle applicazioni può essere usato per visualizzare un indicatore di stato. Ciò consente a una finestra di fornire informazioni sullo stato all'utente senza che l'utente sia necessario passare alla finestra stessa. L'utente può rimanere produttivo in un'altra applicazione e visualizzare a colpo d'occhio lo stato di avanzamento di una o più operazioni che si verificano in altre finestre. È previsto che un indicatore di stato in un pulsante della barra delle applicazioni rifletta un indicatore di stato più dettagliato nella finestra stessa. Questa funzionalità può essere usata per tenere traccia di copie di file, download, installazioni, file multimediali o qualsiasi operazione che potrebbe richiedere un periodo di tempo. Questa funzionalità non è destinata all'uso con azioni normalmente periferiche, ad esempio il caricamento di una pagina Web o la stampa di un documento. Questo tipo di stato deve continuare a essere visualizzato nella barra di stato di una finestra.

L'indicatore di stato del pulsante della barra delle applicazioni è simile al noto controllo Indicatore di stato. Può visualizzare lo stato di avanzamento determinato in base a una percentuale completata dell'operazione o uno stato di avanzamento indeterminato in stile di selezione per indicare che l'operazione è in corso senza alcuna stima del tempo rimanente. Può anche mostrare che l'operazione è sospesa o ha rilevato un errore e richiede l'intervento dell'utente.

### <a name="apis"></a>API

-   [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate)
-   [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue)

## <a name="deskbands"></a>Deskbands

Nelle versioni di Windows precedenti a Windows 7, è possibile ottenere un risultato simile alla funzionalità della barra degli strumenti di anteprima tramite una banda da tavolo, una barra degli strumenti ospitata nella barra delle applicazioni. Ad esempio, Windows Media Player possibile ridurre a icona la barra delle applicazioni come un set di controlli di trasporto anziché un pulsante standard. In Windows 7, i deskband possono ancora essere implementati e le barre degli strumenti delle anteprime non sono progettate per sostituirli tutti. Non tutte le applicazioni si prestano a una barra degli strumenti di anteprima e un'altra soluzione, ad esempio una banda da tavolo o un'attività in un elenco di destinazione, potrebbe essere la risposta giusta per l'applicazione. È necessario decidere quale soluzione funziona meglio per l'applicazione come parte del ciclo di sviluppo. Tuttavia, tenere presente che i deskband devono supportare Windows Con traslucidità ("glass") abilitata e [**l'interfaccia IDeskBand2.**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

### <a name="apis"></a>API

-   [**IDeskBand2**](/windows/desktop/api/Shobjidl/nn-shobjidl-ideskband2)

## <a name="notification-area"></a>Area di notifica

Sono state apportate modifiche all'area di notifica che offrono all'utente un maggiore controllo sulle icone visualizzate sulla barra delle applicazioni. Tutte le icone di notifica sono ora nascoste per impostazione predefinita e non è possibile controllare la visibilità a livello di codice. Solo l'utente può scegliere quali icone di notifica visualizzare sulla barra delle applicazioni. Quando viene visualizzato un fumetto di notifica, l'icona diventa temporaneamente visibile, ma anche in questo caso un utente può scegliere di disattivarle. Una sovrimpressione dell'icona su un pulsante della barra delle applicazioni diventa quindi una scelta interessante quando si vuole che l'applicazione comunichi le informazioni agli utenti.

## <a name="thumbnails"></a>Anteprime

In Windows Vista, passando il puntatore del mouse sul pulsante della barra delle applicazioni di un'applicazione viene visualizzata un'anteprima che rappresenta la finestra in esecuzione. Se la barra delle applicazioni ha compresso le finestre dell'applicazione, l'anteprima lo rappresenta visualizzando come stack, ma solo la finestra attiva viene visualizzata nell'anteprima stessa.

Nella Windows 7, ogni membro di un gruppo viene visualizzato come anteprima separata ed è ora anche una destinazione switch. Un'applicazione può definire i relativi elementi figlio (ad esempio finestre figlio vere, singoli documenti o schede) e fornire anteprime corrispondenti per ognuna di queste finestre anche quando normalmente non vengono visualizzate nella barra delle applicazioni. In questo modo gli utenti possono passare direttamente alla visualizzazione dell'applicazione desiderata anziché passare all'applicazione e quindi passare alla destinazione. Ad esempio, le applicazioni con interfaccia a documenti multipli (MDI)/Interfaccia documento a schede (TDI) possono visualizzare ogni documento o scheda come anteprima separata e passare alla destinazione quando il puntatore del mouse viene posizionato sul pulsante della barra delle applicazioni di un gruppo.

![tre anteprime della barra delle applicazioni che rappresentano singole schede in Windows Internet Explorer](images/taskbar/taskbarthumbnails.png)

> [!Note]  
> Come in Windows Vista, Per visualizzare le anteprime Deve essere attiva.

 

### <a name="api"></a>API

-   [**ITaskbarList3::RegisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-registertab)
-   [**ITaskbarList3::SetTabActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settabactive)
-   [**ITaskbarList3::SetTabOrder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-settaborder)
-   [**ITaskbarList3::UnregisterTab**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-unregistertab)
-   [**ITaskbarList4::SetTabProperties**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties)

Le rappresentazioni di anteprima per le finestre sono in genere automatiche, ma nei casi in cui il risultato non è ottimale, l'anteprima può essere specificata in modo esplicito. Per impostazione predefinita, solo le finestre di primo livello hanno un'anteprima generata automaticamente e le anteprime per le finestre figlio vengono visualizzate come rappresentazione generica. Ciò può comportare un'esperienza meno che ideale (e anche poco chiara) per l'utente finale. Un'anteprima specifica della destinazione del commutatore per ogni finestra figlio, ad esempio, offre un'esperienza utente molto migliore.

### <a name="api"></a>API

-   [**DwmSetWindowAttribute**](/windows/win32/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)
-   [**DwmSetIconicThumbnail**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticonicthumbnail)
-   [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap)
-   [**DwmInvalidateIconicBitmaps**](/windows/win32/api/dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
-   [**WM \_ DWMSENDICONICTHUMBNAIL**](../dwm/wm-dwmsendiconicthumbnail.md)
-   [**WM \_ DWMSENDICONICLIVEPREVIEWBITMAP**](../dwm/wm-dwmsendiconiclivepreviewbitmap.md)

È possibile selezionare una particolare area della finestra da usare come anteprima. Ciò può essere utile quando un'applicazione sa che i documenti o le schede saranno simili quando vengono visualizzati con le dimensioni dell'anteprima. L'applicazione può quindi scegliere di visualizzare solo la parte della relativa area client che l'utente può usare per distinguere le anteprime. Tuttavia, passando il puntatore del mouse su qualsiasi anteprima viene visualizzata una visualizzazione dell'intera finestra dietro di essa, in modo che l'utente possa visualizzare rapidamente anche le anteprime.

Se sono presenti più anteprime di quelle che è possibile visualizzare, l'anteprima ripristina l'anteprima legacy o un'icona standard.

### <a name="api"></a>API

-   [**ITaskbarList3::SetThumbnailClip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setthumbnailclip)

Per aggiungere **Aggiungi** alla barra delle applicazioni al menu di scelta rapida di un elemento, che in genere è necessario solo per i tipi di file che includono la voce [IsShortCut,](./links.md) viene eseguita registrando il gestore del menu di scelta rapida appropriato. Questo vale anche per **Aggiungi al menu Start**. Per [altre informazioni, vedere Registrazione dei gestori delle estensioni](reg-shell-exts.md) della shell.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra delle applicazioni](taskbar.md)
</dt> <dt>

[ID modello utente applicazione (AppUserModelID)](appids.md)
</dt> <dt>

[Notifiche e area di notifica](notification-area.md)
</dt> </dl>

 

 
