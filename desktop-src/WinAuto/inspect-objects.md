---
title: Strumenti di accessibilità - Ispezionare
description: Inspect (Inspect.exe) è uno strumento basato Windows che consente di selezionare qualsiasi elemento dell'interfaccia utente e visualizzare i dati di accessibilità dell'elemento.
ms.assetid: 38edacbc-cf24-4818-b029-561b21e3704c
keywords:
- Strumento Inspect
- Accessibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c72fba29a409fdce60c026c832f68ff6d182bcd9c8a53e1918e7ac847f4332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828710"
---
# <a name="accessibility-tools---inspect"></a>Strumenti di accessibilità - Ispezionare

> [!Important]
> **Inspect** è uno strumento legacy. In alternativa, è [consigliabile Insights](https://accessibilityinsights.io/) accessibilità.

**Inspect** (Inspect.exe) è uno strumento basato Windows che consente di selezionare qualsiasi elemento dell'interfaccia utente e visualizzare i dati di accessibilità dell'elemento. Puoi visualizzare le proprietà e i pattern di controllo di automazione dell'interfaccia utente Microsoft, oltre alle proprietà di Microsoft Active Accessibility. **Inspect** consente anche di testare la struttura di navigazione degli elementi di automazione nell'albero Automazione interfaccia utente e gli oggetti accessibili nella Microsoft Active Accessibility gerarchia.

## <a name="requirements"></a>Requisiti

Per esaminare Automazione interfaccia utente, Automazione interfaccia utente deve essere presente nel sistema. Per altre informazioni, vedere la sezione "Requisiti" di [Automazione interfaccia utente](entry-uiauto-win32.md).

**Inspect** viene installato come parte del set complessivo di strumenti in Windows Software Development Kit (SDK), non viene distribuito come download separato. L Windows SDK include tutti gli strumenti correlati all'accessibilità documentati in questa sezione.

[Scaricare Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/).

> [!NOTE]
> Per le versioni precedenti di Windows SDK, vedere l'sdk [Windows e l'archivio dell'emulatore.](https://developer.microsoft.com/en-us/windows/downloads/sdk-archive/)

**Inspect.exe** si trova nella cartella bin version platform> del percorso di installazione \\ \\ <  > \\ <  dell'SDK (in genere non è necessario eseguire come amministratore).

## <a name="the-inspect-window"></a>Finestra Ispeziona

La **finestra Inspect** (Ispeziona) include diverse parti principali:

- Barra del titolo. Visualizza **l'handle** della finestra Inspect (HWND).
- Barra dei menu. Fornisce l'accesso **alla funzionalità Inspect.**
- Barra degli strumenti Fornisce l'accesso **alla funzionalità Inspect.**
- Visualizzazione albero. Presenta la struttura gerarchica degli elementi dell'interfaccia utente come controllo di visualizzazione albero che è possibile usare per spostarsi tra gli elementi.
- Visualizzazione dati. Visualizza tutte le proprietà di accessibilità esposte per l'elemento dell'interfaccia utente selezionato.

I comandi disponibili nella barra dei menu sono disponibili anche nella barra degli strumenti. L’immagine seguente mostra lo strumento **Inspect** che esegue una query delle proprietà di Automazione interfaccia utente dell’elemento menu **Modifica** nel Blocco note.

![Screenshot che mostra l'interfaccia utente per lo strumento di ispezione](images/inspect.png)

## <a name="using-inspect"></a>Uso di Inspect

Quando si avvia **Inspect**, la visualizzazione **Albero** mostra la posizione dell'elemento dell'interfaccia utente attualmente selezionato nella gerarchia degli elementi e la visualizzazione Dati mostra le informazioni sulle proprietà per l'elemento dell'interfaccia utente selezionato.  È possibile spostarsi nell'interfaccia utente per visualizzare informazioni sull'accessibilità relative a ogni elemento nell'interfaccia utente. Per impostazione predefinita, **Inspect tiene** traccia dello stato attivo della tastiera o del mouse. Quando lo stato attivo cambia, **la visualizzazione** dati viene aggiornata con le informazioni sulle proprietà dell'elemento con lo stato attivo.

Per spostarsi tra gli elementi dell'interfaccia utente, è possibile usare uno degli elementi seguenti:

- Il mouse
- Tastiera
- Controllo di visualizzazione albero nella **visualizzazione Struttura ad** albero
- Opzioni di spostamento nel menu **di** spostamento
- Opzioni di spostamento nella barra degli strumenti

Le ultime tre opzioni consentono di esplorare la gerarchia dell'albero dell'interfaccia utente. La struttura di questo albero può differire leggermente tra Automazione interfaccia utente e Microsoft Active Accessibility modalità.

## <a name="verifying-accessibility-property-information"></a>Verifica delle informazioni sulle proprietà di accessibilità

La **visualizzazione Dati** mostra le informazioni sulle proprietà dell'elemento dell'interfaccia utente attualmente selezionato. È possibile configurare **Inspect per** visualizzare informazioni su tutte le proprietà di accessibilità o su un subset di tali proprietà. È anche possibile specificare altre opzioni di visualizzazione, ad esempio se **Inspect** deve rimanere sopra altre interfacce utente o se **Inspect** deve evidenziare un rettangolo di delimitazione intorno all'elemento selezionato. Dopo aver configurato **Inspect per** il funzionamento desiderato, è possibile iniziare a spostarsi tra gli elementi dell'interfaccia utente e visualizzare le informazioni sulle proprietà. **Inspect** salva le impostazioni di configurazione alla chiusura e le usa per inizializzare la sessione **di ispezione** successiva.

### <a name="configure-property-settings"></a>Configurare la proprietà Impostazioni

1. Dal menu **Opzioni** selezionare **Impostazioni...** o selezionare Mostra finestra Impostazioni **dialogo** sulla barra degli strumenti.
2. **Nell'elenco Visualizza nella finestra** principale selezionare le proprietà da visualizzare nella **visualizzazione** Dati di **Inspect**.
3. **Nell'elenco Visualizza nella descrizione comando** informazioni selezionare le proprietà da visualizzare in una descrizione comando.
4. Per visualizzare le proprietà che l'elemento dell'interfaccia utente potrebbe non supportare, selezionare **la casella Visualizza proprietà non** supportate.
5. Fare clic su **OK**.

### <a name="to-configure-viewing-options"></a>Per configurare le opzioni di visualizzazione

- Nel menu **Opzioni** o nella barra degli strumenti è possibile selezionare le opzioni di visualizzazione seguenti.

| Quando questa opzione è selezionata | **Ispeziona** esegue questa operazione                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Always on Top                | Viene visualizzato nella parte superiore di qualsiasi altra finestra sullo schermo.                                                                                                                                                                                  |
| Modalità MSAA                    | Visualizza Microsoft Active Accessibility proprietà.                                                                                                                                                                      |
| Automazione interfaccia utente modalità           | Visualizza Automazione interfaccia utente proprietà.                                                                                                                                                                                       |
| Visualizzazione Windows visibile    | Disponibile solo in modalità MSAA.                                                                                                                                                                                                       |
| Visualizzazione non elaborata                     | Presenta la [visualizzazione non elaborata](uiauto-treeoverview.md) dell'Automazione interfaccia utente o dell'albero MSAA nella **visualizzazione** Albero.                                                                                                             |
| Visualizzazione controlli                 | Presenta la [visualizzazione controlli](uiauto-treeoverview.md) dell'Automazione interfaccia utente albero nella **visualizzazione** Albero. Disponibile solo in Automazione interfaccia utente predefinita.                                                                            |
| Visualizzazione contenuto                 | Presenta la [visualizzazione contenuto](uiauto-treeoverview.md) dell'Automazione interfaccia utente albero nella **visualizzazione** Albero. Disponibile solo in Automazione interfaccia utente predefinita.                                                                            |
| Barra degli strumenti attiva al passaggio del mouse         | Attiva i pulsanti della barra degli strumenti al passaggio del mouse, anziché richiedere un clic del mouse.                                                                                                                                                      |
| Segnale acustico in base all'errore                | Emire quando viene rilevato un errore durante un'Automazione interfaccia utente o MSAA.                                                                                                                                                          |
| SPI \_ SCREENREADER Flag       | Presuppone che sia presente un'utilità per la lettura dello schermo. Questo flag indica che un'applicazione deve fornire informazioni testualmente anziché graficamente. Non è consigliabile presupporre che questo flag sia impostato semplicemente perché è presente un'utilità per la lettura dello schermo.         |
| Mostra rettangolo di evidenziazione     | Evidenzia un rettangolo intorno all'elemento con lo stato attivo.                                                                                                                                                                              |
| Mostra evidenziazione del punto di evidenziazione         | Evidenzia il punto di evidenziazione. Disponibile solo in modalità MSAA.                                                                                                                                                                                 |
| Mostra descrizione comando informazioni     | Visualizza le informazioni sulle proprietà in una descrizione comando.                                                                                                                                                                                           |
| Guarda lo stato attivo                  | Segue lo stato attivo della tastiera. Quando questa opzione è selezionata, viene installato un hook di evento di stato attivo asincrono e il cursore viene spostato in alto a sinistra dell'elemento con lo stato attivo. In questo **modo Inspect** aggiorna le proprietà in circa un secondo. |
| Guarda il caret                  | Segue il caret. Disponibile solo in modalità MSAA.                                                                                                                                                                                    |
| Cursore espressioni di controllo                 | Segue il cursore.                                                                                                                                                                                                                |
| Descrizioni comando dell'orologio               | Segue le descrizioni comando.                                                                                                                                                                                                              |
| Mostra albero                    | Visualizza la **visualizzazione** Albero.                                                                                                                                                                                                        |

## <a name="verifying-accessibility-navigation"></a>Verifica della navigazione di accessibilità

Dopo aver selezionato un elemento dell'interfaccia utente usando **Inspect**, è possibile verificare che l'elemento esponga la navigazione corretta Windows automazione per assistive technology prodotti.

### <a name="verify-accessibility-navigation"></a>Verificare la navigazione dell'accessibilità

1. Aprire **Inspect** (Ispeziona) e l'applicazione da testare.
2. Selezionare l'elemento dell'interfaccia utente da cui si vuole iniziare la navigazione.
3. Nella visualizzazione **Dati** verificare che l'elemento esponga le proprietà corrette relative alla navigazione.
4. Usare la **visualizzazione Albero,** **il** menu Di spostamento o i pulsanti di spostamento sulla barra degli strumenti per spostarsi nell'interfaccia utente e verificare che ogni elemento esponga le proprietà correlate alla navigazione corrette.
    > [!Note]  
    > Le **opzioni del** menu di spostamento e i pulsanti della barra degli strumenti di spostamento cambiano a seconda della posizione dell'elemento selezionato nell'albero.

## <a name="interacting-with-ui-elements"></a>Interazione con gli elementi dell'interfaccia utente

Windows Automazione espone metodi che consentono assistive technology prodotti di interagire con un elemento dell'interfaccia utente come se si usa il mouse o la tastiera (ad esempio, per fare clic su un pulsante). Il menu **Inspect** Action (Ispeziona azione) consente ai tester di richiamare i metodi di automazione di Windows su un elemento (ad **esempio, Invoke.Invoke** chiama il [**metodo IUIAutomationInvokePattern::Invoke).**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke)

### <a name="interact-with-ui-elements"></a>Interagire con gli elementi dell'interfaccia utente

1. Aprire **Inspect** (Ispeziona) e l'applicazione da testare.
2. Selezionare l'elemento dell'interfaccia utente con cui si vuole interagire.
3. Dal menu **Azione o** dalla barra degli strumenti selezionare l'azione che corrisponde Windows metodo di Automazione che si vuole richiamare.

Il menu **Azione** contiene  gli **elementi Aggiorna** e Stato attivo, insieme ad altri elementi che variano a seconda che sia selezionata la modalità Automazione interfaccia utente o la modalità MSAA. In Automazione interfaccia utente, gli altri elementi riflettono i pattern di controllo supportati dall'elemento dell'interfaccia utente attualmente selezionato. In modalità MSAA gli altri elementi sono sempre costituiti dagli elementi seguenti:

| Azione                | Descrizione                                                                                                           |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Aggiorna               | Aggiorna l'interfaccia utente. Disponibile in modalità msaa e Automazione interfaccia utente sicurezza.                                               |
| Azione predefinita        | Esegue l'azione predefinita per l'elemento.                                                                          |
| Focus                 | Imposta lo stato attivo sull'elemento. Disponibile in modalità msaa e Automazione interfaccia utente sicurezza.                                                  |
| Seleziona                | Seleziona l'elemento.                                                                                                  |
| Estendere la selezione      | Estende la selezione di elementi per includere tutti gli elementi tra il primo elemento selezionato e l'elemento corrente. |
| Aggiungi a selezione      | Seleziona l'elemento corrente, ad esempio un elemento dell'elenco.                                                                    |
| Rimuovi dalla selezione | Rimuove l'elemento corrente dalla selezione.                                                                       |
| SetAccValue           | Imposta il Microsoft Active Accessibility dell'elemento sulla stringa specificata.                                 |
| Figlio con stato attivo         | Passa all'elemento figlio dell'elemento che ha attualmente lo stato attivo.                                                       |
| HitTest al cursore     | Passa all'elemento figlio dell'elemento specificato dal cursore del mouse.                                                      |
| Hittest...            | Apre la **finestra di dialogo HitTest.**                                                                                     |



 

## <a name="keyboard-shortcuts"></a>Tasti di scelta rapida

Molte delle voci di menu possono essere richiamate con un tasto di scelta rapida anche quando **Inspect** non è l'applicazione attiva. Si noti tuttavia che i tasti di scelta rapida sono in conflitto con alcune applicazioni.

I tasti di scelta rapida seguenti attivano le varie opzioni del menu:



| Per                                                                                                                                       | Utilizzare questo tasto di scelta rapida |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Richiamare l'azione predefinita dell'oggetto sotto il cursore (Azione predefinita). Disponibile solo in modalità MSAA.                                       | CTRL+MAIUSC+F2              |
| Selezionare l'oggetto sotto il cursore (Seleziona). Disponibile solo in modalità MSAA.                                                                        | CTRL+MAIUSC+F3              |
| Impostare lo stato attivo della tastiera sull'oggetto sotto il cursore (stato attivo).                                                                                   | CTRL+MAIUSC+F4              |
| Passare all'oggetto di pari livello precedente da quello sotto il cursore. Questo comando consente di passare agli oggetti solo all'interno di un contenitore (elemento di pari livello precedente). | CTRL+MAIUSC+F5              |
| Passare all'elemento padre dell'oggetto (padre).                                                                                                            | CTRL+MAIUSC+F6              |
| Passare al primo elemento figlio dell'oggetto corrente (Primo figlio).                                                                                     | CTRL+MAIUSC+F7              |
| Passare all'oggetto di pari livello successivo da quello sotto il cursore. Questo comando consente di passare agli oggetti solo all'interno di un contenitore (elemento di pari livello successivo).         | CTRL+MAIUSC+F8              |
| Passare all'ultimo elemento figlio dell'oggetto corrente (Ultimo figlio).                                                                                       | CTRL+MAIUSC+F9              |
| Passare all'oggetto sotto il cursore del mouse (HitTest in corrispondenza del cursore). Disponibile solo in modalità MSAA.                                                      | CTRL+MAIUSC+1               |
| Copiare il contenuto della visualizzazione Dati negli Appunti (Copia tutto).                                                                                  | CTRL+MAIUSC+4               |
| Aggiornare il contenuto della visualizzazione Dati (Aggiornamento).                                                                                                 | CTRL+MAIUSC+5               |
| Osservare l'oggetto con lo stato attivo (Stato attivo dell'orologio).                                                                                                   | CTRL+MAIUSC+6               |
| Passare all'oggetto di pari livello a sinistra di quello su cui si trova il cursore (a sinistra). Disponibile solo in modalità MSAA.                                        | CTRL+MAIUSC+7               |
| Passare all'oggetto di pari livello sopra l'oggetto su cui si trova il cursore (Su). Disponibile solo in modalità MSAA.                                                | CTRL+MAIUSC+8               |
| Passare all'oggetto di pari livello sotto quello su cui si trova il cursore (Giù). Disponibile solo in modalità MSAA.                                                 | CTRL+MAIUSC+9               |
| Passare all'oggetto di pari livello a destra di quello su cui si trova il cursore (Destra). Disponibile solo in modalità MSAA.                                      | CTRL+MAIUSC+0               |

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [AccScope](accscope.md)
