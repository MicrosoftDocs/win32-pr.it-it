---
title: Matrici (RPC) (TFS)
description: Le categorie di matrici RPC (Remote Procedure Call) includono dimensioni fisse, conformi, variabili, variabili e complesse.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073491"
---
# <a name="arrays-rpc"></a>Matrici (RPC)

Sono state definite diverse categorie di matrici in base alle caratteristiche delle prestazioni, principalmente se la matrice può essere copiata in blocchi.

Per alcune categorie, ad esempio una matrice di dimensioni fisse, esistono due tipi di descrittori di matrice. sono indicati da un in-fix nel nome del token FC iniziale.



| Carattere di formato | Descrizione                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | Le dimensioni totali del tipo possono essere rappresentate in un valore unsigned int a 16 bit.    |
| LG               | Le dimensioni totali del tipo devono essere rappresentate con una lunghezza senza segno a 32 bit. |



 

Campi comuni alle matrici:

-   dimensioni \_ totali

    Dimensioni totali della matrice in memoria, in byte. Si tratta della stessa dimensione del cavo dopo l'allineamento. Le dimensioni totali vengono calcolate per le categorie per le quali il problema di riempimento non esiste e le dimensioni sono le dimensioni effettive della matrice.

-   dimensione \_ dell'elemento

    Dimensioni totali in memoria di un singolo elemento della matrice, inclusa la spaziatura interna (ciò può verificarsi solo per matrici complesse).

-   Descrizione \_ dell'elemento

    Descrizione del tipo di elemento della matrice.

-   layout del \_ puntatore

    Per altre [informazioni, vedere l'argomento Layout](pointer-layout-tfs.md) puntatore.

## <a name="fixed-sized-arrays"></a>Matrici di dimensioni fisse

Viene generata una stringa di formato matrice di dimensioni fisse per le matrici con dimensioni note e pertanto può essere copiata in blocchi nel buffer di marshalling. I due formati di descrittore di matrice fissi sono i seguenti.

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

e

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>Matrice conforme

Una matrice conforme può essere copiata in blocchi quando le dimensioni della matrice sono note.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

La descrizione della<> è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno usato.

## <a name="conformant-varying-array"></a>Matrice variabile conforme

Una matrice variabile conforme può anche essere copiata in blocchi.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

La descrizione della<> e della varianza<> è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ sia usato [**/robust.**](/windows/desktop/Midl/-robust)

## <a name="varying-array"></a>Matrice variabile

Le matrici variabili hanno due possibilità a seconda delle dimensioni della matrice.

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

La descrizione della<> è un descrittore di correlazione e ha 4 o 6 byte a seconda \_ [**dell'opzione /robust**](/windows/desktop/Midl/-robust) usata.

Per le matrici diverse incorporate all'interno di una struttura, il campo offset<2> della descrizione della varianza<> è un offset relativo dalla posizione della matrice variabile nella struttura al campo di descrizione della \_ varianza. L'offset è in genere relativo all'inizio della struttura .

## <a name="complex-arrays"></a>Matrici complesse

Una matrice complessa è qualsiasi matrice con un elemento che ne impedisce la copia in blocchi e, di conseguenza, è necessario eseguire un'azione aggiuntiva. Questi elementi rendono complessa una matrice:

-   tipi semplici: ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]
-   puntatori di riferimento e di interfaccia (tutti i puntatori su piattaforme a 64 bit)
-   unioni
-   strutture complesse (vedere l'argomento Descrizione della struttura complessa per un elenco completo dei motivi per cui una struttura deve essere complessa)
-   elementi definiti con \[ [**trasmetti \_ come**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ marshalling utente**](/windows/desktop/Midl/user-marshal)\]
-   Tutte le matrici multidimensionali con almeno una dimensione conforme e/o variabile sono complesse indipendentemente dal tipo di elemento sottostante.

La descrizione della matrice complessa è la seguente:

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

Il numero \_ di \_ elementi<2> campo è zero se la matrice è conforme.

La descrizione della<> e della varianza<> è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ sia usato [**/robust.**](/windows/desktop/Midl/-robust) Se la matrice ha conformità e/o varianza, la descrizione della conformità<> e/o la descrizione della varianza<> uno o più campi hanno descrizioni valide, in caso contrario i primi 4 byte del descrittore di correlazione vengono impostati su \_ \_ 0xFFFFFFFF. I flag, se presenti, sono impostati su zero.

 

 
