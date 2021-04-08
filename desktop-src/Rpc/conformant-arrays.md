---
title: Matrici conformi
description: La dimensione di una matrice conforme può variare o essere conforme ogni volta che il client la passa a una procedura remota sul server.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047195"
---
# <a name="conformant-arrays"></a>Matrici conformi

La dimensione di una matrice conforme può variare o essere conforme ogni volta che il client la passa a una procedura remota sul server. La definizione dell'interfaccia nel file MIDL dell'applicazione consente al client di specificare la dimensione della matrice ogni volta che richiama la procedura remota. Usare parentesi quadre vuote ( \[ \] ) o un asterisco tra parentesi quadre ( \[ \* \] ) nella definizione di matrice per indicare una matrice conforme.

L'esempio seguente contiene la definizione di una procedura remota in un'interfaccia in un file MIDL. Il client specifica la dimensione della matrice passata al server dal parametro *arraySize*.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

La definizione dell'interfaccia usa la dimensione dell'attributo MIDL \[ [**\_**](/windows/desktop/Midl/size-is) \] per specificare le dimensioni della matrice che il client passa al server. Se si preferisce indicare il valore massimo dei numeri di indice della matrice, usare invece l' \[ attributo [**Max \_ is**](/windows/desktop/Midl/max-is) \] . Per altre informazioni su questi attributi MIDL, vedere [attributi di matrice](array-attributes.md).

Nel frammento di codice seguente viene illustrato come un client può richiamare la procedura remota definita nel file MIDL precedente.


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



Questo frammento chiama due volte la procedura remota MyRemoteProc. Alla prima chiamata passa una matrice di 20 elementi. Alla seconda chiamata, il client passa una matrice di 200 elementi.

 

 