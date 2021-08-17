---
title: Strumenti di accessibilità - AccEvent (Accessible Event Watcher)
description: AccEvent (Accessible Event Watcher) consente agli sviluppatori e ai tester di convalidare che gli elementi dell'interfaccia utente di un'applicazione generano eventi microsoft Automazione interfaccia utente e Microsoft Active Accessibility corretto quando si verificano modifiche all'interfaccia utente.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb2192bf6973444bf2bfc307ff4613d9d1c593d5a22f9800ecb61bc310b3a210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327804"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Strumenti di accessibilità - AccEvent (Accessible Event Watcher)

**AccEvent (Accessible Event Watcher)** consente a sviluppatori e tester di convalidare che gli elementi dell'interfaccia utente di un'applicazione generano eventi di microsoft Automazione interfaccia utente e Microsoft Active Accessibility corretto quando si verificano modifiche all'interfaccia utente. Le modifiche nell'interfaccia utente possono verificarsi quando lo stato attivo cambia o quando un elemento dell'interfaccia utente viene richiamato, selezionato o ha uno stato o una modifica di proprietà.

**AccEvent** viene installato con Windows Software Development Kit (SDK). Si trova nella cartella bin version platform> del percorso di installazione \\ \\ <  > \\ <  dell'SDK (Accevent.exe).

> [!NOTE]
> **AccEvent** è uno strumento legacy. In alternativa, è [consigliabile Insights](https://accessibilityinsights.io/) accessibilità.

## <a name="requirements"></a>Requisiti

**AccEvent** può essere usato per esaminare i dati di accessibilità nei sistemi che non hanno Automazione interfaccia utente, è stato originariamente scritto per Microsoft Active Accessibility. Per esaminare Automazione interfaccia utente, Automazione interfaccia utente deve essere presente nel sistema. Per altre informazioni, vedere la sezione "Requisiti" di [Automazione interfaccia utente](entry-uiauto-win32.md).

**AccEvent** viene installato come parte del set complessivo di strumenti in Windows SDK, non viene distribuito come download exe separato. L Windows SDK include tutti gli strumenti correlati all'accessibilità documentati in questa sezione. [Ottenere l Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

Per eseguire **AccEvent,** trovare AccEvent.exe nella cartella bin version platform> ed eseguirlo (in genere non è necessario \\ \\ <  > \\ <  eseguire come amministratore).

## <a name="the-accessible-event-watcher-window"></a>Finestra Visualizzatore eventi accessibile

Quando si avvia **AccEvent**, viene visualizzata la finestra principale. La finestra **AccEvent** principale visualizza gli Automazione interfaccia utente o Microsoft Active Accessibility eventi generati dalle applicazioni in esecuzione. La finestra principale include le parti principali seguenti:

- Barra del titolo. Visualizza la modalità operativa e lo stato correnti.
- Barra dei menu. Fornisce l'accesso **alla funzionalità AccEvent.**
- Visualizzazione dati. Visualizza informazioni su ogni evento, inclusi l'ID evento e le proprietà selezionate dell'elemento dell'interfaccia utente che ha generato l'evento.

**AccEvent** ha solo un'interfaccia utente grafica. non sono disponibili argomenti della riga di comando per questo strumento, ma è possibile usare altri strumenti per elaborare il log di output come testo.

L'immagine seguente mostra la finestra **Principale accEvent.**

![l'interfaccia utente per lo strumento Event Watcher accessibile](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Attività di Controllo eventi accessibili

Questa sezione include informazioni sulle attività **AccEvent di uso** comune.

### <a name="configuring-the-operating-mode"></a>Configurazione della modalità operativa

Usare il menu **Modalità** per configurare la **modalità operativa AccEvent** e selezionare le impostazioni che controllano il comportamento dello strumento. È possibile selezionare le opzioni seguenti.



| Quando questa opzione è selezionata | **AccEvent** esegue questa operazione                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Always on Top                | Viene visualizzato sopra qualsiasi altra interfaccia utente sullo schermo.                                                                                                                                                                                    |
| Eventi dell'interfaccia utente                   | Visualizza informazioni sugli Automazione interfaccia utente eventi.                                                                                                                                                                                             |
| WinEvents (nel contesto)       | Visualizza informazioni sugli Microsoft Active Accessibility eventi (WinEvent) passati alle funzioni hook che si trovano nello spazio indirizzi del server. Per altre informazioni, vedere [Funzioni hook nel contesto](in-context-hook-functions.md).         |
| WinEvents (fuori contesto)   | Visualizza informazioni sugli Microsoft Active Accessibility eventi (WinEvent) passati alle funzioni hook che si trovano nello spazio degli indirizzi del client. Per altre informazioni, vedere [Funzioni hook fuori contesto](out-of-context-hook-functions.md). |
| Mostra rettangolo di evidenziazione     | Evidenzia un rettangolo intorno all'elemento dell'interfaccia utente che ha generato l'evento selezionato.                                                                                                                                                                 |
| Mostra descrizione comando informazioni     | Visualizza le informazioni sull'evento in una descrizione comando.                                                                                                                                                                                                        |
| Impostazioni                     | Visualizza la finestra di dialogo Impostazioni eventi **uia** o **WinEvent Impostazioni** finestra di dialogo.                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtraggio Automazione interfaccia utente eventi

Per configurare Automazione interfaccia utente eventi e proprietà visualizzati nella finestra **AccEvent,** fare clic sul **menu** Modalità, selezionare **Eventi UIA** e quindi selezionare Impostazioni **.** Viene visualizzata la finestra di Impostazioni eventi **uia.** È anche possibile usare questa finestra di dialogo per filtrare gli eventi.

La **finestra di dialogo Gestione** Impostazioni eventi dell'interfaccia utente contiene i riquadri seguenti:

- **Eventi globali**

    Selezionare la **casella di controllo FocusChangedEvent** per visualizzare informazioni sugli eventi globali di modifica dello stato attivo.

- **Tipo evento**

    Selezionare gli eventi a cui si è interessati.

- **Ambito**

    Selezionare l'elemento dell'interfaccia utente a **cui si vuole che AccEvent** sia in ascolto degli eventi.

- **Includere eventi da**

    Selezionare **Elementi figlio immediati** se si desidera visualizzare gli eventi degli elementi figlio immediati dell'elemento dell'interfaccia utente selezionato nel **riquadro** Ambito. Per visualizzare gli eventi di tutti gli elementi discendenti, selezionare **Tutti i discendenti**.

- **Proprietà dei report**

    Selezionare le proprietà che si desidera visualizzare dopo ogni evento nella finestra principale. Se nel **menu** **Modalità** è selezionata l'opzione Mostra descrizione comando informazioni, anche le proprietà selezionate vengono visualizzate in una descrizione comando.

### <a name="filtering-active-accessibility-events"></a>Filtraggio Active Accessibility eventi

Per configurare gli eventi e le proprietà Microsoft Active Accessibility visualizzati nella finestra **AccEvent,** fare clic sul **menu** Mode , selezionare **WinEvents (In Context)** o **WinEvents (Out of Context)** e quindi selezionare **Impostazioni**. Viene **visualizzata la Impostazioni** winevent. È anche possibile usare questa finestra di dialogo per filtrare gli eventi.

La **finestra di Impostazioni** winevent contiene i riquadri seguenti:

- **Oggetti**

    Selezionare gli oggetti a cui si **vuole che AccEvent** sia in ascolto degli eventi. **AccEvent** può restare in ascolto di eventi provenienti da finestre, dal cursore o dal cursore. **La finestra** è selezionata per impostazione predefinita.

- **Eventi**

    Selezionare gli eventi a cui si è interessati. Tutti gli eventi vengono visualizzati per impostazione predefinita.

- **Informazioni sull'evento**

    Selezionare le informazioni da visualizzare dopo il nome di ogni evento nella finestra principale.

- **Proprietà degli oggetti**

    Selezionare le proprietà che si desidera visualizzare dopo ogni evento nella finestra principale. Se nel **menu** **Modalità** è selezionata l'opzione Mostra descrizione comando informazioni, anche le proprietà selezionate vengono visualizzate in una descrizione comando. **Per impostazione** **predefinita, vengono** selezionati name , Role e **State.**

- **Filtro**

    Selezionare uno dei pulsanti di opzione nella sezione dei filtri per filtrare gli eventi generati dalle finestre specificate nel **campo hWND.** Il **pulsante di opzione Non filtrare** è selezionato per impostazione predefinita.

    - Selezionare il **pulsante di** opzione Escludi per visualizzare solo gli eventi generati da oggetti diversi dalle finestre specificate.
    - Selezionare il **pulsante di opzione** Includi solo e specificare uno o più handle di finestra per visualizzare solo gli eventi generati da tali finestre.
    - Selezionare la casella di controllo e **Discendenti** per includere gli eventi generati dai discendenti delle finestre specificate.

- **Opzioni**

    Selezionare una o più delle seguenti opzioni:

    

    | Quando questa opzione è selezionata                                  | **AccEvent** esegue questa operazione                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Usare Invoke                                                    | Usa [IDispatch::Invoke per](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) recuperare le proprietà dell'oggetto anziché i [**metodi IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)                               |
    | Ottenere sempre l'oggetto (anche se non è selezionata alcuna proprietà dell'oggetto)     | Recupera l'oggetto associato all'evento anche se non è selezionato alcun elemento nel riquadro Proprietà oggetto .                                                                                        |
    | Visualizzare la proprietà predefinita (oltre alle proprietà selezionate) | Visualizza la proprietà predefinita, se presente, per l'oggetto associato all'evento, insieme agli elementi selezionati nel riquadro Proprietà oggetto.                                                      |
    | Visualizzare le informazioni sugli eventi da finestre invisibili/nascoste       | Visualizza gli elementi selezionati dal riquadro Informazioni evento per tutti gli oggetti, inclusi quelli nelle finestre invisibili o nascoste.                                                                       |
    | Visualizzare informazioni complete sugli eventi da finestre invisibili/nascoste  | Visualizza gli elementi selezionati dal riquadro Informazioni evento e gli elementi selezionati (o predefiniti) dal riquadro Proprietà oggetto per tutti gli oggetti, inclusi quelli in finestre invisibili o nascoste. |
    | DebugBreak all'evento successivo                                      | Causa un'eccezione del punto di interruzione nel processo che ha origine l'evento WinEvent successivo. Ciò segnala al debugger di gestire l'eccezione.                                                        |

### <a name="using-the-event-menu"></a>Uso del menu Eventi

Usare il menu **Evento** per eseguire le attività seguenti:

| Quando questa opzione è selezionata | **AccEvent** esegue questa operazione                                    |
|------------------------------|-------------------------------------------------------|
| Avviare l'ascolto              | Avvia la visualizzazione delle informazioni sull'evento nella visualizzazione Dati. |
| Interrompi ascolto               | Interrompe la visualizzazione delle informazioni sugli eventi nella visualizzazione dati.  |
| Cancella cronologia eventi          | Cancella il contenuto della visualizzazione Dati.                 |
| Seleziona tutti gli eventi            | Seleziona tutti gli eventi elencati nella visualizzazione Dati.           |
| Copiare gli eventi selezionati         | Copia gli eventi selezionati negli Appunti.          |

### <a name="saving-active-accessibility-events"></a>Salvataggio Active Accessibility eventi

Per iniziare a salvare gli eventi in un file di testo, aprire il menu **File** e selezionare **Avvia registrazione in file**. **AccEvent inizia** a scrivere gli eventi nel file specificato fino a quando non si seleziona **Arresta** registrazione dal menu **File.** Il file di testo può essere utile per la risoluzione dei problemi e la revisione degli eventi in un secondo momento.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)