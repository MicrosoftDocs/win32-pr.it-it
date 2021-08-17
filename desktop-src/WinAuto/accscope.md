---
title: Strumenti di accessibilità - AccScope
description: Lo strumento AccScope consente a sviluppatori e tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di test tardivi del ciclo di sviluppo di un'app.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e55aa40822b786ee69185abe753bb0bacd65345d042526a126b4c8343a2639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327723"
---
# <a name="accessibility-tools---accscope"></a>Strumenti di accessibilità - AccScope

Lo **strumento AccScope** consente a sviluppatori e tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di test tardivi del ciclo di sviluppo di un'app. Il testing può anche iniziare nelle fasi iniziali del prototipo. **AccScope** può visualizzare il modo in cui un'utilità per la lettura dello schermo espone le informazioni Automazione interfaccia utente fornite da un'app e può mostrare le aree in cui è possibile aggiungere informazioni o supporto all'app per migliorarne l'accessibilità.

> [!NOTE]
> **AccScope** è uno strumento legacy. In alternativa, è [consigliabile Insights](https://accessibilityinsights.io/) accessibilità.

## <a name="about-accscope"></a>Informazioni su AccScope

**AccScope** viene installato con Windows Software Development Kit (SDK). Si trova nella cartella \\ bin \\ < *version* > \\ < *platform* > \\ AccScope del percorso di installazione dell'SDK. Eseguire il programma AccScope.exe.

**AccScope** è un'app desktop, non un'app Windows Store. È possibile usarlo per esaminare qualsiasi app visualizzata come finestra, inclusa un'app desktop o un'app Windows Store.

Potrebbe essere necessario eseguire **AccScope** come amministratore la prima volta che lo si usa, per abilitare la modalità Assistente vocale.

**AccScope** è disponibile come parte dei file binari degli strumenti di accessibilità in Windows SDK. Non viene distribuito come download exe separato e non esiste negli SDK precedenti.

## <a name="file-menu-options"></a>Opzioni del menu File

- Selezionare **Aggiorna** per aggiornare tutte le informazioni in **AccScope** in modo che corrispondano allo stato corrente della finestra di destinazione. Per un'interfaccia utente che contiene un numero elevato di elementi, il completamento dell'operazione può richiedere alcuni secondi.
- Selezionare o deselezionare **Always on Top (Sempre** in primo piano) per modificare il comportamento di windowing dell'interfaccia **utente di AccScope.** **Always On Top** checked è l'impostazione predefinita.
- Selezionare **Esci** per uscire da **AccScope.**

## <a name="view-options"></a>Visualizzare le opzioni

- Selezionare **Schermo intero per** eseguire lo strumento **AccScope** in una visualizzazione a schermo intero (quindi usare la tabulazione per visualizzare la finestra di destinazione). Se sia **AccScope** che l'app di destinazione eseguono a schermo intero, la posizione, i rettangoli di delimitazione e la visualizzazione complessiva degli elementi corrisponderanno tra l'app e la **visualizzazione AccScope.**
    > [!Note]  
    > **AccScope** e la relativa destinazione devono essere eseguiti sullo stesso schermo.

     

- Selezionare **Stato attivo automatico** per consentire ad AccScope di modificare la finestra di destinazione ogni volta che un utente sposta lo stato attivo sulla finestra (usando il mouse o la tastiera).
- Selezionare **Aggiornamento automatico** per abilitare la modalità **AccScope** che aggiorna tutti i dati di accessibilità della finestra di destinazione ogni 5 secondi. Ciò è utile se i dati Automazione interfaccia utente microsoft della finestra di destinazione cambiano costantemente.
- Selezionare **Aree in tempo** reale per evidenziare tutte le aree in tempo reale che emettere notifiche nella finestra di destinazione. L'attivazione di un evento dell'area live visualizza un popup rosso con informazioni sull'area live, inclusi il nome e il relativo valore "aria-live" (o l'equivalente valore ARIA analogo per le app che non usano direttamente HTML ma usando il concetto di aree live nel supporto Automazione interfaccia utente).

## <a name="element-mode"></a>Modalità elemento

È possibile scegliere di visualizzare una finestra di destinazione tramite una delle modalità seguenti:

- **Controllo foglia:** mostra una Automazione interfaccia utente degli elementi **Control** con relazioni padre-figlio, in altre parole una visualizzazione dei controlli interattivi a "livello foglia". Usare questa opzione per verificare se tutti i controlli interattivi vengono visualizzati correttamente nell'albero Automazione interfaccia utente per una **visualizzazione Controllo.**
- **Modello di testo:** mostra gli intervalli di testo visibili **dei contenitori TextPattern** dalla finestra di destinazione. Usare questa opzione per rappresentare visivamente gli intervalli di testo visibili Automazione interfaccia utente **textPattern.**
- **Assistente** vocale: mostra i Automazione interfaccia utente che l'Assistente vocale può identificare usando la metafora "Navigazione elementi" dell'Assistente vocale.
- **Filtro personalizzato:** mostra un albero dei controlli filtrato con una scelta di subset di controlli: **Pulsante**, **Casella** di controllo , **Casella** combinata , **Griglia** **,** Collegamento ipertestuale , **Elenco**, **Menu** **o Tabella**.

La modifica **dell'impostazione Modalità** elemento attiva un aggiornamento della visualizzazione. Per un'interfaccia utente che contiene un numero elevato di elementi, il completamento dell'operazione può richiedere alcuni secondi.

## <a name="layout-options"></a>Opzioni di layout

È possibile selezionare **Oggetto visivo o** **Elenco** come modalità di visualizzazione per il layout **AccScope.** **L'oggetto** visivo inserisce gli elementi nello spazio delle coordinate nella stessa relazione della finestra di destinazione. **L'elenco** ordina gli elementi in un elenco decrescente allineato a sinistra nella finestra **AccScope** e l'ordine di elenco equivale all'ordine di tabulazione o di lettura.

- Selezionare un'opzione da Mostra immagini per controllare quando i rettangoli semplici per gli elementi immagine vengono sostituiti dall'immagine effettiva (o da un piccolo viewport dell'immagine, poiché spesso i rettangoli sono più piccoli dell'immagine effettiva).  L'impostazione predefinita è **Al passaggio del** mouse, che visualizza l'immagine quando ci si sposta all'interno di **AccScope** e si passa il mouse sul rettangolo per un elemento immagine. Le opzioni alternative sono **Always** o **Never.**
- Selezionare **Mostra descrizione** comando per visualizzare le informazioni di base sull'elemento ogni volta che si passa il mouse sull'elemento nella **visualizzazione AccScope.** Se la **modalità elemento è** **Controllo** foglia o Modello di **testo,** le informazioni visualizzate nella descrizione comando sono le proprietà a livello Automazione interfaccia utente elemento con priorità più alta. Se la **modalità elemento è Assistente** **vocale,** le informazioni includono il testo che l'Assistente vocale leggerebbe per l'elemento.
- Selezionare **Mostra numeri per** visualizzare i numeri di sequenza che indicano l'ordine di rendering del controllo nel layout. Lo schema dei numeri si basa **sull'impostazione Modalità** elemento:
    - **Controllo foglia:** i numeri indicano l'ordine in cui i controlli foglia vengono visualizzati nell'Automazione interfaccia utente albero.
    - **Modello di testo:** i numeri indicano l'ordine in cui gli intervalli di testo vengono visualizzati in un intervallo di documenti.
    - **Assistente** vocale: il numero indica l'ordine in cui gli elementi vengono spostati nella navigazione degli elementi dell'Assistente vocale.

## <a name="choosing-a-window"></a>Scelta di una finestra

Sotto **l'etichetta Finestra** è disponibile un elenco a discesa che elenca tutte le finestre HWND attualmente attive nel sistema. Il testo per ogni finestra visualizzata nell'elenco a discesa è il titolo della finestra e anche un ID finestra esadecimale tra parentesi quadre. Scegliere una di queste opzioni per modificare la finestra di destinazione per **la segnalazione di AccScope.** È possibile scegliere di nuovo lo stesso elemento per ottenere lo stesso comportamento di un aggiornamento **esplicito.**

## <a name="using-the-accscope-visualization"></a>Uso della visualizzazione AccScope

L'immagine seguente è uno screenshot della **visualizzazione AccScope.** Questo particolare screenshot mostra lo **strumento AccScope** che visualizza la finestra di primo livello per l'output dell'esempio di accessibilità [XAML,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) in esecuzione come app nello stesso computer. Questo screenshot mostra la modalità elemento predefinita del **controllo foglia e** il valore **Visivo** per **Layout**.

![Screenshot della visualizzazione AccScope](images/accscopescreenshot.png)

Si noti che questa visualizzazione rappresenta i controlli nello spazio approssimativo delle coordinate visualizzato nell'app. Ma invece di mostrare gli oggetti visivi XAML o il testo completo dei controlli di testo, mostra i valori della proprietà **Name** che provengono da ogni elemento del controllo, usando Automazione interfaccia utente.

Oltre alle opzioni di menu descritte in precedenza, è anche possibile usare queste tecniche:

- Fare clic sul rettangolo di qualsiasi  elemento nelle visualizzazioni **Oggetto visivo** o Elenco per visualizzare un popup **Proprietà uiA.** Vengono elencate alcune delle proprietà Automazione interfaccia utente per tale elemento, tra cui alcune delle proprietà [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) standard e altre informazioni, ad esempio i valori ARIA e una descrizione **del provider.**
- Fare clic con il pulsante destro del  mouse sul rettangolo di qualsiasi elemento nelle visualizzazioni **Oggetto** visivo o Elenco per visualizzare un menu di scelta rapida per l'esecuzione dei modelli supportati dall'elemento. Ad esempio, se un elemento supporta [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), il menu di scelta rapida include un elemento per **Invoke**. Selezionare l'elemento e l'API del modello appropriata viene esercitata nell'app corrispondente. **AccScope** supporta questa funzionalità per i modelli seguenti: **Invoke,** **ExpandCollapse,** **Toggle,** **SelectionItem,** **ScrollItem**.
- Regolare il **dispositivo di** scorrimento Trasparenza per modificare l'opacità/trasparenza della **finestra AccScope.** Per impostazione predefinita, viene visualizzato come opacità al 100%. Rendere la finestra parzialmente trasparente può essere utile per visualizzare le parti della finestra di destinazione tramite l'interfaccia utente **di AccScope** mentre si usa la Always On **modalità Superiore.**
- Se vengono visualizzate, usare le barre di scorrimento orizzontale e verticale per modificare il centro della visualizzazione. Ciò è utile se si usa l'opzione  **Layout** visivo ma non si usa l'opzione Visualizzazione schermo intero, lasciando la finestra **AccScope** piccola rispetto alla finestra di destinazione.

## <a name="testing-the-narrator-scenario"></a>Test dello scenario dell'Assistente vocale

Lo scenario dell'Assistente vocale è l'aspetto più importante da testare quando si usa **AccScope,** progettato in modo specifico per visualizzare il funzionamento della navigazione di base degli elementi dell'Assistente vocale quando viene applicato all'app.

Per testare lo scenario dell'Assistente vocale, usare queste **opzioni di configurazione di AccScope:**

- **Modalità elemento: Assistente** **vocale**
- **Layout:** **oggetto visivo**
- **Opzioni di** layout: **Mostra descrizione comando** e Mostra **numeri** entrambe selezionate

Ecco alcune aree specifiche dell'app da testare per lo scenario dell'Assistente vocale:

- **Ordine degli elementi:** Verificare che l'ordine in cui l'Assistente vocale legge i controlli sia accurato, in base ai numeri (cerchi verdi) visualizzati nelle visualizzazioni. Se gli elementi non sono nell'ordine previsto per la lettura, modificare la struttura dell'interfaccia utente dell'app e l'albero Automazione interfaccia utente risultante ed eseguire di nuovo il test finché non si verifica che gli elementi siano nell'ordine di lettura previsto.
- **Testo parlato:** Spostare il mouse all'interno della visualizzazione e posizionare il puntatore del mouse su ognuno dei rettangoli degli elementi per visualizzare le descrizioni comandi per ogni elemento. In modalità Assistente vocale le descrizioni comandi visualizzano una voce **di** testo dell'Assistente vocale che è letteralmente il testo letto dall'Assistente vocale. In genere questo testo è composto dal **nome e** dal tipo **di controllo**. Verificare che queste siano le informazioni giuste per ogni controllo nell'interfaccia utente. Se le informazioni non sono corrette, modificare le proprietà Automazione interfaccia utente tramite le tecniche abilitate dal framework dell'interfaccia utente specifico per questa operazione. Se il **tipo di controllo** è imprevisto, potrebbe essere necessario usare un controllo diverso, perché spesso è controllato esclusivamente dalle implementazioni del controllo di un framework dell'interfaccia utente. Quindi testare di nuovo e verificare che **testo dell'Assistente vocale** sia corretto.
- **Layout degli elementi:** Controllare ognuno di questi casi:
    - Verificare che gli elementi ridondanti non siano esposti dall'Assistente vocale. Un esempio di elemento ridondante è il controllo delle classificazioni in ogni Windows di riquadro dello Store.
    - Verificare che gli elementi importanti (elementi che l'utente deve eseguire attività chiave nell'app) vengano visualizzati nella navigazione degli elementi dell'Assistente vocale.
    - Se si usa il **layout** Visivo e manca un elemento perché i controlli si sovrappongono, passare a **Layout** elenco per visualizzare la sequenza segnalata dall'Assistente vocale.
    - Verificare che la struttura Automazione interfaccia utente albero sia accurata e prevista per l'app.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [Accessibilità Microsoft](https://www.microsoft.com/accessibility/)
