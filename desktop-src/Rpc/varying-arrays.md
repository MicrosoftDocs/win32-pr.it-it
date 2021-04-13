---
title: Matrici variabili
description: In MIDL, le matrici variabili hanno dimensioni fisse. Consentono ai client di passare parti diverse di matrici dai client ai server. La dimensione della parte della matrice può variare dalla chiamata alla chiamata. Tuttavia, la dimensione della matrice complessiva è fissa.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473878"
---
# <a name="varying-arrays"></a>Matrici variabili

In MIDL, le matrici variabili hanno dimensioni fisse. Consentono ai client di passare parti diverse di matrici dai client ai server. La dimensione della parte della matrice può variare dalla chiamata alla chiamata. Tuttavia, la dimensione della matrice complessiva è fissa.

Ad esempio, nell'esempio seguente viene illustrata la definizione di una procedura remota in un'interfaccia in un file MIDL. La dimensione della matrice che il client passa al server è fissata dalle dimensioni della matrice di costanti \_ . L'interfaccia specifica la parte della matrice che il client passa al server nei parametri FirstElement e chunkSize.

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

La definizione dell'interfaccia USA prima l'attributo MIDL \[ [**\_**](/windows/desktop/Midl/first-is) \] per specificare il numero di indice del primo elemento nella parte della matrice che il client passa al server. L' \[ [**attributo \_ length**](/windows/desktop/Midl/length-is) indica \] il numero totale di elementi della matrice passati dal client. Per altre informazioni su questi attributi MIDL, vedere [attributi di matrice](array-attributes.md).

Nel frammento di codice seguente viene illustrato come un client può richiamare la procedura remota definita nel file MIDL precedente.


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



Questo frammento chiama due volte la procedura remota MyRemoteProc. Alla prima chiamata passa gli elementi della matrice numerati da 20 a 119, come indicato dai valori nelle variabili firstArrayElementNumber e totalElementsPassed. Alla seconda chiamata, il client passa gli elementi della matrice numerati da 120 a 319.

 

 