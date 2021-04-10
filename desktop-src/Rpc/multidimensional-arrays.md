---
title: Matrici multidimensionali
description: Gli attributi di matrice possono essere usati anche con matrici multidimensionali.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb7bcf94d97e1f35fdd6ab432ea5869e47f79ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963301"
---
# <a name="multidimensional-arrays"></a>Matrici multidimensionali

Gli attributi di matrice possono essere usati anche con matrici multidimensionali. Tuttavia, prestare attenzione a garantire che ogni dimensione della matrice disponga di un attributo corrispondente. Ad esempio:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d( [in] short        d1size,
              [in] short        d2len,
              [in, size_is( d1size, ), length_is ( , d2len) ] long array2d[*][30] ) ;
}
```

La matrice precedente è una matrice conforme (di dimensioni d1size) di 30 matrici di elementi (con gli elementi D2LEN spediti per ogni). La virgola tra le parentesi della \[ [**dimensione \_ è**](/windows/desktop/Midl/size-is) \] attribute specifica che il valore in d1size viene applicato alla prima dimensione della matrice. Analogamente, il comando tra le parentesi della \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) \] attributo indica che il valore in D2LEN viene applicato alla seconda dimensione della matrice.

Il compilatore MIDL 2,0 fornisce due metodi per il marshalling dei parametri: modalità mista (/**OS**) e completamente interpretato (/**OIF** o/**Oicf**). Per impostazione predefinita, il compilatore MIDL compila le interfacce in modalità mista. Non è necessario specificare in modo esplicito l'opzione [**/OS**](/windows/desktop/Midl/-os) per ottenere il marshalling in modalità mista.

Il metodo completamente interpretato esegue il marshalling dei dati completamente offline. In questo modo si riduce considerevolmente le dimensioni del codice dello stub, ma si riducono anche le prestazioni. Nel marshalling in modalità mista, gli stub eseguono il marshalling di alcuni parametri online. Sebbene il risultato sia un numero maggiore di dimensioni dello stub, offre prestazioni migliori.

> [!Caution]  
> Prestare attenzione quando si compilano file IDL in questa modalità. L'utilizzo di matrici multidimensionali in modalità mista può causare la mancata corretta marshalling dei parametri. L'opzione della riga di comando [**/Oicf**](/windows/desktop/Midl/-oi) è consigliata quando l'interfaccia definisce parametri che sono matrici multidimensionali.

 

L' \[ attributo [**stringa**](/windows/desktop/Midl/string) \] può essere utilizzato anche con matrici multidimensionali. L'attributo si applica alla dimensione meno significativa, ad esempio una matrice di stringhe conforme. È inoltre possibile utilizzare gli attributi del puntatore multidimensionale. Ad esempio:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface multiarray
{
  void arr2d([in] short  d1len,
             [in] short  d2len,
             [in] size_is(d1len, d2len) ] long  ** ptr2d) ;
}
```

Nell'esempio precedente, la variabile ptr2d è un puntatore a un blocco di puntatori di dimensioni d1len, ognuno dei quali punta a D2LEN puntatori a **Long**.

Le matrici multidimensionali non sono equivalenti a matrici di puntatori. Una matrice multidimensionale è un singolo blocco di dati di grandi dimensioni in memoria. Una matrice di puntatori contiene solo un blocco di puntatori nella matrice. I dati a cui puntano i puntatori possono trovarsi in qualsiasi punto della memoria. Inoltre, la sintassi ANSI C consente di non specificare in una matrice multidimensionale solo la dimensione di matrice più significativa (più a sinistra). Di conseguenza, di seguito è riportata un'istruzione valida:

`long a1[] [20]`

Confrontare questa operazione con l'istruzione non valida seguente:

`long a1[20] []`

 

 