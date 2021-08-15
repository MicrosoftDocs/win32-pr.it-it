---
title: Strumenti di accessibilità - AccScope
description: Lo strumento AccScope consente a sviluppatori e tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di test latenti del ciclo di sviluppo di un'app.
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

Lo **strumento AccScope** consente a sviluppatori e tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di test latenti del ciclo di sviluppo di un'app. Il testing può anche iniziare nelle fasi iniziali del prototipo. **AccScope** può visualizzare il modo in cui un'utilità per la lettura dello schermo espone le informazioni Automazione interfaccia utente fornite da un'app e può mostrare le aree in cui è possibile aggiungere informazioni o supporto all'app per migliorarne l'accessibilità.

> [!NOTE]
> **AccScope** è uno strumento legacy. In alternativa, è [consigliabile Insights](https://accessibilityinsights.io/) accessibilità.

## <a name="about-accscope"></a>Informazioni su AccScope

**AccScope** viene installato con Windows Software Development Kit (SDK). Si trova nella cartella \\ AccScope della piattaforma della versione bin \\ <  > \\ <  > \\ del percorso di installazione dell'SDK. Eseguire il programma AccScope.exe.

**AccScope** è un'app desktop, non un'app Windows Store. È possibile usarlo per esaminare qualsiasi app visualizzata come finestra, inclusa un'app desktop o un'app Windows Store.

Potrebbe essere necessario eseguire **AccScope** come amministratore la prima volta che lo si usa per abilitare la modalità Assistente vocale.

**AccScope** è disponibile come parte dei file binari degli strumenti di accessibilità, in Windows SDK. Non viene distribuito come download exe separato e non esiste negli SDK precedenti.

## <a name="file-menu-options"></a>Opzioni del menu File

- Selezionare **Aggiorna** per aggiornare tutte le informazioni in **AccScope** in modo che corrispondano allo stato corrente della finestra di destinazione. Per un'interfaccia utente che contiene un numero elevato di elementi, il completamento dell'operazione può richiedere alcuni secondi.
- Selezionare o deselezionare **Always On Top (Sempre in alto)** per modificare il comportamento di windowing dell'interfaccia **utente di AccScope.** **Always On Top** selezionato è l'impostazione predefinita.
- Selezionare **Esci** per uscire **da AccScope.**

## <a name="view-options"></a>Visualizzare le opzioni

- Selezionare **Schermo intero per** eseguire lo strumento **AccScope** in una visualizzazione a schermo intero e quindi usare la tabulazione per visualizzare la finestra di destinazione. Se sia **AccScope che** l'app di destinazione sono in esecuzione a schermo intero, la posizione, i rettangoli di delimitazione e la visualizzazione generale degli elementi corrisponderanno tra l'app e la **visualizzazione AccScope.**
    > [!Note]  
    > **AccScope** e la relativa destinazione devono essere eseguiti sullo stesso schermo.

     

- Selezionare **Auto Focus (Stato** attivo automatico) per consentire ad AccScope di modificare la finestra di destinazione ogni volta che un utente sposta lo stato attivo sulla finestra (tramite mouse o tastiera).
- Selezionare **Aggiornamento automatico** per abilitare la modalità **AccScope** che aggiorna tutti i dati di accessibilità della finestra di destinazione ogni 5 secondi. Ciò è utile se i dati della Automazione interfaccia utente di destinazione di Microsoft cambiano costantemente.
- Selezionare **Aree in tempo** reale per evidenziare tutte le aree in tempo reale che emettere notifiche nella finestra di destinazione. La generazione di un evento in un'area live visualizza un popup rosso che contiene informazioni sull'area live, inclusi il nome e il valore "aria-live" (o il valore ARIA equivalente per le app che non usano direttamente HTML ma usando il concetto di aree live nel supporto di Automazione interfaccia utente).

## <a name="element-mode"></a>Modalità elemento

È possibile scegliere di visualizzare una finestra di destinazione in una delle modalità seguenti:

- **Controllo foglia:** mostra Automazione interfaccia utente di elementi **Control** con relazioni padre-figlio, in altre parole una visualizzazione di controlli interattivi a "livello foglia". Usare questa opzione per verificare se tutti i controlli interattivi vengono visualizzati correttamente nell'albero Automazione interfaccia utente per una **visualizzazione Controllo.**
- **Modello di** testo: mostra gli intervalli di testo visibili **dei contenitori TextPattern** dalla finestra di destinazione. Usare questa opzione per rappresentare visivamente gli intervalli di testo visibili Automazione interfaccia utente **elementi TextPattern.**
- **Assistente vocale:** mostra gli elementi Automazione interfaccia utente che l'Assistente vocale può identificare usando la metafora di navigazione degli elementi dell'Assistente vocale.
- **Filtro personalizzato:** mostra una struttura ad albero dei controlli filtrata con una scelta di subset di controlli: **Button,** **Checkbox,** **Combobox,** **Grid,** **Hyperlink,** **List,** **Menu** **o Table.**

La modifica **dell'impostazione Modalità** elemento attiva un aggiornamento della visualizzazione. Per un'interfaccia utente che contiene un numero elevato di elementi, il completamento dell'operazione può richiedere alcuni secondi.

## <a name="layout-options"></a>Opzioni di layout

È possibile selezionare **Oggetto visivo** o **Elenco** come modalità di visualizzazione per il layout **AccScope.** **L'oggetto** visivo posiziona gli elementi nello spazio delle coordinate nella stessa relazione della finestra di destinazione. **L'elenco** ordina gli elementi in un elenco decrescente allineato a sinistra nella finestra **AccScope** e l'ordine di visualizzazione equivale all'ordine di tabulazione o di lettura.

- Selezionare un'opzione in Mostra immagini per controllare quando i rettangoli semplici per gli elementi immagine vengono sostituiti dall'immagine effettiva (o da un piccolo riquadro di visualizzazione dell'immagine, poiché spesso i rettangoli sono più piccoli dell'immagine effettiva).  Il valore predefinito è **Al passaggio del** mouse, che visualizza l'immagine quando ci si sposta all'interno di **AccScope** e si passa il puntatore del mouse sul rettangolo per un elemento immagine. Le scelte alternative sono **Sempre** o **Mai.**
- Selezionare **Mostra descrizione** comando per visualizzare le informazioni di base sull'elemento ogni volta che si passa il mouse su un elemento nella **visualizzazione AccScope.** Se La **modalità elemento è** Controllo **foglia** o Pattern di **testo,** le informazioni visualizzate nella descrizione comando sono le proprietà a livello di elemento con priorità Automazione interfaccia utente proprietà. Se la **modalità elemento è Assistente** **vocale,** le informazioni includono il testo che l'Assistente vocale leggerebbe per l'elemento.
- Selezionare **Mostra numeri per visualizzare** i numeri di sequenza che indicano l'ordine di rendering del controllo nel layout. Lo schema dei numeri si basa **sull'impostazione Modalità** elemento:
    - **Controllo foglia:** i numeri indicano l'ordine in cui i controlli foglia vengono visualizzati nell'Automazione interfaccia utente albero.
    - **Modello di testo:** i numeri indicano l'ordine in cui gli intervalli di testo vengono visualizzati in un intervallo di documenti.
    - **Assistente** vocale: il numero indica l'ordine in cui vengono spostati gli elementi nella navigazione tra gli elementi dell'Assistente vocale.

## <a name="choosing-a-window"></a>Scelta di una finestra

Sotto **l'etichetta Finestra** è disponibile un elenco a discesa che elenca tutte le finestre HWND attualmente attive nel sistema. Il testo per ogni finestra visualizzato nell'elenco a discesa è il titolo della finestra e anche un ID di finestra esadecimale tra parentesi quadre. Scegliere una di queste opzioni per modificare la finestra di destinazione **per la segnalazione di AccScope.** È possibile scegliere di nuovo lo stesso elemento per ottenere lo stesso comportamento di un oggetto **Refresh esplicito.**

## <a name="using-the-accscope-visualization"></a>Uso della visualizzazione AccScope

L'immagine seguente è uno screenshot della **visualizzazione AccScope.** Questa schermata specifica mostra lo **strumento AccScope che** visualizza la finestra di primo livello per l'output dell'esempio di accessibilità [XAML,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) in esecuzione come app nello stesso computer. Questo screenshot mostra la modalità elemento predefinita del **controllo foglia e** il valore **Visual** per **Layout.**

![Screenshot della visualizzazione AccScope](images/accscopescreenshot.png)

Si noti che questa visualizzazione rappresenta i controlli nello spazio approssimativo delle coordinate visualizzato nell'app. Ma invece di mostrare gli oggetti visivi XAML o il testo completo dei controlli di testo, mostra i valori della proprietà **Name** che provengono da ogni elemento del controllo, usando Automazione interfaccia utente.

Oltre alle opzioni di menu descritte in precedenza, è anche possibile usare queste tecniche:

- Fare clic sul rettangolo di qualsiasi  elemento nelle visualizzazioni **Oggetto** visivo o Elenco per visualizzare una finestra popup **Proprietà UIA.** Vengono elencate alcune delle proprietà Automazione interfaccia utente per tale elemento, incluse alcune delle proprietà [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) standard e altre informazioni, ad esempio i valori ARIA e una descrizione **del provider**.
- Fare clic con il pulsante destro del  mouse sul rettangolo di qualsiasi elemento nelle visualizzazioni **Oggetto** visivo o Elenco per visualizzare un menu di scelta rapida per l'esecuzione dei criteri supportati dall'elemento. Ad esempio, se un elemento supporta [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), il menu di scelta rapida include un elemento per **Invoke**. Selezionare l'elemento e l'API modello appropriata viene esercitata nell'app corrispondente. **AccScope** supporta questa funzionalità per i modelli seguenti: **Invoke**, **ExpandCollapse**, **Toggle**, **SelectionItem**, **ScrollItem**.
- Regolare il **dispositivo di scorrimento** Trasparenza per modificare l'opacità/trasparenza della **finestra AccScope.** Per impostazione predefinita, viene visualizzato come opacità del 100%. Rendere parzialmente trasparente la finestra può essere utile per visualizzare le parti della finestra di destinazione tramite l'interfaccia utente di **AccScope** durante l'uso Always On **modalità Superiore.**
- Se vengono visualizzate, usare le barre di scorrimento orizzontale e verticale per modificare il centro della visualizzazione. Ciò è utile se si usa l'opzione  **Layout** visivo ma non si usa l'opzione Visualizzazione schermo intero, lasciando piccola la finestra **AccScope** rispetto alla finestra di destinazione.

## <a name="testing-the-narrator-scenario"></a>Test dello scenario dell'Assistente vocale

Lo scenario dell'Assistente vocale è l'aspetto più importante da testare quando si usa **AccScope,** progettato specificamente per visualizzare il funzionamento della navigazione di base degli elementi dell'Assistente vocale quando viene applicato all'app.

Per testare lo scenario dell'Assistente vocale, usare queste **opzioni di configurazione di AccScope:**

- **Modalità elemento: Assistente** **vocale**
- **Layout:** **oggetto visivo**
- **Opzioni di** layout: **Mostra descrizione comando** e Mostra **numeri** entrambe selezionate

Ecco alcune aree specifiche dell'app da testare per lo scenario dell'Assistente vocale:

- **Ordine degli elementi:** Verificare che l'ordine in cui l'Assistente vocale legge i controlli sia accurato, in base ai numeri (cerchi verdi) visualizzati nelle visualizzazioni. Se gli elementi non sono nell'ordine previsto per la lettura, modificare la struttura dell'interfaccia utente dell'app e l'albero Automazione interfaccia utente risultante ed eseguire di nuovo il test fino a quando non si verifica che gli elementi siano nell'ordine di lettura previsto.
- **Testo parlato:** Spostare il mouse all'interno della visualizzazione e passare il mouse su ognuno dei rettangoli degli elementi per visualizzare le descrizioni comandi per ogni elemento. In modalità Assistente vocale le descrizioni comandi visualizzano una voce **di** testo dell'Assistente vocale che è letteralmente il testo letto dall'Assistente vocale. In genere questo testo è composto dal **nome e** dal tipo **di controllo**. Verificare che queste siano le informazioni giuste per ogni controllo nell'interfaccia utente. Se le informazioni non sono corrette, modificare le Automazione interfaccia utente usando le tecniche abilitate dal framework dell'interfaccia utente specifico a tale scopo. Se il **tipo di controllo** è imprevisto, potrebbe essere necessario usare un controllo diverso, perché spesso è controllato esclusivamente dalle implementazioni dei controlli di un framework dell'interfaccia utente. Eseguire di nuovo il test e verificare che il **testo dell'Assistente vocale** sia corretto.
- **Layout degli elementi:** Controllare ognuno di questi casi:
    - Verificare che gli elementi ridondanti non siano esposti dall'Assistente vocale. Un esempio di elemento ridondante è il controllo ratings in ogni Windows del riquadro Store.
    - Verificare che gli elementi importanti (elementi che l'utente deve eseguire attività chiave nell'app) vengano visualizzati nella navigazione degli elementi dell'Assistente vocale.
    - Se si usa il **layout** Visivo e manca un elemento perché i controlli si sovrappongono, passare a **Layout** elenco per visualizzare la sequenza segnalata dall'Assistente vocale.
    - Verificare che la struttura Automazione interfaccia utente albero sia accurata e prevista per l'app.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [Accessibilità Microsoft](https://www.microsoft.com/accessibility/)
