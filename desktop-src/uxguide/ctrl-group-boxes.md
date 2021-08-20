---
title: Caselle di gruppo
description: Una casella di gruppo è una cornice rettangolare etichettata che racchiude un set di controlli correlati. Una casella di gruppo consente di visualizzare visivamente le relazioni. oltre a fornire una chiave di accesso per un gruppo di controlli, non fornisce alcuna funzionalità.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 335382225e2d9dbb5a216e5aa64dbb5d6047d34845e2bfd72a4866ebafa0fca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118039892"
---
# <a name="group-boxes"></a>Caselle di gruppo

> [!NOTE]
> Questa guida alla progettazione è stata creata Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti.](/windows/uwp/design/)

Una casella di gruppo è una cornice rettangolare etichettata che racchiude un set di controlli correlati. Una casella di gruppo consente di visualizzare visivamente le relazioni. oltre a fornire una chiave di accesso per un gruppo di controlli, non fornisce alcuna funzionalità.

![Screenshot della casella di gruppo contenente le caselle di controllo ](images/ctrl-group-boxes-image1.png)

Casella di gruppo tipica.

> [!Note]  
> Le linee guida correlate [al layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Anche se le caselle di gruppo sono un potente mezzo visivo per indicare le relazioni, l'utilizzo over delle relazioni aggiunge confusione visiva e riduce notevolmente lo spazio disponibile su una superficie. Sono visivamente pesanti e devono essere usati con parsimonio, solo quando non esiste una soluzione migliore.

Una tendenza di progettazione Windows un aspetto più semplice e più pulito eliminando le linee non necessarie.

Per decidere se una casella di gruppo è necessaria, considerare queste domande:

-   **È presente più di un controllo nel gruppo?** In caso contrario, usare un'etichetta di testo normale. Un'eccezione rara è l'uso di una casella di gruppo con un singolo controllo per mantenere la coerenza con altre caselle di gruppo sulla stessa superficie.

**Non corretto:** ![ Screenshot della casella di gruppo contenente una casella di testo ](images/ctrl-group-boxes-image2.png)

In questo esempio la casella di gruppo ha un solo controllo .

-   **I controlli sono correlati? La visualizzazione della relazione aggiunge maggiore chiarezza?** In caso contrario, presentare i controlli separatamente all'esterno di una casella di gruppo.
-   **Tutti i controlli sono all'interno del gruppo?** In tal caso, indicare la relazione sulla superficie più grande, ad esempio la finestra di dialogo o la pagina padre.

**Non corretto:** ![ Screenshot della casella di gruppo contenente tutti i controlli ](images/ctrl-group-boxes-image3.png)

In questo esempio tutti i controlli (oltre ai pulsanti di commit) nella finestra di dialogo si trova all'interno della casella di gruppo.

-   **È possibile comunicare in modo efficace le relazioni usando solo il layout?** In caso contrario, usare [il layout.](vis-layout.md) È possibile posizionare i controlli correlati uno accanto all'altro e inserire una spaziatura aggiuntiva tra i controlli non correlati. È anche possibile usare intestazioni e rientri per visualizzare relazioni gerarchiche.

![Figura di quattro icone che mostrano quattro gruppi di attività ](images/ctrl-group-boxes-image4.png)

In questo esempio il layout viene usato da solo per visualizzare le relazioni tra i controlli.

-   **È possibile comunicare in modo efficace le relazioni usando un separatore?** In caso contrario, usare un separatore. Un separatore è una linea orizzontale che unifica i controlli sottostanti. I separatori offrono un aspetto più semplice e più pulito. Tuttavia, a differenza delle caselle di gruppo, funzionano meglio quando si estendono sull'intera larghezza della superficie.
    -   **Sviluppatori:** È possibile implementare un separatore con un rettangolo inciso con un'altezza di uno.

![Screenshot che mostra i controlli di posta elettronica separati da separatori di rettangoli incisi.](images/ctrl-group-boxes-image5.png)

In questo esempio vengono usati separatori con etichetta per visualizzare le relazioni tra i controlli.

![Screenshot dei controlli separati dai separatori ](images/ctrl-group-boxes-image6.png)

In questo esempio vengono usati separatori senza etichetta per visualizzare le relazioni tra i controlli.

-   **È possibile comunicare in modo efficace le relazioni senza testo?** In tal caso, è consigliabile usare elementi grafici come [sfondi](vis-graphic.md) o aggregatori.

## <a name="guidelines"></a>Indicazioni

-   **Non annidare le caselle di gruppo.** Usare il layout per visualizzare le relazioni all'interno di una casella di gruppo.

**Non corretto:** ![ Screenshot di una casella di gruppo all'interno di una casella di gruppo ](images/ctrl-group-boxes-image7.png)

In questo esempio, le caselle di gruppo annidate comportano un disordine visivo non necessario.

**Corretto:** ![ Screenshot degli stessi controlli all'interno di una casella di gruppo ](images/ctrl-group-boxes-image8.png)

In questo esempio viene mostrata la stessa relazione di controllo usando invece il layout .

-   Non inserire i controlli nelle etichette della casella di gruppo.
    -   **Eccezione:** È possibile utilizzare una casella di controllo come etichetta della casella di gruppo se tutti i controlli all'interno della casella sono abilitati e disabilitati dalla casella di controllo.

**Non corretto:** ![ Screenshot dell'elenco a discesa in un'etichetta della casella di gruppo ](images/ctrl-group-boxes-image9.png)

In questo esempio un elenco a discesa viene inserito in modo non corretto in una casella di gruppo. In questo esempio è consigliabile [usare le tabulazioni.](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx)

-   **Non disabilitare le caselle di gruppo.** Per indicare che un gruppo di controlli non è attualmente applicabile, disabilitare tutti i controlli all'interno della casella di gruppo, ma non la casella di gruppo stessa. Questo approccio è più accessibile e può essere supportato in modo coerente da tutti i framework dell'interfaccia utente.

## <a name="labels"></a>Etichette

-   Etichettare tutte le caselle di gruppo.
-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso. Assegnare invece i tasti di scelta ai controlli all'interno della casella di gruppo.
    -   **Eccezione:** Se una superficie ha molti controlli, è possibile che non siano disponibili chiavi di accesso sufficienti. In tal caso, ridurre il numero di chiavi di accesso assegnandole alle caselle di gruppo anziché ai controlli all'interno delle caselle di gruppo.
-   Usare [l'uso di maiuscole e minuscole in stile frase.](glossary.md)
-   Scrivere l'etichetta usando un sostantivo o una frase sostantiva, non come frase, e senza punteggiatura finale, inclusi i due punti.
-   Usare la formulazione parallela per le etichette della casella di gruppo all'interno della stessa superficie.
-   Mantenere concise le etichette delle casella di gruppo. Non usare il testo informativo come etichetta. È tuttavia possibile avere testo informativo all'interno della casella di gruppo.
-   Non ripetere l'etichetta della casella di gruppo nelle etichette di controllo all'interno della casella. Ad esempio, se la casella di gruppo è etichettata come Allineamento, etichettare i pulsanti di opzione A sinistra, A destra e così via, non Allineamento a sinistra o Allineamento a destra.
-   Non fare riferimento alle caselle di gruppo nel testo dell'interfaccia utente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di gruppo:

-   Fare riferimento alle caselle di gruppo solo nel programmatore e in altre documentazione tecnica. Per la casella di gruppo, usare due parole minuscole.
-   In tutti gli altri casi, non è necessario includere il nome della casella di gruppo in una routine, a meno che una finestra di dialogo non contenga più di un'opzione con lo stesso nome. In questi casi, usare in con il nome della casella di gruppo.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: in **Effetti** selezionare **Nascosto.**

 

 