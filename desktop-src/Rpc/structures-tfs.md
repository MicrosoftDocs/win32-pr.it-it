---
title: Strutture (RPC)
description: Descrizione dei vari tipi di strutture in RPC (Remote Procedure Call).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047089"
---
# <a name="structures-rpc"></a>Strutture (RPC)

Esistono diverse categorie di strutture, progressivamente più complesse in termini di azioni necessarie per il marshalling. Iniziano con una struttura semplice che può essere interamente copiata in blocchi e continuare a una struttura complessa che deve essere gestita campo per campo.

-   [Struttura semplice](#simple-structure)
-   [Struttura semplice con puntatori](#simple-structure-with-pointers)
-   [Struttura conforme](#conformant-structure)
-   [Struttura conforme con puntatori](#conformant-structure-with-pointers)
-   [Struttura variabile conforme (con o senza puntatori)](#conformant-varying-structure-with-or-without-pointers)
-   [Struttura hardware](#hard-structure)
-   [Struttura complessa](#complex-structure)
-   [Descrizione layout membri struttura](#structure-member-layout-description)

> [!Note]  
> Rispetto alle categorie di matrici, diventa chiaro che è possibile descrivere solo le strutture di dimensioni fino a 64K (le dimensioni sono per la parte piatta della struttura), ovvero non esiste alcun equivalente di matrici SM e LG.

 

**Membri comuni alle strutture**

-   **allineamento**

    Allineamento necessario del buffer prima dell'unmarshalling della struttura. I valori validi sono 0, 1, 3 e 7 (l'allineamento effettivo meno 1).

-   **\_Dimensioni memoria**

    Dimensione della struttura in memoria in byte. per le strutture conformi questa dimensione non include la dimensione della matrice.

-   **offset \_ nella \_ Descrizione della matrice \_**

    Offset dal puntatore della stringa di formato corrente alla descrizione della matrice conforme contenuta in una struttura.

-   **layout del membro \_**

    Descrizione di ogni elemento della struttura. Le routine NDR devono solo esaminare questa parte della stringa di formato di un tipo se è necessaria la trasformazione endian o se il tipo è una struttura complessa.

-   **\_layout puntatore**

    Vedere la sezione del [layout del puntatore](pointer-layout-tfs.md) .

## <a name="simple-structure"></a>Struttura semplice

Una struttura semplice contiene solo tipi di base, matrici fisse e altre strutture semplici. La caratteristica principale della struttura semplice è che può essere copiata in blocco nel suo complesso.

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>Struttura semplice con puntatori

Una struttura semplice con puntatori contiene solo i tipi di base, i puntatori, le matrici fisse, le strutture semplici e altre strutture semplici con i puntatori. Poiché la<> del layout deve essere visitata solo quando si esegue una conversione di, viene inserita alla fine della descrizione.

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>Struttura conforme

Una struttura conforme contiene solo tipi di base, matrici fisse e strutture semplici e deve contenere una stringa conforme o una matrice conforme. Questa matrice può essere effettivamente contenuta in un'altra struttura o struttura conforme con i puntatori incorporati nella struttura.

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>Struttura conforme con puntatori

Una struttura conforme con puntatori contiene solo i tipi di base, i puntatori, le matrici fisse, le strutture semplici e le strutture semplici con i puntatori; una struttura conforme deve contenere una matrice conforme. Questa matrice può essere effettivamente contenuta in un'altra struttura o struttura conforme con puntatori incorporati nella struttura.

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>Struttura variabile conforme (con o senza puntatori)

Una struttura a variazione conforme contiene solo tipi semplici, puntatori, matrici fisse, strutture semplici e strutture semplici con i puntatori; una struttura a variazione conforme deve contenere una stringa conforme o una matrice a variazione conforme. La stringa o la matrice conforme può essere effettivamente contenuta in un'altra struttura o struttura conforme con puntatori incorporati nella struttura.

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>Struttura hardware

La struttura hardware era un concetto mirato a eliminare sanzioni ripide correlate all'elaborazione di strutture complesse. Deriva da un'osservazione che una struttura complessa ha in genere solo una o due condizioni che impediscono la copia dei blocchi e pertanto ne danneggiano le prestazioni rispetto a una struttura semplice. I colpevoli sono in genere unioni o campi di enumerazione.

Una struttura rigida è una struttura con un enum16, un riempimento finale in memoria o un'Unione come ultimo membro. Questi tre elementi impediscono alla struttura di rientrare in una delle categorie di struttura precedenti, che sfruttano il sovraccarico dell'interpretazione di piccole dimensioni e il potenziale massimo di ottimizzazione, ma non forzano la categoria della struttura molto costosa.

Il enum16 non deve causare differenze tra la memoria e le dimensioni dei cavi della struttura. La struttura non può contenere matrici conformi, né puntatori (a meno che non faccia parte dell'Unione); gli unici altri membri consentiti sono tipi di base, matrici fisse e strutture semplici.

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

Il \_ campo Offset enum<2> fornisce l'offset dall'inizio della struttura in memoria a un enum16 se ne contiene uno; in caso contrario, l' \_ offset enum<2> campo è-1.

Il \_ campo Copy size<2> fornisce il numero totale di byte nella struttura, che può essere copiato in un blocco nel/dal buffer. Il totale non include alcuna unione finale né alcun riempimento finale nella memoria. Questo valore rappresenta anche la quantità di incremento del puntatore del buffer dopo la copia.

Il \_ \_ campo incr<2> per la copia di MEM è il numero di byte che il puntatore di memoria deve incrementare dopo la copia di blocco prima di gestire qualsiasi unione finale. L'incremento in base a questa quantità (non in base alle dimensioni della copia \_<2> byte) restituisce un puntatore di memoria appropriato a qualsiasi unione finale.

## <a name="complex-structure"></a>Struttura complessa

Una struttura complessa è una struttura che contiene uno o più campi che impediscono la copia del blocco della struttura o per cui è necessario eseguire un controllo aggiuntivo durante il marshalling o l'unmarshalling, ad esempio i controlli associati in un'enumerazione. I tipi di NDR seguenti rientrino in questa categoria:

-   [tipi semplici](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), un integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]
-   riempimento allineamento alla fine della struttura
-   puntatori a interfaccia (utilizzano un complesso incorporato)
-   puntatori ignorati (correlati all'attributo \[ [**Ignore**](/windows/desktop/Midl/ignore) \] e al \_ token FC Ignore)
-   matrici complesse, matrici variabili, matrici di stringhe
-   matrici conformi a più dimensioni con almeno una dimensione non fissa
-   unioni
-   elementi definiti con \[ [**trasmissione \_ come**](/windows/desktop/Midl/transmit-as) \] , \[ [**rappresentano \_ come**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ marshalling del Wire**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ marshalling utente**](/windows/desktop/Midl/user-marshal)\]
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

La \_ dimensione della memoria<2> campo corrisponde alla dimensione della struttura in memoria, in byte.

Se la struttura contiene una matrice conforme, l'offset \_ a una \_ Descrizione della matrice conforme \_ \_<2> campo fornisce l'offset alla descrizione della matrice conforme; in caso contrario, è zero.

Se la struttura dispone di puntatori, l'offset \_ al \_ layout del puntatore \_<2> campo fornisce l'offset oltre il layout della struttura al layout del puntatore, in caso contrario questo campo è zero.

Il layout del puntatore \_<> campo di una struttura complessa viene gestito in modo diverso rispetto alle altre strutture. Il layout del puntatore \_<> campo di una struttura complessa contiene solo le descrizioni dei campi del puntatore effettivi nella struttura stessa. Tutti i puntatori contenuti all'interno di matrici, unioni o strutture incorporate non sono descritti nel campo di layout del puntatore della struttura complessa \_<> campo.

> [!Note]  
> Questo si differenzia dalle altre strutture, che duplicano la descrizione di tutti i puntatori contenuti in matrici o strutture incorporate nel proprio layout di puntatore \_<> campo.

 

Anche il formato del layout del puntatore di una struttura complessa è radicalmente diverso. Poiché contiene solo le descrizioni dei membri effettivi del puntatore e perché viene effettuato il marshalling di una struttura complessa e viene eseguito l'unmarshalling di un campo alla volta, il layout del puntatore \_<> campo contiene semplicemente la descrizione del puntatore di tutti i membri del puntatore. Non è presente alcun inizio FC \_ PP e nessuno dei normali layout del puntatore \_<> informazioni.

## <a name="structure-member-layout-description"></a>Descrizione layout membri struttura

La descrizione del layout di una struttura contiene uno o più dei caratteri di formato seguenti:

-   Qualsiasi carattere di tipo di base, ad esempio FC \_ char e così via
-   Direttive di allineamento. Sono disponibili tre caratteri di formato che specificano l'allineamento del puntatore di memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 e FC \_ ALIGNM8.
    > [!Note]  
    > Sono presenti anche token di allineamento del buffer, FC \_ ALIGNB2 tramite FC \_ ALIGNM8. questi non vengono usati.

     

-   Riempimento memoria. Questi si verificano solo alla fine della descrizione di una struttura e indicano il numero di byte di riempimento in memoria prima della matrice conforme nella struttura: FC \_ STRUCTPADn, dove n è il numero di byte di spaziatura interna.
-   Qualsiasi tipo non di base incorporato (si noti, tuttavia, che una matrice conforme non si verifica mai nel layout della struttura). Questa operazione ha una descrizione di 4 byte:

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    Se non è garantito che l'offset sia allineato a 2 byte.

    \_il riquadro memoria<1> è una spaziatura interna necessaria in memoria prima del campo complesso.

    offset \_ alla \_ Descrizione<2> è un offset di tipo relativo al tipo incorporato.

Potrebbe anche essere presente un \_ Pad FC prima del termine FC di terminazione \_ , se necessario, per garantire che la stringa di formato venga allineata a un limite di 2 byte dopo l' \_ estremità FC.

 

 