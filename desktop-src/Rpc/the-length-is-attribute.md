---
title: Attributo length_is
description: L'attributo \ size \_ is\ consente di specificare le dimensioni massime della matrice.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924260"
---
# <a name="the-length_is-attribute"></a>La \[ lunghezza \_ è \] Attribute

\[ [**\_ L'attributo size**](/windows/desktop/Midl/size-is) è che consente di specificare le dimensioni \] massime della matrice. Quando questo è l'unico attributo, vengono trasmessi tutti gli elementi della matrice. Anziché inviare tutti gli elementi della matrice, è possibile specificare gli elementi trasmessi usando \[ [**l'attributo length \_ is,**](/windows/desktop/Midl/length-is) \] come indicato di seguito:

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

La dimensione descrive l'allocazione, mentre la lunghezza descrive la trasmissione. Il numero di elementi trasmessi deve essere sempre minore o uguale al numero di elementi allocati. Il valore associato a **length \_ è** sempre minore o uguale a **size \_ è**.

 

 