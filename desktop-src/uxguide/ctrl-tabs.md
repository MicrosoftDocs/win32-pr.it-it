---
title: Schede
description: Le schede forniscono un modo per presentare informazioni correlate in pagine con etichetta separate.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b2649862885e55bdfe10fdca7f34b7618d976a38
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104557639"
---
# <a name="tabs"></a>Schede

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Le schede forniscono un modo per presentare informazioni correlate in pagine con etichetta separate.

![Screenshot di cinque schede ](images/ctrl-tabs-image1.png)

Un set tipico di schede.

Le schede sono generalmente associate alle finestre delle proprietà (e viceversa), ma le schede possono essere utilizzate in qualsiasi tipo di finestra.

I controlli struttura a schede rappresentano le cartelle di Manila a schede usate per organizzare le informazioni nei cabinet di archiviazione comunemente presenti nel Stati Uniti. (Le cartelle di Manila non vengono utilizzate in tutto il mondo).

> [!Note]  
> Le linee guida relative a [layout](vis-layout.md), [menu di tabulazione](cmd-menus.md), finestre di [dialogo](win-dialog-box.md)e [finestre delle proprietà](win-property-win.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **I controlli possono adattarsi comodamente a una singola pagina ragionevolmente dimensionata?** In tal caso, utilizzare una singola pagina.
-   **È presente una sola scheda?** In tal caso, utilizzare una singola pagina.
-   **Le schede sono correlate tra loro in modo ovvio?** In caso contrario, è consigliabile suddividere le informazioni in finestre separate di informazioni correlate.
-   **Se vengono usate per le impostazioni, le impostazioni in pagine diverse sono completamente indipendenti?** La modifica di un'impostazione in una pagina influisce sulle impostazioni di altre pagine? Se non sono indipendenti, usare invece le pagine attività o una [procedura guidata](win-wizards.md) .
-   **Le schede sono principalmente peer tra loro o esiste una relazione gerarchica?** Se gerarchico, è possibile usare le [finestre di dialogo](win-dialog-box.md) di divulgazione progressiva o figlio per visualizzare le informazioni correlate.
-   **Le schede sono utilizzate per visualizzare i passaggi all'interno di un'attività?** È possibile usare le "schede" per visualizzare i passaggi all'interno di un'attività solo se vengono presentati come passaggi ed esiste un modo ovvio e alternativo per passare al passaggio del testo, ad esempio un pulsante Avanti. In caso contrario, se i passaggi sono necessari, utilizzare le pagine in un flusso di pagina o una [procedura guidata](win-wizards.md). Se i passaggi sono facoltativi, visualizzare i passaggi facoltativi utilizzando le [finestre di dialogo](win-dialog-box.md) modali.
-   **Le schede sono viste diverse degli stessi dati?** In tal caso, è consigliabile utilizzare un [pulsante di divisione](ctrl-command-buttons.md) o un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) per modificare le visualizzazioni. Sebbene le schede possano essere utilizzate in modo efficace per la modifica delle visualizzazioni, le alternative sono più leggere.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le schede includono diversi modelli di utilizzo:



|                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Superficie dinamica della finestra**<br/> come le barre di scorrimento, è possibile usare le schede per aumentare la superficie di attacco della finestra per visualizzare le informazioni correlate.<br/>                                                    | Con questo modello, l'utilizzo delle schede è concettualmente simile all'inserimento lineare di tutte le informazioni sulle schede in una singola superficie scorrevole, con le etichette delle schede come intestazioni. <br/> ![Screenshot di cinque schede ](images/ctrl-tabs-image1.png)<br/> In questo esempio le schede aumentano in modo efficace la superficie di attacco della finestra.<br/>                          |
| **Più visualizzazioni**<br/> Analogamente ai pulsanti di divisione o agli elenchi a discesa, è possibile usare le schede per mostrare visualizzazioni diverse delle stesse informazioni correlate o. <br/>                                           | ![screenshot delle schede Progettazione, suddivisione e anteprima ](images/ctrl-tabs-image2.png)<br/> In questo esempio, le schede cambiano le visualizzazioni all'interno di un documento.<br/>                                                                                                                                                                                                         |
| **Più documenti**<br/> Analogamente a più finestre, è possibile usare le schede per visualizzare documenti diversi in un'unica finestra. <br/>                                                                   | ![Screenshot di tre schede per documenti diversi ](images/ctrl-tabs-image3.png)<br/> ![Figura delle schede per mesi diversi ](images/ctrl-tabs-image4.png)<br/> In questi esempi, le schede mostrano diversi documenti all'interno di una singola finestra dell'applicazione.<br/>                                                                                       |
| **Opzioni esclusive**<br/> Analogamente ai pulsanti di opzione, è possibile usare le schede per presentare più scelte esclusive. in questo modello viene applicata solo la scheda selezionata e tutte le altre schede vengono ignorate. <br/> | ![screenshot delle schede location, data e messages ](images/ctrl-tabs-image5.png)<br/> In questo esempio le tabulazioni vengono usate (in modo non corretto) come sostituto dei pulsanti di opzione.<br/> **Questo modello non è consigliato** perché usa un comportamento non standard. Le schede si comportano come un'impostazione anziché semplicemente come spostarsi all'interno della finestra. <br/> |



 

**Se si esegue una sola operazione...**

Verificare che le informazioni sulle schede siano correlate, tuttavia le impostazioni in pagine diverse sono indipendenti. L'ultima scheda selezionata non deve avere alcun significato speciale.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **USA tabulazioni orizzontali se:**
    -   La finestra contiene sette o meno schede.
    -   **Tutte le schede si adattano a una riga, anche quando l'interfaccia utente è localizzata.**
-   **Usare le schede verticali se:**
    -   La finestra delle proprietà contiene otto o più schede.
    -   **L'utilizzo di schede orizzontali richiederebbe più di una riga.**

        ![screenshot della finestra delle proprietà con undici opzioni ](images/ctrl-tabs-image6.png)

        In questo esempio, le schede verticali sono adatte a otto o più schede.

-   **Non annidare schede o combinare tabulazioni orizzontali con schede verticali.** Ridurre invece il numero di schede, utilizzare solo schede verticali oppure utilizzare un altro controllo, ad esempio un elenco a discesa.
-   **Non scorrere le schede orizzontali.** Lo scorrimento orizzontale non è immediatamente individuabile. È tuttavia possibile scorrere le schede verticali.

    **Non corretto:**

    ![cattura di schermata dell'etichetta di tabulazione orizzontale troncata ](images/ctrl-tabs-image7.png)

    In questo esempio vengono visualizzate le schede orizzontali.

-   Per le schede in una finestra o un riquadro ridimensionabile, inserire una barra di scorrimento, se necessario, nella pagina, non la finestra o il riquadro. Le schede devono essere sempre visibili e non scorrere al di fuori della visualizzazione.

    ![screenshot della pagina di tabulazione verticale con barra di scorrimento ](images/ctrl-tabs-image8.png)

    In questo esempio, la scheda contiene la barra di scorrimento, non il riquadro.

-   **Verificare che le schede abbiano un aspetto simile a quello delle schede e non di un altro tipo di controllo.**

    **Non corretto:**

    ![screenshot della finestra con pulsanti per le schede ](images/ctrl-tabs-image9.png)

    In questo esempio, queste schede sono simili ai pulsanti di comando.

### <a name="interaction"></a>Interazione

-   **Quando i controlli si applicano solo a una pagina, posizionarli all'interno del bordo della pagina a schede.**
-   **Quando i controlli si applicano all'intera finestra, posizionarli all'esterno della pagina a schede.**
-   **Non assegnare effetti alle schede modificate.** Le schede devono essere accessibili in qualsiasi ordine. La modifica della scheda corrente non deve mai avere effetti collaterali, applicare le impostazioni o generare un messaggio di errore.
-   **Non assegnare un significato speciale all'ultima scheda selezionata.** La selezione della scheda è per la navigazione la selezione dell'ultima scheda dell'utente non è un'impostazione.
-   **Non fare in modo che le impostazioni in una pagina dipendano dalle impostazioni di altre pagine.** In alternativa, inserire le impostazioni dipendenti nella stessa pagina.
-   **Se è probabile che gli utenti inizino con l'ultima scheda visualizzata, rendere la scheda permanente e selezionarla per impostazione predefinita.** Rendere le impostazioni mantenute per ogni singolo utente. In caso contrario, selezionare la prima pagina per impostazione predefinita.

### <a name="icons"></a>Icone

-   **Non inserire icone nelle schede.** Le icone in genere aggiungono confusione visiva superflua, utilizzano lo spazio dello schermo e spesso non migliorano la comprensione dell'utente. Aggiungere solo le icone che facilitano la comprensione, ad esempio i simboli standard.

    **Non corretto:**

    ![screenshot della finestra con icone sulle schede ](images/ctrl-tabs-image10.png)

    In questo esempio, le icone aggiungono confusione visiva e poco per migliorare la comprensione dell'utente.

    **Eccezione:** È possibile usare icone chiaramente riconoscibili se lo spazio disponibile potrebbe essere insufficiente per visualizzare le etichette significative:

    **Corretto:**

    ![screenshot delle schede con icone e Etichette abbreviate ](images/ctrl-tabs-image11.png)

    In questo esempio, la finestra è così limitata che le icone comunicano meglio le schede rispetto alle etichette.

-   **Non usare i logo del prodotto per la scheda grafica.** Le schede non sono per la [personalizzazione](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Modello di superficie della finestra dinamica

-   **Non usare le barre di scorrimento nelle schede.** Le schede funzionano in modo analogo alle barre di scorrimento per aumentare l'area effettiva di una finestra. Un meccanismo dovrebbe essere sufficiente.
-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivano chiaramente il contenuto della pagina. Le etichette più lunghe utilizzano lo spazio dello schermo, soprattutto quando le etichette sono localizzate.
-   **Usare etichette di tabulazioni specifiche e significative.** Evitare le etichette di schede generiche che possono essere applicate a qualsiasi scheda, ad esempio generale, avanzata o impostazioni.
-   **Se una scheda non si applica al contesto corrente e gli utenti non lo prevedono, rimuoverla.** Questa operazione semplifica l'interfaccia utente e gli utenti non lo perdono.

    **Non corretto:**

    ![screenshot della finestra opzioni con il nome della scheda visualizzato in grigio ](images/ctrl-tabs-image12.png)

    In questo esempio la scheda percorsi file è disabilitata in modo errato quando Microsoft Word viene utilizzato come editor di posta elettronica. Anziché disabilitare questa scheda, è necessario rimuoverla perché gli utenti non si aspettano di visualizzare o modificare i percorsi dei file in questo contesto.

-   **Se una scheda non si applica al contesto corrente e gli utenti potrebbero aspettarsi di:**

    -   Visualizzare la scheda.
    -   Disabilitare i controlli nella pagina.
    -   Includere il testo per spiegare il motivo per cui i controlli sono disabilitati.

    Non disabilitare la scheda perché questa operazione non è di facile comprensione e impedisce l'esplorazione. Gli utenti che cercano un valore specifico sarebbero costretti a esaminare tutte le altre schede.

    ![screenshot della finestra con le opzioni della scheda Visualizza in grigio ](images/ctrl-tabs-image13.png)

    In questo esempio, nessuna delle opzioni di visualizzazione si applica al layout di lettura. Tuttavia, gli utenti potrebbero aspettarsi che vengano applicati in base all'etichetta della scheda, in modo che la pagina venga visualizzata, ma le opzioni sono disabilitate.

### <a name="multiple-views-and-documents-patterns"></a>Più visualizzazioni e modelli di documenti

-   **Utilizzare la vista o i nomi dei documenti sulle etichette delle schede.**
-   **Evitare nomi di schede eccessivamente lunghi.** Se necessario, avere una dimensione massima del nome o troncare l'etichetta della scheda visualizzata usando i puntini di sospensione. Le etichette più lunghe utilizzano lo spazio dello schermo, soprattutto quando le etichette sono localizzate.
-   **Se una scheda non si applica al contesto corrente, rimuovere la scheda.**

### <a name="exclusive-options-pattern"></a>Modello di opzioni esclusive

-   **Non usare questo modello.** Usare invece i pulsanti di opzione o un elenco a discesa.

    **Non corretto:**

    ![screenshot della finestra con due schede ' Crea ' ](images/ctrl-tabs-image14.png)

    In questo esempio le tabulazioni vengono usate in modo errato come sostituto dei pulsanti di opzione.

    **Corretto:**

    ![screenshot della finestra con due pulsanti di opzione ](images/ctrl-tabs-image15.png)

    In questo esempio, i pulsanti di opzione vengono utilizzati correttamente.

## <a name="labels"></a>Etichette

-   Etichettare le schede in base al modello. Usare i sostantivi anziché i verbi, senza la punteggiatura finale. Per ulteriori informazioni, vedere le linee guida del modello precedente.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non assegnare una chiave di accesso. Le schede sono accessibili tramite i tasti di scelta rapida (CTRL + TAB, CTRL + MAIUSC + TAB, CTRL + PGSU, Ctrl + PgDn). Si verifica una carenza di scelte valide per le chiavi di accesso, pertanto non è possibile assegnare chiavi di accesso alle schede per facilitarne l'assegnazione ad altri controlli.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento a schede:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la scheda Word.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.
-   Poiché più utilizzi possono essere ambigui, in particolare per i destinatari del mondo, utilizzare solo la scheda sostantivo per fare riferimento solo a un controllo struttura a schede. Per altri usi, chiarire il significato con un descrittore: il tasto TAB, una tabulazione o un segno di tabulazione sul righello.

Esempio: scegliere **Opzioni** dal menu **strumenti** , quindi fare clic sulla scheda **Visualizza** .

