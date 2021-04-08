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
# <a name="conformant-arrays"></a><span data-ttu-id="701c6-103">Matrici conformi</span><span class="sxs-lookup"><span data-stu-id="701c6-103">Conformant Arrays</span></span>

<span data-ttu-id="701c6-104">La dimensione di una matrice conforme può variare o essere conforme ogni volta che il client la passa a una procedura remota sul server.</span><span class="sxs-lookup"><span data-stu-id="701c6-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="701c6-105">La definizione dell'interfaccia nel file MIDL dell'applicazione consente al client di specificare la dimensione della matrice ogni volta che richiama la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="701c6-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="701c6-106">Usare parentesi quadre vuote ( \[ \] ) o un asterisco tra parentesi quadre ( \[ \* \] ) nella definizione di matrice per indicare una matrice conforme.</span><span class="sxs-lookup"><span data-stu-id="701c6-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="701c6-107">L'esempio seguente contiene la definizione di una procedura remota in un'interfaccia in un file MIDL.</span><span class="sxs-lookup"><span data-stu-id="701c6-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="701c6-108">Il client specifica la dimensione della matrice passata al server dal parametro *arraySize*.</span><span class="sxs-lookup"><span data-stu-id="701c6-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

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

<span data-ttu-id="701c6-109">La definizione dell'interfaccia usa la dimensione dell'attributo MIDL \[ [**\_**](/windows/desktop/Midl/size-is) \] per specificare le dimensioni della matrice che il client passa al server.</span><span class="sxs-lookup"><span data-stu-id="701c6-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="701c6-110">Se si preferisce indicare il valore massimo dei numeri di indice della matrice, usare invece l' \[ attributo [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="701c6-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="701c6-111">Per altre informazioni su questi attributi MIDL, vedere [attributi di matrice](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="701c6-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="701c6-112">Nel frammento di codice seguente viene illustrato come un client può richiamare la procedura remota definita nel file MIDL precedente.</span><span class="sxs-lookup"><span data-stu-id="701c6-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="701c6-113">Questo frammento chiama due volte la procedura remota MyRemoteProc.</span><span class="sxs-lookup"><span data-stu-id="701c6-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="701c6-114">Alla prima chiamata passa una matrice di 20 elementi.</span><span class="sxs-lookup"><span data-stu-id="701c6-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="701c6-115">Alla seconda chiamata, il client passa una matrice di 200 elementi.</span><span class="sxs-lookup"><span data-stu-id="701c6-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 