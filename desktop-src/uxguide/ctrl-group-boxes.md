---
title: Caselle di gruppo
description: Una casella di gruppo è una cornice rettangolare con etichetta che racchiude un set di controlli correlati. Una casella di gruppo è un modo per visualizzare le relazioni visivamente; oltre a fornire una chiave di accesso per un gruppo di controlli, non fornisce alcuna funzionalità.
ms.assetid: 5b5ffb36-3ed1-44cd-af87-5cddf46c56a6
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 67f930383f2d4412d30027971c6cab2bd3edcccd
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104559163"
---
# <a name="group-boxes"></a>Caselle di gruppo

> [!NOTE]
> Questa guida alla progettazione è stata creata per Windows 7 e non è stata aggiornata per le versioni più recenti di Windows. Gran parte delle linee guida si applica ancora in linea di principio, ma la presentazione e gli esempi non riflettono le [linee guida di progettazione correnti](/windows/uwp/design/).

Una casella di gruppo è una cornice rettangolare con etichetta che racchiude un set di controlli correlati. Una casella di gruppo è un modo per visualizzare le relazioni visivamente; oltre a fornire una chiave di accesso per un gruppo di controlli, non fornisce alcuna funzionalità.

![screenshot della casella di gruppo contenente le caselle di controllo ](images/ctrl-group-boxes-image1.png)

Una tipica casella di gruppo.

> [!Note]  
> Le linee guida correlate al [layout](vis-layout.md) sono presentate in un articolo separato.

 

## <a name="is-this-the-right-control"></a>È il controllo giusto?

Sebbene le caselle di gruppo siano un metodo visivo sicuro per indicare le relazioni, il loro utilizzo aggiunge confusione visiva e riduce notevolmente lo spazio disponibile su una superficie. Sono visivamente pesanti e devono essere usate con parsimonia, solo quando non è disponibile una soluzione migliore.

Una tendenza di progettazione in Windows è un aspetto più semplice e pulito eliminando le righe non necessarie.

Per decidere se una casella di gruppo è necessaria, prendere in considerazione le domande seguenti:

-   **Esiste più di un controllo del gruppo?** In caso contrario, utilizzare un'etichetta di testo normale. Un'eccezione rara consiste nell'utilizzare una casella di gruppo con un unico controllo per mantenere la coerenza con altre caselle di gruppo nella stessa area.

Non **corretto:** ![ screenshot della casella di gruppo contenente una casella di testo](images/ctrl-group-boxes-image2.png)

In questo esempio, la casella di gruppo dispone di un solo controllo.

-   **I controlli sono correlati? Viene visualizzata la relazione Aggiungi chiarezza?** In caso contrario, presentare i controlli separatamente all'esterno di una casella di gruppo.
-   **Tutti i controlli all'interno del gruppo?** In tal caso, indicare la relazione sulla superficie più grande, ad esempio la pagina o la finestra di dialogo padre.

Non **corretto:** ![ screenshot della casella di gruppo che contiene tutti i controlli](images/ctrl-group-boxes-image3.png)

In questo esempio, tutti i controlli (a parte i pulsanti commit) nella finestra di dialogo si trovano all'interno della casella di gruppo.

-   **È possibile comunicare efficacemente le relazioni usando solo il layout?** In caso affermativo, usare invece il [layout](vis-layout.md) . È possibile posizionare i controlli correlati uno accanto all'altro e inserire spazi aggiuntivi tra i controlli non correlati. È inoltre possibile utilizzare le intestazioni e i rientri per visualizzare le relazioni gerarchiche.

![Figura di quattro icone che mostrano quattro gruppi di attività ](images/ctrl-group-boxes-image4.png)

In questo esempio, viene usato solo il layout per visualizzare le relazioni di controllo.

-   **È possibile comunicare efficacemente le relazioni usando un separatore?** In caso affermativo, usare invece un separatore. Un separatore è una linea orizzontale che unifica i controlli sottostanti. I separatori forniscono un aspetto più semplice e pulito. Tuttavia, a differenza delle caselle di gruppo, funzionano meglio quando si estendono sulla larghezza intera della superficie.
    -   **Sviluppatori:** È possibile implementare un separatore con un rettangolo inciso con un'altezza pari a uno.

![Screenshot che mostra i controlli della posta elettronica impostati separatamente dai separatori di rettangolo con etching.](images/ctrl-group-boxes-image5.png)

In questo esempio, i separatori con etichetta vengono utilizzati per visualizzare le relazioni tra i controlli.

![screenshot dei controlli impostati separatamente da separatori ](images/ctrl-group-boxes-image6.png)

In questo esempio, i separatori senza etichetta vengono utilizzati per visualizzare le relazioni tra i controlli.

-   **È possibile comunicare efficacemente le relazioni senza testo?** In tal caso, è consigliabile usare elementi grafici come gli [sfondi](vis-graphic.md) o gli aggregatori.

## <a name="guidelines"></a>Indicazioni

-   **Non annidare le caselle di gruppo.** Usare il layout per visualizzare le relazioni all'interno di una casella di gruppo.

Non **corretto:** ![ Screenshot di una casella di gruppo all'interno di una casella di gruppo](images/ctrl-group-boxes-image7.png)

In questo esempio le caselle di gruppo annidate generano confusione visiva superflua.

**Corretto:** ![ screenshot degli stessi controlli in una casella di gruppo ](images/ctrl-group-boxes-image8.png)

In questo esempio, la stessa relazione di controllo viene visualizzata utilizzando il layout.

-   Non inserire i controlli nelle etichette delle caselle di gruppo.
    -   **Eccezione:** È possibile utilizzare una casella di controllo come etichetta di casella di gruppo se tutti i controlli all'interno della casella sono abilitati e disabilitati dalla casella di controllo.

Non **corretto:** ![ screenshot dell'elenco a discesa in un'etichetta della casella di gruppo](images/ctrl-group-boxes-image9.png)

In questo esempio un elenco a discesa non viene inserito correttamente in una casella di gruppo. In questo esempio vengono usate le [schede](https://msdn.microsoft.com/library/windows/desktop/aa511493.aspx) .

-   **Non disabilitare le caselle di gruppo.** Per indicare che un gruppo di controlli non è attualmente applicabile, disabilitare tutti i controlli all'interno della casella di gruppo, ma non la casella di gruppo. Questo approccio è più accessibile e può essere supportato in modo coerente da tutti i Framework dell'interfaccia utente.

## <a name="labels"></a>Etichette

-   Etichetta tutte le caselle di gruppo.
-   Non assegnare una chiave di accesso all'etichetta. Questa operazione non è necessaria e rende più difficile l'assegnazione delle altre chiavi di accesso. Assegnare invece chiavi di accesso ai controlli all'interno della casella di gruppo.
    -   **Eccezione:** Se una superficie presenta molti controlli, è possibile che non siano disponibili chiavi di accesso sufficienti. In tal caso, ridurre il numero di chiavi di accesso assegnando loro le caselle di gruppo anziché i controlli all'interno delle caselle di gruppo.
-   Usare l'uso [di maiuscole in stile frase](glossary.md).
-   Scrivere l'etichetta usando un sostantivo o una frase nominale, non come una frase, e non usare segni di punteggiatura finali, inclusi i due punti.
-   Utilizzare il formulazione parallela per le etichette delle caselle di gruppo all'interno della stessa area.
-   Mantiene concise le etichette della casella di gruppo. Non usare il testo dell'istruzione come etichetta. È tuttavia possibile avere un testo informativo all'interno della casella di gruppo.
-   Non ripetere l'etichetta della casella di gruppo nelle etichette dei controlli all'interno della casella. Se, ad esempio, la casella di gruppo è con etichetta allineamento, etichettare i pulsanti di opzione Left, Right e così via, senza allineamento a sinistra o allineamento a destra.
-   Non fare riferimento alle caselle di gruppo nel testo dell'interfaccia utente.

## <a name="documentation"></a>Documentazione

Quando si fa riferimento alle caselle di gruppo:

-   Vedere le caselle di gruppo solo nel programmatore e in altri documenti tecnici. Per la casella di gruppo, usare due parole minuscole.
-   In qualsiasi altra parte, non è necessario includere il nome della casella di gruppo in una procedura, a meno che una finestra di dialogo non contenga più di un'opzione con lo stesso nome. In questi casi, utilizzare con il nome della casella di gruppo.
-   Quando possibile, formattare l'etichetta usando il testo in grassetto. In caso contrario, inserire l'etichetta tra virgolette solo se necessario per evitare confusione.

Esempio: in **Effects** selezionare **Hidden**.

 

 