---
title: Collegamenti ai comandi
description: Con i collegamenti ai comandi, gli utenti selezionano una singola risposta a un'istruzione principale e in questo modo passano al passaggio successivo di un'attività.
ms.assetid: a77819b1-9a32-4468-94fb-3f73a469fb81
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 29031b4456950db6ceff30d75b354dece92c5897
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103761290"
---
# <a name="command-links"></a>Collegamenti ai comandi

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con i collegamenti ai comandi, gli utenti selezionano una singola risposta a un'istruzione principale e in questo modo passano al passaggio successivo di un'attività.

I collegamenti ai comandi hanno un aspetto pulito e leggero che consente le etichette descrittive e vengono visualizzati con una freccia standard o un'icona personalizzata e una spiegazione aggiuntiva facoltativa.

![Screenshot di una tipica finestra di dialogo del collegamento di comando ](images/ctrl-command-links-image1.png)

Un set tipico di collegamenti di comando.

I collegamenti ai comandi sono simili ai [pulsanti di opzione](ctrl-radio-buttons.md) in quanto vengono usati per effettuare una selezione da un set di scelte correlate che si escludono a vicenda. Analogamente ai pulsanti di opzione, i collegamenti ai comandi vengono sempre presentati nei set, mai singolarmente. In apparenza, i collegamenti ai comandi hanno un aspetto leggero simile ai [collegamenti](ctrl-links.md)normali, senza un frame o con un'altra [offerta](glossary.md)di clic forte. I collegamenti ai comandi sono simili anche ai [pulsanti di comando](ctrl-command-buttons.md), in quanto possono essere il "pulsante di comando" predefinito e possono avere una chiave di accesso assegnata. Come i [pulsanti di commit](glossary.md), fare clic su Chiudi la finestra (per le finestre di dialogo) o passare alla pagina successiva (per le procedure guidate e i flussi di pagine).

> [!Note]  
> Le linee guida correlate ai [collegamenti](ctrl-links.md) e al [layout](vis-layout.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Sono disponibili le risposte alle opzioni per l'istruzione principale e relative allo scopo principale della finestra o della pagina?** È necessario che gli utenti rispondano a tali utenti per eseguire un'operazione diversa dalla semplice navigazione a una pagina diversa? In caso contrario, usare un altro controllo, ad esempio i pulsanti di comando o i collegamenti. I collegamenti ai comandi non sono appropriati per le scelte secondarie o facoltative o per la navigazione pura.

    ![Screenshot di un elemento del pannello di controllo personalizzato ](images/ctrl-command-links-image2.png)

    Mentre l'elemento del pannello di controllo della personalizzazione sembra che usi i collegamenti ai comandi, le opzioni sono collegamenti regolari perché questa [pagina Hub](winenv-ctrl-panels.md) è per la navigazione pure.

-   **Il controllo viene usato per scegliere una risposta da un set di risposte che si escludono a vicenda?** Se non è così, usa un altro controllo. Per consentire agli utenti di scegliere i singoli comandi, usare i pulsanti di comando o i collegamenti.
-   **Per le finestre di dialogo, fare clic sul controllo chiudere la finestra?** In caso contrario, usare un controllo che non richiede la chiusura della finestra, ad esempio pulsanti di opzione, pulsanti di comando o collegamenti.

    **Non corretto:**

    ![screenshot della finestra di dialogo impostazioni del firewall a schede ](images/ctrl-command-links-image3.png)

    Non è possibile usare i collegamenti di comando nelle finestre delle proprietà o nelle finestre di dialogo a schede perché fare clic sul controllo chiude la finestra.

-   **Per le procedure guidate e i flussi di pagina, fare clic su passa alla pagina successiva senza impegno?** Non usare i collegamenti di comando per eseguire il commit in un'attività. usare invece i pulsanti di commit. Poiché i collegamenti ai comandi sono simili a collegamenti e gli utenti associano collegamenti con la navigazione all'interno di un flusso di pagine, i collegamenti non sono appropriati per le [pagine di commit](glossary.md) perché gli utenti devono essere sempre in grado di
-   **Per le procedure guidate e i flussi di pagina, sono altre pagine che usano i collegamenti di comando?** In caso affermativo, e tutti gli altri fattori sono uguali, preferire i collegamenti ai comandi per la coerenza tra le pagine.
-   **Il numero di risposte tra due e cinque?** Non dovrebbe mai esistere un solo collegamento di comando. Poiché i collegamenti ai comandi sono controlli di grandi dimensioni e lo spazio dello schermo usato è proporzionale al numero di opzioni, è possibile lasciare il numero di risposte a cinque o meno. Per sei o più opzioni, usare pulsanti di opzione, collegamenti regolari o una [visualizzazione elenco](ctrl-list-views.md)a selezione singola.

    ![screenshot della finestra di dialogo con l'elenco dei comandi ](images/ctrl-command-links-image4.png)

    In questo esempio, la funzionalità AutoPlay in Microsoft Windows utilizza una visualizzazione elenco.

-   **Una combinazione di pulsanti di opzione e un pulsante di commit è la scelta migliore?** I pulsanti di opzione sono la scelta migliore quando si verifica una delle condizioni seguenti:
    -   **È disponibile un'opzione predefinita avanzata che si desidera venga selezionata dalla maggior parte degli utenti.** È meno probabile che gli utenti modifichino un pulsante di opzione predefinito rispetto a un collegamento al comando predefinito, soprattutto in una procedura guidata, in cui gli utenti sono abituati a fare clic su Avanti per accettare le impostazioni predefinite appropriate. D'altra parte, i collegamenti ai comandi sono una scelta migliore se si vuole incoraggiare gli utenti a effettuare una scelta esplicita.
    -   **Gli utenti devono interagire con le scelte, ad esempio per visualizzare informazioni aggiuntive, prima di prendere una decisione.** Ad esempio, la selezione di un pulsante di opzione potrebbe visualizzare una descrizione dell'opzione in modo dinamico.

        ![screenshot della finestra di dialogo con pulsanti di opzione ](images/ctrl-command-links-image5.png)

        In questo esempio, la selezione di un pulsante di opzione consente di visualizzare una descrizione dell'opzione.

    -   **Sono presenti opzioni secondarie o correlate nella pagina.** I collegamenti ai comandi tendono a dominare la pagina, semplificando l'accesso a tutti gli altri elementi. Inoltre, una volta fatto clic sul collegamento di un comando, è Impossibile selezionare le opzioni secondarie.

        **Non corretto:**

        ![screenshot della finestra di dialogo con controlli misti ](images/ctrl-command-links-image6.png)

        In questo esempio sono disponibili due modi diversi per rispondere all'istruzione principale. Non è stato usato un collegamento di comando per la prima risposta perché sarebbe difficile selezionare le opzioni secondarie.

        **Corretto:**

        ![screenshot della finestra di dialogo con gli stessi controlli ](images/ctrl-command-links-image7.png)

        In questo esempio, i pulsanti di opzione rendono evidenti le risposte, consentendo agli utenti di selezionare le opzioni secondarie.

-   **Per le finestre di dialogo, un gruppo di pulsanti di commit è la scelta migliore?** I collegamenti ai comandi funzionano meglio quando le opzioni richiedono risposte più lunghe, più esplicative e spiegazioni aggiuntive, ma un gruppo di pulsanti di commit è la scelta migliore se sono disponibili poche opzioni semplici.

    **Non corretto:**

    ![screenshot della finestra di dialogo con Save e Not Save ](images/ctrl-command-links-image8.png)

    In questo esempio, l'utilizzo di collegamenti di comando per semplici comandi rende la finestra di dialogo inutilmente complessa.

    **Corretto:**

    ![Screenshot che mostra una finestra di dialogo con i pulsanti di commit ' Save ',' not save ' è Cancel '.](images/ctrl-command-links-image9.png)

    In questo esempio, l'uso di semplici pulsanti di commit viene eseguito fino al punto.

    Tuttavia, i collegamenti ai comandi autoesplicativi sono sempre la scelta migliore quando si utilizza il testo per spiegare i pulsanti di commit.

    **Non corretto:**

    ![screenshot della finestra di dialogo con testo superfluo ](images/ctrl-command-links-image10.png)

    In questo esempio il testo viene usato per spiegare i pulsanti di commit.

    **Corretto:**

    ![screenshot delle etichette che non necessitano di più testo ](images/ctrl-command-links-image11.png)

    In questo esempio, i collegamenti ai comandi sono di chiara interpretazione.

> [!Note]  
> I collegamenti ai comandi richiedono Windows Vista o versione successiva, quindi non sono adatti per le versioni precedenti di Windows. È possibile utilizzare i collegamenti normali come sostitutivi.

 

![screenshot dei collegamenti regolari con icone e testo ](images/ctrl-command-links-image12.png)

In questo esempio, i collegamenti regolari con un'icona e una spiegazione supplementare vengono usati come sostituti dei collegamenti ai comandi in Windows XP.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

Solo perché i collegamenti ai comandi consentono di usare etichette più descrittive e spiegazioni aggiuntive facoltative non significa che è necessario. Si consideri l'esempio seguente:

**Non corretto:**

![screenshot della finestra di dialogo con un testo troppo grande ](images/ctrl-command-links-image13.png)

Questa finestra di dialogo sta comunicando seriamente.

Questa finestra di dialogo richiede una semplice domanda e la complica inutilmente con il testo del collegamento del comando. Gli utenti non vogliono leggere tutto il testo per le domande più semplici.

È possibile semplificare questa finestra di dialogo applicando tre linee guida sui collegamenti di comando:

-   **Non usare una spiegazione aggiuntiva che rappresenta una riformulazione del collegamento del comando.** Usare una spiegazione aggiuntiva solo quando non è possibile rendere il collegamento di un comando di chiara interpretazione. Fornire una spiegazione aggiuntiva per un collegamento al comando non significa che è necessario fornirli per tutti i comandi.
-   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e la risposta più sicura come predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o pratica.
-   **Consente di specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo.

Applicando queste linee guida, è possibile eliminare le spiegazioni aggiuntive superflue, rendere la risposta più comoda per impostazione predefinita e fornire un pulsante Annulla esplicito.

**Migliore:**

![screenshot della finestra di dialogo con comandi ed etichette ](images/ctrl-command-links-image14.png)

Una versione migliorata con i collegamenti ai comandi più semplici.

Sebbene sia vero che questa versione non spieghi in modo esplicito che il mancato salvataggio viene conteggiato come una perdita, un numero limitato di utenti cambierà la decisione in base a queste informazioni, rendendo così un compromesso positivo.

Questa finestra di dialogo può essere resa ancora migliore analizzando se i collegamenti ai comandi sono o meno il controllo corretto da usare in questo caso. I pulsanti di commit sono in realtà una scelta migliore, perché non sono necessarie risposte più esplicative.

**Consigliate**

![screenshot della finestra di dialogo con i pulsanti di commit ](images/ctrl-command-links-image15.png)

La versione corretta usa i pulsanti commit per ottenere immediatamente il punto.

I collegamenti ai comandi presentano molti vantaggi, ma quando vengono usati in modo insensato comportano la sovracomunicazione. Per le finestre di dialogo, provare a usare prima i pulsanti di commit e usare i collegamenti ai comandi solo se i pulsanti di commit non eseguono correttamente il processo.

**Se usati in modo appropriato, i collegamenti ai comandi devono semplificare e chiarire l'interfaccia utente.** Se i risultati sono quelli opposti, riesaminare le alternative e concentrarsi sugli elementi effettivamente necessari per comunicare.

**Se si esegue una sola operazione...** Non usare i collegamenti di comando per la comunicazione eccessiva. I collegamenti ai comandi devono semplificare e chiarire la comunicazione, senza renderla più complicata.

## <a name="usage-patterns"></a>Modelli di utilizzo

I collegamenti ai comandi includono diversi modelli di utilizzo:



|                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Risposte di pagina** I collegamenti ai comandi vengono usati per rispondere all'istruzione principale e passare alla pagina successiva.    | con questo modello, i collegamenti ai comandi sostituiscono il pulsante Avanti, ma è ancora presente un pulsante Annulla.<br/>Le risposte della pagina non implicano l'impegno. Poiché i collegamenti ai comandi sono simili a collegamenti e gli utenti associano collegamenti con la navigazione all'interno di un flusso di pagina, i collegamenti non sono appropriati per le pagine Gli utenti devono essere sempre in grado di eseguire il backup. <br/> ![Screenshot che mostra la finestra di dialogo ' Connetti a Internet ' con i collegamenti ai comandi ' wireless ',' Broadband (PPPoE)' è connessione remota '.](images/ctrl-command-links-image16.png)<br/>In questo esempio, i collegamenti ai comandi vengono usati per fornire risposte descrittive all'istruzione principale. Quando è possibile usare i pulsanti di opzione, i collegamenti ai comandi consentono agli utenti di rispondere con un solo clic.<br/> |
| **Risposte della finestra di dialogo** I collegamenti ai comandi vengono utilizzati per rispondere all'istruzione principale e chiudere la finestra di dialogo.  | con questo modello, i collegamenti ai comandi sostituiscono i pulsanti di commit (ad esempio OK), ma è ancora presente un pulsante Annulla.<br/>A differenza dei flussi di pagine, non è possibile eseguire il backup di una risposta basata sulla finestra di dialogo dopo che è stata eseguita. di conseguenza, i collegamenti ai comandi della finestra di dialogo implicano l'impegno. <br/> ![screenshot della finestra di dialogo con i collegamenti ai comandi ](images/ctrl-command-links-image17.png)<br/>In questo esempio, i collegamenti ai comandi vengono usati per fornire risposte descrittive all'istruzione principale. Quando è possibile usare i pulsanti di opzione, i collegamenti ai comandi consentono agli utenti di scegliere con un solo clic.<br/>                                                   |
| **Risposte dettagliate** Risposta A una pagina o A una finestra di dialogo che include informazioni dettagliate.                          | in alcuni casi, gli utenti potrebbero avere bisogno di informazioni più dettagliate per scegliere la risposta. <br/> ![screenshot della finestra di dialogo Copia file e delle anteprime ](images/ctrl-command-links-image18.png)<br/> In questo esempio vengono usati i collegamenti dettagliati per consentire agli utenti di prendere decisioni informate. Le anteprime e i dettagli del file consentono agli utenti di decidere.<br/>                                                                                                                                                                                                                                                                                                         |



 

## <a name="guidelines"></a>Indicazioni

### <a name="interaction"></a>Interazione

-   **Visualizza un puntatore occupato se il risultato della selezione di un collegamento a un comando non è immediato.** Senza commenti, gli utenti potrebbero presupporre che il clic non sia stato fatto, quindi fare clic di nuovo su.

### <a name="presentation"></a>Presentazione

-   **Presentare sempre i collegamenti ai comandi in un set di due o più.** Logicamente, non c'è motivo di porre una domanda con una sola risposta.

    **Non corretto:**

    ![screenshot della finestra di dialogo con un collegamento di comando ](images/ctrl-command-links-image19.png)

    In questo esempio viene visualizzata la finestra di dialogo in cui viene offerta la scelta dell'utente, ma è disponibile solo un'istruzione. Deve essere invece una finestra di dialogo informativa.

-   **Presentare prima i collegamenti ai comandi usati più di frequente.** L'ordine risultante dovrebbe approssimativamente rispettare la probabilità di utilizzo, ma anche un flusso logico.
    -   **Eccezione:** I collegamenti ai comandi che comportano l'operazione devono essere inseriti per primi.
-   **Consente di specificare un pulsante Annulla esplicito.** Non usare un collegamento di comando a questo scopo. Spesso gli utenti si rendono conto che non vogliono eseguire un'attività. L'uso di un collegamento al comando per l'annullamento richiederebbe agli utenti di leggere con attenzione tutti i collegamenti ai comandi per individuare quello che indica l'annullamento. La presenza di un pulsante Annulla esplicito consente agli utenti di annullare un'attività in modo efficiente.

    **Non corretto:**

    ![screenshot della finestra di dialogo con collegamento ' non uscire ' ](images/ctrl-command-links-image20.png)

    In questo esempio il collegamento al comando non Exit deve essere un pulsante Annulla.

-   **Se l'inserimento di un pulsante Annulla esplicito lascia un solo collegamento di comando, specificare sia un collegamento di comando da annullare che un pulsante Annulla.** In questo modo è chiaro che gli utenti hanno una scelta. Frase il collegamento del comando in termini di differenze rispetto alla prima risposta, anziché semplicemente "Annulla" o una variante.

    ![Screenshot di due collegamenti e di un pulsante Annulla ](images/ctrl-command-links-image21.png)

    In questo esempio, il secondo collegamento del comando indica che l'utente ha una scelta, ma tutto è annullato. Tuttavia, viene formulata in base alle differenze rispetto al primo collegamento al comando.

-   **Utilizzare Close anziché Cancel se non è possibile ripristinare lo stato precedente dell'ambiente, lasciando nessun effetto collaterale.**
-   **Non visualizzare i collegamenti ai comandi disabilitati.** Se un collegamento di comando non si applica al contesto corrente, rimuoverlo. Se la rimozione di tutti i collegamenti di comando che non si applicano lascia un solo collegamento al comando, eliminare la finestra o la pagina o visualizzare una [conferma](mess-confirm.md) se è necessario il consenso esplicito dell'utente.

### <a name="icons"></a>Icone

-   **Tutti i collegamenti ai comandi richiedono un'icona.** Le icone consentono agli utenti di distinguere i collegamenti dei comandi da collegamenti regolari e testo dell'interfaccia utente.
-   **Usare l'icona freccia solo per i collegamenti ai comandi.** I collegamenti regolari non devono utilizzare l'icona a forma di freccia a meno che non vengano utilizzati come sostituti per i collegamenti ai comandi in Windows XP.
-   **Usare l'icona dello scudo di sicurezza per indicare che una risposta richiede un'elevazione immediata.** Per altre linee guida sull'uso dell'icona dello scudo di sicurezza, vedere [controllo dell'account utente](winenv-uac.md).
-   **Usare icone personalizzate solo se consentono agli utenti di identificare visivamente e differenziare le opzioni.** Non usare icone personalizzate se non sono immediatamente riconoscibili o significative.

    **Non corretto:**

    ![Screenshot di due collegamenti ai comandi con icone personalizzate ](images/ctrl-command-links-image22.png)

    In questo esempio le icone personalizzate non sono immediatamente riconoscibili.

-   **Per le icone personalizzate, usare le icone 16x16 o 32x32 pixel.** Usare le icone più grandi se lo spazio è sufficiente e si traggono vantaggi visivi dalle dimensioni maggiori. Se sono necessarie sovrapposizioni dello scudo di sicurezza, usare le icone 32x32 o 48x48 pixel.

    ![Screenshot di tre collegamenti comando con icone ](images/ctrl-command-links-image23.png)

    Questo esempio Usa icone personalizzate pixel 32x32.

    ![Screenshot di due collegamenti ai comandi con icone più grandi ](images/ctrl-command-links-image24.png)

    Questo esempio Usa icone personalizzate pixel 48x48 con una sovrapposizione dello scudo di sicurezza.

-   **Evitare di combinare icone personalizzate con l'icona a forma di freccia standard in una finestra o in una pagina.** Se si usa un'icona personalizzata in una superficie, provare a usare tutte le icone personalizzate. È tuttavia preferibile usare l'icona a forma di freccia standard su icone personalizzate significative.

### <a name="default-values"></a>Valori predefiniti

-   **Selezionare il più sicuro (per evitare la perdita di dati o l'accesso al sistema) e la risposta più sicura come predefinita.** Se la sicurezza e la sicurezza non sono fattori, selezionare la risposta più probabile o pratica.
-   **Quando si è pratici, effettuare la prima risposta all'opzione predefinita,** perché gli utenti si aspettano spesso che, a meno che tale ordine non sia logico.
-   **Per le finestre di dialogo, non eseguire un'azione distruttiva sul collegamento del comando predefinito** a meno che non esista un modo semplice per annullare l'azione.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![screenshot delle dimensioni e della spaziatura dei collegamenti ai comandi ](images/ctrl-command-links-image25.png)

## <a name="labels"></a>Etichette

> [!Note]  
> Poiché i collegamenti ai comandi sono risposte a un'istruzione principale, è necessario creare una [corretta istruzione principale](text-ui.md) prima di determinarne le risposte.

 

**Etichette collegamenti comando**

-   **Scegliere un'etichetta concisa che comunichi chiaramente e differenzi il collegamento del comando.** Dovrebbe essere di chiara comprensione e corrispondere all'istruzione principale. Concentrare le etichette sulle differenze tra le risposte. Non è necessario che gli utenti riescano a capire cosa significa il collegamento del comando o come differisce da altri collegamenti di comando.

    **Non corretto:**

    ![Screenshot di un collegamento di comando ridondante ](images/ctrl-command-links-image26.png)

    In questo esempio, qual è la differenza tra la seconda e la terza risposta? Se è presente un pulsante Annulla,

-   **Concentrare il comando sul collegamento delle etichette per aiutare gli utenti a prendere la decisione giusta.** Omettere i dettagli che non influiscono sulla scelta. Le etichette non devono necessariamente essere una specifica completa delle operazioni che si verificheranno.
-   **Avviare i collegamenti ai comandi con un verbo.** Non usare fare clic, tuttavia, perché l'etichetta deve comunicare il collegamento del comando, non come funziona.
    -   **Eccezione:** Se tutti i collegamenti ai comandi iniziano con lo stesso verbo o frase, eliminare il verbo o la frase ridondante.
-   In generale, **utilizzare** la formulazione positiva (che consente di scegliere di eseguire un'operazione). La formulazione negativa, che consente di scegliere di non eseguire alcuna operazione, è accettabile se le etichette sono più facili da comprendere.
-   **Usare la formulazione parallela e le etichette a riga singola.** Le etichette lunghe scoraggiano la lettura e non devono essere necessarie. Inoltre, le etichette di dimensioni moderate sono più semplici da fare riferimento a nella documentazione.
-   **Usare le maiuscole/minuscole come nelle frasi comuni.**
-   **Non usare la punteggiatura finale a meno che l'etichetta non sia una domanda.**
-   **Assegnare una chiave di accesso univoca.** Per le linee guida, vedere [tastiera](inter-keyboard.md).
-   **Non usare ellissi.** I puntini di sospensione indicano che potrebbero essere necessarie più informazioni per eseguire l'azione. I collegamenti ai comandi utilizzati correttamente non necessitano di ellissi perché hanno un effetto immediato.
-   **Se una risposta è fortemente consigliata, aggiungere "(scelta consigliata)" all'etichetta.** Assicurarsi di aggiungere all'etichetta, non la spiegazione aggiuntiva.
-   **Se una risposta è destinata solo agli utenti avanzati, è consigliabile aggiungere "(Advanced)" all'etichetta.** Assicurarsi di aggiungere all'etichetta, non la spiegazione aggiuntiva.

**Suggerimento:** È possibile valutare i collegamenti ai comandi immaginando che un amico ha dichiarato l'istruzione principale ed è stato risposto con i collegamenti ai comandi. Se la risposta con i collegamenti ai comandi non è naturale o scomoda, rivedere i collegamenti ai comandi e possibilmente l'istruzione principale.

**Spiegazioni aggiuntive**

-   Se un collegamento al comando richiede un'ulteriore spiegazione, **fornire una spiegazione aggiuntiva**. Le spiegazioni aggiuntive descrivono perché gli utenti potrebbero voler scegliere una risposta o cosa accade se viene scelta una risposta.

    ![screenshot del testo che descrive i risultati dell'opzione ](images/ctrl-command-links-image27.png)

    In questo esempio la spiegazione supplementare descrive le implicazioni dell'opzione.

-   **Non usare una spiegazione aggiuntiva che prevede la riformulazione del collegamento del comando.** Usare una spiegazione aggiuntiva solo quando non è possibile rendere il collegamento di un comando di chiara interpretazione. Fornire una spiegazione aggiuntiva per un collegamento al comando non significa che è necessario fornirli tutti.
-   **Spiega le spiegazioni aggiuntive per aiutare gli utenti a prendere la decisione giusta.** Omettere i dettagli che non influiscono sulla scelta. Le spiegazioni aggiuntive non devono necessariamente essere una specifica completa delle operazioni che si verificheranno.
-   **Utilizzare il formulazione parallela e al massimo tre righe di testo.** Le spiegazioni aggiuntive lunghe scoraggiano la lettura e non devono essere necessarie.
-   **Usare le frasi complete e la punteggiatura finale.**

**Etichette del gruppo di collegamenti comando**

-   **Non usare etichette di gruppo.** Le istruzioni principali agiscono come etichetta di gruppo per i collegamenti ai comandi.

## <a name="documentation&quot;></a>Documentazione

Quando si fa riferimento a collegamenti comando:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, ma non includere il carattere di sottolineatura della chiave di accesso.
-   Se l'etichetta include un nome di oggetto, omettere il nome dell'oggetto o utilizzare un testo segnaposto.
-   Per descrivere l'interazione dell'utente, utilizzare fare clic su.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

**Esempi:** Per copiare l'immagine, fare clic su **copia e Sostituisci**.

Fare clic su **Reimposta scheda di rete**. (Per un collegamento a un comando denominato &quot;Reimposta il *nome* della scheda di rete").

 

