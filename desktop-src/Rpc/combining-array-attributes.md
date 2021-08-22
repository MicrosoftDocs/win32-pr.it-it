---
title: Combinazione di attributi di matrice
description: Gli attributi di campo possono essere forniti in varie combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd440251a658dd5b888df7275f578369419d4b8b2d4f920b263bc5095c4bd948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931754"
---
# <a name="combining-array-attributes"></a>Combinazione di attributi di matrice

Gli attributi di campo possono essere forniti in varie combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server. Le relazioni tra gli attributi vengono definite usando le formule seguenti:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

I valori associati agli attributi devono rispettare diverse regole di senso comune basate su tali formule. Queste regole sono:

-   Non specificare un primo \[ [**è un \_ valore**](/windows/desktop/Midl/first-is) \] di indice minore di zero o un ultimo \[ [**\_ è**](/windows/desktop/Midl/last-is) \] il valore maggiore di max \[ [**\_ è**](/windows/desktop/Midl/max-is) \] .
-   Non specificare una dimensione negativa per una matrice. Definire il primo e l'ultimo elemento in modo che il risultato sia un valore di lunghezza pari a zero o maggiore. Definire il \[ [**valore max \_ is**](/windows/desktop/Midl/max-is) \] in modo che la dimensione sia uguale o maggiore di zero. Se MIDL è stato richiamato con l'opzione [**/error**](/windows/desktop/Midl/-error) bounds check, lo stub genera un'eccezione quando la dimensione è minore di zero o la lunghezza trasmessa è minore \_ di zero.
-   Non usare gli attributi length is e last is contemporaneamente, né la dimensione \[ [**\_**](/windows/desktop/Midl/length-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] \[ **\_ è** \] \[ **e \_ l'ultimo** \] è contemporaneamente.

A causa della relazione di chiusura in C tra matrici e puntatori, MIDL consente anche di dichiarare matrici negli elenchi di parametri usando la notazione del puntatore. MIDL considera un parametro che è un puntatore a un tipo come una matrice di quel tipo se il parametro ha uno degli attributi comunemente associati alle matrici.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

Nell'esempio precedente i parametri di matrice e puntatore nelle funzioni fArray6 e fArray7 sono equivalenti.

 

 