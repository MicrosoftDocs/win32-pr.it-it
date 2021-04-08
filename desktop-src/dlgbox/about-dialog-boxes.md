---
title: Finestre di dialogo Informazioni
description: In questo argomento viene illustrato l'utilizzo delle finestre di dialogo per creare interfacce utente per le applicazioni.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- finestre di dialogo, informazioni
- finestre di dialogo, quando utilizzare
- finestre di dialogo modali
- finestre di dialogo non modali
- finestre di dialogo, modali
- finestre di dialogo, non modale
- finestre di dialogo, modelli
- finestre di dialogo, finestre proprietarie
- finestre di dialogo, finestre di messaggio
- routine della finestra di dialogo
- finestre di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dd78713c3b87e54e8a992ea9415577c522fc9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047124"
---
# <a name="about-dialog-boxes"></a>Finestre di dialogo Informazioni

Sono disponibili numerose funzioni, messaggi e controlli predefiniti che consentono di creare e gestire finestre di dialogo, semplificando così lo sviluppo dell'interfaccia utente per un'applicazione. In questa panoramica vengono descritte le funzioni e i messaggi della finestra di dialogo e viene illustrato come utilizzarli per creare e utilizzare le finestre di dialogo.

Questa panoramica include gli argomenti seguenti:

-   [Quando usare una finestra di dialogo](#when-to-use-a-dialog-box)
-   [Finestra del proprietario della finestra di dialogo](#dialog-box-owner-window)
-   [Finestre di messaggio](#message-boxes)
-   [Finestre di dialogo modali](#modal-dialog-boxes)
-   [Finestre di dialogo non modali](#modeless-dialog-boxes)
-   [Modelli di finestra di dialogo](#dialog-box-templates)
    -   [Stili del modello della finestra di dialogo](#dialog-box-template-styles)
    -   [Misurazioni della finestra di dialogo](#dialog-box-measurements)
    -   [Controlli della finestra di dialogo](#dialog-box-controls)
    -   [Menu finestra di dialogo](#dialog-box-window-menu)
    -   [Tipi di carattere della finestra di dialogo](#dialog-box-fonts)
    -   [Modelli in memoria](#templates-in-memory)

Per ulteriori informazioni sulle finestre di dialogo comuni, vedere [Common Dialog Box Library](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Quando usare una finestra di dialogo

La maggior parte delle applicazioni usa le finestre di dialogo per richiedere informazioni aggiuntive per le voci di menu che richiedono l'input dell'utente. L'uso di una finestra di dialogo è l'unico modo consigliato per recuperare l'input da parte di un'applicazione. Ad esempio, una tipica voce di menu **Apri** richiede il nome di un file da aprire, quindi un'applicazione deve usare una finestra di dialogo per richiedere all'utente il nome. In questi casi, l'applicazione crea la finestra di dialogo quando l'utente fa clic sulla voce di menu ed elimina la finestra di dialogo immediatamente dopo che l'utente ha fornito le informazioni.

Molte applicazioni usano anche le finestre di dialogo per visualizzare informazioni o opzioni mentre l'utente lavora in un'altra finestra. Ad esempio, le applicazioni di elaborazione di Word utilizzano spesso una finestra di dialogo con un'opzione di ricerca di testo. Mentre l'applicazione cerca il testo, la finestra di dialogo rimane sullo schermo. L'utente può quindi tornare alla finestra di dialogo e cercare nuovamente la stessa parola. in alternativa, l'utente può modificare la voce nella finestra di dialogo e cercare una nuova parola. Le applicazioni che utilizzano le finestre di dialogo in questo modo in genere ne creano una quando l'utente fa clic sulla voce di menu e continua a visualizzarla fino a quando l'applicazione è in esecuzione o fino a quando l'utente non chiude in modo esplicito la finestra di dialogo.

Per supportare le diverse modalità di utilizzo delle finestre di dialogo da parte delle applicazioni, sono disponibili due tipi di finestra di dialogo: modale e non modale. Una finestra di *dialogo modale* richiede all'utente di fornire informazioni o annullare la finestra di dialogo prima di consentire all'applicazione di continuare. Le applicazioni utilizzano le finestre di dialogo modali insieme alle voci di menu che richiedono informazioni aggiuntive prima di poter continuare. Una finestra di *dialogo non modale* consente all'utente di fornire informazioni e tornare all'attività precedente senza chiudere la finestra di dialogo. Le finestre di dialogo modali sono più semplici da gestire rispetto alle finestre di dialogo non modali perché vengono create, eseguono le attività e vengono distrutte chiamando una singola funzione.

Per creare una finestra di dialogo modale o non modale, un'applicazione deve fornire un modello di finestra di dialogo per descrivere lo stile e il contenuto della finestra di dialogo. l'applicazione deve inoltre fornire una routine della finestra di dialogo per eseguire le attività. Il *modello* della finestra di dialogo è una descrizione binaria della finestra di dialogo e dei controlli in essa contenuti. Lo sviluppatore può creare questo modello come risorsa da caricare dal file eseguibile dell'applicazione o creato in memoria durante l'esecuzione dell'applicazione. La *routine* della finestra di dialogo è una funzione di callback definita dall'applicazione chiamata dal sistema quando dispone di un input per la finestra di dialogo o le attività per la finestra di dialogo da eseguire. Anche se una routine della finestra di dialogo è simile a una routine della finestra, non ha le stesse responsabilità.

In genere, un'applicazione crea una finestra di dialogo tramite la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) . **DialogBox** crea una finestra di dialogo modale; **CreateDialog** crea una finestra di dialogo non modale. Queste due funzioni caricano un modello di finestra di dialogo dal file eseguibile dell'applicazione e creano una finestra popup che corrisponde alle specifiche del modello. Sono disponibili altre funzioni che creano una finestra di dialogo usando i modelli in memoria. passano informazioni aggiuntive alla routine della finestra di dialogo durante la creazione della finestra di dialogo.

In genere, le finestre di dialogo appartengono a una classe di finestra esclusiva e predefinita. Il sistema utilizza questa classe della finestra e la corrispondente routine della finestra per le finestre di dialogo modali e non modali. Quando la funzione viene chiamata, crea la finestra per la finestra di dialogo, nonché le finestre per i controlli nella finestra di dialogo, quindi invia i messaggi selezionati alla routine della finestra di dialogo. Quando la finestra di dialogo è visibile, la routine della finestra predefinita gestisce tutti i messaggi, elaborando alcuni messaggi e passando altri alla routine della finestra di dialogo in modo che la procedura possa eseguire le attività. Le applicazioni non dispongono di accesso diretto alla classe della finestra o alla routine della finestra predefinita, ma possono utilizzare il modello della finestra di dialogo e la procedura della finestra di dialogo per modificare lo stile e il comportamento di una finestra di dialogo.

## <a name="dialog-box-owner-window"></a>Finestra del proprietario della finestra di dialogo

Per la maggior parte delle finestre di dialogo è presente una finestra proprietaria (o più semplicemente un proprietario). Quando si crea la finestra di dialogo, l'applicazione imposta il proprietario specificando l'handle della finestra del proprietario. Il sistema utilizza il proprietario per determinare la posizione della finestra di dialogo nel z order in modo che la finestra di dialogo sia sempre posizionata sopra il proprietario. Inoltre, il sistema può inviare messaggi alla routine della finestra del proprietario, inviando notifiche sugli eventi nella finestra di dialogo.

Il sistema nasconde o Elimina automaticamente la finestra di dialogo ogni volta che il proprietario viene nascosto o eliminato definitivamente. Ciò significa che la routine della finestra di dialogo non richiede alcuna elaborazione speciale per rilevare le modifiche apportate allo stato della finestra proprietaria.

Poiché la finestra di dialogo tipica viene utilizzata insieme a una voce di menu, la finestra proprietaria è in genere la finestra contenente il menu. Sebbene sia possibile creare una finestra di dialogo senza proprietario, non è consigliabile. Ad esempio, quando una finestra di dialogo modale non dispone di un proprietario, il sistema non Disabilita alcuna delle altre finestre dell'applicazione e consente all'utente di continuare a eseguire il lavoro nelle altre finestre, vanificando lo scopo della finestra di dialogo modale.

Quando una finestra di dialogo non modale non dispone di un proprietario, il sistema non nasconde né elimina la finestra di dialogo quando altre finestre nell'applicazione vengono nascoste o distrutte. Sebbene questo non superi lo scopo della finestra di dialogo non modale, è necessario che l'applicazione effettui un'elaborazione speciale per assicurarsi che la finestra di dialogo venga nascosta ed eliminata in momenti appropriati.

## <a name="message-boxes"></a>Finestre di messaggio

Una finestra di messaggio è una finestra di dialogo speciale che può essere utilizzata da un'applicazione per visualizzare i messaggi e richiedere un input semplice. Una finestra di messaggio contiene in genere un messaggio di testo e uno o più pulsanti. Un'applicazione crea la finestra di messaggio utilizzando la funzione [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , specificando il testo e il numero e i tipi di pulsanti da visualizzare. Si noti che attualmente non esiste alcuna differenza tra il funzionamento di **MessageBox** e **MessageBoxEx** .

Sebbene la finestra di messaggio sia una finestra di dialogo, il sistema acquisisce il controllo completo della creazione e della gestione della finestra di messaggio. Ciò significa che l'applicazione non fornisce un modello di finestra di dialogo e una procedura di finestra di dialogo. Il sistema crea il proprio modello in base al testo e ai pulsanti specificati per la finestra di messaggio e fornisce la propria routine della finestra di dialogo.

Una finestra di messaggio è una finestra di dialogo modale che viene creata dal sistema utilizzando le stesse funzioni interne utilizzate da [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) . Se l'applicazione specifica una finestra proprietaria quando si chiama [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa), il proprietario viene disabilitato dal sistema. Un'applicazione può anche indicare al sistema di disabilitare tutte le finestre di primo livello che appartengono al thread corrente specificando il valore **MB \_ TASKMODAL** durante la creazione della finestra di dialogo.

Il sistema può inviare messaggi al proprietario, ad esempio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) e [**WM \_ Enable**](/windows/desktop/winmsg/wm-enable), così come avviene quando si crea una finestra di dialogo modale. La finestra proprietario deve eseguire qualsiasi azione richiesta da questi messaggi.

## <a name="modal-dialog-boxes"></a>Finestre di dialogo modali

Una finestra di dialogo modale dovrebbe essere una finestra popup con un menu finestra, una barra del titolo e un bordo spessa; ovvero, nel modello della finestra di dialogo devono essere specificati gli stili **WS \_ popup**, **WS \_ SYSMENU**, **WS \_ Caption** e **DS \_ MODALFRAME** . Sebbene un'applicazione possa designare lo stile di visualizzazione **WS \_** , il sistema Visualizza sempre una finestra di dialogo modale indipendentemente dal fatto che il modello di finestra di dialogo specifichi lo stile **\_ visibile di WS** . Un'applicazione non deve creare una finestra di dialogo modale con lo stile **WS \_ figlio** . Una finestra di dialogo modale con questo stile viene disabilitata, impedendo a tutti gli input successivi di raggiungere l'applicazione.

Un'applicazione crea una finestra di dialogo modale utilizzando la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) . **DialogBox** richiede il nome o l'identificatore di una risorsa che contiene un modello di finestra di dialogo. **DialogBoxIndirect** richiede un handle a un oggetto memoria contenente un modello di finestra di dialogo. Le funzioni [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) e [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) creano anche finestre di dialogo modali. sono identici alle funzioni indicate in precedenza, ma passano un parametro specificato alla routine della finestra di dialogo quando viene creata la finestra di dialogo.

Quando si crea la finestra di dialogo modale, il sistema lo rende la finestra attiva. La finestra di dialogo rimane attiva fino a quando la routine della finestra di dialogo chiama la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) o il sistema attiva una finestra in un'altra applicazione. Né l'utente né l'applicazione possono rendere attiva la finestra proprietaria finché non viene eliminata definitivamente la finestra di dialogo modale.

Quando la finestra proprietaria non è già disabilitata, il sistema Disabilita automaticamente la finestra e tutte le finestre figlio appartenenti al momento in cui viene creata la finestra di dialogo modale. La finestra proprietaria rimane disabilitata fino a quando la finestra di dialogo non viene distrutta. Anche se una routine della finestra di dialogo potrebbe potenzialmente abilitare la finestra proprietaria in qualsiasi momento, l'abilitazione del proprietario sconfigge lo scopo della finestra di dialogo modale e non è consigliata. Quando la routine della finestra di dialogo viene distrutta, il sistema Abilita di nuovo la finestra proprietaria, ma solo se la finestra di dialogo modale ha causato la disabilitazione del proprietario.

Quando il sistema crea la finestra di dialogo modale, invia il [**messaggio \_ CANCELMODE WM**](/windows/desktop/winmsg/wm-cancelmode) alla finestra (se presente) che attualmente acquisisce l'input del mouse. Un'applicazione che riceve questo messaggio deve rilasciare il mouse capture in modo che l'utente possa spostare il mouse nella finestra di dialogo modale. Poiché il sistema Disabilita la finestra proprietaria, l'input del mouse viene perso se il proprietario non riesce a rilasciare il mouse alla ricezione del messaggio.

Per elaborare i messaggi per la finestra di dialogo modale, il sistema avvia il proprio ciclo di messaggi, assumendo il controllo temporaneo della coda di messaggi per l'intera applicazione. Quando il sistema Recupera un messaggio che non è in modo esplicito per la finestra di dialogo, il messaggio viene inviato alla finestra appropriata. Se viene recuperato un messaggio [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) , il messaggio viene inserito di nuovo nella coda di messaggi dell'applicazione in modo che il ciclo di messaggi principale dell'applicazione possa recuperare il messaggio.

Il sistema invia il messaggio [**WM \_ ENTERIDLE**](wm-enteridle.md) alla finestra proprietaria ogni volta che la coda di messaggi dell'applicazione è vuota. L'applicazione può utilizzare questo messaggio per eseguire un'attività in background mentre la finestra di dialogo rimane sullo schermo. Quando un'applicazione utilizza il messaggio in questo modo, l'applicazione deve spesso restituire il controllo, ad esempio utilizzando la funzione [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) , in modo che la finestra di dialogo modale possa ricevere qualsiasi input utente. Per evitare che la finestra di dialogo modale invii i messaggi **WM \_ ENTERIDLE** , l'applicazione può specificare lo \_ stile DS NOIDLEMSG durante la creazione della finestra di dialogo.

Un'applicazione elimina una finestra di dialogo modale utilizzando la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) . Nella maggior parte dei casi, la routine della finestra di dialogo chiama **EndDialog** quando l'utente fa clic su **Chiudi** dal menu della finestra di dialogo o fa clic sul pulsante **OK** o **Annulla** nella finestra di dialogo. La finestra di dialogo può restituire un valore tramite la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (o altre funzioni di creazione) specificando un valore quando si chiama la funzione **EndDialog** . Il sistema restituisce questo valore dopo la distruzione della finestra di dialogo. La maggior parte delle applicazioni utilizza questo valore restituito per determinare se la finestra di dialogo ha completato correttamente l'attività o è stata annullata dall'utente. Il sistema non restituisce il controllo dalla funzione che crea la finestra di dialogo fino a quando la routine della finestra di dialogo non ha chiamato la funzione **EndDialog** .

## <a name="modeless-dialog-boxes"></a>Finestre di dialogo non modali

Una finestra di dialogo non modale dovrebbe essere una finestra popup con un menu finestra, una barra del titolo e un bordo sottile; ovvero, nel modello della finestra di dialogo devono essere specificati gli stili **WS \_ popup**, **WS \_ Caption**, **WS \_ Border** e **WS \_ SYSMENU** . Il sistema non visualizza automaticamente la finestra di dialogo, a meno che il modello non specifichi lo stile **\_ visibile WS** .

Un'applicazione crea una finestra di dialogo non modale usando la funzione [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) o [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) . **CreateDialog** richiede il nome o l'identificatore di una risorsa che contiene un modello di finestra di dialogo. **CreateDialogIndirect** richiede un handle a un oggetto memoria contenente un modello di finestra di dialogo. Altre due funzioni, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) e [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), creano anche finestre di dialogo non modali. passano un parametro specificato alla routine della finestra di dialogo quando viene creata la finestra di dialogo.

[**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) e altre funzioni di creazione restituiscono un handle di finestra alla finestra di dialogo. L'applicazione e la routine della finestra di dialogo possono utilizzare questo handle per gestire la finestra di dialogo. Se, ad esempio, **WS \_ Visible** non è specificato nel modello della finestra di dialogo, l'applicazione può visualizzare la finestra di dialogo passando l'handle della finestra alla funzione [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

Una finestra di dialogo non modale non consente di disabilitare la finestra proprietaria né di inviarvi messaggi. Quando si crea la finestra di dialogo, il sistema lo rende la finestra attiva, ma l'utente o l'applicazione può modificare la finestra attiva in qualsiasi momento. Se la finestra di dialogo diventa inattiva, resta al di sopra della finestra proprietaria nella z order, anche se la finestra proprietaria è attiva.

L'applicazione è responsabile del recupero e dell'invio di messaggi di input alla finestra di dialogo. Per la maggior parte delle applicazioni viene utilizzato il ciclo di messaggi principale per. Per consentire all'utente di spostarsi e selezionare i controlli tramite la tastiera, tuttavia, l'applicazione deve chiamare la funzione [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) . Per ulteriori informazioni su questa funzione, vedere [interfaccia della tastiera della finestra di dialogo](dlgbox-programming-considerations.md).

Una finestra di dialogo non modale non può restituire un valore all'applicazione come finestra di dialogo modale, ma la routine della finestra di dialogo può inviare informazioni alla finestra proprietaria utilizzando la funzione [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

Un'applicazione deve eliminare tutte le finestre di dialogo non modali prima di terminare. Può eliminare una finestra di dialogo non modale usando la funzione [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Nella maggior parte dei casi, la routine della finestra di dialogo chiama **DestroyWindow** in risposta all'input dell'utente, ad esempio facendo clic sul pulsante **Annulla** . Se l'utente non chiude mai la finestra di dialogo in questo modo, l'applicazione deve chiamare **DestroyWindow**.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalida l'handle della finestra per la finestra di dialogo, in modo che tutte le chiamate successive alle funzioni che usano l'handle restituiscano i valori di errore. Per evitare errori, la routine della finestra di dialogo deve notificare al proprietario che la finestra di dialogo è stata eliminata definitivamente. Molte applicazioni gestiscono una variabile globale contenente l'handle per la finestra di dialogo. Quando la routine della finestra di dialogo Elimina la finestra di dialogo, imposta anche la variabile globale su **null**, a indicare che la finestra di dialogo non è più valida.

La routine della finestra di dialogo non deve chiamare la funzione [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per eliminare definitivamente una finestra di dialogo non modale.

## <a name="dialog-box-templates"></a>Modelli di finestra di dialogo

Un modello di finestra di dialogo è dati binari che descrivono la finestra di dialogo, definendo l'altezza, la larghezza, lo stile e i controlli in esso contenuti. Per creare una finestra di dialogo, il sistema carica un modello di finestra di dialogo dalle risorse nel file eseguibile dell'applicazione oppure utilizza il modello passato nella memoria globale dall'applicazione. In entrambi i casi, l'applicazione deve fornire un modello durante la creazione di una finestra di dialogo.

Uno sviluppatore crea le risorse del modello usando un compilatore di risorse o un editor della finestra di dialogo. Un compilatore di risorse converte una descrizione di testo in una risorsa binaria e un editor della finestra di dialogo Salva una finestra di dialogo costruita in modo interattivo come risorsa binaria.

> [!Note]  
> Una spiegazione di come creare le risorse modello e aggiungerle al file eseguibile dell'applicazione esula dall'ambito di questa panoramica. Per ulteriori informazioni sulla creazione di risorse modello e sull'aggiunta di tali risorse a un file eseguibile, vedere la documentazione fornita con gli strumenti di sviluppo dell'applicazione.

 

Per creare una finestra di dialogo senza usare le risorse modello, è necessario creare un modello in memoria e passarlo alla funzione [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) o [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) oppure alla macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) o [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

Un modello di finestra di dialogo in memoria è costituito da un'intestazione che descrive la finestra di dialogo, seguita da uno o più blocchi di dati aggiuntivi che descrivono ognuno dei controlli della finestra di dialogo. Il modello può usare il formato standard o il formato esteso. In un modello standard, l'intestazione è una struttura [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguita da matrici di lunghezza variabile aggiuntive. e i dati per ogni controllo sono costituiti da una struttura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello di finestra di dialogo esteso l'intestazione usa il formato [**DLGTEMPLATEEX**](dlgtemplateex.md) e le definizioni dei controlli usano il formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

È possibile creare un modello di memoria allocando un oggetto memoria globale e inserendolo con le definizioni standard o estesa dell'intestazione e del controllo. Un modello di memoria è identico in forma e contenuto a una risorsa modello. Molte applicazioni che usano i modelli di memoria usano prima la funzione [**LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) per caricare una risorsa modello in memoria, quindi modificare la risorsa caricata per creare un nuovo modello di memoria. Per ulteriori informazioni sulla creazione di un modello di finestra di dialogo in memoria, vedere [modelli in memoria](#templates-in-memory).

Nelle sezioni seguenti vengono descritti gli stili, le misurazioni e altri valori utilizzati in un modello di finestra di dialogo.

-   [Stili del modello della finestra di dialogo](#dialog-box-template-styles)
-   [Misurazioni della finestra di dialogo](#dialog-box-measurements)
-   [Controlli della finestra di dialogo](#dialog-box-controls)
-   [Menu finestra di dialogo](#dialog-box-window-menu)
-   [Tipi di carattere della finestra di dialogo](#dialog-box-fonts)
-   [Modelli in memoria](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Stili del modello della finestra di dialogo

Ogni modello di finestra di dialogo specifica una combinazione di valori di stile che definiscono l'aspetto e le funzionalità della finestra di dialogo. I valori di stile possono essere stili di finestra, ad esempio **WS \_ popup** e **WS \_ SYSMENU**, e stili della finestra di dialogo, ad esempio **DS \_ MODALFRAME**. Il numero e il tipo di stili per un modello dipendono dal tipo e dallo scopo della finestra di dialogo. Per un elenco di valori, vedere [**stili della finestra di dialogo**](dialog-box-styles.md).

Il sistema passa tutti gli stili della finestra specificati nel modello alla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) durante la creazione della finestra di dialogo. Il sistema può passare uno o più stili estesi a seconda degli stili specificati per la finestra di dialogo. Ad esempio, quando il modello specifica **DS \_ MODALFRAME**, il sistema usa **WS \_ ex \_ DLGMODALFRAME** durante la creazione della finestra di dialogo.

La maggior parte delle finestre di dialogo sono finestre popup con un menu finestra e una barra del titolo. Pertanto, il modello tipico specifica gli stili del **\_ titolo** WS **\_ popup**, **WS \_ SYSMENU** e WS. Il modello specifica inoltre uno stile del bordo: **WS \_ Border** per le finestre di dialogo non modali e **DS \_ MODALFRAME** per le finestre di dialogo modali. Un modello può specificare un tipo di finestra diverso da popup (ad esempio **WS \_ OVERLAPPED**) se crea una finestra personalizzata anziché una finestra di dialogo.

Il sistema Visualizza sempre una finestra di dialogo modale indipendentemente dal fatto che lo stile di visualizzazione **WS \_** sia specificato. Quando il modello per una finestra di dialogo non modale specifica lo stile di visualizzazione **WS \_** , il sistema visualizza automaticamente la finestra di dialogo al momento della creazione. In caso contrario, l'applicazione è responsabile della visualizzazione della finestra di dialogo mediante la funzione [**ShowWindow**](/windows/desktop/api/winuser/nf-winuser-showwindow) .

### <a name="dialog-box-measurements"></a>Misurazioni della finestra di dialogo

Ogni modello di finestra di dialogo contiene misure che specificano la posizione, la larghezza e l'altezza della finestra di dialogo e i controlli in esso contenuti. Queste misurazioni sono indipendenti dal dispositivo, quindi un'applicazione può usare un singolo modello per creare la stessa finestra di dialogo per tutti i tipi di dispositivi di visualizzazione. In questo modo si garantisce che una finestra di dialogo abbia le stesse proporzioni e l'aspetto di tutte le schermate nonostante le diverse risoluzioni e le proporzioni tra le schermate.

Le misurazioni in un modello di finestra di dialogo vengono specificate nelle unità del modello di finestra di dialogo. Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la funzione [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) , che prende in considerazione il tipo di carattere usato dalla finestra di dialogo e converte correttamente un rettangolo dalle unità del modello di finestra in pixel. Per le finestre di dialogo che usano il tipo di carattere del sistema, è possibile usare la funzione [**GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) per eseguire manualmente i calcoli di conversione, anche se l'uso di **MapDialogRect** è più semplice.

Il modello deve specificare le coordinate iniziali dell'angolo superiore sinistro della finestra di dialogo. In genere le coordinate sono relative all'angolo superiore sinistro dell'area client della finestra proprietaria. Quando il modello specifica lo \_ stile DS ABSALIGN o la finestra di dialogo non dispone di un proprietario, la posizione è relativa all'angolo superiore sinistro dello schermo. Il sistema imposta questa posizione iniziale durante la creazione della finestra di dialogo, ma consente a un'applicazione di modificare la posizione prima di visualizzare la finestra di dialogo. Ad esempio, un'applicazione può recuperare le dimensioni della finestra proprietaria, calcolare una nuova posizione che centra la finestra di dialogo nella finestra proprietaria, quindi impostare la posizione utilizzando la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Il modello deve specificare una larghezza e un'altezza della finestra di dialogo che non superino la larghezza e l'altezza dello schermo e garantisce che tutti i controlli si trovino nell'area client della finestra di dialogo. Sebbene il sistema consenta a una finestra di dialogo di essere di qualsiasi dimensione, la creazione di un valore troppo piccolo o troppo grande può impedire all'utente di fornire input, vanificando lo scopo della finestra di dialogo. In molte applicazioni viene utilizzata più di una finestra di dialogo in presenza di un numero elevato di controlli. In questi casi, la finestra di dialogo iniziale contiene in genere uno o più pulsanti che l'utente può scegliere di visualizzare la finestra di dialogo successiva.

### <a name="dialog-box-controls"></a>Controlli della finestra di dialogo

Il modello specifica la posizione, la larghezza, l'altezza, lo stile, l'identificatore e la classe della finestra per ogni controllo nella finestra di dialogo. Il sistema crea ogni controllo passando questi dati alla funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . I controlli vengono creati nell'ordine in cui sono specificati nel modello. Il modello deve specificare il numero, il tipo e l'ordine dei controlli appropriati per assicurarsi che l'utente possa immettere l'input necessario per completare l'attività associata alla finestra di dialogo.

Per ogni controllo, il modello specifica i valori di stile che definiscono l'aspetto e il funzionamento del controllo. Ogni controllo è una finestra figlio e pertanto deve avere lo stile **WS \_ figlio** . Per assicurarsi che il controllo sia visibile quando viene visualizzata la finestra di dialogo, anche ogni controllo deve avere lo stile di visualizzazione **WS \_** . Altri stili di finestra comunemente usati sono il **\_ bordo WS** per i controlli che dispongono di bordi facoltativi, **WS \_ disabled** per i controlli che devono essere disabilitati quando la finestra di dialogo viene inizialmente creata e **WS \_ TABSTOP** e **WS \_ Group** per i controlli a cui è possibile accedere tramite la tastiera. Gli stili **WS \_ TABSTOP** e **WS \_ Group** vengono utilizzati insieme all'interfaccia della tastiera della finestra di dialogo descritta più avanti in questo argomento.

Il modello può inoltre specificare gli stili di controllo specifici della classe finestra del controllo. Ad esempio, un modello che specifica un controllo Button deve fornire uno stile di controllo Button, ad esempio il pulsante **BS \_** o la **\_ casella** di controllo BS. Il sistema passa gli stili del controllo alla routine della finestra di controllo tramite il messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) , consentendo alla procedura di adattare l'aspetto e il funzionamento del controllo.

Il sistema converte le coordinate di posizione e le misurazioni di larghezza e altezza dalle unità di base della finestra di dialogo ai pixel, prima di passarle a [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Quando il sistema crea un controllo, specifica la finestra di dialogo come finestra padre. Ciò significa che il sistema interpreta sempre le coordinate di posizione del controllo come coordinate client, in relazione all'angolo superiore sinistro dell'area client della finestra di dialogo.

Il modello specifica la classe della finestra per ogni controllo. Una tipica finestra di dialogo contiene i controlli appartenenti alle classi della finestra di controllo predefinite, ad esempio le classi di finestra del controllo Button e Edit. In questo caso, il modello specifica le classi della finestra fornendo i valori Atom predefiniti corrispondenti per le classi. Quando una finestra di dialogo contiene un controllo che appartiene a una classe della finestra del controllo personalizzata, il modello restituisce il nome della classe di finestra registrata o il valore Atom attualmente associato al nome.

Ogni controllo in una finestra di dialogo deve avere un identificatore univoco per distinguerlo dagli altri controlli. I controlli inviano informazioni alla routine della finestra di dialogo tramite i messaggi di [**\_ comando WM**](/windows/desktop/menurc/wm-command) , quindi gli identificatori di controllo sono essenziali affinché la procedura determini quale controllo ha inviato un messaggio specificato. L'unica eccezione a questa regola è costituita dagli identificatori di controllo per i controlli statici. I controlli statici non richiedono identificatori univoci perché non inviano messaggi di **\_ comando WM** .

Per consentire all'utente di chiudere la finestra di dialogo, il modello deve specificare almeno un pulsante di push e assegnargli l'identificatore di controllo **IDCANCEL**. Per consentire all'utente di scegliere tra il completamento o l'annullamento dell'attività associata alla finestra di dialogo, nel modello devono essere specificati due pulsanti di push, con etichetta **OK** e **Annulla**, con identificatori di controllo rispettivamente **IDOK** e **IDCANCEL**.

Un modello specifica anche il testo facoltativo e i dati di creazione per un controllo. Il testo fornisce in genere etichette per i controlli Button o specifica il contenuto iniziale di un controllo testo statico. I dati di creazione sono uno o più byte di dati che il sistema passa alla routine della finestra di controllo durante la creazione del controllo. I dati di creazione sono utili per i controlli che richiedono ulteriori informazioni sul contenuto o lo stile iniziale rispetto a quello specificato da altri dati. Ad esempio, un'applicazione può usare i dati di creazione per impostare l'impostazione iniziale e l'intervallo per un controllo barra di scorrimento.

### <a name="dialog-box-window-menu"></a>Menu finestra di dialogo

Il sistema Visualizza una finestra di dialogo quando il modello specifica lo stile **WS \_ SYSMENU** . Per evitare un input non appropriato, il sistema Disabilita automaticamente tutti gli elementi del menu eccetto **Sposta** e **Chiudi**. L'utente può fare clic su **Sposta** per spostare la finestra di dialogo. Quando l'utente fa clic su **Chiudi**, il sistema invia un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) alla routine della finestra di dialogo con il parametro *wParam* impostato su **IDCANCEL**. Questo è identico al messaggio inviato dal pulsante **Annulla** quando l'utente fa clic su di esso. L'azione consigliata per questo messaggio consiste nel chiudere la finestra di dialogo e annullare l'attività richiesta.

Sebbene non sia consigliabile usare altri menu nelle finestre di dialogo, un modello di finestra di dialogo può specificare un menu fornendo l'identificatore o il nome di una risorsa di menu. In questo caso, il sistema carica la risorsa e crea il menu per la finestra di dialogo. Le applicazioni in genere utilizzano gli identificatori o i nomi dei menu nei modelli quando si utilizzano i modelli per creare finestre personalizzate anziché finestre di dialogo.

### <a name="dialog-box-fonts"></a>Tipi di carattere della finestra di dialogo

Il sistema utilizza la larghezza media dei caratteri del tipo di carattere della finestra di dialogo per calcolare la posizione e le dimensioni della finestra di dialogo. Per impostazione predefinita, il sistema disegna tutto il testo in una finestra di dialogo usando il tipo di carattere di **sistema \_** .

Per specificare un tipo di carattere per una finestra di dialogo diversa da quella predefinita, è necessario creare la finestra di dialogo utilizzando un modello di finestra di dialogo. In una risorsa modello usare l' [istruzione font](../menurc/font-statement.md). In un modello di finestra di dialogo, impostare lo stile **DS \_ sefont** o **DS \_ SHELLFONT** e specificare una dimensione del punto e un nome del carattere tipografico. Anche se un modello di finestra di dialogo specifica un tipo di carattere in questo modo, il sistema usa sempre il tipo di carattere del sistema per il titolo della finestra di dialogo e i menu della finestra di dialogo.

Quando la finestra di dialogo dispone dello stile **DS \_ sefont** o **DS \_ SHELLFONT** , il sistema invia un messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) alla routine della finestra di dialogo e a ogni controllo durante la creazione del controllo. La procedura della finestra di dialogo è responsabile del salvataggio dell'handle del tipo di carattere passato con il messaggio di **\_ tipo carattere di WM** e della selezione dell'handle nel contesto del dispositivo di visualizzazione ogni volta che scrive testo nella finestra. Per impostazione predefinita, i controlli predefiniti lo eseguono.

Il tipo di carattere del sistema può variare a seconda delle diverse versioni di Windows. Per fare in modo che l'applicazione usi il tipo di carattere del sistema indipendentemente dal sistema in cui è in esecuzione, usare **DS \_ SHELLFONT** con il carattere tipografico MS Shell Dlg e usare la [risorsa DIALOGEX](../menurc/dialogex-resource.md) anziché la [risorsa finestra di dialogo](../menurc/dialog-resource.md). Il sistema esegue il mapping di questo carattere tipografico in modo che la finestra di dialogo utilizzi il tipo di carattere Tahoma. Si noti che **DS \_ SHELLFONT** non ha alcun effetto se il carattere tipografico non è MS Shell Dlg.

### <a name="templates-in-memory"></a>Modelli in memoria

Un modello di finestra di dialogo in memoria è costituito da un'intestazione che descrive la finestra di dialogo, seguita da uno o più blocchi di dati aggiuntivi che descrivono ognuno dei controlli della finestra di dialogo. Il modello può usare il formato standard o il formato esteso. In un modello standard, l'intestazione è una struttura [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguita da matrici di lunghezza variabile aggiuntive. I dati per ogni controllo sono costituiti da una struttura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello di finestra di dialogo esteso l'intestazione usa il formato [**DLGTEMPLATEEX**](dlgtemplateex.md) e le definizioni dei controlli usano il formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Per distinguere tra un modello standard e un modello esteso, controllare i primi 16 bit di un modello di finestra di dialogo. In un modello esteso la prima **parola** è 0xFFFF; qualsiasi altro valore indica un modello standard.

Se si crea un modello di finestra di dialogo in memoria, è necessario assicurarsi che ogni definizione di controllo [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) sia allineata ai limiti **DWORD** . Inoltre, i dati di creazione che seguono la definizione di un controllo devono essere allineati su un limite **DWORD** . Tutte le altre matrici a lunghezza variabile in un modello di finestra di dialogo devono essere allineate sui limiti di **parola** .

### <a name="template-header"></a>Intestazione del modello

Nei modelli standard ed Extended per le finestre di dialogo, l'intestazione include le informazioni generali seguenti:

-   Posizione e dimensioni della finestra di dialogo
-   Gli stili della finestra e della finestra di dialogo per la finestra di dialogo
-   Numero di controlli nella finestra di dialogo. Questo valore determina il numero di definizioni di controllo [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) nel modello.
-   Risorsa di menu facoltativa per la finestra di dialogo. Il modello può indicare che la finestra di dialogo non dispone di un menu oppure è possibile specificare un valore ordinale o una stringa Unicode con terminazione null che identifichi una risorsa di menu in un file eseguibile.
-   Classe Window della finestra di dialogo. Può essere la classe della finestra di dialogo predefinita o un valore ordinale o una stringa Unicode con terminazione null che identifica una classe della finestra registrata.
-   Stringa Unicode con terminazione null che specifica il titolo della finestra di dialogo. Se la stringa è vuota, la barra del titolo della finestra di dialogo è vuota. Se la finestra di dialogo non ha lo stile della **\_ didascalia WS** , il sistema imposta il titolo sulla stringa specificata, ma non lo Visualizza.
-   Se nella finestra di dialogo è presente lo stile del tipo di **\_ carattere DS** , l'intestazione specifica le dimensioni e il nome tipografico del tipo di carattere da utilizzare per il testo nell'area client e i controlli della finestra di dialogo.

In un modello esteso, l'intestazione [**DLGTEMPLATEEX**](dlgtemplateex.md) specifica anche le informazioni aggiuntive seguenti:

-   Identificatore di contesto della guida della finestra di dialogo quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) .
-   Se nella finestra di dialogo è presente lo stile **DS \_ sefont** o **DS \_ SHELLFONT** , l'intestazione specifica lo spessore del carattere e indica se il tipo di carattere è in corsivo.

### <a name="control-definitions"></a>Definizioni dei controlli

La seguente intestazione del modello è costituita da una o più definizioni di controllo che descrivono i controlli della finestra di dialogo. Nei modelli standard ed Extended, l'intestazione della finestra di dialogo include un membro che indica il numero di definizioni di controllo nel modello. In un modello standard, ogni definizione di controllo è costituita da una struttura [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello esteso, le definizioni di controllo usano il formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) .

Nei modelli standard ed Extended la definizione del controllo include le informazioni seguenti:

-   Posizione e dimensioni del controllo.
-   Stili della finestra e del controllo per il controllo.
-   Identificatore del controllo.
-   Classe della finestra del controllo. Può corrispondere al valore ordinale di una classe di sistema predefinita o a una stringa Unicode con terminazione null che specifica il nome di una classe di finestra registrata.
-   Stringa Unicode con terminazione null che specifica il testo iniziale del controllo o un valore ordinale che identifica una risorsa, ad esempio un'icona, in un file eseguibile.
-   Un blocco facoltativo di lunghezza variabile dei dati di creazione. Quando il sistema crea il controllo, passa un puntatore a questi dati nel parametro *lParam* del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) inviato al controllo.

In un modello esteso la definizione del controllo specifica anche un identificatore di contesto della Guida per il controllo quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) .

 

 