---
title: Strumenti di accessibilità-AccScope
description: Lo strumento AccScope consente agli sviluppatori e ai tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di testing ritardato del ciclo di sviluppo di un'app.
ms.assetid: 7C4D78CD-CDDA-8369-B747-6224C152A997
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d057e818a0fe01ef6f219f1a03d82190d21ac14
ms.sourcegitcommit: 305298a7727a428310fa138b45a933bcd7ef2532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/25/2020
ms.locfileid: "104570333"
---
# <a name="accessibility-tools---accscope"></a>Strumenti di accessibilità-AccScope

Lo strumento **AccScope** consente agli sviluppatori e ai tester di valutare l'accessibilità dell'app durante lo sviluppo e la progettazione dell'app, anziché nelle fasi di testing ritardato del ciclo di sviluppo di un'app. Il testing può anche iniziare nelle fasi iniziali del prototipo. **AccScope** può visualizzare il modo in cui un'applicazione per la lettura dello schermo espone le informazioni di automazione interfaccia utente fornite da un'app e può visualizzare le aree in cui è possibile aggiungere informazioni o supporto all'app per migliorarne l'accessibilità.

> [!NOTE]
> **AccScope** è uno strumento legacy. È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .

## <a name="about-accscope"></a>Informazioni su AccScope

**AccScope** viene installato con Windows Software Development Kit (SDK). Si trova nella \\ cartella bin \\ < *versione* > \\ <  > \\ della piattaforma AccScope del percorso di installazione di SDK. Eseguire il programma AccScope.exe.

**AccScope** è un'app desktop, non un'app di Windows Store. È possibile usarlo per esaminare qualsiasi app visualizzata come finestra, tra cui un'app desktop o un'app di Windows Store.

Per abilitare la modalità Assistente vocale, potrebbe essere necessario eseguire **AccScope** come amministratore la prima volta che lo si utilizza.

**AccScope** è disponibile come parte dei file binari degli strumenti di accessibilità, nel Windows SDK. Non viene distribuito come download di exe separato e non esiste negli SDK precedenti.

## <a name="file-menu-options"></a>Opzioni del menu file

- Selezionare **Aggiorna** per aggiornare tutte le informazioni in **AccScope** in modo che corrispondano allo stato corrente della finestra di destinazione. Per un'interfaccia utente contenente un numero elevato di elementi, l'operazione può richiedere alcuni secondi.
- Selezionare o deselezionare **Always on top** per modificare il comportamento della finestra dell'interfaccia utente di **AccScope** . **Always on top** checked è il valore predefinito.
- Selezionare **Esci** per uscire da **AccScope**.

## <a name="view-options"></a>Visualizzare le opzioni

- Selezionare **schermo intero** per eseguire lo strumento **AccScope** in una visualizzazione a schermo intero (quindi usare la tabulazione per visualizzare la finestra di destinazione). Se **AccScope** e l'app di destinazione sono in esecuzione a schermo intero, la selezione host, i rettangoli di delimitazione e la visualizzazione complessiva degli elementi corrisponderanno tra l'app e la vista **AccScope** .
    > [!Note]  
    > **AccScope** e la relativa destinazione devono essere eseguiti sulla stessa visualizzazione.

     

- Selezionare **attivazione automatica** per consentire a AccScope di modificare la finestra di destinazione ogni volta che un utente sposta lo stato attivo sulla finestra usando il mouse o la tastiera.
- Selezionare **aggiornamento automatico** per abilitare la modalità **AccScope** che aggiorna tutti i dati di accessibilità della finestra di destinazione ogni 5 secondi. Questa operazione è utile se i dati di automazione interfaccia utente Microsoft della finestra di destinazione cambiano costantemente.
- Selezionare **aree attive** per evidenziare le aree attive che inviano notifiche nella finestra di destinazione. Un evento di attivazione dell'area dinamica Visualizza una finestra popup rossa con informazioni sull'area dinamica, inclusi il nome e il valore "aria-live" (oppure il valore ARIA equivalente analogo per le app che non usano direttamente il codice HTML, ma con il concetto di aree attive nel supporto di automazione interfaccia utente).

## <a name="element-mode"></a>Modalità elemento

È possibile scegliere di visualizzare una finestra di destinazione tramite una di queste modalità:

- **Controllo foglia**: Mostra una visualizzazione di automazione interfaccia utente di elementi di **controllo** con relazioni padre-figlio, in altre parole una vista dei controlli interattivi "a livello foglia". Usare questa opzione per verificare se tutti i controlli interattivi sono visualizzati correttamente nell'albero di automazione interfaccia utente per una visualizzazione **controlli** .
- **Testo pattern**: Mostra gli intervalli di testo visibili dei contenitori **TextPattern** dalla finestra di destinazione. Usare questa opzione per rappresentare visivamente gli intervalli di testo visibili degli elementi **TextPattern** di automazione interfaccia utente.
- **Assistente vocale**: Mostra gli elementi di automazione interfaccia utente che l'Assistente vocale può identificare usando la metafora di navigazione degli elementi dell'Assistente vocale.
- **Filtro personalizzato**: Mostra una struttura ad albero dei controlli filtrata con una scelta di subset di controllo: **Button**, **CheckBox**, **ComboBox**, **Grid**, **Hyperlink**, **List**, **menu** o **Table**.

La modifica dell'impostazione della **modalità elemento** attiva un aggiornamento della visualizzazione. Per un'interfaccia utente contenente un numero elevato di elementi, l'operazione può richiedere alcuni secondi.

## <a name="layout-options"></a>Opzioni di layout

È possibile selezionare oggetto **visivo** o **elenco** come modalità di visualizzazione per il layout **AccScope** . L'oggetto **visivo** posiziona gli elementi nello spazio delle coordinate nella stessa relazione della finestra di destinazione. **Elenca** gli elementi in un elenco decrescente allineato a sinistra nella finestra **AccScope** e l'ordine dell'elenco è equivalente a un ordine di tabulazione o di lettura.

- Selezionare un'opzione da **Mostra immagini** per controllare quando i rettangoli semplici per gli elementi immagine vengono sostituiti dall'immagine effettiva (o da un piccolo viewport dell'immagine, poiché spesso i rettangoli sono più piccoli dell'immagine effettiva). Il valore predefinito è **al passaggio** del mouse, che Visualizza l'immagine quando ci si sposta all'interno di **AccScope** e si posiziona il puntatore del mouse sul rettangolo per un elemento Image. Le scelte alternative sono **sempre** o **mai**.
- Selezionare **Mostra descrizione comando** per visualizzare le informazioni di base sull'elemento quando si posiziona il puntatore del mouse su un elemento nella visualizzazione **AccScope** . Se la **modalità elemento** è un **controllo foglia** o un **modello di testo** , le informazioni visualizzate nella descrizione comando sono le proprietà di automazione interfaccia utente a livello di elemento con priorità più elevata. Se la **modalità elemento** è **Assistente vocale** , le informazioni includono il testo letto dall'Assistente vocale per l'elemento.
- Selezionare **Mostra numeri** per visualizzare i numeri di sequenza che indicano l'ordine di rendering del controllo nel layout. Lo schema numerico è basato sull'impostazione della **modalità elemento** :
    - **Controllo foglia**: i numeri indicano l'ordine in cui i controlli foglia vengono visualizzati nell'albero di automazione interfaccia utente.
    - **Pattern di testo**: i numeri indicano l'ordine in cui gli intervalli di testo vengono visualizzati in un intervallo di documenti.
    - **Assistente vocale**: il numero indica l'ordine in cui gli elementi vengono spostati nell'esplorazione degli elementi dell'Assistente vocale.

## <a name="choosing-a-window"></a>Scelta di una finestra

Nella **finestra** etichetta è disponibile un elenco a discesa in cui sono elencate tutte le finestre HWND attualmente attive nel sistema. Il testo per ogni finestra visualizzata nell'elenco a discesa è il titolo della finestra e anche un ID di finestra esadecimale tra parentesi quadre. Scegliere uno di questi per modificare la finestra di destinazione su cui viene segnalato **AccScope** . È possibile scegliere di nuovo lo stesso elemento per ottenere lo stesso comportamento di un **aggiornamento** esplicito.

## <a name="using-the-accscope-visualization"></a>Uso della visualizzazione AccScope

L'immagine seguente è una schermata della visualizzazione **AccScope** . Questa schermata specifica Mostra lo strumento **AccScope** che visualizza la finestra di primo livello per l'output di [esempio di accessibilità XAML](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/XAML%20accessibility%20sample) , in esecuzione come app nello stesso computer. Questa schermata mostra la modalità elemento predefinita del **controllo foglia** e il valore **visivo** per **layout**.

![Screenshot della visualizzazione AccScope](images/accscopescreenshot.png)

Si noti come questa visualizzazione rappresenti i controlli nello spazio delle coordinate approssimativo visualizzato nell'app. Invece di visualizzare gli oggetti visivi XAML o il testo completo dei controlli di testo, Mostra i valori delle proprietà dei **nomi** che provengono da ogni elemento di controllo, usando l'automazione interfaccia utente.

Oltre alle opzioni di menu descritte in precedenza, è possibile usare anche queste tecniche:

- Fare clic sul rettangolo di qualsiasi elemento in visualizzazioni **visive** o **elenco** per visualizzare un popup delle **proprietà di UIA** . Elenca una serie di importanti proprietà di automazione interfaccia utente per l'elemento, incluse alcune delle proprietà standard di [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) e altre informazioni, ad esempio i valori aria e una **Descrizione del provider**.
- Fare clic con il pulsante destro del mouse sul rettangolo di qualsiasi elemento in visualizzazioni **visive** o **elenco** per visualizzare un menu di scelta rapida per l'esercizio dei modelli supportati dall'elemento. Se, ad esempio, un elemento supporta [**InvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern), il menu di scelta rapida include un elemento per **Invoke**. Selezionare tale elemento e l'API del criterio appropriato viene esercitata nell'app corrispondente. **AccScope** supporta questa funzionalità per i modelli seguenti: **Invoke**, **ExpandCollapse**, **interruttore**, **SelectionItem**, **ScrollItem**.
- Regolare il dispositivo di scorrimento **trasparenza** per modificare l'opacità o la trasparenza della finestra **AccScope** . Per impostazione predefinita, viene visualizzato come opacità del 100%. Rendere la finestra parzialmente trasparente può essere utile per visualizzare le parti della finestra di destinazione tramite l'interfaccia utente di **AccScope** durante l'uso della modalità **Always on top** .
- Se vengono visualizzate, usare le barre di scorrimento orizzontali e verticali per modificare il centro di visualizzazione della visualizzazione. Questa operazione è utile se si usa l'opzione di layout **visivo** , ma non si usa l'opzione di visualizzazione a **schermo intero** , lasciando la finestra **AccScope** di piccole dimensioni rispetto alla finestra di destinazione.

## <a name="testing-the-narrator-scenario"></a>Test dello scenario di Assistente vocale

Lo scenario dell'Assistente vocale è l'aspetto più importante da testare quando si usa **AccScope**, progettato in modo specifico per visualizzare il funzionamento di base dell'esplorazione degli elementi dell'Assistente vocale quando viene applicato all'app.

Per testare lo scenario di Assistente vocale, usare queste opzioni di configurazione **AccScope** :

- **Modalità elemento**: **Assistente vocale**
- **Layout**: **Visual**
- Opzioni di **layout** : **Mostra la descrizione comando** e **Mostra i numeri** selezionati

Di seguito sono riportate alcune aree specifiche dell'app da testare per lo scenario dell'Assistente vocale:

- **Ordine elementi:** Verificare che l'ordine in cui l'Assistente vocale legga i controlli sia preciso, in base ai numeri (cerchi verdi) visualizzati nelle visualizzazioni. Se gli elementi non sono nell'ordine previsto per la lettura, modificare la struttura dell'interfaccia utente dell'app e l'albero di automazione interfaccia utente risultante e testare di nuovo fino a quando non si è verificato che gli elementi siano in ordine di lettura previsto.
- **Testo vocale:** Spostare il mouse all'interno della visualizzazione e posizionare il puntatore del mouse su ognuno dei rettangoli degli elementi per visualizzare le descrizioni comandi per ogni elemento. In modalità Assistente vocale le descrizioni comandi mostrano una voce di **testo vocale** che rappresenta letteralmente il testo letto dall'Assistente vocale. Questo testo è in genere composto dal **nome** e dal **tipo di controllo**. Verificare che si tratta delle informazioni corrette per ogni controllo nell'interfaccia utente. Se le informazioni non sono corrette, modificare le proprietà di automazione interfaccia utente tramite le tecniche abilitate da un particolare framework dell'interfaccia utente. Se il **tipo di controllo** è imprevisto, potrebbe essere necessario usare un controllo diverso, perché spesso è controllato esclusivamente dalle implementazioni dei controlli di un Framework dell'interfaccia utente. Quindi eseguire di nuovo il test e verificare che il **testo dell'Assistente vocale** sia corretto.
- **Layout elemento:** Controllare ognuno di questi casi:
    - Verificare che gli elementi ridondanti non siano esposti da Assistente vocale. Un esempio di elemento ridondante è il controllo ratings in ogni elemento del riquadro di Windows Store.
    - Verificare che gli elementi importanti (elementi necessari all'utente per eseguire le attività principali nell'app) vengano visualizzati nell'esplorazione degli elementi dell'Assistente vocale.
    - Se si usa il layout **visivo** e manca un elemento perché i controlli si sovrappongono, passare al layout dell' **elenco** per visualizzare la sequenza segnalata dall'Assistente vocale.
    - Verificare che la struttura ad albero di automazione interfaccia utente complessiva sia accurata e prevista per l'app.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [Accessibilità Microsoft](https://www.microsoft.com/accessibility/)
