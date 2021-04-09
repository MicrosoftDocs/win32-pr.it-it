---
title: Caselle di ricerca
description: Con una casella di ricerca, gli utenti possono individuare rapidamente oggetti o testo specifici all'interno di un set di dati di grandi dimensioni filtrando o evidenziando corrispondenze.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9d1fca8fdb96b17098cee79fd5b62ecd7ab7531
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103968830"
---
# <a name="search-boxes"></a>Caselle di ricerca

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con una casella di ricerca, gli utenti possono individuare rapidamente oggetti o testo specifici all'interno di un set di dati di grandi dimensioni filtrando o evidenziando corrispondenze. Non esiste un controllo di ricerca standard, ma è necessario impegnarsi per rendere le funzionalità di ricerca del programma coerenti con quelle di Windows.

Esistono due tipi di ricerche:

-   **Ricerca immediata**, in cui i risultati vengono visualizzati immediatamente come tipi di utente. Non è necessario fare clic su un pulsante, quindi il simbolo di ricerca lente di ingrandimento viene visualizzato come grafico e non come pulsante.

    ![Screenshot che mostra una casella di ricerca immediata con un callout "prompt" che punta alla casella di ricerca e un callout di "simbolo di ricerca" che punta alla grafica della lente di ingrandimento.](images/ctrl-search-boxes-image1.png)

    Casella di ricerca tipica che usa la ricerca immediata. La ricerca viene eseguita automaticamente a ogni pressione di tasto.

-   **Ricerca regolare**, in cui viene eseguita una ricerca quando l'utente fa clic sul pulsante Cerca. Il simbolo di ricerca lente di ingrandimento viene visualizzato su un pulsante.

    ![Screenshot di una casella di ricerca normale ](images/ctrl-search-boxes-image2.png)

    Casella di ricerca tipica che usa la ricerca normale. Gli utenti fanno clic su un pulsante per eseguire la ricerca.

    È possibile specificare uno o entrambi i tipi di opzioni di ricerca per gli utenti.

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Sono oggetti specifici difficili da trovare?** Questa situazione può verificarsi quando:
    -   Sono presenti molti oggetti.
    -   Gli oggetti non si trovano in un'unica posizione. La ricerca è particolarmente utile per trovare oggetti negli alberi.
    -   I dati di ricerca sono difficili da trovare (ad esempio, i metadati).
-   **Gli utenti devono trovare testo specifico all'interno di documenti?**
-   **La funzionalità restituisce i risultati di ricerca pertinenti entro cinque secondi?** In caso contrario, è possibile fornire una funzionalità di ricerca, ma utilizzare una progettazione alternativa che fornisce feedback visibile per gestire ricerche con esecuzione prolungata, ad esempio una finestra di dialogo di ricerca.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

La ricerca è un primo passaggio cruciale in molti scenari: gli utenti devono trovare gli oggetti prima di poterli usare. Gli utenti stanno salvando più oggetti su dischi rigidi sempre più grandi, ma l'esplorazione degli oggetti non è adatta. La ricerca deve essere una parte semplice, coerente e affidabile dell'esperienza utente.

Caselle di ricerca in Windows:

-   Sono parte di tutte le finestre di esplorazione, quindi sono facili da trovare e riconoscere.
-   Hanno un aspetto e un comportamento coerenti.
-   Sono efficienti e veloci e offrono risultati istantanei in modalità di ricerca immediata.

Una casella di ricerca viene usata in Windows in queste posizioni:

-   Strumenti di esplorazione
-   Esperienze (Microsoft Windows Media Player, raccolta foto di Windows, Windows Internet Explorer)
-   Menu Start (per trovare i programmi e i file recenti)
-   Pannello di controllo home page (per trovare elementi e attività del pannello di controllo)
-   Guida (per trovare gli argomenti della guida pertinenti)

### <a name="look-and-feel"></a>Aspetto

L'aspetto della ricerca in Windows è notevolmente migliorato grazie al supporto della ricerca immediata. I risultati istantanei rendono Windows più potente e diretto.

In Esplora risorse e finestre delle applicazioni, la ricerca si trova nell'angolo in alto a destra se è un punto di ingresso supplementare. In questo caso, gli utenti cercano un meccanismo di ricerca quando non trovano ciò che cercano nella finestra. Tuttavia, se la ricerca è il punto di ingresso primario, viene centrata nella parte superiore della finestra.

Il pulsante Cerca è connesso visivamente a una casella di ricerca. Per ridurre al minimo lo spazio, viene usata una [richiesta](ctrl-text-boxes.md) facoltativa all'interno di una casella di ricerca invece che di un'etichetta. Il prompt può essere un'istruzione (ad esempio, digitare per eseguire la ricerca) o indicare l'ambito della ricerca (ad esempio, cercare immagini).

![Screenshot di una casella di ricerca immediata ](images/ctrl-search-boxes-image3.png)

Senza etichette e pulsanti distinti, la ricerca immediata in Windows presenta un aspetto leggero.

L'esecuzione di una ricerca riuscita crea una pagina virtuale dei risultati della ricerca e la aggiunge allo stack e alla barra degli indirizzi back. Gli utenti hanno diversi modi per ripristinare la pagina originale e deselezionare una casella di ricerca, incluso il clic indietro, fare clic sulla pagina originale nella barra degli indirizzi, premere ESC o deselezionare la casella di ricerca.

Inoltre, gli utenti possono semplicemente deselezionare la casella di ricerca senza ripristinare una pagina di risultati precedente. In modalità ricerca immediata viene visualizzato un pulsante Cancella dopo che l'utente inizia a digitare; una "x" sostituisce il simbolo di ricerca lente di ingrandimento. Al passaggio del mouse, la "x" Ottiene l'aspetto di un pulsante e può essere selezionato.

![Screenshot di una casella di ricerca con icona "x" ](images/ctrl-search-boxes-image4.png)

L'utente può deselezionare la casella di ricerca facendo clic su "x" all'estremità destra del controllo.

In modalità di ricerca regolare, il pulsante Cancella è facoltativo. Gli utenti possono risultare utili, ad esempio, se la ricerca richiede molto tempo per il completamento. Gli utenti possono fare clic sulla "x" per arrestare la ricerca in corso. Se una ricerca è già stata completata, gli utenti possono fare clic sulla "x" per deselezionare la casella di ricerca.

## <a name="guidelines"></a>Indicazioni

### <a name="location"></a>Location

-   Per le finestre delle applicazioni, individuare Cerca nell'angolo in alto a destra.
-   Per le finestre popup, individua la ricerca laddove è più sensata e comoda.
-   **Eccezione:** Se la ricerca è in genere la prima operazione eseguita dagli utenti in una finestra (il punto di ingresso primario), centrarla nella parte superiore della finestra.

### <a name="look"></a>Cercare

-   Usare il pulsante di ricerca standard graphics. Sono disponibili tre versioni:
    -   **Solo simbolo di ricerca lente di ingrandimento (nessun pulsante al passaggio del mouse).** Da usare per la ricerca immediata.
    -   **Simbolo di ricerca di ingrandimento vetro con pulsante.** Usare quando è necessario fare clic sul pulsante per avviare la ricerca.
    -   **Simbolo di ricerca lente di ingrandimento con pulsante e freccia a discesa.** Aggiungere una freccia a discesa quando gli utenti possono modificare l'ambito o quando sono disponibili altre impostazioni.
        -   Per la ricerca immediata, usare solo una freccia a discesa e visualizzare un pulsante al passaggio del mouse.
        -   Per la ricerca regolare, visualizzare la freccia a discesa di un pulsante.

![Figura delle caselle di ricerca immediata in Stati diversi ](images/ctrl-search-boxes-image5.png)

Specifiche visive per la ricerca immediata.

![Figura delle caselle di ricerca normali in Stati diversi ](images/ctrl-search-boxes-image6.png)

Specifiche visive per la ricerca normale.

-   Non usare un'etichetta; usare invece una richiesta facoltativa. Se gli utenti tendono a presupporre che la ricerca sia una ricerca di file generica, utilizzare la richiesta per assegnare l'ambito. In caso contrario, utilizzare il tipo per la ricerca o una frase concisa simile.

    ![screenshot del prompt ' tipo da cercare ' ](images/ctrl-search-boxes-image7.png)

    ![screenshot del prompt ' Cerca tutti i gadget ' ](images/ctrl-search-boxes-image8.png)

    In questi esempi, brevi messaggi di richiesta testuale consentono agli utenti di lavorare con la ricerca.

### <a name="interaction"></a>Interazione

-   **In stato attivo per l'input selezionare automaticamente eventuali testo immesso in precedenza.** Questa operazione consente agli utenti di immettere una nuova ricerca digitando o di modificare la ricerca precedente posizionando il punto di inserimento usando i tasti di direzione.

    ![screenshot della casella di ricerca con il testo evidenziato ](images/ctrl-search-boxes-image9.png)

    In questo esempio, il testo immesso in precedenza è selezionato per lo stato attivo per l'input.

-   **Assegnare il tasto di scelta rapida per la casella di ricerca a CTRL + E.**

### <a name="functionality"></a>Funzionalità

-   **Supporta la ricerca immediata quando possibile.** Fornire le ricerche sia regolari che immediate se sono presenti scenari in cui la ricerca regolare vale il tempo di attesa aggiuntivo.
-   Le ricerche regolari devono restituire risultati rilevanti entro cinque secondi e la ricerca immediata deve restituire risultati entro due secondi. A questo punto, la ricerca può continuare a compilare risultati meno rilevanti nel tempo, purché il programma sia reattivo e gli utenti possano eseguire altre attività. Potrebbe essere necessario indicizzare i dati di ricerca per garantire la velocità di risposta.
-   Se si forniscono modalità di ricerca sia regolari che immediate, i risultati della ricerca immediata devono essere un subset dei normali risultati della ricerca.
-   Tutte le ricerche sono basate su prefisso (nessuna ricerca di sottostringa o suffisso). L'utilizzo di caratteri jolly finali è facoltativo e non influisce sui risultati. Se vengono immesse più parole, utilizzare o eseguire ricerche.
-   Una ricerca riuscita consente di aggiungere una pagina virtuale con i risultati della ricerca allo stack indietro e alla barra degli indirizzi. Più ricerche generano una singola pagina virtuale, quindi fare clic su indietro restituisce sempre la pagina originale.
-   Se necessario per la scalabilità, classificare i risultati della ricerca in base alla pertinenza.
-   Una ricerca vuota restituisce la pagina originale.

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![Figura di ridimensionamento e spaziatura della casella di ricerca immediata ](images/ctrl-search-boxes-image10.png)

Dimensionamento e spaziatura consigliati per la ricerca immediata.

![Figura del ridimensionamento e della spaziatura normali della casella di ricerca ](images/ctrl-search-boxes-image11.png)

Dimensionamento e spaziatura consigliati per la ricerca periodica.

## <a name="text"></a>Testo

-   Per la formulazione del messaggio di richiesta nella casella di ricerca, impostarla come istruzione (ad esempio, digitare per eseguire la ricerca) o indicare l'ambito della ricerca (ad esempio, cercare immagini).
-   Il testo della richiesta dovrebbe essere breve. È sufficiente una singola parola o una breve frase.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare la punteggiatura finale o i puntini di sospensione.

## <a name="documentation"></a>Documentazione

-   Fare riferimento a questo controllo come casella di ricerca. Capitalizzare la lettera iniziale della prima parola; non capitalizzare la lettera iniziale di box.
-   Vedere i due tipi di ricerca come ricerca immediata e ricerca normale. Capitalizzare la lettera iniziale della ricerca immediata; non capitalizzare la lettera iniziale della ricerca normale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 