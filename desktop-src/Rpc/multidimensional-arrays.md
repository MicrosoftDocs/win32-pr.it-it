---
title: Matrici multidimensionali
description: Gli attributi di matrice possono essere utilizzati anche con matrici multidimensionali.
ms.assetid: a01b904c-fbe8-4af4-8393-6864f7ef7364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f7dac2b6d093fa56383ecaf976a83acf13fec9aa0c3820c1d608ccb69e9e9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928083"
---
# <a name="multidimensional-arrays"></a>Matrici multidimensionali

Gli attributi di matrice possono essere utilizzati anche con matrici multidimensionali. Tuttavia, assicurarsi che ogni dimensione della matrice abbia un attributo corrispondente. Esempio:

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

La matrice precedente è una matrice conforme (di dimensioni d1size ) di 30 matrici di elementi (con elementi d2len forniti per ognuno). La virgola tra parentesi dell'attributo size è specifica che il valore in d1size viene applicato alla prima dimensione della \[ [**\_**](/windows/desktop/Midl/size-is) \] matrice. Analogamente, il comando tra parentesi della lunghezza è l'attributo indica che il valore \[ [**\_**](/windows/desktop/Midl/length-is) in d2len viene applicato alla seconda dimensione \] della matrice.

Il compilatore MIDL 2.0 fornisce due metodi per il marshalling dei parametri: in modalità mista **(/Os**) e completamente interpretati (/**Oif** o /**Oicf**). Per impostazione predefinita, il compilatore MIDL compila le interfacce in modalità mista. Non è necessario specificare in modo esplicito [**l'opzione /Os**](/windows/desktop/Midl/-os) per ottenere il marshalling in modalità mista.

Il metodo completamente interpretato effettua il marshalling dei dati completamente offline. Ciò riduce notevolmente le dimensioni del codice stub, ma comporta anche una riduzione delle prestazioni. Nel marshalling in modalità mista, gli stub effettuano il marshalling di alcuni parametri online. Anche se ciò comporta una dimensione di stub maggiore, offre anche prestazioni migliori.

> [!Caution]  
> Prestare attenzione durante la compilazione di file IDL in questa modalità. L'uso di matrici multidimensionali in modalità mista può comportare parametri di cui non è stato eseguito correttamente il marshalling. L'opzione della riga di comando [**/Oicf**](/windows/desktop/Midl/-oi) è consigliata quando l'interfaccia definisce parametri che sono matrici multidimensionali.

 

\[ [**L'attributo**](/windows/desktop/Midl/string) \] stringa può essere usato anche con matrici multidimensionali. L'attributo si applica alla dimensione meno significativa, ad esempio una matrice di stringhe conforme. È anche possibile usare gli attributi del puntatore multidimensionale. Esempio:

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

Nell'esempio precedente la variabile ptr2d è un puntatore a un blocco di puntatori di dimensioni d1len, ognuno dei quali punta a puntatori d2len a **long.**

Le matrici multidimensionali non sono equivalenti alle matrici di puntatori. Una matrice multidimensionale è un singolo blocco di dati di grandi dimensioni in memoria. Una matrice di puntatori contiene solo un blocco di puntatori nella matrice. I dati a cui puntano i puntatori possono essere in qualsiasi punto della memoria. Inoltre, la sintassi ANSI C consente di non specificare solo la dimensione di matrice più significativa (più a sinistra) in una matrice multidimensionale. Di conseguenza, di seguito è riportata un'istruzione valida:

`long a1[] [20]`

Confrontarlo con l'istruzione non valida seguente:

`long a1[20] []`

 

 