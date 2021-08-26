---
title: Strutture (RPC)
description: Descrizione dei vari tipi di strutture in RPC (Remote Procedure Call).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1783508a834ce2fa3d93d3db04edc1de362d6f888c29511c1eb6852cce0e83ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017411"
---
# <a name="structures-rpc"></a>Strutture (RPC)

Esistono diverse categorie di strutture, progressivamente più complesse in termini di azioni necessarie per il marshalling. Iniziano con una struttura semplice che può essere copiata in blocchi nel suo complesso e continuano con una struttura complessa che deve essere utilizzata campo per campo.

-   [Struttura semplice](#simple-structure)
-   [Struttura semplice con puntatori](#simple-structure-with-pointers)
-   [Struttura conforme](#conformant-structure)
-   [Struttura conforme ai puntatori](#conformant-structure-with-pointers)
-   [Struttura variabile conforme (con o senza puntatori)](#conformant-varying-structure-with-or-without-pointers)
-   [Struttura rigida](#hard-structure)
-   [Struttura complessa](#complex-structure)
-   [Descrizione del layout dei membri della struttura](#structure-member-layout-description)

> [!Note]  
> Rispetto alle categorie di matrici, risulta evidente che è possibile descrive solo le strutture con dimensioni fino a 64 KB (la dimensione è per la parte piana della struttura), ovvero non esiste un equivalente di matrici SM e LG.

 

**Membri comuni alle strutture**

-   **Allineamento**

    Allineamento necessario del buffer prima di annullare ilmarshaling della struttura . I valori validi sono 0, 1, 3 e 7 (l'allineamento effettivo meno 1).

-   **dimensioni \_ della memoria**

    Dimensioni della struttura in memoria in byte. per le strutture conformi, questa dimensione non include le dimensioni della matrice.

-   **offset \_ alla \_ descrizione della \_ matrice**

    Offset dal puntatore della stringa di formato corrente alla descrizione della matrice conforme contenuta in una struttura .

-   **\_layout dei membri**

    Descrizione di ogni elemento della struttura . Le routine NDR devono esaminare questa parte della stringa di formato di un tipo solo se è necessaria la trasformazione endian o se il tipo è una struttura complessa.

-   **layout del \_ puntatore**

    Vedere la sezione [Pointer Layout (Layout puntatore).](pointer-layout-tfs.md)

## <a name="simple-structure"></a>Struttura semplice

Una struttura semplice contiene solo tipi di base, matrici fisse e altre strutture semplici. La caratteristica principale della struttura semplice è che può essere copiata in blocchi nel suo complesso.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Struttura semplice con puntatori

Una struttura semplice con puntatori contiene solo tipi di base, puntatori, matrici fisse, strutture semplici e altre strutture semplici con puntatori. Poiché il layout<> deve essere visitato solo quando si esegue una conversione endianess, viene inserito alla fine della descrizione.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Struttura conforme

Una struttura conforme contiene solo tipi di base, matrici fisse e strutture semplici e deve contenere una stringa conforme o una matrice conforme. Questa matrice potrebbe essere effettivamente contenuta in un'altra struttura conforme o conforme con puntatori incorporati in questa struttura.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Struttura conforme ai puntatori

Una struttura conforme con puntatori contiene solo tipi di base, puntatori, matrici fisse, strutture semplici e strutture semplici con puntatori; Una struttura conforme deve contenere una matrice conforme. Questa matrice potrebbe essere effettivamente contenuta in un'altra struttura conforme o in una struttura conforme con puntatori incorporati in questa struttura.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Struttura variabile conforme (con o senza puntatori)

Una struttura variabile conforme contiene solo tipi semplici, puntatori, matrici fisse, strutture semplici e strutture semplici con puntatori; Una struttura variabile conforme deve contenere una stringa conforme o una matrice di variabili conformi. La stringa o la matrice conforme può essere effettivamente contenuta in un'altra struttura conforme o in una struttura conforme con puntatori incorporati in questa struttura.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Struttura rigida

La struttura rigida era un concetto che mirava a eliminare le gravi penalità correlate all'elaborazione di strutture complesse. Deriva da un'osservazione del fatto che una struttura complessa presenta in genere solo una o due condizioni che impediscono la copia dei blocchi e quindi ne distoglie le prestazioni rispetto a una struttura semplice. I responsabili sono in genere unioni o campi di enumerazione.

Una struttura rigida è una struttura che ha un enum16, un riempimento finale in memoria o un'unione come ultimo membro. Questi tre elementi impediscono alla struttura di entrare in una delle categorie di struttura precedenti, che hanno un sovraccarico di interpretazione ridotto e il massimo potenziale di ottimizzazione, ma non la forzano nella categoria di struttura molto complessa.

L'enumerazione 16 non deve causare differenze tra le dimensioni di memoria e di collegamento della struttura. La struttura non può avere alcuna matrice conforme, né puntatori (a meno che non sia parte dell'unione); gli unici altri membri consentiti sono i tipi di base, le matrici fisse e le strutture semplici.

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

L'offset dell'enumerazione<2> fornisce l'offset dall'inizio della struttura in memoria a un enum16 se ne contiene uno. In caso contrario, l'offset di enumerazione<2> campo \_ \_ è -1.

Il campo copy size<2> indica il numero totale di byte nella struttura, che può essere copiato in blocchi nel \_ buffer o dal buffer. Questo totale non include alcuna unione finale né la spaziatura interna finale in memoria. Questo valore è anche la quantità in cui il puntatore del buffer deve essere incrementato dopo la copia.

Il campo mem copy incr<2> è il numero di byte che il puntatore di memoria deve incrementare dopo la copia in blocchi prima di gestire qualsiasi unione \_ \_ finale. L'incremento di questa quantità (non per dimensioni di copia<2> byte) produce un puntatore di memoria appropriato a qualsiasi \_ unione finale.

## <a name="complex-structure"></a>Struttura complessa

Una struttura complessa è una struttura contenente uno o più campi che impediscono la copia in blocchi della struttura o per cui è necessario eseguire controlli aggiuntivi durante il marshalling o l'unmarsshaling (ad esempio, controlli associati su un'enumerazione). In questa categoria rientrano i tipi di NDR seguenti:

-   [tipi semplici:](simple-types-tfs.md)ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]
-   spaziatura interna di allineamento alla fine della struttura
-   puntatori a interfaccia (usano un complesso incorporato)
-   puntatori ignorati (correlati \[ [**all'attributo ignore**](/windows/desktop/Midl/ignore) \] e al token FC \_ IGNORE)
-   matrici complesse, matrici variabili, matrici di stringhe
-   Matrici conformi multidimensionali con almeno una dimensione non suffissa
-   unioni
-   Gli elementi definiti con \[ [**trasmettono \_ come**](/windows/desktop/Midl/transmit-as) \] , rappresentano \[ [**\_ come**](/windows/desktop/Midl/represent-as) \] , wire \[ [**\_ marshal,**](/windows/desktop/Midl/wire-marshal) \] \[ [**marshalling \_ utente**](/windows/desktop/Midl/user-marshal)\]
-   strutture complesse incorporate
-   riempimento alla fine della struttura

Una struttura complessa presenta la descrizione del formato seguente:

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

Le dimensioni della<2> campo sono le \_ dimensioni della struttura in memoria, in byte.

Se la struttura contiene una matrice conforme, l'offset alla descrizione della matrice conforme<2 campo> fornisce \_ l'offset alla descrizione della matrice conforme, in caso contrario è \_ \_ \_ zero.

Se la struttura contiene puntatori, l'offset al layout dell'indicatore di misura<2> fornisce l'offset oltre il layout della struttura al layout del puntatore; in caso contrario, questo campo è \_ \_ \_ zero.

Il layout del puntatore<> campo di una struttura complessa viene gestito in modo diverso rispetto ad \_ altre strutture. Il layout del puntatore<> campo di una struttura complessa contiene solo le descrizioni \_ dei campi puntatore effettivi nella struttura stessa. Tutti i puntatori contenuti in qualsiasi matrice, unione o struttura incorporata non sono descritti nel layout del puntatore della struttura complessa<> \_ campo.

> [!Note]  
> Questo è in contrasto con altre strutture, che duplicano la descrizione di qualsiasi puntatore contenuto in matrici o strutture incorporate nel proprio layout del puntatore<> \_ campo.

 

Anche il formato del layout del puntatore di una struttura complessa è radicalmente diverso. Poiché contiene solo descrizioni dei membri puntatore effettivi e poiché viene effettuato il marshalling e l'unmarssing di una struttura complessa di un campo alla volta, il layout del puntatore<> campo contiene semplicemente la descrizione del puntatore di tutti i membri del \_ puntatore. Non è presente alcun punto di connessione del punto di controllo iniziale e \_ nessuno dei normali layout del \_ puntatore<> informazioni.

## <a name="structure-member-layout-description"></a>Descrizione del layout dei membri della struttura

La descrizione del layout di una struttura contiene uno o più dei caratteri di formato seguenti:

-   Qualsiasi carattere del tipo di base, ad esempio FC \_ CHAR e così via
-   Direttive di allineamento. Sono disponibili tre caratteri di formato che specificano l'allineamento del puntatore di memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 e FC \_ ALIGNM8.
    > [!Note]  
    > Sono disponibili anche token di allineamento del buffer, da FC \_ ALIGNB2 a FC \_ ALIGNM8, che non vengono usati.

     

-   Riempimento della memoria. Si verificano solo alla fine della descrizione di una struttura e indicano il numero di byte di riempimento in memoria prima della matrice conforme nella struttura: FC STRUCTPADn, dove n è il numero di byte di \_ riempimento.
-   Qualsiasi tipo non di base incorporato (si noti, tuttavia, che una matrice conforme non si verifica mai nel layout della struttura). Questa è una descrizione a 4 byte:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    in cui non è garantito che l'offset sia allineato a 2 byte.

    memory \_ pad<1> è una spaziatura interna necessaria in memoria prima del campo complesso.

    offset \_ alla \_ descrizione<2> è un offset del tipo relativo al tipo incorporato.

Potrebbe anche essere presente un PAD fc prima della terminazione FC END, se necessario, per garantire che la stringa di formato venga allineata a un limite di 2 byte dopo \_ \_ l'END \_ FC.

 

 