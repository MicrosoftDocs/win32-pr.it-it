---
title: Matrici variabili
description: In MIDL le dimensioni delle matrici variabili sono fisse. Consentono ai client di passare parti diverse di matrici dai client ai server. Le dimensioni della parte della matrice possono variare da una chiamata all'altro. Tuttavia, le dimensioni della matrice complessiva sono fisse.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3919eed28ef7a9c888d7c23e4ebe12a1db39c97b18fa325c6daf8a4cd62d6554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010549"
---
# <a name="varying-arrays"></a>Matrici variabili

In MIDL le dimensioni delle matrici variabili sono fisse. Consentono ai client di passare parti diverse di matrici dai client ai server. Le dimensioni della parte della matrice possono variare da una chiamata all'altro. Tuttavia, le dimensioni della matrice complessiva sono fisse.

Ad esempio, nell'esempio seguente viene illustrata la definizione di una procedura remota in un'interfaccia in un file MIDL. La dimensione della matrice che il client passa al server è fissata dalla costante ARRAY \_ SIZE. L'interfaccia specifica la parte della matrice che il client passa al server nei parametri firstElement e chunkSize.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

La definizione dell'interfaccia usa prima l'attributo MIDL per specificare il numero di indice del primo elemento nella parte della matrice che il client passa al \[ [**\_**](/windows/desktop/Midl/first-is) \] server. \[ [**\_ L'attributo length**](/windows/desktop/Midl/length-is) è che specifica il numero totale di elementi della matrice passati dal \] client. Per altre informazioni su questi attributi MIDL, vedere [Attributi di matrice.](array-attributes.md)

Il frammento di codice seguente illustra come un client può richiamare la procedura remota definita nel file MIDL precedente.


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



Questo frammento chiama la procedura remota MyRemoteProc due volte. Alla prima chiamata passa gli elementi della matrice numerati da 20 a 119, come indicato dai valori nelle variabili firstArrayElementNumber e totalElementsPassed. Nella seconda chiamata, il client passa gli elementi della matrice numerati da 120 a 319.

 

 