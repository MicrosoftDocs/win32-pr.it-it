---
title: Strumenti di accessibilità-AccEvent (monitoraggio eventi accessibili)
description: AccEvent (monitoraggio eventi accessibile) consente agli sviluppatori e ai tester di verificare che gli elementi dell'interfaccia utente di un'applicazione generino eventi di automazione interfaccia utente Microsoft e di Microsoft Active Accessibility appropriati quando si verificano modifiche all'interfaccia utente.
ms.assetid: 0077da81-7a1f-4f8b-b519-ebefcc63d264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76e6fa4896c0cfe3155536537099b1c00af8ebe5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399437"
---
# <a name="accessibility-tools---accevent-accessible-event-watcher"></a>Strumenti di accessibilità-AccEvent (monitoraggio eventi accessibili)

**Accevent (monitoraggio eventi accessibile)** consente agli sviluppatori e ai tester di verificare che gli elementi dell'interfaccia utente di un'applicazione generino eventi di automazione interfaccia utente Microsoft e di Microsoft Active Accessibility appropriati quando si verificano modifiche all'interfaccia utente. Le modifiche nell'interfaccia utente possono verificarsi quando lo stato attivo cambia o quando un elemento dell'interfaccia utente viene richiamato, selezionato o presenta una modifica dello stato o della proprietà.

**Accevent** viene installato con Windows Software Development Kit (SDK). Si trova nella \\ cartella bin \\ < *Version* > \\ < > cartella del percorso di installazione SDK (Accevent.exe).

> [!NOTE]
> **Accevent** è uno strumento legacy. È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisiti

**Accevent** può essere usato per esaminare i dati di accessibilità nei sistemi che non hanno l'automazione dell'interfaccia utente, ma è stata originariamente scritta per Microsoft Active Accessibility. Per esaminare l'automazione dell'interfaccia utente, è necessario che l'automazione interfaccia utente sia presente nel sistema. Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).

**Accevent** viene installato come parte del set di strumenti completo nel Windows SDK, non viene distribuito come download di exe separato. Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione. [Ottenere il Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

Per eseguire **Accevent**, trovare AccEvent.exe nella \\ cartella bin \\ < *versione* > \\ < *Platform*> ed eseguirlo (in genere non è necessario eseguirlo come amministratore).

## <a name="the-accessible-event-watcher-window"></a>Finestra Monitoraggio eventi accessibile

Quando si avvia **Accevent**, viene visualizzata la finestra principale. Nella finestra principale di **Accevent** vengono visualizzati gli eventi di automazione interfaccia utente o di Microsoft Active Accessibility generati dalle applicazioni in esecuzione. La finestra principale include le parti principali seguenti:

- Barra del titolo. Visualizza la modalità operativa e lo stato correnti.
- Barra dei menu. Consente di accedere alla funzionalità **Accevent** .
- Visualizzazione dati. Visualizza informazioni su ogni evento, inclusi l'ID evento e le proprietà selezionate dell'elemento dell'interfaccia utente che ha generato l'evento.

**Accevent** dispone solo di un'interfaccia utente grafica; non sono disponibili argomenti della riga di comando per questo strumento, ma è possibile usare altri strumenti per elaborare il log di output come testo.

La figura seguente mostra la finestra principale di **Accevent** .

![interfaccia utente per lo strumento Monitoraggio eventi accessibile](images/accevent.png)

## <a name="accessible-event-watcher-tasks"></a>Attività di monitoraggio eventi accessibili

Questa sezione include informazioni sulle attività **Accevent** di uso comune.

### <a name="configuring-the-operating-mode"></a>Configurazione della modalità operativa

Usare il menu **modalità** per configurare la modalità operativa **Accevent** e selezionare le impostazioni che controllano il comportamento dello strumento. È possibile selezionare le opzioni seguenti.



| Quando questa opzione è selezionata | **Accevent** esegue questa operazione                                                                                                                                                                                                                           |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sempre in primo piano                | Viene visualizzato nella parte superiore di qualsiasi altra interfaccia utente sullo schermo.                                                                                                                                                                                    |
| Eventi UIA                   | Visualizza informazioni sugli eventi di automazione interfaccia utente.                                                                                                                                                                                             |
| WinEvents (nel contesto)       | Visualizza informazioni sugli eventi di Microsoft Active Accessibility passati alle funzioni hook che risiedono nello spazio degli indirizzi del server. Per altre informazioni, vedere [funzioni hook nel contesto](in-context-hook-functions.md).         |
| WinEvents (fuori contesto)   | Visualizza informazioni sugli eventi di Microsoft Active Accessibility passati alle funzioni hook che risiedono nello spazio degli indirizzi del client. Per altre informazioni, vedere [funzioni hook out-of-Context](out-of-context-hook-functions.md). |
| Mostra rettangolo di evidenziazione     | Evidenzia un rettangolo intorno all'elemento dell'interfaccia utente che ha generato l'evento selezionato.                                                                                                                                                                 |
| Mostra descrizione comando     | Mostra informazioni sull'evento in una descrizione comando.                                                                                                                                                                                                        |
| Impostazioni                     | Consente di visualizzare la finestra di dialogo **Impostazioni eventi** o impostazioni **WinEvent** .                                                                                                                                                                     |



 

### <a name="filtering-ui-automation-events"></a>Filtro degli eventi di automazione interfaccia utente

Per configurare gli eventi e le proprietà di automazione interfaccia utente visualizzati nella finestra **Accevent** , fare clic sul menu **modalità** , selezionare **eventi UIA**, quindi selezionare **Impostazioni**. Verrà visualizzata la finestra di dialogo **Impostazioni evento UIA** . È inoltre possibile utilizzare questa finestra di dialogo per filtrare gli eventi.

La finestra di dialogo **Impostazioni evento UIA** contiene i riquadri seguenti:

- **Eventi globali**

    Selezionare la casella di controllo **FocusChangedEvent** per visualizzare informazioni sugli eventi di modifica dello stato attivo globale.

- **Tipo evento**

    Selezionare gli eventi a cui si è interessati.

- **Scope**

    Selezionare l'elemento dell'interfaccia utente a cui si desidera che **Accevent** per gli eventi.

- **Includi eventi da**

    Selezionare elementi figlio **diretti** se si desidera visualizzare gli eventi dagli elementi figlio immediati dell'elemento dell'interfaccia utente selezionato nel riquadro **ambito** . Se si desidera visualizzare gli eventi di tutti gli elementi discendenti, selezionare **tutti i discendenti**.

- **Proprietà dei report**

    Selezionare le proprietà che si desidera visualizzare dopo ogni evento nella finestra principale. Se la **Descrizione comando Mostra informazioni** è selezionata nel menu **modalità** , le proprietà selezionate vengono visualizzate anche in una descrizione comando.

### <a name="filtering-active-accessibility-events"></a>Filtro di eventi Active Accessibility

Per configurare gli eventi e le proprietà di Microsoft Active Accessibility visualizzati nella finestra **Accevent** , fare clic sul menu **modalità** , selezionare **winEvents (in contesto)** o **winEvents (fuori contesto)**, quindi selezionare **Impostazioni**. Verrà visualizzata la finestra di dialogo **Impostazioni WinEvent** . È inoltre possibile utilizzare questa finestra di dialogo per filtrare gli eventi.

La finestra di dialogo **Impostazioni WinEvent** contiene i riquadri seguenti:

- **Oggetti**

    Selezionare gli oggetti per i quali si desidera che il **Accevent** sia in ascolto per gli eventi. **Accevent** può restare in ascolto di eventi originati da Windows, dal cursore o dal punto di inserimento. Per impostazione predefinita, la **finestra** è selezionata.

- **Eventi**

    Selezionare gli eventi a cui si è interessati. Tutti gli eventi vengono visualizzati per impostazione predefinita.

- **Informazioni evento**

    Selezionare le informazioni che si desidera visualizzare dopo il nome di ogni evento nella finestra principale.

- **Proprietà degli oggetti**

    Selezionare le proprietà che si desidera visualizzare dopo ogni evento nella finestra principale. Se la **Descrizione comando Mostra informazioni** è selezionata nel menu **modalità** , le proprietà selezionate vengono visualizzate anche in una descrizione comando. Il **nome**, il **ruolo** e **lo stato** sono selezionati per impostazione predefinita.

- **Filtro**

    Selezionare uno dei pulsanti di opzione nella sezione filtro per filtrare gli eventi generati dalle finestre specificate nel campo **HWND** . Il pulsante di opzione **non filtrare** è selezionato per impostazione predefinita.

    - Selezionare il pulsante di opzione **Escludi** per visualizzare solo gli eventi generati da oggetti diversi dalle finestre specificate.
    - Selezionare il pulsante di opzione **Includi solo** e specificare uno o più handle di finestra per visualizzare solo gli eventi generati da tali finestre.
    - Selezionare la casella di controllo **e i discendenti** per includere gli eventi generati dai discendenti delle finestre specificate.

- **Opzioni**

    Selezionare una o più delle seguenti opzioni:

    

    | Quando questa opzione è selezionata                                  | **Accevent** esegue questa operazione                                                                                                                                                                                 |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | USA Invoke                                                    | USA [IDispatch:: Invoke](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) per recuperare le proprietà dell'oggetto anziché usare i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .                               |
    | Ottieni sempre l'oggetto (anche se non è stata selezionata alcuna proprietà dell'oggetto)     | Recupera l'oggetto associato all'evento anche se non è selezionato alcun elemento nel riquadro proprietà oggetto.                                                                                        |
    | Visualizza la proprietà predefinita (oltre alle proprietà selezionate) | Consente di visualizzare la proprietà predefinita, se disponibile, per l'oggetto associato all'evento, insieme agli elementi selezionati nel riquadro proprietà oggetto.                                                      |
    | Visualizzare le informazioni sugli eventi da finestre invisibili/nascoste       | Consente di visualizzare gli elementi selezionati dal riquadro informazioni evento per tutti gli oggetti, inclusi quelli nelle finestre invisibile o nascosta.                                                                       |
    | Visualizza le informazioni complete sugli eventi da finestre nascoste/nascoste  | Consente di visualizzare gli elementi selezionati dal riquadro informazioni evento e gli elementi selezionati (o predefiniti) dal riquadro proprietà oggetto, per tutti gli oggetti, inclusi quelli in finestre nascoste o nascoste. |
    | DebugBreak evento successivo                                      | Causa l'eccezione di un punto di interruzione nel processo che ha origine il WinEvent successivo. In questo modo si segnala al debugger di gestire l'eccezione.                                                        |

### <a name="using-the-event-menu"></a>Uso del menu eventi

Usare il menu **evento** per eseguire le attività seguenti:

| Quando questa opzione è selezionata | **Accevent** esegue questa operazione                                    |
|------------------------------|-------------------------------------------------------|
| Avvia ascolto              | Inizia a visualizzare le informazioni sugli eventi nella vista dati. |
| Interrompi ascolto               | Interrompe la visualizzazione delle informazioni sugli eventi nella visualizzazione dati.  |
| Cancella cronologia eventi          | Cancella il contenuto della visualizzazione dati.                 |
| Seleziona tutti gli eventi            | Seleziona tutti gli eventi elencati nella visualizzazione dati.           |
| Copia eventi selezionati         | Copia gli eventi selezionati negli Appunti.          |

### <a name="saving-active-accessibility-events"></a>Salvataggio di eventi Active Accessibility

Per iniziare a salvare gli eventi in un file di testo, aprire il menu **file** e selezionare **Avvia registrazione nel file**. **Accevent** inizia a scrivere gli eventi nel file specificato fino a quando non si seleziona **Interrompi registrazione** dal menu **file** . Il file di testo può essere utile per la risoluzione dei problemi e la revisione degli eventi in un secondo momento.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
- [Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
- [WinEvents](winevents-infrastructure.md)