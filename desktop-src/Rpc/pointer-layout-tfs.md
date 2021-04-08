---
title: Layout puntatore
description: Il layout del puntatore descrive i puntatori di una struttura o di una matrice.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856638"
---
# <a name="pointer-layout"></a>Layout puntatore

Il layout del puntatore descrive i puntatori di una struttura o di una matrice.

## <a name="pointer_layout"></a>\_<> layout puntatore

Il \_ layout di un puntatore<> campo è costituito dai caratteri di formato FC \_ PP FC \_ , seguiti da una o più descrizioni del puntatore, come descritto più avanti e termina con un \_ carattere di formato finale FC:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Il \_ \_ layout di un'istanza del puntatore<> campo è una stringa di formato che descrive una o più istanze di puntatori. Nei descrittori vengono usati i campi seguenti:

-   offset \_ in \_ memoria

    Offset con segno sulla posizione in memoria del puntatore. Per un puntatore che si trova in una struttura, questo offset è un offset negativo rispetto alla fine della struttura (la fine della parte non conforme delle strutture conformi); per le matrici, l'offset è dall'inizio della matrice.

-   offset \_ nel \_ buffer

    Offset con segno sulla posizione del puntatore nel buffer. Per un puntatore che si trova in una struttura, questo offset è un offset negativo rispetto alla fine della struttura (la fine della parte non conforme di strutture conformi): per le matrici, l'offset è dall'inizio della matrice.

-   offset \_ alla \_ matrice

    Offset da una struttura di inclusione alla matrice incorporata di cui vengono gestiti i puntatori. Per le matrici di primo livello, questo campo sarà sempre zero.

-   iterazioni

    Numero totale di puntatori con lo stesso layout<> descritti.

-   increment

    Incremento tra puntatori successivi durante la ripetizione.

-   numero \_ di \_ puntatori

    Numero di puntatori diversi in un'istanza di ripetizione.

-   Descrizione indicatore di misura \_

    Descrizione del puntatore.

Tutti i layout dell'istanza del puntatore utilizzano la seguente istanza a puntatore singolo \_<8>:

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

Di seguito sono riportati i descrittori di istanza:

**Singola istanza di un puntatore a un tipo semplice:**

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

**Puntatore di ripetizione fisso:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Puntatore di ripetizione della variabile:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Per le istanze di ripetizione fissa e di ripetizione del puntatore variabile è presente un set di descrizioni offset e puntatore per ogni puntatore nell'istanza di ripetizione.

## <a name="pointers-layout-design-issues"></a>Problemi di progettazione del layout dei puntatori

In questa sezione vengono illustrati i problemi relativi all'elaborazione di strutture conformi e puntatori incorporati. Il problema è che il compilatore genera layout di puntatore per strutture e matrici con una certa ridondanza. Questa operazione è utile perché le informazioni sono utili e, ad esempio, una struttura conforme può esaminare un layout di puntatore per servire tutti i puntatori dalla struttura e dalla matrice conforme che fanno parte della struttura conforme. Tuttavia, esistono alcune situazioni incorporate che richiedono al motore di NDR di eseguire ulteriori operazioni per elaborare tutti i layout del puntatore nella sequenza corretta, elaborando ogni puntatore esattamente una volta.

## <a name="what-the-compiler-generates"></a>Cosa genera il compilatore

Ogni oggetto illustrato in questa sezione include puntatori, ad esempio una struttura conforme ha puntatori nella parte della struttura e negli elementi della matrice. L'elemento è una struttura semplice con un puntatore.

1.  Struttura conforme, singolo livello

    Il descrittore conforme ha una parte PP in cui vengono descritti tutti i puntatori, sia dalla struttura che dalla matrice. L'elenco dei membri ha \_ un FC lungo invece di un puntatore. Il descrittore della matrice CARRAy contiene elementi tramite l'uso di un oggetto \_ complesso incorporato senza descrittori di puntatore. L'elemento ha ancora il descrittore del puntatore singolo. Il layout del puntatore precede il layout del membro in una struttura conforme e descrittori di struttura semplici.

2.  Struttura conforme, due o più livelli

    La descrizione PP contiene puntatori di tutti i livelli. Riutilizza la stessa descrizione della matrice della struttura conforme interna. L'elenco dei membri ha \_ un FC lungo invece di un puntatore. Una struttura incorporata passa attraverso l'uso di un complesso incorporato. Il descrittore di struttura conforme viene riusato così com'è. Anche le dimensioni della parte piatta della struttura sono state completate, vale a dire che la dimensione della struttura di primo livello includerà le dimensioni flat della struttura incorporata.

3.  Struttura complessa, a singolo livello

    I membri del puntatore sono contrassegnati dal \_ puntatore FC. Il layout del puntatore è semplificato in modo da disporre di un descrittore del puntatore (4 byte) per ogni voce del puntatore FC nell' \_ elenco. Il layout del puntatore viene camminato in parallelo con una passeggiata del membro, ovvero un \_ puntatore FC causa l'elaborazione della descrizione del puntatore successiva. La matrice CARRAy presenta il layout del puntatore con tutti i descrittori della matrice e quindi l'elemento, tramite l'uso di un complesso incorporato. Il descrittore dell'elemento viene riutilizzato. Le dimensioni della parte piana della struttura vengono completate. in altre parole, le dimensioni flat della struttura di livello superiore includono le dimensioni flat della struttura incorporata. Il layout del membro precede il layout del puntatore per le strutture complesse.

    Di conseguenza, la generazione della descrizione della matrice conforme è diversa a seconda che si tratti di una matrice all'interno di una struttura conforme o all'interno di una struttura complessa.

4.  Struttura complessa, 2 o più livelli, complesso in complesso

    La struttura complessa di primo livello presenta i puntatori ai membri, la struttura complessa incorporata presenta i puntatori ai membri. Il descrittore di struttura conforme viene riutilizzato. Il descrittore della matrice dalla parte superiore è la matrice riutilizzata dalla struttura incorporata.

5.  Struttura complessa con una struttura conforme incorporata

    Top = la struttura conforme al livello ha i puntatori dei membri. Il descrittore di struttura conforme viene riusato così com'è. Il descrittore della matrice viene riutilizzato dalla struttura conforme incorporata; in altre parole, non ha alcun puntatore al descrittore della matrice. Il descrittore dell'elemento è relativo al puntatore.

6.  Matrici di strutture con puntatori

    Una matrice di strutture semplici con puntatori viene generata come SMFARRAY o CARRAy a seconda che la matrice sia ridimensionata, ma in entrambi i casi dispone di un layout del puntatore completato ( \_ ripetizione fissa o ripetizione della variabile \_ ). Il layout del puntatore precede il layout del membro.

    Una matrice di strutture complesse con puntatori viene generata come matrice FASULLa \_ , indipendentemente dal fatto che sia fissa o ridimensionata, e in entrambi i casi non disponga di un layout di puntatore.

## <a name="what-the-ndr-engine-does"></a>Funzione del motore di NDR

In questa sezione viene descritto il comportamento del motore NDR.

**Passaggio di marshalling**

1.  Strutture conformi e struttura conforme incorporata.

    La struttura di livello superiore si comporta come una struttura a un solo livello.

2.  Struttura complessa incorporata con matrice conforme

    Qualsiasi struttura complessa forza la struttura esterna a essere una struttura complessa. La struttura incorporata non esegue mai il marshalling della relativa matrice. Ogni struttura passa sempre attraverso puntatori incorporati semplicemente effettuando il marshalling dei membri e un membro che sta per essere un \_ puntatore FC.

3.  Struttura complessa con struttura conforme

    La struttura più in alto conforme incorporata esegue il marshalling della matrice conforme e di tutti i puntatori. Il motore di mancato recapito non scende mai a strutture conformi annidate più approfondite, se presenti; in questo modo la soluzione viene semplificata perché una struttura conforme è un oggetto foglia per quanto riguarda il marshalling degli oggetti incorporati. La struttura complessa di primo livello ignora il marshalling della matrice.

**Unmarshaling, bufsizing e Free Pass**

L'unmarshalling è simmetrico al marshalling; la prima operazione eseguita per le strutture complesse consiste nel trovare la posizione dei puntatori nel buffer per mezzo della chiamata alla funzione **NdrComplexStructBufferSize** . Esegue quindi l'unmarshalling dei puntatori in parallelo, abilitando lo stesso schema per l'unmarshalling dei puntatori correttamente da usare. Non dovrebbero esserci confusione sugli oggetti e le unioni di dimensioni; l'immagine di memoria non deve essere utilizzata per gli oggetti e le unioni di dimensioni, solo per il contenuto del buffer.

I flag usati per eseguire correttamente il marshalling e l'unmarshalling vengono usati nello stesso modo in bufsizing e liberando per assicurarsi che i puntatori vengano passati esattamente una volta.

**Superamento della sessione**

In primo luogo, il passaggio dell'oggetto è analogo al marshalling e all'unmarshalling; per elaborare strutture complesse sono necessarie due sessioni. Il primo passaggio converte la parte flat e trova la posizione dei puntatori nel buffer in modo analogo a come bufsizing esegue questa operazione per l'unmarshalling. Il secondo passaggio converte quindi i puntatori.

I passaggi di registrazione variano in modo analogo al seguente: ogni struttura e ogni membro deve essere rientrata fino a quando il membro foglia o l'elemento non è un tipo semplice. Questa operazione è diversa dall'unmarshalling; Quando si esegue l'unmarshalling, ad esempio, non è mai necessario elaborare le strutture conformi incorporate in strutture conformi o qualsiasi membro della struttura conforme, a tale proposito. Un altro problema è rappresentato dal fatto che la conversione non è un'operazione idempotente, di conseguenza il passaggio di unmarshalling può ripetere l'unmarshalling di alcune parti senza danni, mentre la conversione deve essere eseguita in base a un tipo rigorosamente singolo.

Di conseguenza, è possibile riepilogare l'algoritmo delle opzioni come indicato di seguito. NDR presenta una nozione di struttura conforme di primo livello e un flag per contrassegnare questo, a seconda dei casi. Quando si esegue la prima volta, ad esempio per convertire la parte piatta e ottenere la posizione dei puntatori, questa nozione non verrà usata. Il rapporto di mancato recapito attraverso le parti piane di tutti i livelli di strutture e mai venture nell'elaborazione del puntatore. Infine, il rapporto di MANCAto consiste nella conversione flat della matrice al livello superiore.

Quando si esamina la seconda volta, il flag viene usato per contrassegnare il passaggio del puntatore incorporato per evitare di immettere livelli più profondi delle strutture conformi, quindi la struttura più in alto. In questo modo, il flag forza il comportamento comune di marshalling/unmarshalling, che consente di evitare decrescente in livelli più profondi di strutture conformi.

Il secondo passaggio per le strutture complesse con matrici conformi funziona nel modo seguente: le strutture complesse funzionano in modo comune; il che significa che i livelli più profondi non dovrebbero mai esaminare o ignorare le dimensioni conformi o le matrici conformi ed è piuttosto semplice scorrere i membri senza toccare la matrice.

Per le strutture complesse con strutture conformi, la struttura conforme deve essere in grado di riconoscere se è di primo livello e se si trova in una struttura complessa. La parte piatta della matrice viene elaborata dalla struttura conforme più in alto. Al secondo passaggio, la struttura più in alto conforme ignora la parte piatta e passa attraverso il layout del puntatore e restituisce il risultato. La struttura più alta più complessa ignora la parte piatta e ignora anche il layout del puntatore.

**Il solido aspetto dei percorsi di un'esercitazione**

Il percorso di inserimento controlla le normali condizioni di esaurimento del buffer ed esegue altri controlli su una natura non correlata. I controlli destinati a valori correlati, ad esempio l'argomento di ridimensionamento rispetto alla dimensione conforme, non possono essere eseguiti con questo passaggio. vengono eseguite in un secondo momento, durante l'unmarshalling.

 

 




