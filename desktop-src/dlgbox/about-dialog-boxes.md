---
title: Finestre di dialogo Informazioni
description: Questo argomento illustra l'uso di finestre di dialogo per creare interfacce utente per le applicazioni.
ms.assetid: 51960c28-a178-4ad3-b45e-426fec42a945
keywords:
- finestre di dialogo, informazioni
- finestre di dialogo,quando usare
- finestre di dialogo modali
- finestre di dialogo non modali
- finestre di dialogo, modali
- finestre di dialogo, non modali
- finestre di dialogo,modelli
- finestre di dialogo, finestre proprietarie
- finestre di dialogo, finestre di messaggio
- procedure della finestra di dialogo
- finestre di messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7855ba67a04558e0df8ffad0f63d2bd78856f84829bf029fbf811a4b89eb4b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786809"
---
# <a name="about-dialog-boxes"></a>Finestre di dialogo Informazioni

Sono disponibili molte funzioni, messaggi e controlli predefiniti che consentono di creare e gestire finestre di dialogo, semplificando così lo sviluppo dell'interfaccia utente per un'applicazione. Questa panoramica descrive le funzioni e i messaggi della finestra di dialogo e spiega come usarli per creare e usare le finestre di dialogo.

Questa panoramica include gli argomenti seguenti:

-   [Quando usare una finestra di dialogo](#when-to-use-a-dialog-box)
-   [Finestra proprietario della finestra di dialogo](#dialog-box-owner-window)
-   [Finestre di messaggio](#message-boxes)
-   [Finestre di dialogo modali](#modal-dialog-boxes)
-   [Finestre di dialogo non modali](#modeless-dialog-boxes)
-   [Modelli di finestra di dialogo](#dialog-box-templates)
    -   [Stili del modello della finestra di dialogo](#dialog-box-template-styles)
    -   [Misure della finestra di dialogo](#dialog-box-measurements)
    -   [Controlli della finestra di dialogo](#dialog-box-controls)
    -   [Menu della finestra di dialogo](#dialog-box-window-menu)
    -   [Tipi di carattere della finestra di dialogo](#dialog-box-fonts)
    -   [Modelli in memoria](#templates-in-memory)

Per altre informazioni sulle finestre di dialogo comuni, vedere [Common Dialog Box Library](common-dialog-box-library.md).

## <a name="when-to-use-a-dialog-box"></a>Quando usare una finestra di dialogo

La maggior parte delle applicazioni usa finestre di dialogo per richiedere informazioni aggiuntive per le voci di menu che richiedono l'input dell'utente. L'uso di una finestra di dialogo è l'unico modo consigliato per recuperare l'input da parte di un'applicazione. Ad esempio, una tipica voce di **menu** Apri richiede il nome di un file da aprire, quindi un'applicazione deve usare una finestra di dialogo per richiedere il nome all'utente. In questi casi, l'applicazione crea la finestra di dialogo quando l'utente fa clic sulla voce di menu ed elimina la finestra di dialogo immediatamente dopo che l'utente ha fornito le informazioni.

Molte applicazioni usano anche finestre di dialogo per visualizzare informazioni o opzioni mentre l'utente lavora in un'altra finestra. Ad esempio, le applicazioni di elaborazione di testo spesso usano una finestra di dialogo con un'opzione di ricerca di testo. Mentre l'applicazione cerca il testo, la finestra di dialogo rimane sullo schermo. L'utente può quindi tornare alla finestra di dialogo e cercare di nuovo la stessa parola. oppure l'utente può modificare la voce nella finestra di dialogo e cercare una nuova parola. Le applicazioni che usano le finestre di dialogo in questo modo in genere ne creano una quando l'utente fa clic sulla voce di menu e continuano a visualizzarla fino a quando l'applicazione viene eseguita o fino a quando l'utente non chiude in modo esplicito la finestra di dialogo.

Per supportare i diversi modi in cui le applicazioni usano le finestre di dialogo, sono disponibili due tipi di finestra di dialogo: modale e non modale. Una *finestra di dialogo modale* richiede all'utente di fornire informazioni o annullare la finestra di dialogo prima di consentire all'applicazione di continuare. Le applicazioni usano finestre di dialogo modali in combinazione con voci di menu che richiedono informazioni aggiuntive prima di poter procedere. Una *finestra di dialogo non modabile* consente all'utente di fornire informazioni e tornare all'attività precedente senza chiudere la finestra di dialogo. Le finestre di dialogo modali sono più semplici da gestire rispetto alle finestre di dialogo non modali perché vengono create, eseguite e vengono distrutte chiamando una singola funzione.

Per creare una finestra di dialogo modale o non modale, un'applicazione deve fornire un modello di finestra di dialogo per descrivere lo stile e il contenuto della finestra di dialogo. L'applicazione deve anche fornire una procedura della finestra di dialogo per eseguire attività. Il *modello di finestra di* dialogo è una descrizione binaria della finestra di dialogo e dei controlli in essa contenuti. Lo sviluppatore può creare questo modello come risorsa da caricare dal file eseguibile dell'applicazione o creare in memoria durante l'esecuzione dell'applicazione. La *routine della finestra di* dialogo è una funzione di callback definita dall'applicazione che il sistema chiama quando ha input per la finestra di dialogo o le attività da eseguire per la finestra di dialogo. Anche se una routine della finestra di dialogo è simile a una routine finestra, non ha le stesse responsabilità.

Un'applicazione crea in genere una finestra di dialogo usando la [**funzione DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) [**o CreateDialog.**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) **DialogBox crea** una finestra di dialogo modale. **CreateDialog crea** una finestra di dialogo non modabile. Queste due funzioni caricano un modello di finestra di dialogo dal file eseguibile dell'applicazione e creano una finestra popup che corrisponde alle specifiche del modello. Esistono altre funzioni che creano una finestra di dialogo usando i modelli in memoria. passano informazioni aggiuntive alla routine della finestra di dialogo durante la creazione della finestra di dialogo.

Le finestre di dialogo appartengono in genere a una classe di finestra esclusiva predefinita. Il sistema usa questa classe finestra e la relativa routine finestra corrispondente per le finestre di dialogo modali e non modali. Quando la funzione viene chiamata, crea la finestra per la finestra di dialogo, nonché le finestre per i controlli nella finestra di dialogo, quindi invia i messaggi selezionati alla routine della finestra di dialogo. Mentre la finestra di dialogo è visibile, la procedura predefinita della finestra gestisce tutti i messaggi, elaborando alcuni messaggi e passando altri alla routine della finestra di dialogo in modo che la procedura possa eseguire attività. Le applicazioni non hanno accesso diretto alla classe di finestra predefinita o alla routine della finestra, ma possono usare il modello di finestra di dialogo e la procedura della finestra di dialogo per modificare lo stile e il comportamento di una finestra di dialogo.

## <a name="dialog-box-owner-window"></a>Finestra proprietario della finestra di dialogo

La maggior parte delle finestre di dialogo ha una finestra proprietaria (o, più semplicemente, un proprietario). Quando si crea la finestra di dialogo, l'applicazione imposta il proprietario specificando l'handle della finestra del proprietario. Il sistema usa il proprietario per determinare la posizione della finestra di dialogo nell'ordine Z in modo che la finestra di dialogo sia sempre posizionata sopra il proprietario. Inoltre, il sistema può inviare messaggi alla routine della finestra del proprietario, notificando gli eventi nella finestra di dialogo.

Il sistema nasconde o elimina automaticamente la finestra di dialogo ogni volta che il proprietario viene nascosto o eliminato. Ciò significa che la procedura della finestra di dialogo non richiede alcuna elaborazione speciale per rilevare le modifiche apportate allo stato della finestra proprietaria.

Poiché la tipica finestra di dialogo viene usata insieme a una voce di menu, la finestra proprietaria è in genere la finestra contenente il menu. Anche se è possibile creare una finestra di dialogo senza proprietario, non è consigliabile. Ad esempio, quando una finestra di dialogo modale non ha alcun proprietario, il sistema non disabilita nessuna delle altre finestre dell'applicazione e consente all'utente di continuare a lavorare nelle altre finestre, sconfiendo lo scopo della finestra di dialogo modale.

Quando una finestra di dialogo non modali non ha alcun proprietario, il sistema non nasconde né elimina la finestra di dialogo quando altre finestre dell'applicazione vengono nascoste o distrutte. Anche se questo non elimina lo scopo della finestra di dialogo non modabile, è necessario che l'applicazione eserciti un'elaborazione speciale per assicurarsi che la finestra di dialogo sia nascosta ed distrutta nei momenti appropriati.

## <a name="message-boxes"></a>Finestre di messaggio

Una finestra di messaggio è una finestra di dialogo speciale che un'applicazione può usare per visualizzare messaggi e richiedere un input semplice. Una finestra di messaggio contiene in genere un SMS e uno o più pulsanti. Un'applicazione crea la finestra di messaggio usando la [**funzione MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) specificando il testo e il numero e i tipi di pulsanti da visualizzare. Si noti che attualmente non esiste alcuna differenza tra il funzionamento di **MessageBox** **e MessageBoxEx.**

Anche se la finestra di messaggio è una finestra di dialogo, il sistema assume il controllo completo della creazione e della gestione della finestra di messaggio. Ciò significa che l'applicazione non fornisce un modello di finestra di dialogo e una procedura della finestra di dialogo. Il sistema crea il proprio modello in base al testo e ai pulsanti specificati per la finestra di messaggio e fornisce la propria procedura della finestra di dialogo.

Una finestra di messaggio è una finestra di dialogo modale e il sistema la crea usando le stesse funzioni interne utilizzate [**da DialogBox.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) Se l'applicazione specifica una finestra proprietaria quando si chiama [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) o [**MessageBoxEx,**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)il sistema disabilita il proprietario. Un'applicazione può anche indicare al sistema di disabilitare tutte le finestre di primo livello appartenenti al thread corrente specificando il valore **\_ MB TASKMODAL** durante la creazione della finestra di dialogo.

Il sistema può inviare messaggi al proprietario, ad esempio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) e [**WM \_ ENABLE,**](/windows/desktop/winmsg/wm-enable)esattamente come quando si crea una finestra di dialogo modale. La finestra del proprietario deve eseguire tutte le azioni richieste da questi messaggi.

## <a name="modal-dialog-boxes"></a>Finestre di dialogo modali

Una finestra di dialogo modale deve essere una finestra popup con un menu della finestra, una barra del titolo e un bordo spesso. il modello di finestra di dialogo deve specificare gli stili **WS \_ POPUP**, **WS \_ SYSMENU**, **WS \_ CAPTION** e **DS \_ MODALFRAME.** Anche se un'applicazione può designare lo stile **WS \_ VISIBLE,** il sistema visualizza sempre una finestra di dialogo modale indipendentemente dal fatto che il modello di finestra di dialogo specifichi **lo stile WS \_ VISIBLE.** Un'applicazione non deve creare una finestra di dialogo modale con **lo stile \_ WS CHILD.** Una finestra di dialogo modale con questo stile viene disabilitata, impedendo a qualsiasi input successivo di raggiungere l'applicazione.

Un'applicazione crea una finestra di dialogo modale usando la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) o [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) **DialogBox richiede** il nome o l'identificatore di una risorsa contenente un modello di finestra di dialogo. **DialogBoxIndirect richiede** un handle per un oggetto di memoria contenente un modello di finestra di dialogo. Le [**funzioni DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama) e [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) creano anche finestre di dialogo modali. sono identiche alle funzioni indicate in precedenza, ma passano un parametro specificato alla routine della finestra di dialogo quando viene creata la finestra di dialogo.

Quando si crea la finestra di dialogo modale, il sistema la rende la finestra attiva. La finestra di dialogo rimane attiva fino a quando la routine della finestra di dialogo non chiama la [**funzione EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) o il sistema non attiva una finestra in un'altra applicazione. Né l'utente né l'applicazione possono rendere attiva la finestra del proprietario fino a quando la finestra di dialogo modale non viene distrutta.

Quando la finestra proprietaria non è già disabilitata, il sistema disabilita automaticamente la finestra e tutte le finestre figlio che la appartengono quando crea la finestra di dialogo modale. La finestra proprietaria rimane disabilitata fino a quando la finestra di dialogo non viene distrutta. Sebbene una procedura della finestra di dialogo possa potenzialmente abilitare la finestra del proprietario in qualsiasi momento, l'abilitazione del proprietario non consente di utilizzare la finestra di dialogo modale e non è consigliabile. Quando la procedura della finestra di dialogo viene distrutta, il sistema abilita di nuovo la finestra del proprietario, ma solo se la finestra di dialogo modale ha causato la disattivazione del proprietario.

Quando il sistema crea la finestra di dialogo modale, invia il messaggio [**WM \_ CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) alla finestra (se presente) che acquisisce l'input del mouse. Un'applicazione che riceve questo messaggio deve rilasciare il mouse capture in modo che l'utente possa spostare il mouse nella finestra di dialogo modale. Poiché il sistema disabilita la finestra proprietaria, tutto l'input del mouse viene perso se il proprietario non riesce a rilasciare il mouse alla ricezione del messaggio.

Per elaborare i messaggi per la finestra di dialogo modale, il sistema avvia il proprio ciclo di messaggi, assumendo il controllo temporaneo della coda di messaggi per l'intera applicazione. Quando il sistema recupera un messaggio che non è in modo esplicito per la finestra di dialogo, invia il messaggio alla finestra appropriata. Se recupera un messaggio [**WM \_ QUIT,**](/windows/desktop/winmsg/wm-quit) lo invia nuovamente alla coda di messaggi dell'applicazione in modo che il ciclo di messaggi principale dell'applicazione possa recuperare il messaggio.

Il sistema invia il [**messaggio WM \_ ENTERIDLE**](wm-enteridle.md) alla finestra del proprietario ogni volta che la coda di messaggi dell'applicazione è vuota. L'applicazione può usare questo messaggio per eseguire un'attività in background mentre la finestra di dialogo rimane sullo schermo. Quando un'applicazione usa il messaggio in questo modo, l'applicazione deve spesso produrre il controllo (ad esempio, usando la funzione [**PeekMessage)**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) in modo che la finestra di dialogo modale possa ricevere qualsiasi input dell'utente. Per impedire alla finestra di dialogo modale di inviare i messaggi **WM \_ ENTERIDLE,** l'applicazione può specificare lo stile DS NOIDLEMSG durante la creazione \_ della finestra di dialogo.

Un'applicazione elimina una finestra di dialogo modale usando la [**funzione EndDialog.**](/windows/desktop/api/Winuser/nf-winuser-enddialog) Nella maggior parte dei casi, la routine della  finestra di dialogo chiama **EndDialog** quando l'utente fa clic su Chiudi dal menu della finestra di dialogo o fa clic sul pulsante **OK** o Annulla nella finestra di dialogo.  La finestra di dialogo può restituire un valore tramite la funzione [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) (o altre funzioni di creazione) specificando un valore quando si chiama la **funzione EndDialog.** Il sistema restituisce questo valore dopo l'eliminazione della finestra di dialogo. La maggior parte delle applicazioni usa questo valore restituito per determinare se la finestra di dialogo ha completato correttamente l'attività o è stata annullata dall'utente. Il sistema non restituisce il controllo dalla funzione che crea la finestra di dialogo finché la routine della finestra di dialogo non ha chiamato la **funzione EndDialog.**

## <a name="modeless-dialog-boxes"></a>Finestre di dialogo non modali

Una finestra di dialogo non modata deve essere una finestra popup con un menu della finestra, una barra del titolo e un bordo sottile. il modello di finestra di dialogo deve specificare gli stili **WS \_ POPUP,** **WS \_ CAPTION,** **WS \_ BORDER** e **WS \_ SYSMENU.** Il sistema non visualizza automaticamente la finestra di dialogo a meno che il modello non specifichi lo **stile WS \_ VISIBLE.**

Un'applicazione crea una finestra di dialogo non modabile usando la [**funzione CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) o [**CreateDialogIndirect.**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) **CreateDialog richiede** il nome o l'identificatore di una risorsa contenente un modello di finestra di dialogo. **CreateDialogIndirect richiede** un handle per un oggetto memoria contenente un modello di finestra di dialogo. Anche altre due funzioni, [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama) [**e CreateDialogIndirectParam,**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)creano finestre di dialogo non modali. passano un parametro specificato alla routine della finestra di dialogo quando viene creata la finestra di dialogo.

[**CreateDialog e**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) altre funzioni di creazione restituiscono un handle di finestra alla finestra di dialogo. L'applicazione e la procedura della finestra di dialogo possono usare questo handle per gestire la finestra di dialogo. Ad esempio, se **WS \_ VISIBLE** non è specificato nel modello di finestra di dialogo, l'applicazione può visualizzare la finestra di dialogo passando l'handle di finestra alla [**funzione ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

Una finestra di dialogo non modali non disabilita né invia messaggi alla finestra proprietaria. Quando si crea la finestra di dialogo, il sistema la rende la finestra attiva, ma l'utente o l'applicazione può modificare la finestra attiva in qualsiasi momento. Se la finestra di dialogo diventa inattiva, rimane sopra la finestra del proprietario nell'ordine Z, anche se la finestra del proprietario è attiva.

L'applicazione è responsabile del recupero e dell'invio di messaggi di input alla finestra di dialogo. La maggior parte delle applicazioni usa il ciclo di messaggi principale a questo scopo. Per consentire all'utente di spostarsi e selezionare i controlli usando la tastiera, tuttavia, l'applicazione deve chiamare la [**funzione IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Per altre informazioni su questa funzione, vedere [Interfaccia della tastiera della finestra di dialogo](dlgbox-programming-considerations.md).

Una finestra di dialogo non modale non può restituire un valore all'applicazione come una finestra di dialogo modale, ma la routine della finestra di dialogo può inviare informazioni alla finestra proprietaria usando la [**funzione SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

Un'applicazione deve eliminare tutte le finestre di dialogo non modali prima di terminare. Può eliminare una finestra di dialogo non modale usando la [**funzione DestroyWindow.**](/windows/desktop/api/winuser/nf-winuser-destroywindow) Nella maggior parte dei casi, la routine della finestra di dialogo chiama **DestroyWindow** in risposta all'input dell'utente, ad esempio facendo clic **sul pulsante** Annulla. Se l'utente non chiude mai la finestra di dialogo in questo modo, l'applicazione deve chiamare **DestroyWindow**.

[**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) invalida l'handle di finestra nella finestra di dialogo, pertanto tutte le chiamate successive alle funzioni che usano i valori di errore restituiti dall'handle. Per evitare errori, la procedura della finestra di dialogo deve notificare al proprietario che la finestra di dialogo è stata distrutta. Molte applicazioni mantengono una variabile globale contenente l'handle per la finestra di dialogo. Quando la routine della finestra di dialogo elimina la finestra di dialogo, imposta anche la variabile globale su **NULL,** a indicare che la finestra di dialogo non è più valida.

La routine della finestra di dialogo non deve chiamare la [**funzione EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) per eliminare una finestra di dialogo non modabile.

## <a name="dialog-box-templates"></a>Modelli di finestra di dialogo

Un modello di finestra di dialogo è dati binari che descrivono la finestra di dialogo, definendo l'altezza, la larghezza, lo stile e i controlli in essa contenuti. Per creare una finestra di dialogo, il sistema carica un modello di finestra di dialogo dalle risorse nel file eseguibile dell'applicazione o usa il modello passato all'applicazione nella memoria globale. In entrambi i casi, l'applicazione deve fornire un modello quando si crea una finestra di dialogo.

Uno sviluppatore crea risorse modello usando un compilatore di risorse o un editor di finestre di dialogo. Un compilatore di risorse converte una descrizione di testo in una risorsa binaria e un editor di finestre di dialogo salva una finestra di dialogo costruita in modo interattivo come risorsa binaria.

> [!Note]  
> Una spiegazione di come creare risorse modello e aggiungerle al file eseguibile dell'applicazione non è in questo ambito di questa panoramica. Per altre informazioni sulla creazione di risorse modello e sull'aggiunta a un file eseguibile, vedere la documentazione fornita con gli strumenti di sviluppo delle applicazioni.

 

Per creare una finestra di dialogo senza usare risorse modello, è necessario creare un modello in memoria e passarlo alla funzione [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama) o [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama) o alla macro [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta) o [**DialogBoxIndirect.**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)

Un modello di finestra di dialogo in memoria è costituito da un'intestazione che descrive la finestra di dialogo, seguita da uno o più blocchi di dati aggiuntivi che descrivono ognuno dei controlli nella finestra di dialogo. Il modello può usare il formato standard o il formato esteso. In un modello standard l'intestazione è una [**struttura DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguita da matrici di lunghezza variabile aggiuntive. e i dati per ogni controllo sono costituiti da una [**struttura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello di finestra di dialogo esteso, l'intestazione usa il formato [**DLGTEMPLATEEX**](dlgtemplateex.md) e le definizioni dei controlli usano il [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

È possibile creare un modello di memoria allocando un oggetto di memoria globale e compilando l'oggetto con le definizioni di intestazione e controllo standard o estese. Un modello di memoria è identico nel formato e nel contenuto a una risorsa modello. Molte applicazioni che usano i modelli di memoria usano prima la [**funzione LoadResource**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadresource) per caricare una risorsa modello in memoria, quindi modificano la risorsa caricata per creare un nuovo modello di memoria. Per altre informazioni sulla creazione di un modello di finestra di dialogo in memoria, vedere [Modelli in memoria](#templates-in-memory).

Le sezioni seguenti descrivono gli stili, le misure e altri valori usati in un modello di finestra di dialogo.

-   [Stili del modello della finestra di dialogo](#dialog-box-template-styles)
-   [Misure della finestra di dialogo](#dialog-box-measurements)
-   [Controlli della finestra di dialogo](#dialog-box-controls)
-   [Menu della finestra di dialogo](#dialog-box-window-menu)
-   [Tipi di carattere della finestra di dialogo](#dialog-box-fonts)
-   [Modelli in memoria](#templates-in-memory)

### <a name="dialog-box-template-styles"></a>Stili del modello della finestra di dialogo

Ogni modello di finestra di dialogo specifica una combinazione di valori di stile che definiscono l'aspetto e le funzionalità della finestra di dialogo. I valori di stile possono essere stili di finestra, ad esempio **WS \_ POPUP** e **WS \_ SYSMENU,** e stili di finestra di dialogo, ad esempio **DS \_ MODALFRAME**. Il numero e il tipo di stili per un modello dipendono dal tipo e dallo scopo della finestra di dialogo. Per un elenco di valori, vedere [**Stili delle finestre di dialogo**](dialog-box-styles.md).

Il sistema passa tutti gli stili di finestra specificati nel modello alla [**funzione CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) durante la creazione della finestra di dialogo. Il sistema può passare uno o più stili estesi a seconda degli stili della finestra di dialogo specificati. Ad esempio, quando il modello specifica **DS \_ MODALFRAME**, il sistema usa **WS \_ EX \_ DLGMODALFRAME** durante la creazione della finestra di dialogo.

La maggior parte delle finestre di dialogo sono finestre popup con un menu della finestra e una barra del titolo. Pertanto, il modello tipico specifica gli **stili \_ WS POPUP,** **WS \_ SYSMENU** e **WS \_ CAPTION.** Il modello specifica anche uno stile del bordo: **WS \_ BORDER** per le finestre di dialogo non modali e **DS \_ MODALFRAME** per le finestre di dialogo modali. Un modello può specificare un tipo di finestra diverso da popup (ad esempio **WS \_ OVERLAPPED)** se crea una finestra personalizzata anziché una finestra di dialogo.

Il sistema visualizza sempre una finestra di dialogo modale indipendentemente dal fatto che sia specificato lo **stile \_ WS VISIBLE.** Quando il modello per una finestra di dialogo non modali specifica lo **stile WS \_ VISIBLE,** il sistema visualizza automaticamente la finestra di dialogo al momento della creazione. In caso contrario, l'applicazione è responsabile della visualizzazione della finestra di dialogo tramite la [**funzione ShowWindow.**](/windows/desktop/api/winuser/nf-winuser-showwindow)

### <a name="dialog-box-measurements"></a>Misure della finestra di dialogo

Ogni modello di finestra di dialogo contiene misure che specificano la posizione, la larghezza e l'altezza della finestra di dialogo e i controlli in essa contenuti. Queste misurazioni sono indipendenti dal dispositivo, quindi un'applicazione può usare un singolo modello per creare la stessa finestra di dialogo per tutti i tipi di dispositivi di visualizzazione. Ciò garantisce che una finestra di dialogo abbia le stesse proporzioni e lo stesso aspetto su tutti gli schermi, nonostante le diverse risoluzioni e proporzioni tra gli schermi.

Le misurazioni in un modello di finestra di dialogo vengono specificate in unità del modello di finestra di dialogo. Per convertire le misurazioni dalle unità del modello di finestra di dialogo alle unità dello schermo (pixel), usare la [**funzione MapDialogRect,**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) che prende in considerazione il tipo di carattere usato dalla finestra di dialogo e converte correttamente un rettangolo dalle unità del modello di finestra di dialogo in pixel. Per le finestre di dialogo che usano il tipo di carattere di sistema, è possibile usare la [**funzione GetDialogBaseUnits**](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits) per eseguire i calcoli di conversione manualmente, anche se l'uso **di MapDialogRect** è più semplice.

Il modello deve specificare le coordinate iniziali dell'angolo superiore sinistro della finestra di dialogo. In genere le coordinate sono relative all'angolo superiore sinistro dell'area client della finestra proprietaria. Quando il modello specifica lo stile DS ABSALIGN o la finestra di dialogo non ha alcun proprietario, la posizione è relativa all'angolo superiore \_ sinistro dello schermo. Il sistema imposta questa posizione iniziale durante la creazione della finestra di dialogo, ma consente a un'applicazione di modificare la posizione prima di visualizzare la finestra di dialogo. Ad esempio, un'applicazione può recuperare le dimensioni della finestra proprietaria, calcolare una nuova posizione che centra la finestra di dialogo nella finestra proprietaria e quindi impostare la posizione usando la [**funzione SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)

Il modello deve specificare la larghezza e l'altezza di una finestra di dialogo che non supera la larghezza e l'altezza dello schermo e garantisce che tutti i controlli siano all'interno dell'area client della finestra di dialogo. Anche se il sistema consente a una finestra di dialogo di qualsiasi dimensione, la creazione di una finestra di dialogo troppo piccola o troppo grande può impedire all'utente di fornire l'input, sconfiendo lo scopo della finestra di dialogo. Molte applicazioni usano più finestre di dialogo quando è presente un numero elevato di controlli. In questi casi, la finestra di dialogo iniziale contiene in genere uno o più pulsanti che l'utente può scegliere di visualizzare la finestra di dialogo successiva.

### <a name="dialog-box-controls"></a>Controlli della finestra di dialogo

Il modello specifica la posizione, la larghezza, l'altezza, lo stile, l'identificatore e la classe della finestra per ogni controllo nella finestra di dialogo. Il sistema crea ogni controllo passando questi dati alla [**funzione CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) I controlli vengono creati nell'ordine in cui sono specificati nel modello. Il modello deve specificare il numero, il tipo e l'ordine dei controlli appropriati per garantire che l'utente possa immettere l'input necessario per completare l'attività associata alla finestra di dialogo.

Per ogni controllo, il modello specifica i valori di stile che definiscono l'aspetto e il funzionamento del controllo. Ogni controllo è una finestra figlio e pertanto deve avere lo **stile \_ WS CHILD.** Per garantire che il controllo sia visibile quando viene visualizzata la finestra di dialogo, ogni controllo deve avere anche lo **stile \_ WS VISIBLE.** Altri stili di finestra di uso comune sono **WS \_ BORDER** per i controlli con bordi facoltativi, **WS \_ DISABLED** per i controlli che devono essere disabilitati quando la finestra di dialogo viene creata inizialmente e **WS \_ TABSTOP** e **WS \_ GROUP** per i controlli a cui è possibile accedere tramite tastiera. Gli **stili WS \_ TABSTOP** e **WS \_ GROUP** vengono usati insieme all'interfaccia della tastiera della finestra di dialogo descritta più avanti in questo argomento.

Il modello può anche specificare stili di controllo specifici per la classe finestra del controllo. Ad esempio, un modello che specifica un controllo pulsante deve assegnare uno stile di controllo pulsante, ad esempio **BS \_ PUSHBUTTON** o **BS \_ CHECKBOX.** Il sistema passa gli stili di controllo alla routine della finestra di controllo tramite il [**messaggio WM \_ CREATE,**](/windows/desktop/winmsg/wm-create) consentendo alla procedura di adattare l'aspetto e il funzionamento del controllo.

Il sistema converte le coordinate di posizione e le misure di larghezza e altezza dalle unità di base del dialogo in pixel, prima di passarli a [**CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Quando il sistema crea un controllo , specifica la finestra di dialogo come finestra padre. Ciò significa che il sistema interpreta sempre le coordinate di posizione del controllo come coordinate client, rispetto all'angolo superiore sinistro dell'area client della finestra di dialogo.

Il modello specifica la classe della finestra per ogni controllo. Una tipica finestra di dialogo contiene controlli appartenenti alle classi predefinite della finestra di controllo, ad esempio le classi di pulsanti e finestre di controllo di modifica. In questo caso, il modello specifica le classi finestra fornendo i valori atom predefiniti corrispondenti per le classi. Quando una finestra di dialogo contiene un controllo appartenente a una classe della finestra di controllo personalizzata, il modello assegna il nome della classe della finestra registrata o il valore atom attualmente associato al nome.

Ogni controllo in una finestra di dialogo deve avere un identificatore univoco per distinguerlo dagli altri controlli. I controlli inviano informazioni alla routine della finestra di dialogo tramite messaggi [**WM \_ COMMAND,**](/windows/desktop/menurc/wm-command) pertanto gli identificatori di controllo sono essenziali per la procedura per determinare quale controllo ha inviato un messaggio specificato. L'unica eccezione a questa regola sono gli identificatori di controllo per i controlli statici. I controlli statici non richiedono identificatori univoci perché non inviano **messaggi WM \_ COMMAND.**

Per consentire all'utente di chiudere la finestra di dialogo, il modello deve specificare almeno un pulsante push e assegnargli l'identificatore **di controllo IDCANCEL.** Per consentire all'utente di scegliere tra il completamento o l'annullamento dell'attività associata alla finestra di dialogo, il modello deve specificare due pulsanti push, etichettati **rispettivamente OK** e **Annulla,** con gli identificatori di controllo **IDOK** e **IDCANCEL.**

Un modello specifica anche il testo facoltativo e i dati di creazione per un controllo. Il testo fornisce in genere etichette per i controlli pulsante o specifica il contenuto iniziale di un controllo testo statico. I dati di creazione sono uno o più byte di dati passati dal sistema alla routine della finestra di controllo durante la creazione del controllo. I dati di creazione sono utili per i controlli che richiedono più informazioni sul contenuto o sullo stile iniziale rispetto a quanto specificato da altri dati. Ad esempio, un'applicazione può usare i dati di creazione per impostare l'impostazione iniziale e l'intervallo per un controllo barra di scorrimento.

### <a name="dialog-box-window-menu"></a>Menu della finestra di dialogo

Il sistema fornisce a una finestra di dialogo un menu finestra quando il modello specifica lo **stile \_ SYSMENU WS.** Per evitare input non appropriato, il sistema disabilita automaticamente tutte le voci del menu ad eccezione **di Sposta** **e Chiudi**. L'utente può fare **clic su Sposta** per spostare la finestra di dialogo. Quando l'utente fa clic su **Chiudi**, il sistema invia un messaggio [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command) alla procedura della finestra di dialogo con il parametro *wParam* impostato su **IDCANCEL**. È identico al messaggio inviato dal pulsante **Annulla** quando l'utente fa clic su di esso. L'azione consigliata per questo messaggio è chiudere la finestra di dialogo e annullare l'attività richiesta.

Anche se non sono consigliati altri menu nelle finestre di dialogo, un modello di finestra di dialogo può specificare un menu specificando l'identificatore o il nome di una risorsa di menu. In questo caso, il sistema carica la risorsa e crea il menu per la finestra di dialogo. Le applicazioni usano in genere identificatori di menu o nomi nei modelli quando si usano i modelli per creare finestre personalizzate anziché finestre di dialogo.

### <a name="dialog-box-fonts"></a>Tipi di carattere della finestra di dialogo

Il sistema usa la larghezza media dei caratteri del tipo di carattere della finestra di dialogo per calcolare la posizione e le dimensioni della finestra di dialogo. Per impostazione predefinita, il sistema disegna tutto il testo in una finestra di dialogo usando il tipo **di carattere SYSTEM \_ FONT.**

Per specificare un tipo di carattere per una finestra di dialogo diversa da quella predefinita, è necessario creare la finestra di dialogo usando un modello di finestra di dialogo. In una risorsa modello usare [l'istruzione FONT](../menurc/font-statement.md). In un modello di finestra di dialogo impostare lo stile **\_ DS SETFONT** o **DS \_ SHELLFONT** e specificare una dimensione in punti e un nome di carattere tipografico. Anche se un modello di finestra di dialogo specifica un tipo di carattere in questo modo, il sistema usa sempre il tipo di carattere di sistema per il titolo della finestra di dialogo e i menu della finestra di dialogo.

Quando la finestra di dialogo ha lo stile **DS \_ SETFONT** o **DS \_ SHELLFONT,** il sistema invia un messaggio [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) alla routine della finestra di dialogo e a ogni controllo durante la creazione del controllo. La procedura della finestra di dialogo è responsabile del salvataggio dell'handle del tipo di carattere passato con il messaggio **WM \_ SETFONT** e della selezione dell'handle nel contesto di dispositivo di visualizzazione ogni volta che scrive testo nella finestra. I controlli predefiniti eseere questa operazione per impostazione predefinita.

Il tipo di carattere di sistema può variare tra versioni diverse Windows. Per fare in modo che l'applicazione usi il tipo di carattere di sistema indipendentemente dal sistema in cui è in esecuzione, usare **DS \_ SHELLFONT** con il carattere tipografico MS Shell Dlg e usare la risorsa [DIALOGEX](../menurc/dialogex-resource.md) anziché la risorsa [DIALOG](../menurc/dialog-resource.md). Il sistema esegue il mapping di questo carattere tipografico in modo che la finestra di dialogo usi il tipo di carattere Tahoma. Si noti **che DS \_ SHELLFONT** non ha alcun effetto se il carattere tipografico non è MS Shell Dlg.

### <a name="templates-in-memory"></a>Modelli in memoria

Un modello di finestra di dialogo in memoria è costituito da un'intestazione che descrive la finestra di dialogo, seguita da uno o più blocchi di dati aggiuntivi che descrivono ognuno dei controlli nella finestra di dialogo. Il modello può usare il formato standard o il formato esteso. In un modello standard l'intestazione è una [**struttura DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) seguita da matrici di lunghezza variabile aggiuntive. I dati per ogni controllo sono costituiti da [**una struttura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello di finestra di dialogo esteso, l'intestazione usa il formato [**DLGTEMPLATEEX**](dlgtemplateex.md) e le definizioni dei controlli usano il [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Per distinguere tra un modello standard e un modello esteso, controllare i primi 16 bit di un modello di finestra di dialogo. In un modello esteso, la prima **parola è** 0xFFFF; qualsiasi altro valore indica un modello standard.

Se si crea un modello di finestra di dialogo in memoria, è necessario assicurarsi che le definizioni di controllo [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) siano allineate sui limiti **DWORD.** Inoltre, tutti i dati di creazione che seguono una definizione di controllo devono essere allineati su un **limite DWORD.** Tutte le altre matrici a lunghezza variabile in un modello di finestra di dialogo devono essere allineate ai limiti **di WORD.**

### <a name="template-header"></a>Intestazione modello

Nei modelli standard ed estesi per le finestre di dialogo, l'intestazione include le informazioni generali seguenti:

-   Posizione e dimensioni della finestra di dialogo
-   Stili della finestra e della finestra di dialogo per la finestra di dialogo
-   Numero di controlli nella finestra di dialogo. Questo valore determina il numero di definizioni di controllo [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) o [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) nel modello.
-   Risorsa di menu facoltativa per la finestra di dialogo. Il modello può indicare che la finestra di dialogo non dispone di un menu oppure può specificare un valore ordinale o una stringa Unicode con terminazione Null che identifica una risorsa di menu in un file eseguibile.
-   Classe della finestra della finestra di dialogo. Può trattarsi della classe predefinita della finestra di dialogo o di un valore ordinale o di una stringa Unicode con terminazione Null che identifica una classe finestra registrata.
-   Stringa Unicode con terminazione Null che specifica il titolo per la finestra di dialogo. Se la stringa è vuota, la barra del titolo della finestra di dialogo è vuota. Se la finestra di dialogo non ha lo **stile WS \_ CAPTION,** il sistema imposta il titolo sulla stringa specificata, ma non lo visualizza.
-   Se la finestra di dialogo ha lo stile **\_ SETFONT DS,** l'intestazione specifica le dimensioni in punti e il nome del carattere tipografico del tipo di carattere da usare per il testo nell'area client e i controlli della finestra di dialogo.

In un modello esteso, [**l'intestazione DLGTEMPLATEEX**](dlgtemplateex.md) specifica anche le informazioni aggiuntive seguenti:

-   Identificatore del contesto della Guida della finestra di dialogo quando il sistema invia un [**messaggio WM \_ HELP.**](../shell/wm-help.md)
-   Se la finestra di dialogo ha lo stile **DS \_ SETFONT** o **DS \_ SHELLFONT,** l'intestazione specifica lo spessore del carattere e indica se il tipo di carattere è in corsivo.

### <a name="control-definitions"></a>Definizioni di controllo

Dopo l'intestazione del modello sono disponibili una o più definizioni di controllo che descrivono i controlli della finestra di dialogo. Nei modelli standard ed estesi, l'intestazione della finestra di dialogo ha un membro che indica il numero di definizioni di controllo nel modello. In un modello standard, ogni definizione di controllo è costituita da una [**struttura DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) seguita da matrici di lunghezza variabile aggiuntive. In un modello esteso, le definizioni di controllo usano il [**formato DLGITEMTEMPLATEEX.**](dlgitemtemplateex.md)

Nei modelli standard ed estesi la definizione del controllo include le informazioni seguenti:

-   Posizione e dimensioni del controllo.
-   Stili della finestra e del controllo.
-   Identificatore del controllo.
-   Classe della finestra del controllo. Può trattarsi del valore ordinale di una classe di sistema predefinita o di una stringa Unicode con terminazione Null che specifica il nome di una classe finestra registrata.
-   Stringa Unicode con terminazione Null che specifica il testo iniziale del controllo o un valore ordinale che identifica una risorsa, ad esempio un'icona, in un file eseguibile.
-   Blocco facoltativo di dati di creazione a lunghezza variabile. Quando il sistema crea il controllo, passa un puntatore a questi dati nel *parametro lParam* del messaggio [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) inviato al controllo.

In un modello esteso, la definizione del controllo specifica anche un identificatore di contesto della Guida per il controllo quando il sistema invia un [**messaggio WM \_ HELP.**](../shell/wm-help.md)

 

 