---
title: Matrici conformi
description: Le dimensioni di una matrice conforme possono variare o essere conformi ogni volta che il client la passa a una procedura remota nel server.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19766b7b9552bcab08a4d194629892e51d5185ed39b0bedddbaef32f08cececf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073431"
---
# <a name="conformant-arrays"></a>Matrici conformi

Le dimensioni di una matrice conforme possono variare o essere conformi ogni volta che il client la passa a una procedura remota nel server. La definizione dell'interfaccia nel file MIDL dell'applicazione consente al client di specificare le dimensioni della matrice ogni volta che richiama la procedura remota. Usare parentesi quadre vuote ( ) o un asterisco tra parentesi quadre ( ) nella definizione della matrice per indicare \[ \] una matrice \[ \* \] conforme.

L'esempio seguente contiene la definizione di una procedura remota in un'interfaccia in un file MIDL. Il client specifica le dimensioni della matrice che passa al server dal parametro *arraySize.*

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

La definizione dell'interfaccia usa le dimensioni dell'attributo MIDL per specificare le dimensioni della matrice che il client passa al \[ [**\_**](/windows/desktop/Midl/size-is) \] server. Se si preferisce indicare il valore massimo dei numeri di indice della matrice, usare invece \[ [**\_ l'attributo max**](/windows/desktop/Midl/max-is) \] is. Per altre informazioni su questi attributi MIDL, vedere [Attributi di matrice.](array-attributes.md)

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



Questo frammento chiama la procedura remota MyRemoteProc due volte. Alla prima chiamata passa una matrice di 20 elementi. Nella seconda chiamata, il client passa una matrice di 200 elementi.

 

 