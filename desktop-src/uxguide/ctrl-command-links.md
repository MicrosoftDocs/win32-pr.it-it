---
title: Collegamenti ai comandi
description: Con i collegamenti di comando, gli utenti selezionano una singola risposta a un'istruzione principale e, in questo modo, passano al passaggio successivo di un'attività.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b579f554d46d48fd7e373d28df516ae1c0baca6a
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524275"
---
# <a name="command-links"></a>Collegamenti ai comandi

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con i collegamenti di comando, gli utenti selezionano una singola risposta a un'istruzione principale e, in questo modo, passano al passaggio successivo di un'attività.

I collegamenti di comando hanno un aspetto pulito e leggero che consente etichette descrittive e vengono visualizzati con una freccia standard o un'icona personalizzata e una spiegazione supplementare facoltativa.

![Screenshot di una tipica finestra di dialogo di collegamento ai comandi ](images/ctrl-command-links-image1.png)

Un set tipico di collegamenti di comando.

I collegamenti di comando sono simili ai [pulsanti](ctrl-radio-buttons.md) di opzione in quanto vengono usati per selezionare da un set di scelte correlate che si escludono a vicenda. Come i pulsanti di opzione, i collegamenti ai comandi vengono sempre visualizzati in set, mai singolarmente. In aspetto, i collegamenti ai comandi hanno un aspetto leggero simile ai collegamenti [normali,](ctrl-links.md)senza cornice o altri tipi di [clic.](glossary.md) I collegamenti ai comandi sono simili [ai](ctrl-command-buttons.md)pulsanti di comando , in quanto possono essere il "pulsante di comando" predefinito e possono avere un tasto di scelta assegnato. Come [i pulsanti di](glossary.md)commit, quando si fa clic si chiude la finestra (per le finestre di dialogo) o si passa alla pagina successiva (per procedure guidate e flussi di pagine).

> [!Note]  
> Le linee guida [relative ai collegamenti](ctrl-links.md) e al [layout](vis-layout.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Le risposte delle opzioni all'istruzione principale sono correlate allo scopo principale della finestra o della pagina?** Gli utenti devono rispondere per eseguire un'operazione diversa dalla semplice navigazione in un'altra pagina? In caso contrario, usare un altro controllo, ad esempio pulsanti di comando o collegamenti. I collegamenti ai comandi non sono appropriati per le scelte secondarie o facoltative o per la navigazione pura.

    ![Screenshot di un elemento personalizza del Pannello di controllo ](images/ctrl-command-links-image2.png)

    Mentre l'Pannello di controllo personalizzazione sembra usare collegamenti di comando, le opzioni sono collegamenti normali perché questa pagina [dell'hub](winenv-ctrl-panels.md) è per la navigazione pura.

-   **Il controllo viene usato per scegliere una risposta da un set di risposte che si escludono a vicenda?** Se non è così, usa un altro controllo. Per consentire agli utenti di scegliere singoli comandi, usare pulsanti di comando o collegamenti.
-   **Per le finestre di dialogo, facendo clic sul controllo si chiude la finestra?** In caso contrario, usare un controllo che non richiede la chiusura della finestra, ad esempio pulsanti di opzione, pulsanti di comando o collegamenti.

    **Non corretto:**

    ![Screenshot della finestra di dialogo Impostazioni firewall a schede ](images/ctrl-command-links-image3.png)

    I collegamenti ai comandi non possono essere usati nelle finestre delle proprietà o nelle finestre di dialogo a schede perché facendo clic sul controllo la finestra viene chiusa.

-   **Per le procedure guidate e i flussi di pagina, fare clic su Passa alla pagina successiva senza impegno?** Non usare collegamenti di comando per eseguire il commit in un'attività. usare invece i pulsanti di commit. Poiché i collegamenti di comando sono simili a collegamenti e gli utenti associano collegamenti alla navigazione all'interno di un flusso di pagina, i collegamenti non sono appropriati per le pagine di [commit](glossary.md) perché gli utenti devono sempre essere in grado di eseguire il back-out.
-   **Per le procedure guidate e i flussi di pagina, altre pagine usano collegamenti di comando?** In tal caso, e tutti gli altri fattori sono uguali, preferire i collegamenti di comando per la coerenza tra le pagine.
-   **Il numero di risposte è compreso tra due e cinque?** Non deve mai essere presente un singolo collegamento di comando. Poiché i collegamenti ai comandi sono controlli di grandi dimensioni e lo spazio dello schermo usato è proporzionale al numero di opzioni, mantenere il numero di risposte a cinque o meno. Per sei o più opzioni, usare pulsanti di opzione, collegamenti regolari o una visualizzazione elenco [a selezione singola.](ctrl-list-views.md)

    ![Screenshot della finestra di dialogo con l'elenco di comandi ](images/ctrl-command-links-image4.png)

    In questo esempio la funzionalità AutoPlay in Microsoft Windows usa una visualizzazione elenco.

-   **Una combinazione di pulsanti di opzione e un pulsante di commit sarebbe una scelta migliore?** I pulsanti di opzione sono una scelta migliore quando si verifica una delle condizioni seguenti:
    -   **È disponibile un'opzione predefinita valida che si vuole selezionare per la maggior parte degli utenti.** È meno probabile che gli utenti cambino un pulsante di opzione predefinito rispetto a un collegamento di comando predefinito, soprattutto in una procedura guidata, in cui gli utenti sono abituati a fare clic su Avanti per accettare le impostazioni predefinite appropriate. D'altra parte, i collegamenti ai comandi sono una scelta migliore se si vuole invitare gli utenti a effettuare una scelta esplicita.
    -   **Gli utenti devono interagire con le scelte (ad esempio per visualizzare informazioni aggiuntive) prima di prendere una decisione.** Ad esempio, la selezione di un pulsante di opzione potrebbe visualizzare una descrizione dell'opzione in modo dinamico.

        ![Screenshot della finestra di dialogo con pulsanti di opzione ](images/ctrl-command-links-image5.png)

        In questo esempio, selezionando un pulsante di opzione viene visualizzata una descrizione dell'opzione.

    -   **Nella pagina sono disponibili opzioni secondarie o correlate.** I collegamenti ai comandi tendono a dominare la pagina, rendendo più semplice ignorare tutto il resto. Inoltre, dopo aver fatto clic su un collegamento di comando, è impossibile selezionare le opzioni secondarie.

        **Non corretto:**

        ![Screenshot della finestra di dialogo con controlli misti ](images/ctrl-command-links-image6.png)

        In questo esempio, esistono due modi diversi per rispondere all'istruzione main. Non è stato usato un collegamento di comando per la prima risposta perché sarebbe difficile selezionare le opzioni secondarie.

        **Corretto:**

        ![Screenshot della finestra di dialogo con gli stessi controlli ](images/ctrl-command-links-image7.png)

        In questo esempio, i pulsanti di opzione rendono chiare le risposte, consentendo allo stesso tempo agli utenti di selezionare le opzioni secondarie.

-   **Per le finestre di dialogo, un gruppo di pulsanti di commit è una scelta migliore?** I collegamenti ai comandi funzionano meglio quando le opzioni richiedono risposte più lunghe e più dettagliate e spiegazioni supplementari, ma un gruppo di pulsanti di commit è una scelta migliore se sono disponibili alcune opzioni semplici.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con salva e non salva ](images/ctrl-command-links-image8.png)

    In questo esempio, l'uso di collegamenti di comando per comandi semplici rende la finestra di dialogo inutilmente complessa.

    **Corretto:**

    ![Screenshot che mostra una finestra di dialogo con i pulsanti di commit "Salva", "Non salvare" e "Annulla".](images/ctrl-command-links-image9.png)

    In questo esempio, l'uso di pulsanti di commit semplici viene eseguito fino al punto.

    Tuttavia, i collegamenti ai comandi auto-esplicativi sono sempre la scelta migliore quando il testo viene usato per spiegare i pulsanti di commit.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con testo non necessario ](images/ctrl-command-links-image10.png)

    In questo esempio il testo viene usato per spiegare i pulsanti di commit.

    **Corretto:**

    ![Screenshot delle etichette che non necessitano di altro testo ](images/ctrl-command-links-image11.png)

    In questo esempio, i collegamenti ai comandi sono auto-esplicativi.

> [!Note]  
> I collegamenti ai comandi richiedono Windows Vista o versioni successive, quindi non sono adatti per le versioni precedenti di Windows. È possibile usare collegamenti regolari come sostituzione.

 

![Screenshot di collegamenti regolari con icone e testo ](images/ctrl-command-links-image12.png)

In questo esempio vengono usati collegamenti regolari con un'icona e una spiegazione supplementare come sostituzione dei collegamenti di comando in Windows XP.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Solo perché i collegamenti ai comandi consentono di usare etichette più descrittive e spiegazioni supplementari facoltative non significa che sia consigliabile. Si consideri l'esempio seguente:

**Non corretto:**

![Screenshot della finestra di dialogo con troppo testo ](images/ctrl-command-links-image13.png)

Questa finestra di dialogo è molto eserere comunicante.

Questa finestra di dialogo accetta una semplice domanda e la complica inutilmente con il testo del collegamento al comando. Gli utenti non vogliono leggere tutto il testo per domande così semplici.

È possibile semplificare questa finestra di dialogo applicando tre linee guida per il collegamento ai comandi:

-   **Non usare una spiegazione supplementare che sia una formulazione wordy del collegamento al comando.** Usare una spiegazione supplementare solo quando non è possibile rendere autoesplicativo un collegamento di comando. Fornire una spiegazione supplementare per un collegamento di comando non significa che è necessario specificarli per tutti i comandi.
-   **Selezionare la risposta più sicura (per evitare la perdita di dati o l'accesso al sistema) e la risposta più sicura come predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o conveniente.
-   **Specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo.

Applicando queste linee guida, è possibile eliminare le spiegazioni supplementari non necessarie, impostare la risposta più comoda come predefinita e fornire un pulsante Annulla esplicito.

**Migliore:**

![Screenshot della finestra di dialogo con comandi ed etichette ](images/ctrl-command-links-image14.png)

Una versione migliorata con collegamenti di comando più semplici.

Anche se è vero che questa versione non spiega in modo esplicito che il non risparmio viene conteggiato come perdita, pochi utenti modificheranno la decisione in base a queste informazioni, rendendo questo un buon compromesso.

Questa finestra di dialogo può essere resa ancora più migliore analizzando se i collegamenti ai comandi sono anche il controllo giusto da usare in questo caso. I pulsanti di commit sono in realtà una scelta migliore, perché le risposte più lunghe e più esplicativi non sono necessarie.

**Miglior:**

![Screenshot della finestra di dialogo con i pulsanti di commit ](images/ctrl-command-links-image15.png)

La versione corretta usa i pulsanti di commit per arrivare direttamente al punto.

I collegamenti di comando presentano molti vantaggi, ma quando vengono usati in modo inconsa they lead to over-communication(Over communication). Per le finestre di dialogo, è consigliabile usare prima i pulsanti di commit e usare i collegamenti di comando solo se i pulsanti di commit non consentono di eseguire il processo.

**Se usati in modo appropriato, i collegamenti ai comandi dovrebbero semplificare e chiarire l'interfaccia utente.** Se i risultati sono l'opposto, fare un passo indietro, esaminare le alternative e concentrarsi su ciò che è effettivamente necessario comunicare.

**Se si fa una sola cosa...** Non usare collegamenti di comando per comunicare in modo over. I collegamenti ai comandi devono semplificare e chiarire la comunicazione, non renderla più complicata.

## <a name="usage-patterns"></a>Modelli di utilizzo

I collegamenti ai comandi hanno diversi modelli di utilizzo:



| Utilizzo                                                                                                                      | Esempio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Risposte alle pagine** I collegamenti di comando vengono usati per rispondere all'istruzione principale e passare alla pagina successiva.    | con questo modello, i collegamenti di comando sostituiscono il pulsante successivo, ma è ancora presente un pulsante Annulla.<br/>Le risposte alle pagine non implicano l'impegno. Poiché i collegamenti di comando sono simili a collegamenti e gli utenti associano collegamenti alla navigazione all'interno di un flusso di pagina, i collegamenti non sono appropriati per le pagine di commit. gli utenti devono essere sempre in grado di eseguire il back-out. <br/> ![Screenshot che mostra una finestra di dialogo "Connetti a Internet" con i collegamenti di comando "Wireless", "Broadband (PPPoE)" e "Dial-up".](images/ctrl-command-links-image16.png)<br/>In questo esempio i collegamenti ai comandi vengono usati per fornire risposte descrittive all'istruzione principale. Anche se qui è possibile usare i pulsanti di opzione, i collegamenti ai comandi consentono agli utenti di rispondere con un solo clic.<br/> |
| **Risposte della finestra di dialogo** I collegamenti di comando vengono usati per rispondere all'istruzione principale e chiudere la finestra di dialogo.  | con questo modello, i collegamenti di comando sostituiscono i pulsanti di commit (ad esempio ok), ma è ancora presente un pulsante di annullamento.<br/>A differenza dei flussi di pagina, non è possibile eseguire il back-out di una risposta basata su finestra di dialogo dopo che è stata effettuata. Di conseguenza, i collegamenti ai comandi della finestra di dialogo implicano l'impegno. <br/> ![Screenshot della finestra di dialogo con collegamenti di comando ](images/ctrl-command-links-image17.png)<br/>In questo esempio i collegamenti ai comandi vengono usati per fornire risposte descrittive all'istruzione principale. Anche se qui è possibile usare i pulsanti di opzione, i collegamenti ai comandi consentono agli utenti di scegliere con un solo clic.<br/>                                                   |
| **Risposte dettagliate** Risposta a una pagina o a una finestra di dialogo che include informazioni dettagliate.                          | In alcuni casi, gli utenti potrebbero avere bisogno di informazioni più dettagliate per scegliere la risposta. <br/> ![Screenshot della finestra di dialogo copia file e delle anteprime ](images/ctrl-command-links-image18.png)<br/> In questo esempio vengono usati collegamenti di comando dettagliati per consentire agli utenti di prendere decisioni informate. Le anteprime e i dettagli del file consentono agli utenti di decidere.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Visualizzare un puntatore occupato se il risultato della selezione di un collegamento di comando non è istantaneo.** Senza commenti e suggerimenti, gli utenti potrebbero presupporre che il clic non sia stato fatto e fare di nuovo clic.

### <a name="presentation"></a>Presentazione

-   **Presentare sempre i collegamenti di comando in un set di due o più elementi.** Logicamente, non c'è alcun motivo per porre una domanda che abbia una sola risposta.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con un collegamento di comando ](images/ctrl-command-links-image19.png)

    In questo esempio la finestra di dialogo sembra offrire all'utente una scelta, ma c'è solo un'istruzione . Deve trattarsi invece di un dialogo informativo.

-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante deve seguire approssimativamente la probabilità di utilizzo, ma avere anche un flusso logico.
    -   **Eccezione:** I collegamenti di comando che comportano l'esecuzione di tutti gli elementi devono essere posizionati per primi.
-   **Specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo. Spesso gli utenti si rendono conto di non voler eseguire un'attività. L'uso di un collegamento di comando per annullare richiederebbe agli utenti di leggere attentamente tutti i collegamenti di comando per determinare quale significa annullare. La presenza di un pulsante Annulla esplicito consente agli utenti di annullare un'attività in modo efficiente.

    **Non corretto:**

    ![Screenshot della finestra di dialogo con il collegamento "Non uscire" ](images/ctrl-command-links-image20.png)

    In questo esempio il collegamento di comando Non uscire deve essere un pulsante Annulla.

-   **Se si specifica un pulsante Annulla esplicito, lasciare un singolo collegamento di comando, specificare sia un collegamento di comando per annullare che un pulsante Annulla.** In questo modo è chiaro che gli utenti hanno la possibilità di scegliere. Formulare questo collegamento di comando in termini di differenza rispetto alla prima risposta, anziché semplicemente "Cancel" o alcune variazioni.

    ![Screenshot di due collegamenti e di un pulsante Annulla ](images/ctrl-command-links-image21.png)

    In questo esempio, il secondo collegamento al comando indica che l'utente ha una scelta, ma non fa altro che annullare. Tuttavia, viene formulata in termini di differenza rispetto al primo collegamento di comando.

-   **Usare Close invece di Cancel se non è possibile ripristinare lo stato precedente dell'ambiente, senza lasciare alcun effetto collaterale.**
-   **Non visualizzare i collegamenti ai comandi disabilitati.** Se un collegamento al comando non si applica al contesto corrente, rimuoverlo. Se si rimuovono tutti i collegamenti di comando non applicabili, viene lasciato un [](mess-confirm.md) singolo collegamento di comando, eliminare la finestra o la pagina oppure visualizzare una conferma se è necessario il consenso esplicito dell'utente.

### <a name="icons"></a>Icone

-   **Tutti i collegamenti di comando necessitano di un'icona.** Le icone consentono agli utenti di distinguere i collegamenti ai comandi dai collegamenti normali e dal testo dell'interfaccia utente.
-   **Usare l'icona a forma di freccia solo per i collegamenti di comando.** I collegamenti normali non devono usare l'icona a forma di freccia a meno che non vengano usati come sostituzione dei collegamenti di comando in Windows XP.
-   **Usare l'icona dello shield di sicurezza per indicare che una risposta richiede un'elevazione immediata.** Per altre linee guida sull'uso dell'icona dello shield di sicurezza, vedere [Controllo dell'account utente.](winenv-uac.md)
-   **Usare icone personalizzate solo se consentono agli utenti di identificare visivamente e distinguere le opzioni.** Non usare icone personalizzate se non sono immediatamente riconoscibili o significative.

    **Non corretto:**

    ![Screenshot di due collegamenti di comando con icone personalizzate ](images/ctrl-command-links-image22.png)

    In questo esempio le icone personalizzate non sono immediatamente riconoscibili.

-   **Per le icone personalizzate, usare icone 16x16 o 32x32 pixel.** Usare le icone più grandi se lo spazio è sufficiente e traggono vantaggio visivo dalle dimensioni maggiori. Se sono necessarie sovrimpressione dello shield di sicurezza, usare icone da 32x32 o 48x48 pixel.

    ![Screenshot di tre collegamenti di comando con icone ](images/ctrl-command-links-image23.png)

    Questo esempio usa icone personalizzate da 32x32 pixel.

    ![Screenshot di due collegamenti di comando con icone più grandi ](images/ctrl-command-links-image24.png)

    Questo esempio usa icone personalizzate da 48x48 pixel, con una sovrimpressione dello shield di sicurezza.

-   **Evitare di combinare icone personalizzate con l'icona a forma di freccia standard in una finestra o in una pagina.** Se si usa un'icona personalizzata su una superficie, provare a usare tutte le icone personalizzate. È tuttavia preferibile usare l'icona a forma di freccia standard rispetto alle icone personalizzate senza significato.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare la risposta più sicura (per evitare la perdita di dati o l'accesso al sistema) e la risposta più sicura come predefinita.** Se sicurezza e sicurezza non sono fattori, selezionare la risposta più probabile o comoda.
-   **Quando possibile, impostare la prima risposta come opzione predefinita,** perché spesso gli utenti lo prevedono, a meno che l'ordine non sia logico.
-   **Per le finestre di dialogo, non impostare un'azione** distruttiva come collegamento di comando predefinito a meno che non sia disponibile un modo semplice per annullare l'azione.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![Screenshot del ridimensionamento e della spaziatura del collegamento di comando ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Etichette

> [!Note]  
> Poiché i collegamenti di comando sono risposte a un'istruzione principale, è consigliabile creare un'istruzione [principale valida](text-ui.md) prima di determinarne le risposte.

 

**Etichette dei collegamenti ai comandi**

-   **Scegliere un'etichetta concisa che comunichi chiaramente e distingue ciò che fa il collegamento al comando.** Deve essere auto-esplicativo e corrispondere all'istruzione principale. Concentrare le etichette sulle differenze tra le risposte. Gli utenti non devono capire cosa significa realmente il collegamento al comando o in che modo è diverso da altri collegamenti di comando.

    **Non corretto:**

    ![Screenshot di un collegamento di comando ridondante ](images/ctrl-command-links-image26.png)

    In questo esempio, qual è la differenza tra la seconda e la terza risposta? Non è contento che sia presente un pulsante Annulla?

-   **Concentrare le etichette dei collegamenti ai comandi per aiutare gli utenti a prendere la decisione giusta.** Omettere i dettagli che non influiscono sulla scelta. Le etichette non devono essere una specifica completa di ciò che accadrà.
-   **Avviare i collegamenti di comando con un verbo.** Non usare il clic, tuttavia, perché l'etichetta deve comunicare cosa fa il collegamento al comando, non come funziona.
    -   **Eccezione:** Se tutti i collegamenti di comando iniziano con lo stesso verbo o frase, eliminare il verbo o la frase ridondante.
-   In generale, **usare formulazioni positive** (fornendo una scelta per eseguire un'operazione). La formulazione negativa (che consente di scegliere di non eseguire operazioni) è accettabile se rende le etichette più facili da comprendere.
-   **Usare formulazioni parallele e etichette a riga singola.** Le etichette lunghe sconsigliano la lettura e non devono essere necessarie. Inoltre, le etichette con dimensioni moderate sono più facili da fare riferimento nella documentazione.
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Non usare la punteggiatura finale a meno che l'etichetta non sia una domanda.**
-   **Assegnare una chiave di accesso univoca.** Per le linee guida, vedere [Tastiera](inter-keyboard.md).
-   **Non usare i puntini di sospensione.** I puntini di sospensione significano che potrebbero essere necessarie altre informazioni per eseguire l'azione. I collegamenti ai comandi usati correttamente non necessitano di puntini di sospensione perché hanno un effetto immediato.
-   **Se una risposta è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** Assicurarsi di aggiungere all'etichetta, non la spiegazione supplementare.
-   **Se una risposta è destinata solo agli utenti avanzati, è consigliabile aggiungere "(advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta, non la spiegazione supplementare.

**Suggerimento:** È possibile valutare i collegamenti di comando immaginando che un amico ha dichiarato l'istruzione principale ed è stato risposto con i collegamenti di comando. Se rispondere con i collegamenti di comando sarebbe innaturale o scomodo, rivedere i collegamenti di comando ed eventualmente l'istruzione principale.

**Spiegazioni supplementari**

-   Se un collegamento al comando richiede ulteriori spiegazioni, **fornire una spiegazione supplementare.** Le spiegazioni supplementari descrivono il motivo per cui gli utenti potrebbero voler scegliere una risposta o cosa accade se viene scelta una risposta.

    ![Screenshot del testo che descrive i risultati dell'opzione ](images/ctrl-command-links-image27.png)

    In questo esempio la spiegazione supplementare descrive le implicazioni dell'opzione .

-   **Non usare una spiegazione supplementare che sia una formulazione wordy del collegamento al comando.** Usare una spiegazione supplementare solo quando non è possibile rendere autoesplicativo un collegamento di comando. Fornire una spiegazione supplementare per un collegamento di comando non significa che è necessario specificarli per tutti.
-   **Concentrarsi su spiegazioni supplementari per aiutare gli utenti a prendere la decisione giusta.** Omettere i dettagli che non influiscono sulla scelta. Le spiegazioni supplementari non devono essere una specifica completa di ciò che accadrà.
-   **Usare la formulazione parallela e al massimo tre righe di testo.** Le spiegazioni supplementari lunghe sconsigliano la lettura e non devono essere necessarie.
-   **Usare frasi complete e punteggiatura finale.**

**Etichette dei gruppi di collegamenti di comando**

-   **Non usare etichette di gruppo.** Le istruzioni principali fungono da etichetta di gruppo per i collegamenti ai comandi.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai collegamenti di comando:

-   Usare il testo esatto dell'etichetta, inclusa la relativa combinazione di maiuscole e minuscole, ma non includere il carattere di sottolineatura della chiave di accesso.
-   Se l'etichetta include un nome di oggetto, omettere il nome dell'oggetto o usare il testo segnaposto.
-   Per descrivere l'interazione dell'utente, usare click.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

**Esempi:** Per copiare l'immagine, fare **clic su Copia e sostituisci**.

Fare clic **su Reimposta scheda di rete**. (Per un collegamento di comando con l'etichetta "Reset the network adaptor *adaptor name" (Reimposta* il nome dell'adattatore di rete)

 

