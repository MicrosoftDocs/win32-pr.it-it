---
title: Dispositivi di scorrimento (nozioni di base sulla progettazione)
description: Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori.
ms.assetid: dee70fbc-6f18-43c7-9d41-4e97eac41e53
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 73c6ae0cc490c338ec552d0e23e829c791689f6f822d324feaa863ccbb441d73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349894"
---
# <a name="sliders-design-basics"></a>Dispositivi di scorrimento (nozioni di base sulla progettazione)

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Con un dispositivo di scorrimento, gli utenti possono scegliere tra un intervallo continuo di valori. Un dispositivo di scorrimento ha una barra che mostra l'intervallo e un indicatore che mostra il valore corrente. I segni di graduazione facoltativi mostrano i valori.

![Figura che mostra barra, dispositivo di scorrimento e segni di graduazione ](images/ctrl-sliders-image1.png)

Un dispositivo di scorrimento tipico.

> [!Note]  
> Le linee guida [correlate al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Usare un dispositivo di scorrimento quando si vuole che gli utenti siano in grado di impostare valori contigui definiti (ad esempio volume o luminosità) o un intervallo di valori **discreti ,ad** esempio le impostazioni di risoluzione dello schermo.

Un dispositivo di scorrimento è una buona scelta quando sai che gli utenti considerano il valore una quantità relativa e non un valore numerico. Ad esempio, gli utenti vogliono impostare il volume audio su basso o medio e non su 2 o 5.

Per decidere, prendi in considerazione queste domande:

-   **L'impostazione sembra una quantità relativa?** In caso contrario, usare [i pulsanti di](ctrl-radio-buttons.md)opzione o un elenco a [discesa](/windows/desktop/uxguide/ctrl-drop) o a [selezione singola.](ctrl-list-boxes.md)
-   **L'impostazione è un valore numerico noto esatto?** In tal caso, usare una [casella di testo numerica](ctrl-text-boxes.md).
-   **Un utente trarrebbe vantaggio da un riscontro immediato sull'effetto delle modifiche dell'impostazione?** Se sì, usa un dispositivo di scorrimento. Gli utenti possono ad esempio scegliere più facilmente un colore esaminando immediatamente l'effetto delle modifiche dei valori di tonalità, saturazione o luminosità.
-   **L'impostazione ha un intervallo di quattro o più valori?** In caso contrario, usa pulsanti di opzione.
-   **L'utente può modificare il valore?** I dispositivi di scorrimento consentono l'interazione dell'utente. Se un utente non può modificare il valore, usare invece una casella [di testo di sola](ctrl-text-boxes.md) lettura.

Se è possibile usare un dispositivo di scorrimento o una casella di testo numerica, usare una casella di testo numerica se:

-   Lo spazio sullo schermo è limitato.
-   È probabile che un utente preferisca usare la tastiera.

Usa un dispositivo di scorrimento se:

-   Gli utenti trarranno vantaggio da un riscontro immediato.

## <a name="guidelines"></a>Indicazioni

-   **Usa un orientamento naturale.** Ad esempio, se il dispositivo di scorrimento rappresenta un valore reale indicato di solito in verticale (come la temperatura), usa un orientamento verticale.
-   **Orientare il dispositivo di scorrimento in modo da riflettere le impostazioni cultura degli utenti.** Ad esempio, le impostazioni cultura occidentali leggono da sinistra a destra, quindi per i dispositivi di scorrimento orizzontali, inserire l'estremità inferiore dell'intervallo a sinistra e l'estremità superiore a destra. Per le impostazioni cultura che leggono da destra a sinistra, fare il contrario.
-   **Ridimensionare il controllo in modo che un utente possa impostare facilmente il valore desiderato.** Per le impostazioni con valori discreti, assicurati che l'utente possa selezionare agevolmente i valori con il mouse.
-   **È consigliabile usare una scala non lineare se l'intervallo di valori è elevato e gli utenti probabilmente selezioneranno i valori a un'estremità dell'intervallo.** Ad esempio, il valore dell'ora potrebbe essere 1 minuto, 1 ora, 1 giorno o 1 mese.
-   **Ogni volta che è pratico, inviare commenti e suggerimenti immediati mentre o dopo che un utente effettua una selezione.** Ad esempio, microsoft Windows il controllo del volume esemplizza per indicare il volume audio risultante.
-   **Usa etichette per indicare l'intervallo di valori.**

    **Eccezione:** Se il dispositivo di scorrimento è orientato verticalmente e l'etichetta superiore è Maximum, High, More o equivalente, è possibile omettere le altre etichette perché il significato è chiaro.

    ![figura di un dispositivo di scorrimento verticale ](images/ctrl-sliders-image2.png)

    In questo esempio, l'orientamento verticale del dispositivo di scorrimento rende superflue le etichette dell'intervallo.

-   **Usare i segni di graduazione quando gli utenti devono conoscere il valore approssimativo dell'impostazione.**
-   **Usare i segni di graduazione e un'etichetta di valore quando gli utenti devono conoscere il valore esatto dell'impostazione scelta.** Usare sempre un'etichetta di valore se un utente deve conoscere le unità per dare un senso all'impostazione.

    ![Figura del dispositivo di scorrimento che mostra il numero di pixel selezionati ](images/ctrl-sliders-image3.png)

    In questo esempio viene usata un'etichetta per indicare chiaramente il valore selezionato.

-   **Per i dispositivi di scorrimento orientati orizzontalmente, posizionare i segni di graduazione sotto il dispositivo di scorrimento.** Per i dispositivi di scorrimento orientati verticalmente, posizionare i segni di graduazione a destra per le impostazioni cultura occidentali; per le impostazioni cultura che leggono da destra a sinistra, fare il contrario.
-   **Posizionare completamente l'etichetta del valore sotto il dispositivo di scorrimento in modo che la relazione sia chiara.**

    **Non corretto:**

    ![figura di un'etichetta più lunga del dispositivo di scorrimento ](images/ctrl-sliders-image4.png)

    In questo esempio l'etichetta del valore non è allineata sotto il dispositivo di scorrimento.

-   **Quando si disabilita un dispositivo di scorrimento, disabilitare anche le etichette associate.**
-   **Non usare sia un dispositivo di scorrimento che una casella di testo numerica per la stessa impostazione.** Usare solo il controllo più appropriato.

    **Eccezione:** Usare entrambi i controlli quando l'utente necessita di feedback immediato e la possibilità di impostare un valore numerico esatto.

-   **Non usare un dispositivo di scorrimento come indicatore di stato.**
-   **Non modificare le dimensioni dell'indicatore di scorrimento rispetto alle dimensioni predefinite.**

    **Non corretto:**

    ![figura del dispositivo di scorrimento inferiore a quella predefinita ](images/ctrl-sliders-image5.png)

    In questo esempio viene usata una dimensione inferiore a quella predefinita.

    **Corretto:**

    ![Figura che mostra il dispositivo di scorrimento predefinito ](images/ctrl-sliders-image6.png)

    In questo esempio vengono usate le dimensioni predefinite.

-   **Non etichettare ogni segno di graduazione.**

## <a name="recommended-sizing-and-spacing"></a>Dimensioni e spaziatura consigliate

![figura del ridimensionamento e della spaziatura consigliati del dispositivo di scorrimento ](images/ctrl-sliders-image7.png)

Dimensioni e spaziatura consigliate per i dispositivi di scorrimento.

## <a name="labels"></a>Etichette

### <a name="slider-labels"></a>Etichette del dispositivo di scorrimento

-   Usare un'etichetta di testo statica che termina con i due punti o un'etichetta della casella di gruppo senza punteggiatura finale.
-   Assegnare una chiave di accesso univoca a ogni etichetta. Per le linee guida per l'assegnazione, [vedere Tastiera](inter-keyboard.md).
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Posizionare l'etichetta del dispositivo di scorrimento a sinistra del dispositivo di scorrimento o sopra e allineata al bordo sinistro del dispositivo di scorrimento (o al relativo identificatore di intervallo sinistro, se presente).

### <a name="range-labels"></a>Etichette di intervallo

-   Usa due etichette per le due estremità dell'intervallo del dispositivo di scorrimento, se non usi un orientamento verticale che le rende superflue.
-   Usare solo parola, se possibile, per ogni etichetta.
-   Non usare punteggiatura finale.
-   Controlla che queste etichette siano descrittive e parallele. Di seguito sono riportati alcuni esempi. Massimo/Minimo, Più/Meno, Alto/Basso, Piano/Forte.
-   Usare le maiuscole/minuscole come nelle frasi comuni.
-   Non assegnare chiavi di accesso.

### <a name="value-labels"></a>Etichette di valore

-   Se ti serve un'etichetta di valore, visualizzala sotto il dispositivo di scorrimento.
-   Centra il testo rispetto al controllo e includi le unità (ad esempio, i pixel).

    ![Figura dell'etichetta centrata sotto il dispositivo di scorrimento ](images/ctrl-sliders-image8.png)

    In questo esempio l'etichetta del valore è centrata sotto il dispositivo di scorrimento e include le unità.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento ai dispositivi di scorrimento:

-   Usare il testo esatto dell'etichetta, inclusa l'uso di maiuscole e minuscole, e includere il dispositivo di scorrimento della parola. Non includere il carattere di sottolineatura o i due punti della chiave di accesso.
-   Per descrivere l'interazione dell'utente, usare move.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: per aumentare la risoluzione dello schermo, spostare **il** dispositivo di scorrimento Risoluzione dello schermo verso destra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Glossario](glossary.md)
</dt> </dl>

 

 