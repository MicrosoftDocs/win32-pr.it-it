---
title: Layout dell'indicatore di misura
description: Il layout del puntatore descrive i puntatori di una struttura o di una matrice.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6616cc7d1000b042c6039b2abf3f79d4900cd0e5fadac748881666610b139c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019193"
---
# <a name="pointer-layout"></a>Layout dell'indicatore di misura

Il layout del puntatore descrive i puntatori di una struttura o di una matrice.

## <a name="pointer_layout"></a>Layout \_ puntatore<>

Un layout puntatore<> campo è costituito dai caratteri di formato FC PP FC PAD seguiti da una o più descrizioni del puntatore, come descritto più avanti, e termina con un carattere di formato \_ \_ FC \_ \_ END:

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

Un layout \_ di \_ istanza del puntatore<> campo è una stringa di formato che descrive una o più istanze di puntatori. In questi descrittori vengono usati i campi seguenti:

-   offset \_ in \_ memoria

    Offset con segno alla posizione del puntatore in memoria. Per un puntatore che risiede in una struttura , questo offset è un offset negativo dalla fine della struttura (la fine della parte non conforme delle strutture conformi); per le matrici, l'offset è dall'inizio della matrice.

-   offset \_ nel \_ buffer

    Offset con segno alla posizione del puntatore nel buffer. Per un puntatore che risiede in una struttura , questo offset è un offset negativo dalla fine della struttura (la fine della parte non conforme delle strutture conformi): per le matrici, l'offset è dall'inizio della matrice.

-   offset \_ in \_ array

    Offset da una struttura di inclusione alla matrice incorporata i cui puntatori vengono gestiti. Per le matrici di primo livello, questo campo sarà sempre zero.

-   iterazioni

    Numero totale di puntatori con lo stesso layout<> descritto.

-   increment

    Incremento tra puntatori successivi durante un'istruzione REPEAT.

-   numero \_ di \_ puntatori

    Numero di puntatori diversi in un'istanza repeat.

-   Descrizione del \_ puntatore

    Descrizione del puntatore.

Tutti i layout dell'istanza del puntatore usano l'istanza a puntatore \_ singolo<8>:

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

**Correzione del puntatore di ripetizione:**

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

**Puntatore di ripetizione variabile:**

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

Per le istanze del puntatore a ripetizione fissa e variabile è disponibile un set di descrizioni di offset e puntatore per ogni puntatore nell'istanza di ripetizione.

## <a name="pointers-layout-design-issues"></a>Problemi di progettazione del layout dei puntatori

In questa sezione vengono risolti i problemi relativi all'elaborazione di strutture conformi e puntatori incorporati. Il problema è che il compilatore genera layout puntatore per strutture e matrici con una certa ridondanza. Ciò è utile perché le informazioni sono utili e, di conseguenza, una struttura conforme può ad esempio essere conforme a un layout puntatore per eseguire il servizio di tutti i puntatori dalla struttura e dalla matrice conforme che fa parte della struttura conforme. Esistono tuttavia alcune situazioni incorporate che richiedono al motore NDR di eseguire operazioni aggiuntive per elaborare tutti i layout dei puntatori nella sequenza corretta, elaborando ogni puntatore esattamente una volta.

## <a name="what-the-compiler-generates"></a>Elementi generati dal compilatore

Ogni oggetto illustrato in questa sezione contiene puntatori, quindi, ad esempio, una struttura conforme ha puntatori nella parte della struttura e negli elementi della matrice. L'elemento è una struttura semplice con un puntatore .

1.  Struttura conforme, livello singolo

    Il descrittore conforme ha una parte PP in cui vengono descritti tutti i puntatori, sia dalla struttura che dalla matrice. L'elenco di membri ha FC \_ LONG al posto di un puntatore. Il descrittore di matrice CARRAY include elementi tramite l'uso di un oggetto complesso incorporato \_ e nessun descrittore di puntatore. L'elemento ha ancora il relativo descrittore di puntatore singolo. Il layout del puntatore precede il layout dei membri in una struttura conforme e in descrittori di struttura semplici.

2.  Struttura conforme, due o più livelli

    La descrizione PP contiene puntatori di tutti i livelli. Riutilizza la stessa descrizione della matrice della struttura conforme interna. L'elenco di membri ha FC \_ LONG al posto di un puntatore. Una struttura incorporata passa attraverso l'uso di un complesso incorporato. Il descrittore di struttura conforme viene riutilizzato così come è. Anche le dimensioni della parte piana della struttura sono complete, vale a dire che le dimensioni della struttura di primo livello includerebbero le dimensioni piatte della struttura incorporata.

3.  Struttura complessa, livello singolo

    I membri del puntatore sono contrassegnati da FC \_ POINTER. Il layout del puntatore è semplificato in modo che sia presente un descrittore di puntatore (4 byte) per ogni voce \_ FC POINTER nell'elenco. Il layout del puntatore viene gestito in parallelo con una procedura dettagliata dei membri, in altre informazioni, un PUNTATORe FC \_ determina l'elaborazione della descrizione del puntatore successiva. La matrice CARRAY ha il layout del puntatore con tutti i descrittori della matrice e quindi dell'elemento, tramite l'uso di una complessa incorporata. Il descrittore dell'elemento viene riutilizzato. Le dimensioni della parte piana della struttura vengono completate; in altre parole, le dimensioni flat della struttura di primo livello includono le dimensioni flat della struttura incorporata. Il layout dei membri precede il layout del puntatore per le strutture complesse.

    Di conseguenza, la generazione della descrizione della matrice conforme è diversa a seconda che si tratta di una matrice all'interno di una struttura conforme o all'interno di una struttura complessa.

4.  Struttura complessa, 2 o più livelli, complessa in complessa

    La struttura complessa di primo livello ha i puntatori ai membri, la struttura complessa incorporata ha i relativi puntatori ai membri. Il descrittore della struttura conforme viene riutilizzato. Il descrittore di matrice dall'alto è la matrice riutilizzata dalla struttura incorporata.

5.  Struttura complessa con una struttura conforme incorporata

    La struttura conforme top=level ha i relativi puntatori ai membri. Il descrittore di struttura conforme viene riutilizzato così come è. Il descrittore di matrice viene riutilizzato dalla struttura conforme incorporata. in altre parole, non ha puntatori al descrittore di matrice. L'elemento ha il relativo descrittore di puntatore.

6.  Matrici di strutture con puntatori

    Una matrice di strutture semplici con puntatori viene generata come SMFARRAY o CARRAY a seconda che la matrice sia ridimensionata, ma in entrambi i casi ha un layout del puntatore completo (FIXED REPEAT o \_ VARIABLE \_ REPEAT). Il layout del puntatore viene prima del layout del membro.

    Una matrice di strutture complesse con puntatori viene generata come ARRAY BOGUS indipendentemente dal fatto che sia fissa o ridimensionata e in entrambi i casi non ha \_ alcun layout del puntatore.

## <a name="what-the-ndr-engine-does"></a>Funzione del motore di routing di rete

In questa sezione viene descritto il comportamento del motore NDR.

**Passaggio di marshalling**

1.  Strutture conformi e struttura conforme incorporata.

    La struttura di primo livello si comporta come una struttura a livello singolo.

2.  Struttura complessa incorporata con matrice conforme

    Qualsiasi struttura complessa forza la struttura esterna a essere una struttura complessa. La struttura incorporata non effettua mai il marshalling della relativa matrice. Ogni struttura passa sempre attraverso puntatori incorporati semplicemente effettuando il marshalling dei membri e un membro che si verifica come puntatore \_ FC.

3.  Struttura complessa con struttura conforme

    La struttura conforme più in alto incorporata effettua il marshalling della matrice conforme e di tutti i puntini di riferimento. Il motore NDR non scende mai a strutture conformi annidate più approfondite, se presenti; Ciò semplifica la soluzione, poiché una struttura conforme è un oggetto foglia per quanto riguarda il marshalling degli oggetti incorporati. La struttura complessa di primo livello ignora il marshalling delle matrici.

**Unmarshaling, bufsizing e freeing pass**

L'unmarsshaling è simmetrico al marshalling. La prima operazione eseguita per le strutture complesse è individuare la posizione dei punti nel buffer tramite la chiamata alla funzione **NdrComplexStructBufferSize.** Quindi unmarshals punta in parallelo, abilitando lo stesso schema per l'unmarsshaling corretto dei puntini di puntamento da usare. Non deve esserci confusione sugli oggetti ridimensionati e sulle unioni. L'immagine di memoria non deve essere usata per gli oggetti ridimensionati e le unioni, solo per il contenuto del buffer.

I flag usati per eseguire correttamente il marshalling e l'unmarsshaling vengono usati nello stesso modo per il bufsizing e la liberazione per assicurarsi che i punti vengano accodati esattamente una volta.

**Passaggio di endianess**

All'inizio, il passaggio di endianess è simile al marshalling/unmarshaling; Per elaborare strutture complesse sono necessari due passaggi. Il primo passaggio converte la parte flat e trova la posizione dei punti nel buffer in modo simile a come il bufsizing esegue questa operazione per l'unmarshaling. Il secondo passaggio converte quindi i puntini.

I passaggi di endianess differiscono nel modo seguente: ogni struttura e ogni membro deve essere messo fino a quando il membro o l'elemento foglia non è un tipo semplice. Questo è diverso dall'unmarshaling. nell'unmarshaling, ad esempio, non è mai necessario elaborare strutture conformi incorporate in strutture conformi o qualsiasi membro della struttura conforme. Un altro problema è che la conversione non è un'operazione idempotente, quindi il passaggio di unmarshaling potrebbe annullare l'unmarsshaling di alcune parti senza danni, mentre la conversione deve essere eseguita esclusivamente una volta per ogni tipo semplice.

Di conseguenza, l'algoritmo di endianess può essere riepilogato come segue. Il rapporto di mancato recapito ha una nozione di struttura conforme di primo livello e un flag per contrassegnare tale elemento, in base alle esigenze. Quando si percorre la prima volta, ad esempio per convertire la parte piana e per ottenere la posizione dei puntini, questa nozione non viene usata. Il rapporto di mancato recapito scenderebbe attraverso le parti flat di tutti i livelli di strutture e non si azzarderebbe mai nell'elaborazione dei puntatori. Infine, il rapporto di mancato recapito converte la matrice al livello superiore.

Quando si passa la seconda volta, il flag viene usato per contrassegnare il passaggio del puntatore incorporato per evitare di immettere livelli più approfonditi delle strutture conformi, quindi la struttura più conforme. In questo modo, il flag forza il comportamento comune di marshalling/unmarshaling, che consente di evitare di decrescere in livelli più profondi di strutture conformi.

Il secondo passaggio per le strutture complesse con matrici conformi funziona come segue: le strutture complesse funzionano in modo comune; ciò significa che i livelli più approfonditi non guarderebbe mai o ignorano le dimensioni conformi o le matrici conformi e preferirebbe semplicemente esaminare i membri senza toccare la matrice.

Per le strutture complesse con strutture conformi, la struttura conforme deve sapere se è di livello superiore e se si trova in una struttura complessa. La parte flat della matrice viene elaborata dalla struttura più conforme all'inizio. Al secondo passaggio, la struttura più conforme in alto ignora la parte piana e passa attraverso il layout del puntatore e restituisce . La struttura più complessa ignora la parte piana e ignora anche il layout del puntatore.

**L'aspetto solido del percorso di endianess**

La procedura di endianess controlla le normali condizioni out-of-the-buffer ed esegue altri controlli di natura non correlata. Non è possibile eseguire i controlli mirati a valori correlati (ad esempio l'argomento di ridimensionamento rispetto alle dimensioni conformi) usando questo passaggio. vengono eseguite in un secondo momento, quando si esegue l'unmarsaling.

 

 




