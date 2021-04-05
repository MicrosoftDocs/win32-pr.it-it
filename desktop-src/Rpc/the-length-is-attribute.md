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
# <a name="the-length_is-attribute"></a><span data-ttu-id="41c33-104">La \[ lunghezza \_ è \] attribute</span><span class="sxs-lookup"><span data-stu-id="41c33-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="41c33-105">La \[ [**dimensione \_ è**](/windows/desktop/Midl/size-is) \] attributo che consente di specificare la dimensione massima della matrice.</span><span class="sxs-lookup"><span data-stu-id="41c33-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="41c33-106">Quando si tratta dell'unico attributo, vengono trasmessi tutti gli elementi della matrice.</span><span class="sxs-lookup"><span data-stu-id="41c33-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="41c33-107">Anziché inviare tutti gli elementi della matrice, è possibile specificare gli elementi trasmessi utilizzando l'attributo \[ [**length \_**](/windows/desktop/Midl/length-is) \] , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="41c33-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

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

<span data-ttu-id="41c33-108">Dimensioni descrive l'allocazione mentre la lunghezza descrive la trasmissione.</span><span class="sxs-lookup"><span data-stu-id="41c33-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="41c33-109">Il numero di elementi trasmessi deve sempre essere minore o uguale al numero di elementi allocati.</span><span class="sxs-lookup"><span data-stu-id="41c33-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="41c33-110">Il valore associato a **length \_** è sempre minore o uguale a **size \_ è**.</span><span class="sxs-lookup"><span data-stu-id="41c33-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 