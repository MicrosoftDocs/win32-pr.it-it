---
title: Caselle di ricerca
description: Con una casella di ricerca, gli utenti possono individuare rapidamente oggetti o testo specifici all'interno di un set di dati di grandi dimensioni filtrando o evidenziando le corrispondenze.
ms.assetid: e2d77b36-e001-403c-9b66-2d136c394a24
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 71e0ce45e2fd0b84b0abda9462f2cb42c945790e93ea06e7dfc6ece0f65ffd65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842985"
---
# <a name="search-boxes"></a>Caselle di ricerca

> [!NOTE]
> Questa guida di progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con una casella di ricerca, gli utenti possono individuare rapidamente oggetti o testo specifici all'interno di un set di dati di grandi dimensioni filtrando o evidenziando le corrispondenze. Non esiste alcun controllo di ricerca standard, ma è consigliabile cercare di rendere coerenti le funzionalità di ricerca del programma con quelle Windows.

Esistono due tipi di ricerche:

-   **Ricerca immediata,** in cui i risultati vengono visualizzati immediatamente durante la di tipistica dell'utente. Non è necessario fare clic su alcun pulsante, quindi il simbolo di ricerca della lente di ingrandimento viene visualizzato come elemento grafico, non come pulsante.

    ![Screenshot che mostra una casella di ricerca immediata con un callout "Prompt" che punta alla casella di ricerca e un callout "Simbolo di ricerca" che punta alla lente di ingrandimento.](images/ctrl-search-boxes-image1.png)

    Casella di ricerca tipica con Ricerca immediata. La ricerca viene eseguita automaticamente a ogni pressione di tasto.

-   **Ricerca regolare,** in cui viene eseguita una ricerca quando l'utente fa clic sul pulsante di ricerca. Il simbolo di ricerca della lente di ingrandimento viene visualizzato su un pulsante.

    ![Screenshot di una casella di ricerca normale ](images/ctrl-search-boxes-image2.png)

    Casella di ricerca tipica che usa la ricerca normale. Gli utenti fare clic su un pulsante per eseguire la ricerca.

    È possibile fornire uno o entrambi i tipi di opzioni di ricerca per gli utenti.

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **È difficile trovare oggetti specifici?** Questa situazione può verificarsi quando:
    -   Sono disponibili molti oggetti.
    -   Gli oggetti non si trovano in un'unica posizione. La ricerca è particolarmente utile per la ricerca di oggetti negli alberi.
    -   I dati di ricerca sono difficili da trovare, ad esempio i metadati.
-   **Gli utenti devono trovare testo specifico all'interno dei documenti?**
-   **La funzionalità restituisce risultati di ricerca pertinenti entro cinque secondi?** In caso contrario, è possibile fornire una funzionalità di ricerca, ma usare una progettazione alternativa che fornisce feedback visibile per supportare ricerche con esecuzione di lunga durata, ad esempio una finestra di dialogo di ricerca.

## <a name="design-concepts"></a>Concetti relativi alla progettazione

La ricerca è un primo passaggio fondamentale in molti scenari: gli utenti devono trovare gli oggetti prima di poterli usare. Gli utenti salvano sempre più oggetti su dischi rigidi sempre più grandi, ma la ricerca di oggetti non è scalabile bene. La ricerca deve essere una parte semplice, coerente e affidabile dell'esperienza utente.

Caselle di ricerca Windows:

-   Fanno parte di tutte le finestre di Explorer, quindi sono facili da trovare e riconoscere.
-   Hanno un aspetto e un comportamento coerenti.
-   Sono efficienti e veloci, offrendo risultati immediati in modalità di ricerca immediata.

Una casella di ricerca viene usata in Windows in queste posizioni:

-   Strumenti di esplorazione
-   Esperienze (Microsoft Windows Media Player, Windows Raccolta foto, Windows Internet Explorer)
-   menu Start (per trovare programmi e file recenti)
-   Pannello di controllo home page (per trovare attività e elementi del Pannello di controllo)
-   Guida (per trovare gli argomenti della Guida pertinenti)

### <a name="look-and-feel"></a>Aspetto

L'aspetto della ricerca Windows è notevolmente migliorato grazie al supporto della ricerca immediata. La presenza di risultati immediati Windows è più potente e diretta.

In Windows explorer e nelle finestre dell'applicazione, La ricerca si trova nell'angolo superiore destro se si tratta di un punto di ingresso supplementare. In questo caso, gli utenti cercano un meccanismo di ricerca quando non trovano ciò che cercano nella finestra. Tuttavia, se Search è il punto di ingresso principale, viene centrato nella parte superiore della finestra.

Il pulsante Cerca è connesso visivamente a una casella di ricerca. Per ridurre al minimo lo spazio, [viene usato un prompt](ctrl-text-boxes.md) facoltativo all'interno di una casella di ricerca anziché di un'etichetta. Il prompt può essere un'istruzione (ad esempio, Digitare per la ricerca) o indicare l'ambito della ricerca (ad esempio, Cerca immagini).

![screenshot di una casella di ricerca immediata ](images/ctrl-search-boxes-image3.png)

Senza etichette e pulsanti separati, la ricerca immediata Windows ha un aspetto leggero.

L'esecuzione di una ricerca corretta crea una pagina virtuale dei risultati della ricerca e la aggiunge alla barra degli indirizzi e dello stack Indietro. Gli utenti possono ripristinare la pagina originale in diversi modi e deselezionare una casella di ricerca, ad esempio facendo clic su Indietro, facendo clic sulla pagina originale nella barra degli indirizzi, premendo ESC o deselezionando la casella di ricerca.

Gli utenti possono anche semplicemente deselezionare la casella di ricerca senza ripristinare una pagina di risultati precedente. In modalità di ricerca immediata viene visualizzato un pulsante cancella dopo che l'utente inizia a digitare. una "x" sostituisce il simbolo di ricerca della lente di ingrandimento. Al passaggio del mouse, la "x" ottiene l'aspetto di un pulsante e può essere selezionato.

![Screenshot di una casella di ricerca con l'icona "x" ](images/ctrl-search-boxes-image4.png)

L'utente può cancellare la casella di ricerca facendo clic su "x" all'estremità destra del controllo.

In modalità di ricerca normale, il pulsante cancella è facoltativo. Gli utenti possono trovarlo utile, ad esempio, se il completamento di una ricerca sta richiedere molto tempo. Gli utenti possono fare clic sulla "x" per arrestare la ricerca in corso. Se una ricerca è già stata completata, gli utenti possono fare clic sulla "x" per deselezionare la casella di ricerca.

## <a name="guidelines"></a>Indicazioni

### <a name="location"></a>Località

-   Per le finestre dell'applicazione, individuare Cerca nell'angolo in alto a destra.
-   Per le finestre popup, individuare Cerca ovunque sia più ragionevole e pratico.
-   **Eccezione:** Se la ricerca è in genere la prima operazione che gli utenti ese trovano in una finestra (il punto di ingresso principale), centrarla nella parte superiore della finestra.

### <a name="look"></a>Guardare

-   Usare la grafica standard del pulsante di ricerca. Sono disponibili tre versioni:
    -   **Solo simbolo di ricerca della lente di ingrandimento (nessun pulsante al passaggio del mouse).** Usare per la ricerca immediata.
    -   **Simbolo di ricerca della lente di ingrandimento con il pulsante .** Usare quando è necessario fare clic sul pulsante per avviare la ricerca.
    -   **Simbolo di ricerca della lente di ingrandimento con pulsante e freccia a discesa.** Aggiungere una freccia a discesa quando gli utenti possono modificare l'ambito o quando sono disponibili altre impostazioni.
        -   Per Ricerca immediata, usare solo una freccia a discesa e visualizzare un pulsante al passaggio del mouse.
        -   Per la ricerca normale, visualizzare la freccia a discesa su un pulsante.

![figura delle caselle di ricerca immediata in stati diversi ](images/ctrl-search-boxes-image5.png)

Specifiche visive per la ricerca immediata.

![figura delle normali caselle di ricerca in stati diversi ](images/ctrl-search-boxes-image6.png)

Specifiche visive per la ricerca regolare.

-   Non usare un'etichetta. usare invece un prompt facoltativo. Se gli utenti tendono a presupporre che la ricerca sia una ricerca di file generica, usare il prompt per assegnare l'ambito. In caso contrario, usare Il tipo per cercare o una frase concisa simile.

    ![Screenshot del prompt 'type to search' ](images/ctrl-search-boxes-image7.png)

    ![screenshot del prompt "cerca tutti i file" ](images/ctrl-search-boxes-image8.png)

    In questi esempi, brevi richieste testuali consentono agli utenti di usare la ricerca.

### <a name="interaction"></a>Interazione

-   **Sullo stato attivo per l'input, selezionare automaticamente qualsiasi testo immesso in precedenza.** In questo modo gli utenti possono immettere una nuova ricerca digitando o modificare la ricerca precedente posizionando il cursore usando i tasti di direzione.

    ![Screenshot della casella di ricerca con il testo evidenziato ](images/ctrl-search-boxes-image9.png)

    In questo esempio, il testo immesso in precedenza viene selezionato sullo stato attivo per l'input.

-   **Assegnare alla casella di ricerca la combinazione di tasti CTRL+E.**

### <a name="functionality"></a>Funzionalità

-   **Supporto della ricerca immediata quando possibile.** Fornire sia ricerche regolari che istantanee se in alcuni scenari la ricerca regolare vale il tempo di attesa aggiuntivo.
-   Le ricerche regolari devono restituire risultati rilevanti entro cinque secondi e ricerca immediata deve restituire risultati entro due secondi. Dopo questo punto, la ricerca può continuare a compilare risultati meno rilevanti nel tempo, purché il programma sia reattivo e gli utenti possano eseguire altre attività. Potrebbe essere necessario indicizzare i dati di ricerca per garantire questa velocità di risposta.
-   Se si specificano entrambe le modalità di ricerca normale e immediata, i risultati della ricerca immediata devono essere un subset dei risultati della ricerca normale.
-   Tutte le ricerche sono basate sul prefisso (nessuna ricerca di sottostringhe o suffissi). L'uso di caratteri jolly finali è facoltativo e non influisce sui risultati. Se vengono immesse più parole, usare la ricerca OR.
-   Una ricerca riuscita aggiunge una pagina virtuale con i risultati della ricerca nello stack Indietro e nella barra degli indirizzi. Più ricerche comportano una singola pagina virtuale, quindi facendo clic su Indietro viene sempre restituita la pagina originale.
-   Se necessario per la scalabilità, classificare i risultati della ricerca in base alla pertinenza.
-   Una ricerca vuota restituisce la pagina originale.

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![figura del ridimensionamento e della spaziatura della casella di ricerca immediata ](images/ctrl-search-boxes-image10.png)

Dimensioni e spaziatura consigliate per Ricerca immediata.

![Figura del ridimensionamento e della spaziatura normali della casella di ricerca ](images/ctrl-search-boxes-image11.png)

Dimensioni e spaziatura consigliate per la ricerca regolare.

## <a name="text"></a>Testo

-   Per la formulazione del prompt nella casella Di ricerca, impostarlo come istruzione (ad esempio, Digitare per cercare) o indicare l'ambito della ricerca ,ad esempio Cerca immagini.
-   Il testo della richiesta deve essere breve. Deve essere sufficiente una singola parola o frase breve.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non usare la punteggiatura finale o i puntini di sospensione.

## <a name="documentation"></a>Documentazione

-   Fare riferimento a questo controllo come casella di ricerca. In maiuscolo la lettera iniziale della prima parola; non in maiuscolo la lettera iniziale della casella.
-   Fare riferimento ai due tipi di ricerca come Ricerca immediata e Ricerca normale. In maiuscolo la lettera iniziale di Ricerca immediata; non convertire in maiuscolo la lettera iniziale della ricerca regolare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 