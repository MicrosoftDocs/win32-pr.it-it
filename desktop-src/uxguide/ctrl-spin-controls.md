---
title: Controlli di selezione
description: Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare il valore in modo incrementale all'interno della casella di testo numerica associata.
ms.assetid: 5f791fb9-1354-41b9-a9de-ddab35302d50
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 54ce622983e52d65fa58ef05aca783ff67ebce66
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351101"
---
# <a name="spin-controls"></a>Controlli di selezione

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un controllo di selezione, gli utenti possono fare clic sui pulsanti freccia per modificare il valore in modo incrementale all'interno della [casella di testo numerica](ctrl-text-boxes.md)associata. Il termine casella di selezione si riferisce alla combinazione di una casella di testo e del controllo di selezione associato.

![screenshot del controllo di selezione e della casella di testo ](images/ctrl-spin-controls-image1.png)

Casella di selezione tipica.

Spesso gli utenti preferiscono i controlli spin, perché possono apportare modifiche senza trasferire le mani dal mouse. Quando il controllo di selezione è associato a una casella di testo, gli utenti possono digitare o incollare input direttamente nella casella di testo, in modo che l'uso del controllo di selezione sia facoltativo.

Mentre i controlli di selezione vengono usati per l'input numerico, l'input non deve essere un numero intero puro. L'input può essere costituito da numeri decimali e può presentare segni negativi, delimitatori (ad esempio, due punti o trattini) e modificatori di unità.

> [!Note]  
> Le linee guida correlate alle [caselle di testo](ctrl-text-boxes.md) e al [layout](vis-layout.md) sono presentate in articoli distinti.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Per decidere, prendi in considerazione queste domande:

-   **Il controllo è utilizzato per l'input numerico?** In caso contrario, utilizzare un altro controllo, ad esempio un [elenco a discesa](/windows/desktop/uxguide/ctrl-drop) o un [dispositivo di scorrimento](ctrl-sliders.md), per effettuare una selezione da un set fisso di valori. Utilizzare le barre di scorrimento per lo scorrimento.
-   **Gli utenti considerano il valore come una quantità relativa, non un valore numerico?** In caso affermativo, usare invece un dispositivo di scorrimento. Usare le caselle di selezione solo per i valori numerici esatti e noti. Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.
-   **Il controllo è associato a una casella di testo?** In caso contrario, non usare. I controlli di selezione non devono essere usati da solo o con altri tipi di controlli oltre a una casella di testo.

    **Non corretto:**

    ![screenshot del controllo di selezione, immagine, nessuna casella di testo ](images/ctrl-spin-controls-image2.png)

    In questo esempio viene usato un controllo di selezione per controllare un'immagine dinamica.

-   **Gli intervalli di valori contigui sono validi?** In caso contrario, usare invece un elenco a discesa di valori validi.

    ![screenshot dell'elenco a discesa ](images/ctrl-spin-controls-image3.png)

    In questo esempio, non tutti i numeri di unità disco sono validi, quindi un elenco a discesa rappresenta una scelta migliore.

-   **È possibile utilizzare il controllo di selezione?** L'uso di un controllo di selezione è utile per:

    -   Immissione di un numero ridotto, in genere inferiore a 100.
    -   Apportare piccole modifiche a un valore predefinito o esistente.

    Sebbene i controlli di selezione possano essere usati per qualsiasi input numerico, sono inefficienti in situazioni diverse da queste.

-   **Il controllo di selezione è utile?** Il controllo viene utilizzato in un contesto in cui è probabile che gli utenti utilizzino il mouse? In caso contrario, prendere in considerazione un controllo di selezione facoltativo.
-   **Gli elenchi a discesa dei controlli di pari livello?** Se sono presenti altri elenchi a discesa, provare a usare un elenco a discesa per verificarne la coerenza.

    ![screenshot della finestra di dialogo con elenchi a discesa ](images/ctrl-spin-controls-image4.png)

    In questo esempio è possibile usare una casella di selezione, ma per coerenza viene usato un elenco a discesa.

-   **Gli utenti di touch o Pen sono una destinazione primaria?** In tal caso, prendere in considerazione l'uso di un elenco a discesa. I pulsanti freccia in un controllo di selezione sono troppo piccoli per essere usati in modo efficiente con il tocco o con una penna.

Se è possibile un dispositivo di scorrimento o una casella di selezione, utilizzare una casella di selezione se:

-   Lo spazio sullo schermo è limitato.
-   È probabile che un utente preferisca utilizzare la tastiera.

Usa un dispositivo di scorrimento se:

-   Gli utenti trarranno vantaggio da un riscontro immediato.

## <a name="guidelines"></a>Indicazioni

### <a name="general"></a>Generale

-   **Usare i controlli di selezione ogni volta che sono pratici e utili.** Vedere qual [è il controllo corretto?](#is-this-the-right-control)

    -   **Eccezione:** Per coerenza con altre caselle di testo nella stessa interfaccia utente, usare i controlli di selezione anche se non sono sempre pratici.

    **Corretto:**

    ![screenshot dei controlli di selezione mese, giorno e anno ](images/ctrl-spin-controls-image5.png)

    In questo esempio viene usato un controllo di selezione con il controllo Year per la coerenza, anche se non è sempre pratico.

    **Non corretto:**

    ![screenshot del controllo di selezione degli indirizzi IP ](images/ctrl-spin-controls-image6.png)

    In questo esempio, il controllo di selezione è inutilizzabile.

-   **Creare sempre un controllo di rotazione per "Buddy" della casella di testo.** Questa operazione posiziona il controllo di selezione all'interno della casella di testo.

    **Corretto:**

    ![screenshot del controllo di selezione inserito nella casella di testo ](images/ctrl-spin-controls-image7.png)

    **Non corretto:**

    ![cattura di schermata del controllo di selezione inserito all'esterno della casella di testo ](images/ctrl-spin-controls-image8.png)

    Nell'esempio corretto, il controllo di selezione viene inserito all'interno della casella di testo associata.

-   **Disabilitare un controllo di selezione quando la casella di testo associata è disabilitata.** Il controllo di selezione è un metodo di input supplementare, mai l'unico metodo di input.

### <a name="values"></a>Valori

-   **Definire il pulsante superiore per aumentare il valore di un'unità e il pulsante inferiore per ridurla di un'unità.** In genere, l'unità è uno, ma deve essere la più piccola modifica comune nel valore. Idealmente, il controllo di selezione dovrebbe coprire tutti i valori validi e dovrebbe essere più pratico rispetto alla digitazione del testo.

    ![screenshot del controllo di selezione dei margini ](images/ctrl-spin-controls-image9.png)

    In questo esempio, se si fa clic su un controllo di selezione, i valori vengono modificati in base a 1, che è la più piccola modifica comune nel valore. L'uso di un'unità di dimensioni inferiori coprirebbe l'intervallo di valori validi, ma renderebbe inutilizzabili i controlli di rotazione.

-   **Usare il controllo di selezione per limitare l'input ai valori validi.** L'uso di un controllo di selezione non dovrebbe mai produrre un valore non corretto.
-   **Alla fine di un intervallo di valori validi, riavviare l'intervallo.** La metafora del controllo spin è che l'utente sta ruotando una rotellina di valori, quindi questo comportamento simile alla rotellina.
    -   **Eccezione:** Non riavviare l'intervallo se il valore risultante è certo che non è corretto.

        ![screenshot del controllo di selezione ' numero di copie ' ](images/ctrl-spin-controls-image10.png)

        In questo esempio, facendo clic sul pulsante freccia giù non viene riavviato l'intervallo (passando al valore massimo), perché tale valore è certo che non è corretto.

-   **Usare il testo anziché i valori numerici speciali.** Consentire agli utenti di passare a questi valori speciali invece di conoscerli e digitarli.

    ![screenshot del controllo di selezione ' sospensione dopo (mai)' ](images/ctrl-spin-controls-image11.png)

    In questo esempio, non è mai un valore speciale, ma gli utenti possono eseguire la rotazione.

-   **Se il valore contiene delimitatori, nella casella di testo associata devono essere presenti più punti di interesse per l'input.** In questo modo è possibile modificare i segmenti numerici singolarmente.

    ![cattura di schermata del controllo di selezione ora, minuti selezionati ](images/ctrl-spin-controls-image12.png)

    In questo esempio, il controllo di selezione influiscono sui valori per hours, minutes, seconds e A.M./P.M., a seconda di quale sia lo stato attivo.

-   **Se il valore è costituito da unità, usare il controllo di selezione per modificare anche tali unità.**

    ![cattura di schermata del controllo di selezione ora,' a.m.' selezionato ](images/ctrl-spin-controls-image13.png)

    In questo esempio, il controllo di selezione può essere usato per modificare le unità.

## <a name="labels"></a>Etichette

-   Applicare le linee guida per l' [etichettatura della casella di testo](ctrl-text-boxes.md) per etichettare la casella di testo associata. I controlli di selezione non vengono mai etichettati direttamente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai controlli di selezione:

-   Non fare riferimento ai controlli di selezione nella documentazione dell'utente. Al contrario, fare riferimento all'etichetta della casella di testo associata.
-   Vedere controlli di selezione e caselle di selezione solo nella programmazione e in altri documenti tecnici.

Esempio: nella casella **Data** Digitare o selezionare la parte della data che si desidera modificare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 