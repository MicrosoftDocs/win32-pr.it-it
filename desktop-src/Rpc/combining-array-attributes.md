---
title: Combinazione di attributi di matrice
description: Gli attributi di campo possono essere forniti in diverse combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300251"
---
# <a name="combining-array-attributes"></a>Combinazione di attributi di matrice

Gli attributi di campo possono essere forniti in diverse combinazioni, purché lo stub possa usare le informazioni per determinare le dimensioni della matrice e il numero di byte da trasmettere al server. Le relazioni tra gli attributi vengono definite utilizzando le formule seguenti:

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

I valori associati agli attributi devono rispettare diverse regole comuni basate su tali formule. Queste regole sono:

-   Non specificare un \[ [**primo \_**](/windows/desktop/Midl/first-is) \] valore di indice minore di zero o un valore \[ [**Last \_ è**](/windows/desktop/Midl/last-is) \] maggiore di \[ [**Max \_ è**](/windows/desktop/Midl/max-is) \] .
-   Non specificare dimensioni negative per una matrice. Definire il primo e l'ultimo elemento in modo da ottenere un valore di lunghezza pari a zero o superiore. Definire il \[ [**valore \_ massimo**](/windows/desktop/Midl/max-is) in \] modo che le dimensioni siano pari a zero o superiori. Se MIDL è stato richiamato con l'opzione di controllo dei limiti di [**/Error**](/windows/desktop/Midl/-error) \_ , lo stub genera un'eccezione quando la dimensione è minore di zero oppure la lunghezza trasmessa è minore di zero.
-   Non utilizzare la \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) \] e l' \[ [**Ultima \_ è**](/windows/desktop/Midl/last-is) \] Attributes contemporaneamente, né la \[ **dimensione \_ è** \] e l' \[ **Ultima \_ è** \] attribuita allo stesso tempo.

A causa della relazione di chiusura in C tra matrici e puntatori, MIDL consente inoltre di dichiarare matrici negli elenchi di parametri utilizzando la notazione del puntatore. MIDL considera un parametro che è un puntatore a un tipo come matrice di tale tipo se il parametro dispone di uno qualsiasi degli attributi associati comunemente alle matrici.

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

Nell'esempio precedente, i parametri della matrice e del puntatore nelle funzioni fArray6 e fArray7 sono equivalenti.

 

 