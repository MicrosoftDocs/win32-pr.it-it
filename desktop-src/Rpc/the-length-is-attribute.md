---
title: Attributo length_is
description: L'attributo \ size \_ is \ consente di specificare la dimensione massima della matrice.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729791"
---
# <a name="the-length_is-attribute"></a>La \[ lunghezza \_ è \] attribute

La \[ [**dimensione \_ è**](/windows/desktop/Midl/size-is) \] attributo che consente di specificare la dimensione massima della matrice. Quando si tratta dell'unico attributo, vengono trasmessi tutti gli elementi della matrice. Anziché inviare tutti gli elementi della matrice, è possibile specificare gli elementi trasmessi utilizzando l'attributo \[ [**length \_**](/windows/desktop/Midl/length-is) \] , come indicato di seguito:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

Dimensioni descrive l'allocazione mentre la lunghezza descrive la trasmissione. Il numero di elementi trasmessi deve sempre essere minore o uguale al numero di elementi allocati. Il valore associato a **length \_** è sempre minore o uguale a **size \_ è**.

 

 