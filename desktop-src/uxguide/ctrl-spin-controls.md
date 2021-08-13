---
title: Controlli di spin
description: Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare in modo incrementale il valore all'interno della casella di testo numerica associata.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b97f5acc8a3f904df3a868274356e5337f5cc9280a5eed81693d92ce9bf9a37c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118217397"
---
# <a name="spin-controls"></a>Controlli di spin

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare in modo incrementale il valore all'interno della casella [di testo numerica associata.](ctrl-text-boxes.md) Il termine casella di selezione si riferisce alla combinazione di una casella di testo e del controllo di selezione associato.

![Screenshot del controllo selezione e della casella di testo ](images/ctrl-spin-controls-image1.png)

Casella di selezione tipica.

Gli utenti preferiscono spesso i controlli di selezione perché possono apportare modifiche senza spostare le mani dal mouse. Quando il controllo di selezione è associato a una casella di testo, gli utenti possono digitare o incollare l'input direttamente nella casella di testo, quindi l'uso del controllo di selezione è facoltativo.

Mentre i controlli di selezione vengono usati per l'input numerico, l'input non deve essere un numero intero puro. L'input può essere numeri decimali e può avere segni negativi, delimitatori (ad esempio due punti o trattini) e modificatori di unità.

> [!Note]  
> Le linee guida relative [alle caselle di](ctrl-text-boxes.md) testo [e al layout](vis-layout.md) sono presentate in articoli separati.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo viene usato per l'input numerico?** In caso contrario, usare un altro controllo, ad esempio [un](/windows/desktop/uxguide/ctrl-drop) elenco a discesa o un dispositivo di scorrimento, [](ctrl-sliders.md)per eseguire la selezione da un set fisso di valori. Usare le barre di scorrimento per lo scorrimento.
-   **Gli utenti possono pensare al valore come a una quantità relativa, non a un valore numerico?** In caso contrario, usare un dispositivo di scorrimento. Usare le caselle di selezione solo per valori numerici esatti e noti. Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.
-   **Il controllo è associato a una casella di testo?** In caso contrario, non usare . I controlli di selezione non devono essere usati da soli o con altri tipi di controlli oltre a una casella di testo.

    **Non corretto:**

    ![Screenshot del controllo di selezione, immagine, nessuna casella di testo ](images/ctrl-spin-controls-image2.png)

    In questo esempio viene usato un controllo di selezione per controllare un elemento grafico dinamico.

-   **Gli intervalli di valori contigui sono validi?** In caso contrario, usare un elenco a discesa di valori validi.

    ![Screenshot dell'elenco a discesa ](images/ctrl-spin-controls-image3.png)

    In questo esempio non tutti i numeri di unità disco sono validi, quindi un elenco a discesa è una scelta migliore.

-   **L'uso del controllo di selezione è pratico?** L'uso di un controllo di selezione è pratico per:

    -   Immissione di un numero ridotto, in genere inferiore a 100.
    -   Apportare piccole modifiche a un valore esistente o predefinito.

    Sebbene i controlli di selezione possano essere usati per qualsiasi input numerico, sono inefficienti in situazioni diverse da queste.

-   **Il controllo di selezione è utile?** Il controllo viene usato in un contesto in cui è probabile che gli utenti utilizzino il mouse? In caso contrario, considerare un controllo di selezione facoltativo.
-   **Gli elenchi a discesa dei controlli di pari livello sono?** Se sono presenti altri elenchi a discesa, è consigliabile usare un elenco a discesa per la coerenza.

    ![Screenshot della finestra di dialogo con elenchi a discesa ](images/ctrl-spin-controls-image4.png)

    In questo esempio è possibile usare una casella di selezione, ma per coerenza viene usato un elenco a discesa.

-   **Gli utenti con tocco o penna sono una destinazione primaria?** In tal caso, è consigliabile usare un elenco a discesa. I pulsanti freccia in un controllo di selezione sono troppo piccoli per essere usati in modo efficiente con il tocco o una penna.

Se è possibile usare un dispositivo di scorrimento o una casella di selezione, usare una casella di selezione se:

-   Lo spazio sullo schermo è limitato.
-   È probabile che un utente preferisca usare la tastiera.

Usa un dispositivo di scorrimento se:

-   Gli utenti trarranno vantaggio da un riscontro immediato.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Usare i controlli di selezione ogni volta che sono pratici e utili.** Vedere [È il controllo giusto?](#is-this-the-right-control)

    -   **Eccezione:** Per essere coerenti con altre caselle di testo nella stessa interfaccia utente, usare i controlli di selezione anche se non sono sempre pratici.

    **Corretto:**

    ![Screenshot dei controlli di selezione mese, giorno e anno ](images/ctrl-spin-controls-image5.png)

    In questo esempio, un controllo di selezione viene usato con il controllo year per garantire la coerenza, anche se non è sempre pratico.

    **Non corretto:**

    ![Screenshot del controllo di selezione dell'indirizzo IP ](images/ctrl-spin-controls-image6.png)

    In questo esempio, il controllo di selezione è inutilizzabile.

-   **Creare sempre un controllo di selezione come "amico" della casella di testo.** In questo modo, il controllo di selezione viene posto all'interno della casella di testo.

    **Corretto:**

    ![Screenshot del controllo di selezione posizionato all'interno di una casella di testo ](images/ctrl-spin-controls-image7.png)

    **Non corretto:**

    ![Screenshot del controllo di selezione posizionato all'esterno della casella di testo ](images/ctrl-spin-controls-image8.png)

    Nell'esempio corretto, il controllo di selezione viene inserito all'interno della casella di testo associata.

-   **Disabilitare un controllo di selezione quando la casella di testo associata è disabilitata.** Il controllo di selezione è un metodo di input supplementare, mai l'unico metodo di input.

### <a name="values"></a>Valori

-   **Definire il pulsante superiore per aumentare il valore di un'unità e il pulsante inferiore per diminuire di un'unità.** In genere, l'unità è una, ma deve essere la più piccola modifica comune nel valore. Idealmente, il controllo di selezione deve coprire tutti i valori validi e dovrebbe essere più comodo che digitare il testo.

    ![Screenshot del controllo di selezione dei "margini" ](images/ctrl-spin-controls-image9.png)

    In questo esempio, facendo clic su un controllo di selezione, i valori vengono 0,1, ovvero la più piccola modifica comune nel valore. L'uso di un'unità più piccola copre l'intervallo di valori validi, ma rende inutilizzabili i controlli di selezione.

-   **Usare il controllo spin per limitare l'input ai valori validi.** L'uso di un controllo di selezione non dovrebbe mai comportare un valore non corretto.
-   **Alla fine di un intervallo di valori validi, riavviare l'intervallo.** La metafora del controllo di rotazione è che l'utente ruota una ruota di valori, quindi questo comportamento simile alla ruota.
    -   **Eccezione:** Non riavviare l'intervallo se il valore risultante non è corretto.

        ![Screenshot del controllo di selezione "numero di copie" ](images/ctrl-spin-controls-image10.png)

        In questo esempio, facendo clic sul pulsante freccia giù non viene riavviato l'intervallo (andando al valore massimo) perché tale valore non è certo corretto.

-   **Usare testo anziché valori numerici speciali.** Consentire agli utenti di selezionare questi valori speciali invece di doverli conoscere e digitare.

    ![Screenshot del controllo di selezione "Sospensione dopo (mai)" ](images/ctrl-spin-controls-image11.png)

    In questo esempio Non è mai un valore speciale, ma gli utenti possono eseguire lo spin su di esso.

-   **Se il valore contiene delimitatori, la casella di testo associata deve avere più punti di attivazione dell'input.** In questo modo i segmenti numerici possono essere manipolati singolarmente.

    ![Screenshot del controllo di selezione tempo, minuti selezionati ](images/ctrl-spin-controls-image12.png)

    In questo esempio, il controllo di selezione influisce sui valori per ore, minuti, secondi e A.M./P.M., a seconda di quale sia lo stato attivo.

-   **Se il valore ha unità, usare il controllo di selezione per modificare anche queste unità.**

    ![Screenshot del controllo di selezione temporale, 'a.m.' selezionato ](images/ctrl-spin-controls-image13.png)

    In questo esempio, il controllo spin può essere usato per modificare le unità.

## <a name="labels"></a>Etichette

-   Applicare le linee [guida per l'etichettatura delle caselle](ctrl-text-boxes.md) di testo per etichettare la casella di testo associata. I controlli di selezione non vengono mai etichettati direttamente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai controlli di selezione:

-   Non fare riferimento ai controlli di selezione nella documentazione dell'utente. Fare invece riferimento all'etichetta della casella di testo associata.
-   Fare riferimento ai controlli di selezione e alle caselle di selezione solo nella programmazione e in altri documenti tecnici.

Esempio: nella **casella Data** digitare o selezionare la parte della data da modificare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 