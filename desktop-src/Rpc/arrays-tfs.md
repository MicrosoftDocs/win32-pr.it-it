---
title: Matrici (RPC) (TFS)
description: Le categorie di matrici RPC (Remote Procedure Call) includono dimensioni fisse, conformi, variabili conformi, variabili e complesse.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388813"
---
# <a name="arrays-rpc"></a>Matrici (RPC)

Sono state definite diverse categorie di matrici in base alle relative caratteristiche di prestazioni, soprattutto se la matrice può essere copiata in blocchi.

Per alcune categorie, ad esempio una matrice di dimensioni fisse, esistono due tipi di descrittori di matrici. sono indicati da una correzione nel nome del token FC principale.



| Formato carattere | Descrizione                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | Le dimensioni totali del tipo possono essere rappresentate in un int senza segno a 16 bit.    |
| LG               | La dimensione totale del tipo richiede una lunghezza senza segno a 32 bit per essere rappresentata. |



 

Campi comuni alle matrici:

-   \_dimensioni totali

    Dimensioni totali della matrice in memoria, in byte. Corrisponde alla dimensione del Wire dopo l'allineamento. La dimensione totale viene calcolata per le categorie per le quali non esiste un problema di riempimento e le dimensioni sono effettive della matrice.

-   \_dimensioni elemento

    Dimensioni totali in memoria di un singolo elemento della matrice, inclusa la spaziatura interna (questo può verificarsi solo per matrici complesse).

-   \_Descrizione elemento

    Descrizione del tipo di elemento della matrice.

-   \_layout puntatore

    Per ulteriori informazioni, vedere l'argomento relativo al [layout del puntatore](pointer-layout-tfs.md) .

## <a name="fixed-sized-arrays"></a>Matrici a dimensione fissa

Una stringa di formato di matrice a dimensione fissa viene generata per le matrici con una dimensione nota e pertanto può essere copiata in blocchi nel buffer di marshalling. I due formati di descrittori di matrici fisse sono i seguenti.

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

Una matrice conforme può essere copiata in blocco una volta che la dimensione della matrice è nota.

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

La descrizione della conformità \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .

## <a name="conformant-varying-array"></a>Matrice a variazione conforme

Una matrice a variazione conforme può anche essere copiata in blocchi.

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

La descrizione della conformità \_<> e la descrizione della varianza \_<> è un descrittore di correlazione e include 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .

## <a name="varying-array"></a>Matrice variabile

Le matrici variabili hanno due possibilità a seconda della dimensione della matrice.

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

La descrizione della varianza \_<> è un descrittore di correlazione e ha 4 o 6 byte a seconda del [**/robust**](/windows/desktop/Midl/-robust) in uso.

Per matrici variabili incorporate all'interno di una struttura, il campo Offset<2> della descrizione della varianza \_<> è un offset relativo dalla posizione della matrice variabile nella struttura al campo varianza descrittiva. L'offset è in genere relativo all'inizio della struttura.

## <a name="complex-arrays"></a>Matrici complesse

Una matrice complessa è una matrice con un elemento che impedisce che venga copiata in blocco e, di conseguenza, deve essere eseguita un'azione aggiuntiva. Questi elementi rendono un array complesso:

-   tipi semplici: ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), un integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]
-   puntatori di riferimento e interfaccia (tutti i puntatori sulle piattaforme a 64 bit)
-   unioni
-   strutture complesse (per un elenco completo dei motivi per cui una struttura è complessa), vedere l'argomento relativo alla descrizione della struttura complessa.
-   elementi definiti con \[ [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ marshalling utente**](/windows/desktop/Midl/user-marshal)\]
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

La descrizione della conformità \_<> e la descrizione della varianza \_<> è un descrittore di correlazione e include 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) . Se la matrice ha una conformità e/o una varianza, la descrizione della conformità \_<> e/o la descrizione della varianza \_<> campo/i hanno descrizioni valide, in caso contrario i primi 4 byte del descrittore di correlazione vengono impostati su 0xFFFFFFFF. I flag, quando presenti, vengono impostati su zero.

 

 
