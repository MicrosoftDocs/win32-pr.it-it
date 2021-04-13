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
# <a name="varying-arrays"></a><span data-ttu-id="01ee1-106">Matrici variabili</span><span class="sxs-lookup"><span data-stu-id="01ee1-106">Varying Arrays</span></span>

<span data-ttu-id="01ee1-107">In MIDL, le matrici variabili hanno dimensioni fisse.</span><span class="sxs-lookup"><span data-stu-id="01ee1-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="01ee1-108">Consentono ai client di passare parti diverse di matrici dai client ai server.</span><span class="sxs-lookup"><span data-stu-id="01ee1-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="01ee1-109">La dimensione della parte della matrice può variare dalla chiamata alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="01ee1-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="01ee1-110">Tuttavia, la dimensione della matrice complessiva è fissa.</span><span class="sxs-lookup"><span data-stu-id="01ee1-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="01ee1-111">Ad esempio, nell'esempio seguente viene illustrata la definizione di una procedura remota in un'interfaccia in un file MIDL.</span><span class="sxs-lookup"><span data-stu-id="01ee1-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="01ee1-112">La dimensione della matrice che il client passa al server è fissata dalle dimensioni della matrice di costanti \_ .</span><span class="sxs-lookup"><span data-stu-id="01ee1-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="01ee1-113">L'interfaccia specifica la parte della matrice che il client passa al server nei parametri FirstElement e chunkSize.</span><span class="sxs-lookup"><span data-stu-id="01ee1-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

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

<span data-ttu-id="01ee1-114">La definizione dell'interfaccia USA prima l'attributo MIDL \[ [**\_**](/windows/desktop/Midl/first-is) \] per specificare il numero di indice del primo elemento nella parte della matrice che il client passa al server.</span><span class="sxs-lookup"><span data-stu-id="01ee1-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="01ee1-115">L' \[ [**attributo \_ length**](/windows/desktop/Midl/length-is) indica \] il numero totale di elementi della matrice passati dal client.</span><span class="sxs-lookup"><span data-stu-id="01ee1-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="01ee1-116">Per altre informazioni su questi attributi MIDL, vedere [attributi di matrice](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="01ee1-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="01ee1-117">Nel frammento di codice seguente viene illustrato come un client può richiamare la procedura remota definita nel file MIDL precedente.</span><span class="sxs-lookup"><span data-stu-id="01ee1-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


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



<span data-ttu-id="01ee1-118">Questo frammento chiama due volte la procedura remota MyRemoteProc.</span><span class="sxs-lookup"><span data-stu-id="01ee1-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="01ee1-119">Alla prima chiamata passa gli elementi della matrice numerati da 20 a 119, come indicato dai valori nelle variabili firstArrayElementNumber e totalElementsPassed.</span><span class="sxs-lookup"><span data-stu-id="01ee1-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="01ee1-120">Alla seconda chiamata, il client passa gli elementi della matrice numerati da 120 a 319.</span><span class="sxs-lookup"><span data-stu-id="01ee1-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 