---
title: Schede
description: Le schede consentono di presentare informazioni correlate in pagine etichettate separate.
ms.assetid: d90228ce-aa95-4359-be8e-ea2014d71ae6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 167b74bab228398eb0334452a5eacd359578d5bfc01efecb52ccafbcd90d376d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819024"
---
# <a name="tabs"></a>Schede

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Le schede consentono di presentare informazioni correlate in pagine etichettate separate.

![Screenshot di cinque schede ](images/ctrl-tabs-image1.png)

Set tipico di schede.

Le schede sono in genere associate alle finestre delle proprietà (e viceversa), ma le schede possono essere usate in qualsiasi tipo di finestra.

I controlli Struttura a schede rappresentano le cartelle manila a schede usate per organizzare le informazioni nei file CAB di archiviazione comunemente presenti nel Stati Uniti. Le cartelle Manila non vengono usate in tutto il mondo.

> [!Note]  
> Le linee guida relative [al layout,](vis-layout.md) [ai menu delle schede,](cmd-menus.md)alle finestre di [dialogo](win-dialog-box.md)e alle [finestre](win-property-win.md) delle proprietà vengono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **I controlli possono adattarsi facilmente a una singola pagina di dimensioni ragionevoli?** In tal caso, usare una singola pagina.
-   **Esiste una sola scheda?** In tal caso, usare una singola pagina.
-   **Le schede sono correlate tra loro in modo ovvio?** In caso contrario, è consigliabile suddividere le informazioni in finestre separate di informazioni correlate.
-   **Se usate per le impostazioni, le impostazioni in pagine diverse sono completamente indipendenti?** La modifica di un'impostazione in una pagina influirà sulle impostazioni di altre pagine? Se non sono indipendenti, usare invece le pagine delle attività o una [procedura](win-wizards.md) guidata.
-   **Le schede sono per lo più peer tra loro o esiste una relazione gerarchica?** Se gerarchico, è consigliabile usare la divulgazione progressiva o [le finestre di dialogo figlio](win-dialog-box.md) per visualizzare le informazioni correlate.
-   **Le schede vengono usate per visualizzare i passaggi all'interno di un'attività?** È possibile usare le "schede" per visualizzare i passaggi all'interno di un'attività solo se vengono presentati come passaggi ed esiste un modo ovvio e alternativo per accedere al passaggio di testo, ad esempio un pulsante Avanti. In caso contrario, se i passaggi sono necessari, utilizzare le pagine in un flusso di pagina o in una [procedura guidata.](win-wizards.md) Se i passaggi sono facoltativi, visualizzare i passaggi facoltativi usando le finestre [di dialogo modali.](win-dialog-box.md)
-   **Le schede hanno visualizzazioni diverse degli stessi dati?** In tal caso, è consigliabile usare un pulsante di menu [suddiviso](ctrl-command-buttons.md) [o un elenco a discesa](/windows/desktop/uxguide/ctrl-drop) per modificare le visualizzazioni. Anche se le schede possono essere usate in modo efficace per modificare le visualizzazioni, le alternative sono più leggere.

## <a name="usage-patterns"></a>Modelli di utilizzo

Le schede hanno diversi modelli di utilizzo:



|  Utilizzo                                                                                                                                                                                                 |    Esempio                                                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Superficie della finestra dinamica**<br/> Come le barre di scorrimento, le schede possono essere usate per aumentare l'area della finestra in modo da visualizzare le informazioni correlate.<br/>                                                    | Con questo modello, l'uso delle schede è concettualmente simile all'inserimento lineare di tutte le informazioni sulle schede in una singola area scorrevole, con le etichette delle schede come intestazioni. <br/> ![Screenshot di cinque schede ](images/ctrl-tabs-image1.png)<br/> In questo esempio le schede aumentano in modo efficace l'area di superficie della finestra.<br/>                          |
| **Più visualizzazioni**<br/> Come i pulsanti di menu suddivisi o gli elenchi a discesa, le schede possono essere usate per visualizzare visualizzazioni diverse delle stesse informazioni o correlate. <br/>                                           | ![Screenshot delle schede progettazione, divisione e anteprima ](images/ctrl-tabs-image2.png)<br/> In questo esempio le schede cambiano visualizzazione all'interno di un documento.<br/>                                                                                                                                                                                                         |
| **Più documenti**<br/> Come per più finestre, le schede possono essere usate per visualizzare documenti diversi in un'unica finestra. <br/>                                                                   | ![Screenshot di tre schede per documenti diversi ](images/ctrl-tabs-image3.png)<br/> ![figura delle schede per i diversi mesi ](images/ctrl-tabs-image4.png)<br/> In questi esempi, le schede mostrano documenti diversi all'interno di una singola finestra dell'applicazione.<br/>                                                                                       |
| **Opzioni esclusive**<br/> Come i pulsanti di opzione, le schede possono essere usate per presentare più scelte esclusive. In questo modello viene applicata solo la scheda selezionata e tutte le altre schede vengono ignorate. <br/> | ![Screenshot delle schede posizione, dati e messaggi ](images/ctrl-tabs-image5.png)<br/> In questo esempio le schede vengono usate (in modo errato) come sostituzione dei pulsanti di opzione.<br/> **Questo modello non è consigliato** perché usa un comportamento non standard. Le schede si comportano come un'impostazione anziché semplicemente un modo per spostarsi all'interno della finestra. <br/> |



 

**Se si fa una sola cosa...**

Assicurarsi che le informazioni nelle schede siano correlate, ma le impostazioni in pagine diverse sono indipendenti. L'ultima scheda selezionata non deve avere un significato speciale.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Usare le schede orizzontali se:**
    -   La finestra ha sette o meno schede.
    -   **Tutte le schede si adattano a una riga, anche quando l'interfaccia utente è localizzata.**
-   **Usare le schede verticali se:**
    -   La finestra delle proprietà include otto o più schede.
    -   **L'uso di schede orizzontali richiederebbe più di una riga.**

        ![Screenshot della finestra delle proprietà con 11 opzioni ](images/ctrl-tabs-image6.png)

        In questo esempio le schede verticali si adattano a otto o più schede.

-   **Non annidare le schede o combinare le schede orizzontali con le schede verticali.** Ridurre invece il numero di schede, usare solo le schede verticali o usare un altro controllo, ad esempio un elenco a discesa.
-   **Non scorrere le schede orizzontali.** Lo scorrimento orizzontale non è facilmente individuabile. È tuttavia possibile scorrere le schede verticali.

    **Non corretto:**

    ![Screenshot dell'etichetta di tabulazione orizzontale troncata ](images/ctrl-tabs-image7.png)

    In questo esempio vengono scorrete le schede orizzontali.

-   Per le schede in una finestra o un riquadro ridimensionabile, inserire una barra di scorrimento, quando necessario, nella pagina, non nella finestra o nel riquadro. Le schede devono essere sempre visibili e non scorrere all'uscita dalla visualizzazione.

    ![Screenshot della pagina della scheda verticale con barra di scorrimento ](images/ctrl-tabs-image8.png)

    In questo esempio la scheda contiene la barra di scorrimento, non il riquadro.

-   **Assicurarsi che le schede siano simili a schede e non a un altro tipo di controllo.**

    **Non corretto:**

    ![Screenshot della finestra con i pulsanti per le schede ](images/ctrl-tabs-image9.png)

    In questo esempio queste schede sono simili ai pulsanti di comando.

### <a name="interaction"></a>Interazione

-   **Quando i controlli si applicano solo a una pagina, posizionarli all'interno del bordo della pagina a schede.**
-   **Quando i controlli si applicano all'intera finestra, posizionarli all'esterno della pagina a schede.**
-   **Non assegnare effetti alla modifica delle schede.** Le schede devono essere accessibili in qualsiasi ordine. La modifica della scheda corrente non dovrebbe mai avere effetti collaterali, applicare le impostazioni o causare un messaggio di errore.
-   **Non assegnare un significato speciale all'ultima scheda selezionata.** La selezione tramite tabulazione è un'impostazione per lo spostamento dell'ultima scheda dell'utente.
-   **Non rendere le impostazioni di una pagina dipendenti dalle impostazioni di altre pagine.** Inserire invece le impostazioni dipendenti nella stessa pagina.
-   **Se è probabile che gli utenti inizino con l'ultima scheda visualizzata, rendere persistente la scheda e selezionarla per impostazione predefinita.** Rendere persistenti le impostazioni per ogni finestra, per utente. In caso contrario, selezionare la prima pagina per impostazione predefinita.

### <a name="icons"></a>Icone

-   **Non inserire icone nelle schede.** Le icone in genere aggiungono confusione visiva non necessaria, consumano spazio sullo schermo e spesso non migliorano la comprensione dell'utente. Aggiungere solo icone che sono di aiuto per la comprensione, ad esempio i simboli standard.

    **Non corretto:**

    ![Screenshot della finestra con icone nelle schede ](images/ctrl-tabs-image10.png)

    In questo esempio, le icone aggiungono confusione visiva e fanno poco per migliorare la comprensione dell'utente.

    **Eccezione:** È possibile usare icone chiaramente riconoscibili se lo spazio potrebbe non essere sufficiente per visualizzare etichette significative:

    **Corretto:**

    ![Screenshot delle schede con icone ed etichette abbreviate ](images/ctrl-tabs-image11.png)

    In questo esempio la finestra è così stretta che le icone comunicano meglio le schede rispetto alle etichette.

-   **Non usare i logo del prodotto per la grafica delle schede.** Le schede non sono per [la personalizzazione di](exper-branding.md).

### <a name="dynamic-window-surface-pattern"></a>Modello dinamico della superficie della finestra

-   **Non usare le barre di scorrimento nelle schede.** Le schede funzionano in modo analogo alle barre di scorrimento per aumentare l'area effettiva di una finestra. Un meccanismo dovrebbe essere sufficiente.
-   **Usare etichette di tabulazione concise.** Usare una o due parole che descrivono chiaramente il contenuto della pagina. Le etichette più lunghe consumano spazio sullo schermo, soprattutto quando le etichette sono localizzate.
-   **Usare etichette di tabulazione specifiche e significative.** Evitare etichette di tabulazione generiche che potrebbero essere applicate a qualsiasi scheda, ad esempio Generale, Avanzate o Impostazioni.
-   **Se una scheda non si applica al contesto corrente e gli utenti non lo prevedono, rimuoverla.** In questo modo si semplifica l'interfaccia utente e gli utenti non mancheranno.

    **Non corretto:**

    ![Screenshot della finestra delle opzioni con il nome della scheda in grigio ](images/ctrl-tabs-image12.png)

    In questo esempio la scheda Percorsi file viene disabilitata in modo errato quando Microsoft Word come editor di posta elettronica. Anziché disabilitare questa scheda, deve essere rimossa perché gli utenti non si aspetterebbe di visualizzare o modificare i percorsi dei file in questo contesto.

-   **Se una scheda non si applica al contesto corrente e gli utenti potrebbero aspettarsi che:**

    -   Visualizzare la scheda .
    -   Disabilitare i controlli nella pagina.
    -   Includere il testo che spiega perché i controlli sono disabilitati.

    Non disabilitare la scheda, perché questa operazione non è auto-esplicativa e impedisce l'esplorazione. Gli utenti che cercano un valore specifico verrebbero costretti a cercare tutte le altre schede.

    ![Screenshot della finestra con le opzioni della scheda Visualizza in grigio ](images/ctrl-tabs-image13.png)

    In questo esempio nessuna delle opzioni Di visualizzazione è applicabile in Layout di lettura. Tuttavia, gli utenti potrebbero aspettarsi che siano applicati in base all'etichetta della scheda, quindi la pagina viene visualizzata ma le opzioni sono disabilitate.

### <a name="multiple-views-and-documents-patterns"></a>Più visualizzazioni e modelli di documenti

-   **Usare i nomi della vista o del documento nelle etichette delle schede.**
-   **Evitare nomi di schede troppo lunghi.** Se necessario, avere una dimensione massima del nome o troncare l'etichetta della scheda visualizzata usando i puntini di sospensione. Le etichette più lunghe consumano spazio sullo schermo, soprattutto quando le etichette sono localizzate.
-   **Se una scheda non si applica al contesto corrente, rimuovere la scheda.**

### <a name="exclusive-options-pattern"></a>Modello di opzioni esclusive

-   **Non usare questo modello.** Usare invece i pulsanti di opzione o un elenco a discesa.

    **Non corretto:**

    ![Screenshot della finestra con due schede 'create' ](images/ctrl-tabs-image14.png)

    In questo esempio le schede vengono usate erroneamente come sostituti dei pulsanti di opzione.

    **Corretto:**

    ![Screenshot della finestra con due pulsanti di opzione ](images/ctrl-tabs-image15.png)

    In questo esempio vengono usati correttamente i pulsanti di opzione.

## <a name="labels"></a>Etichette

-   Etichettare le schede in base al modello. Usare sostantivi anziché verbi, senza terminare la punteggiatura. Per altre informazioni, vedere le linee guida per il modello precedente.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non assegnare una chiave di accesso. Le schede sono accessibili tramite i relativi tasti di scelta rapida (CTRL+TAB, CTRL+MAIUSC+TAB, CTRL+PGSU, CTRL+PGDN). Esiste una mancanza di scelte valide per le chiavi di accesso, quindi non assegnare i tasti di scelta alle schede semplifica l'assegnazione ad altri controlli.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle schede:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, e includere la scheda della parola.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.
-   Poiché più usi possono essere ambigui, in particolare per i destinatari di tutto il mondo, usare la sola scheda sostantivo per fare riferimento solo a un controllo Struttura a schede. Per altri usi, chiarire il significato con un descrittore: il tasto TAB, una tabulazione o un segno di tabulazione sul righello.

Esempio: scegliere **Opzioni** dal menu Strumenti **e** quindi fare clic **sulla scheda** Visualizza.

