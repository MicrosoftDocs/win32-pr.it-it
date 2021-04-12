---
title: Strumenti di accessibilità-ispeziona
description: Controllare (Inspect.exe) è uno strumento basato su Windows che consente di selezionare qualsiasi elemento dell'interfaccia utente e visualizzare i dati di accessibilità dell'elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Controlla strumento
- Accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1770c6c4db812ea7d2880c50fcc72cd0edc15022
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398664"
---
# <a name="accessibility-tools---inspect"></a>Strumenti di accessibilità-ispeziona

**Controllare** (Inspect.exe) è uno strumento basato su Windows che consente di selezionare qualsiasi elemento dell'interfaccia utente e visualizzare i dati di accessibilità dell'elemento. Puoi visualizzare le proprietà e i pattern di controllo di automazione dell'interfaccia utente Microsoft, oltre alle proprietà di Microsoft Active Accessibility. L' **ispezione** consente inoltre di testare la struttura di spostamento degli elementi di automazione nell'albero di automazione interfaccia utente e gli oggetti accessibili nella gerarchia di Microsoft Active Accessibility.

**Ispezionare** viene installato con Windows Software Development Kit (SDK). (È disponibile anche nelle versioni precedenti di Windows SDK). Si trova nella \\ cartella bin \\ < *Version* > \\ < > cartella del percorso di installazione SDK (Inspect.exe).

> [!NOTE]
> **Controllare** è uno strumento legacy. È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisiti

**Ispezionare** può essere usato per esaminare i dati di accessibilità nei sistemi che non dispongono di automazione interfaccia utente, ma può solo esaminare le proprietà di Microsoft Active Accessibility. Per esaminare l'automazione dell'interfaccia utente, è necessario che l'automazione interfaccia utente sia presente nel sistema. Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).

L' **ispezione** viene installata come parte del set di strumenti completo nel Windows SDK, non viene distribuita come download separato. Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione. [Ottenere il Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

Per eseguire il **controllo**, trovare Inspect.exe nella \\ cartella bin \\ < *versione* > \\ < *Platform*> ed eseguirlo (in genere non è necessario eseguirlo come amministratore).

## <a name="the-inspect-window"></a>Finestra Controlla

La finestra **ispezione** include diverse parti principali:

- Barra del titolo. Consente di visualizzare l'handle della finestra **Controlla** (HWND).
- Barra dei menu. Fornisce l'accesso per **verificare** la funzionalità.
- Barra degli strumenti Fornisce l'accesso per **verificare** la funzionalità.
- Visualizzazione struttura ad albero. Presenta la struttura gerarchica degli elementi dell'interfaccia utente come controllo di visualizzazione albero che è possibile usare per spostarsi tra gli elementi.
- Visualizzazione dati. Visualizza tutte le proprietà di accessibilità esposte per l'elemento dell'interfaccia utente selezionato.

I comandi disponibili nella barra dei menu sono disponibili anche nella barra degli strumenti. L’immagine seguente mostra lo strumento **Inspect** che esegue una query delle proprietà di Automazione interfaccia utente dell’elemento menu **Modifica** nel Blocco note.

![screenshot che mostra l'interfaccia utente per lo strumento di controllo](images/inspect.png)

## <a name="using-inspect"></a>Utilizzo di ispeziona

Quando si inizia a **esaminare**, la visualizzazione **albero** Mostra la posizione dell'elemento dell'interfaccia utente attualmente selezionato nella gerarchia degli elementi e la visualizzazione **dati** Mostra le informazioni sulle proprietà per l'elemento dell'interfaccia utente selezionato. È possibile spostarsi nell'interfaccia utente per visualizzare le informazioni sull'accessibilità relative a ogni elemento nell'interfaccia utente. Per impostazione predefinita, **controllare** tiene traccia dello stato attivo della tastiera o del mouse. Quando lo stato attivo cambia, la visualizzazione **dati** viene aggiornata con le informazioni sulla proprietà dell'elemento con lo stato attivo.

Per spostarsi tra gli elementi dell'interfaccia utente, è possibile usare uno dei seguenti elementi:

- Il mouse
- Tastiera
- Controllo di visualizzazione albero nella visualizzazione **struttura ad albero**
- Opzioni di navigazione nel menu di **navigazione**
- Opzioni di navigazione sulla barra degli strumenti

Le ultime tre opzioni consentono di spostarsi nella gerarchia della struttura ad albero dell'interfaccia utente. La struttura di questo albero può variare leggermente tra l'automazione interfaccia utente e le modalità di Active Accessibility Microsoft.

## <a name="verifying-accessibility-property-information"></a>Verifica delle informazioni sulle proprietà di accessibilità

Nella vista **dati** sono visualizzate le informazioni sulla proprietà dell'elemento dell'interfaccia utente attualmente selezionato. È possibile configurare **ispeziona** per visualizzare informazioni su tutte le proprietà di accessibilità o un subset di tali proprietà. È anche possibile specificare altre opzioni di visualizzazione, ad esempio se l' **ispezione** deve rimanere oltre ad altre interfacce utente o se l' **ispezione** deve evidenziare un rettangolo di delimitazione intorno all'elemento selezionato. Dopo aver configurato il **controllo** per lavorare nel modo desiderato, è possibile iniziare a spostarsi tra gli elementi dell'interfaccia utente e visualizzare le informazioni sulle proprietà. **Controllare** Salva le impostazioni di configurazione quando si chiude e le usa per inizializzare la sessione di **ispezione** successiva.

### <a name="configure-property-settings"></a>Configurare le impostazioni delle proprietà

1. Dal menu **Opzioni** selezionare **impostazioni...** o selezionare **Mostra impostazioni** dalla barra degli strumenti.
2. Nell'elenco **Visualizza in finestra principale** selezionare le proprietà che si desidera visualizzare nella visualizzazione **dati** di **Controlla**.
3. Nell'elenco della **Descrizione comando Visualizza in informazioni** selezionare le proprietà che si desidera visualizzare in una descrizione comando.
4. Per visualizzare le proprietà che l'elemento dell'interfaccia utente potrebbe non supportare, selezionare la casella **Visualizza proprietà non supportate** .
5. Fare clic su **OK**.

### <a name="to-configure-viewing-options"></a>Per configurare le opzioni di visualizzazione

- Nel menu **Opzioni** o nella barra degli strumenti è possibile selezionare le opzioni di visualizzazione seguenti.

| Quando questa opzione è selezionata | **Controlla**                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sempre in primo piano                | Viene visualizzato nella parte superiore di qualsiasi altra finestra sullo schermo.                                                                                                                                                                                  |
| Modalità MSAA                    | Visualizza le informazioni sulla proprietà Active Accessibility Microsoft.                                                                                                                                                                      |
| Modalità di automazione interfaccia utente           | Visualizza le informazioni sulle proprietà di automazione interfaccia utente.                                                                                                                                                                                       |
| Visualizzazione solo Windows visibile    | Disponibile solo in modalità MSAA.                                                                                                                                                                                                       |
| Visualizzazione non elaborata                     | Visualizza la [visualizzazione non elaborata](uiauto-treeoverview.md) della struttura ad albero di automazione interfaccia utente o MSAA nella visualizzazione **albero** .                                                                                                             |
| Visualizzazione controlli                 | Viene visualizzata la [visualizzazione controlli](uiauto-treeoverview.md) dell'albero di automazione interfaccia utente nella visualizzazione **albero** . Disponibile solo in modalità di automazione interfaccia utente.                                                                            |
| Visualizzazione contenuto                 | Viene visualizzata la [visualizzazione contenuto](uiauto-treeoverview.md) dell'albero di automazione interfaccia utente nella visualizzazione **albero** . Disponibile solo in modalità di automazione interfaccia utente.                                                                            |
| Barra degli strumenti del passaggio attivo         | Attiva i pulsanti della barra degli strumenti al passaggio del mouse, anziché richiedere un clic del mouse.                                                                                                                                                      |
| Segnale acustico in errore                | Emette un segnale acustico quando viene rilevato un errore durante un'operazione di automazione interfaccia utente o MSAA.                                                                                                                                                          |
| \_Flag SCREENREADER SPI       | Presuppone che sia presente un'Reader per la lettura dello schermo. Questo flag indica che un'applicazione deve fornire informazioni testuali anziché graficamente. Non presupporre che questo flag sia impostato semplicemente perché è presente un'opzione per la lettura dello schermo.         |
| Mostra rettangolo di evidenziazione     | Evidenzia un rettangolo intorno all'elemento con lo stato attivo.                                                                                                                                                                              |
| Mostra evidenziazione punto di inserimento         | Evidenzia il punto di inserimento. Disponibile solo in modalità MSAA.                                                                                                                                                                                 |
| Mostra descrizione comando     | Mostra informazioni sulle proprietà in una descrizione comando.                                                                                                                                                                                           |
| Guarda lo stato attivo                  | Segue lo stato attivo della tastiera. Quando questa opzione è selezionata, viene installato un hook dell'evento di stato attivo asincrono che sposta il punto di inserimento in alto a sinistra dell'elemento con lo stato attivo. In questo modo l' **ispezione** aggiorna le proprietà in circa un secondo. |
| Guarda il cursore                  | Segue il punto di inserimento. Disponibile solo in modalità MSAA.                                                                                                                                                                                    |
| Cursore espressioni di controllo                 | Segue il cursore.                                                                                                                                                                                                                |
| Espressioni di controllo               | Segue le descrizioni comandi.                                                                                                                                                                                                              |
| Mostra albero                    | Consente di visualizzare la visualizzazione **struttura ad albero** .                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Verifica della navigazione con accessibilità

Dopo aver selezionato un elemento dell'interfaccia utente tramite **ispezionare**, è possibile verificare che l'elemento esponga la corretta navigazione di automazione di Windows per i prodotti di Assistive Technology.

### <a name="verify-accessibility-navigation"></a>Verifica spostamento accessibilità

1. Aprire **Controlla** e l'applicazione che si desidera testare.
2. Selezionare l'elemento dell'interfaccia utente da cui si desidera avviare la navigazione.
3. Nella vista **dati** , verificare che l'elemento esponga le proprietà relative alla navigazione corrette.
4. Utilizzare la visualizzazione **albero** , il menu di **navigazione** o i pulsanti di spostamento sulla barra degli strumenti per spostarsi nell'interfaccia utente e verificare che ogni elemento esponga le proprietà corrette relative alla navigazione.
    > [!Note]  
    > Le opzioni del menu di **navigazione** e i pulsanti della barra degli strumenti di spostamento variano a seconda della posizione dell'elemento selezionato nell'albero.

## <a name="interacting-with-ui-elements"></a>Interazione con gli elementi dell'interfaccia utente

Automazione di Windows espone metodi che consentono ai prodotti di Assistive Technology di interagire con un elemento dell'interfaccia utente come se venisse utilizzato il mouse o la tastiera, ad esempio facendo clic su un pulsante. Il menu **Controlla** azione consente ai tester di richiamare i metodi di automazione di Windows su un elemento (ad esempio, **Invoke. Invoke** chiama il metodo [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) ).

### <a name="interact-with-ui-elements"></a>Interagire con gli elementi dell'interfaccia utente

1. Aprire **Controlla** e l'applicazione che si desidera testare.
2. Selezionare l'elemento dell'interfaccia utente con cui si desidera interagire.
3. Dal menu **azione** o dalla barra degli strumenti selezionare l'azione che corrisponde al metodo di automazione di Windows che si desidera richiamare.

Il menu **azione** contiene gli elementi di **aggiornamento** e di **stato attivo** , insieme ad altri elementi che variano a seconda che la modalità di automazione interfaccia utente o la modalità MSAA sia selezionata. In modalità di automazione interfaccia utente, gli altri elementi riflettono i pattern di controllo supportati dall'elemento dell'interfaccia utente attualmente selezionato. In modalità MSAA gli altri elementi sono sempre costituiti dagli elementi seguenti:

| Azione                | Descrizione                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Aggiorna               | Aggiorna l'interfaccia utente. Disponibile in modalità di automazione interfaccia utente e MSAA.                                               |
| Azione predefinita        | Esegue l'azione predefinita per l'elemento.                                                                          |
| Focus                 | Imposta lo stato attivo sull'elemento. Disponibile in modalità di automazione interfaccia utente e MSAA.                                                  |
| Select                | Seleziona l'elemento.                                                                                                  |
| Estendi selezione      | Estende la selezione di elementi per includere tutti gli elementi tra il primo elemento selezionato e l'elemento corrente. |
| Aggiungi a selezione      | Seleziona l'elemento corrente (ad esempio un elemento elenco).                                                                    |
| Rimuovi dalla selezione | Rimuove l'elemento corrente dalla selezione.                                                                       |
| SetAccValue           | Imposta il valore di Microsoft Active Accessibility dell'elemento sulla stringa specificata.                                 |
| Figlio con stato attivo         | Passa al figlio dell'elemento che ha attualmente lo stato attivo.                                                       |
| HitTest al cursore     | Passa al figlio dell'elemento specificato dal cursore del mouse.                                                      |
| HitTest...            | Apre la finestra di dialogo **HitTest** .                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Tasti di scelta rapida

Molte voci di menu possono essere richiamate con un tasto di scelta rapida anche quando il **controllo** non è l'applicazione attiva. Si noti tuttavia che i tasti di scelta rapida sono in conflitto con alcune applicazioni.

I tasti di scelta rapida seguenti attivano le varie opzioni del menu:



| Per                                                                                                                                       | Utilizzare questo tasto di scelta rapida |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Richiama l'azione predefinita dell'oggetto sotto il cursore (azione predefinita). Disponibile solo in modalità MSAA.                                       | CTRL+MAIUSC+F2              |
| Selezionare l'oggetto sotto il cursore (Select). Disponibile solo in modalità MSAA.                                                                        | CTRL+MAIUSC+F3              |
| Impostare lo stato attivo della tastiera sull'oggetto sotto il cursore (stato attivo).                                                                                   | CTRL + MAIUSC + F4              |
| Passa all'oggetto di pari livello precedente da quello sotto il cursore. Questo comando consente di passare agli oggetti solo all'interno di un contenitore (precedente di pari livello). | CTRL+MAIUSC+F5              |
| Passare all'elemento padre (padre) dell'oggetto.                                                                                                            | CTRL+MAIUSC+F6              |
| Passa al primo elemento figlio dell'oggetto corrente (primo elemento figlio).                                                                                     | CTRL + MAIUSC + F7              |
| Passa all'oggetto di pari livello successivo da quello sotto il cursore. Questo comando consente di passare agli oggetti solo all'interno di un contenitore (successivo elemento di pari livello).         | CTRL + MAIUSC + F8              |
| Passa all'ultimo elemento figlio dell'oggetto corrente (ultimo elemento figlio).                                                                                       | CTRL+MAIUSC+F9              |
| Spostarsi nell'oggetto sotto il cursore del mouse (HitTest al cursore). Disponibile solo in modalità MSAA.                                                      | CTRL+MAIUSC+1               |
| Copiare il contenuto della visualizzazione dati negli Appunti (Copy All).                                                                                  | CTRL+MAIUSC+4               |
| Aggiornare il contenuto della visualizzazione dati (aggiornamento).                                                                                                 | CTRL+MAIUSC+5               |
| Controllare l'oggetto con lo stato attivo (guardare lo stato attivo).                                                                                                   | CTRL+MAIUSC+6               |
| Spostare l'oggetto di pari livello a sinistra di quello in cui si trova il cursore (a sinistra). Disponibile solo in modalità MSAA.                                        | CTRL+MAIUSC+7               |
| Spostare l'oggetto di pari livello sopra l'oggetto su cui è posizionato il cursore (verso l'alto). Disponibile solo in modalità MSAA.                                                | CTRL+MAIUSC+8               |
| Spostare l'oggetto di pari livello sotto quello del cursore (in basso). Disponibile solo in modalità MSAA.                                                 | CTRL+MAIUSC+9               |
| Spostare l'oggetto di pari livello a destra di quello in cui si trova il cursore (a destra). Disponibile solo in modalità MSAA.                                      | CTRL + MAIUSC + 0               |

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [AccScope](accscope.md)
