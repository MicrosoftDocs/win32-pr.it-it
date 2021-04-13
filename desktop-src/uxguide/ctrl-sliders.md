---
title: Dispositivi di scorrimento (nozioni di base sulla progettazione)
description: Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7ff9791ab49c338e4c11e014a3e996771571add9
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104555191"
---
# <a name="sliders-design-basics"></a>Dispositivi di scorrimento (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori. Un dispositivo di scorrimento ha una barra che mostra l'intervallo e un indicatore che mostra il valore corrente. I segni di graduazione facoltativi mostrano i valori.

![figura che Mostra barra, dispositivo di scorrimento e segni di graduazione ](images/ctrl-sliders-image1.png)

Un dispositivo di scorrimento tipico.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Utilizzare un dispositivo di scorrimento quando si desidera che gli utenti siano in grado di **impostare valori contigui definiti, ad esempio volume o luminosità, oppure un intervallo di valori discreti, ad esempio le impostazioni di risoluzione dello schermo.**

Un dispositivo di scorrimento è una buona scelta quando sai che gli utenti considerano il valore una quantità relativa e non un valore numerico. Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.

Per decidere, prendi in considerazione queste domande:

-   **L'impostazione sembra una quantità relativa?** In caso contrario, utilizzare [pulsanti di opzione](ctrl-radio-buttons.md)o un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) o a [selezione singola](ctrl-list-boxes.md).
-   **L'impostazione è un valore numerico noto esatto?** In tal caso, utilizzare una [casella di testo numerica](ctrl-text-boxes.md).
-   **Un utente trarrebbe vantaggio da un riscontro immediato sull'effetto delle modifiche dell'impostazione?** Se sì, usa un dispositivo di scorrimento. Gli utenti possono ad esempio scegliere più facilmente un colore esaminando immediatamente l'effetto delle modifiche dei valori di tonalità, saturazione o luminosità.
-   **L'impostazione ha un intervallo di quattro o più valori?** In caso contrario, usa pulsanti di opzione.
-   **L'utente può modificare il valore?** I dispositivi di scorrimento consentono l'interazione dell'utente. Se un utente non può modificare il valore, usare invece una casella di [testo](ctrl-text-boxes.md) di sola lettura.

Se è possibile un dispositivo di scorrimento o una casella di testo numerica, utilizzare una casella di testo numerica se:

-   Lo spazio sullo schermo è limitato.
-   È probabile che un utente preferisca utilizzare la tastiera.

Usa un dispositivo di scorrimento se:

-   Gli utenti trarranno vantaggio da un riscontro immediato.

## <a name="guidelines"></a>Indicazioni

-   **Usa un orientamento naturale.** Ad esempio, se il dispositivo di scorrimento rappresenta un valore reale indicato di solito in verticale (come la temperatura), usa un orientamento verticale.
-   **Orientare il dispositivo di scorrimento in modo da riflettere le impostazioni cultura degli utenti.** Ad esempio, le impostazioni cultura occidentali sono lette da sinistra a destra, quindi per i dispositivi di scorrimento orizzontali posizionare la parte inferiore dell'intervallo a sinistra e l'estremità superiore a destra. Per le impostazioni cultura che leggono da destra a sinistra, eseguire l'operazione opposta.
-   **Ridimensionare il controllo in modo che un utente possa facilmente impostare il valore desiderato.** Per le impostazioni con valori discreti, assicurati che l'utente possa selezionare agevolmente i valori con il mouse.
-   **Si consiglia di usare una scala non lineare se l'intervallo di valori è elevato e gli utenti possono selezionare i valori in un'estremità dell'intervallo.** Ad esempio, il valore di ora può essere 1 minuto, 1 ora, 1 giorno o 1 mese.
-   **Quando si pratica, è possibile fornire commenti e suggerimenti immediatamente durante o dopo la selezione di un utente.** Il controllo del volume di Microsoft Windows, ad esempio, emette un segnale acustico per indicare il volume audio risultante.
-   **Usa etichette per indicare l'intervallo di valori.**

    **Eccezione:** Se il dispositivo di scorrimento è orientato verticalmente e l'etichetta superiore è massima, alta, più o equivalente, è possibile omettere le altre etichette perché il significato è chiaro.

    ![Figura di un dispositivo di scorrimento verticale ](images/ctrl-sliders-image2.png)

    In questo esempio, l'orientamento verticale del dispositivo di scorrimento rende le etichette di intervallo non necessarie.

-   **Usare i segni di graduazione quando è necessario che gli utenti conoscano il valore approssimativo dell'impostazione.**
-   **Usare i segni di graduazione e un'etichetta del valore quando gli utenti devono ottenere il valore esatto dell'impostazione scelta.** Usare sempre un'etichetta di valore se un utente deve essere a conoscenza delle unità per dare senso all'impostazione.

    ![Figura del dispositivo di scorrimento che mostra il numero di pixel selezionati ](images/ctrl-sliders-image3.png)

    In questo esempio viene usata un'etichetta per indicare chiaramente il valore selezionato.

-   **Per i dispositivi di scorrimento orientati orizzontalmente, posizionare i segni di graduazione sotto il dispositivo di scorrimento.** Per i dispositivi di scorrimento orientati verticalmente, posizionare i segni di graduazione a destra per le impostazioni cultura occidentali; per le impostazioni cultura che leggono da destra a sinistra, eseguire l'operazione opposta.
-   **Posizionare l'etichetta del valore completamente sotto il controllo dispositivo di scorrimento in modo che la relazione sia chiara.**

    **Non corretto:**

    ![Figura di un'etichetta più lunga del relativo dispositivo di scorrimento ](images/ctrl-sliders-image4.png)

    In questo esempio, l'etichetta del valore non è allineata sotto il dispositivo di scorrimento.

-   **Quando si disabilita un dispositivo di scorrimento, disabilitare anche le etichette associate.**
-   **Non usare sia un dispositivo di scorrimento che una casella di testo numerica per la stessa impostazione.** Usare solo il controllo più appropriato.

    **Eccezione:** Usare entrambi i controlli quando l'utente necessita di un feedback immediato e della possibilità di impostare un valore numerico esatto.

-   **Non usare un dispositivo di scorrimento come indicatore di stato.**
-   **Non modificare le dimensioni dell'indicatore del dispositivo di scorrimento dalla dimensione predefinita.**

    **Non corretto:**

    ![Figura del dispositivo di scorrimento minore del valore predefinito ](images/ctrl-sliders-image5.png)

    In questo esempio viene usata una dimensione inferiore a quella predefinita.

    **Corretto:**

    ![figura che mostra il dispositivo di scorrimento predefinito ](images/ctrl-sliders-image6.png)

    In questo esempio vengono usate le dimensioni predefinite.

-   **Non etichettare ogni segno di graduazione.**

## <a name="recommended-sizing-and-spacing"></a>Ridimensionamento e spaziatura consigliati

![Figura di ridimensionamento e spaziatura del dispositivo di scorrimento consigliati ](images/ctrl-sliders-image7.png)

Dimensionamento e spaziatura consigliati per i dispositivi di scorrimento.

## <a name="labels"></a>Etichette

### <a name="slider-labels"></a>Etichette del dispositivo di scorrimento

-   Utilizzare un'etichetta di testo statico che termina con i due punti oppure un'etichetta di casella di gruppo senza punteggiatura finale.
-   Assegnare una chiave di accesso univoca a ogni etichetta. Per le linee guida di assegnazione, vedere [tastiera](inter-keyboard.md).
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Posizionare l'etichetta del dispositivo di scorrimento a sinistra del dispositivo di scorrimento o superiore e allineato al bordo sinistro del dispositivo di scorrimento (o all'identificatore di intervallo sinistro, se presente).

### <a name="range-labels"></a>Etichette di intervallo

-   Usa due etichette per le due estremità dell'intervallo del dispositivo di scorrimento, se non usi un orientamento verticale che le rende superflue.
-   Usare solo Word, se possibile, per ogni etichetta.
-   Non usare punteggiatura finale.
-   Controlla che queste etichette siano descrittive e parallele. Di seguito sono riportati alcuni esempi. Massimo/Minimo, Più/Meno, Alto/Basso, Piano/Forte.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non assegnare chiavi di accesso.

### <a name="value-labels"></a>Etichette di valore

-   Se ti serve un'etichetta di valore, visualizzala sotto il dispositivo di scorrimento.
-   Centra il testo rispetto al controllo e includi le unità (ad esempio, i pixel).

    ![Figura dell'etichetta centrata sotto il dispositivo di scorrimento ](images/ctrl-sliders-image8.png)

    In questo esempio, l'etichetta del valore viene centrata sotto il dispositivo di scorrimento e include le unità.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai dispositivi di scorrimento:

-   Usare il testo esatto dell'etichetta, inclusa la relativa maiuscola, e includere la parola slider. Non includere il carattere di sottolineatura della chiave di accesso o i due punti.
-   Per descrivere l'interazione dell'utente, utilizzare Move.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: per aumentare la risoluzione dello schermo, spostare il dispositivo di scorrimento **risoluzione schermo** a destra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 