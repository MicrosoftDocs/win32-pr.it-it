---
title: Più livelli di puntatori
description: Utilizzo di più livelli di puntatori in RPC (Remote Procedure Call).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963300"
---
# <a name="multiple-levels-of-pointers"></a><span data-ttu-id="cecb1-103">Più livelli di puntatori</span><span class="sxs-lookup"><span data-stu-id="cecb1-103">Multiple Levels of Pointers</span></span>

<span data-ttu-id="cecb1-104">Quando sono presenti più livelli di puntatori, gli attributi sono associati al puntatore più vicino al nome della variabile.</span><span class="sxs-lookup"><span data-stu-id="cecb1-104">When there are multiple levels of pointers, the attributes are associated with the pointer closest to the variable name.</span></span> <span data-ttu-id="cecb1-105">Il client è ancora responsabile dell'allocazione di memoria associata alla risposta.</span><span class="sxs-lookup"><span data-stu-id="cecb1-105">The client is still responsible for allocating any memory associated with the response.</span></span>

<span data-ttu-id="cecb1-106">L'esempio seguente consente allo stub di chiamare il server senza conoscere in anticipo la quantità di dati che verrà restituita:</span><span class="sxs-lookup"><span data-stu-id="cecb1-106">The following example allows the stub to call the server without knowing in advance how much data will be returned:</span></span>

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

<span data-ttu-id="cecb1-107">In questo esempio lo stub passa il server a un puntatore univoco, che il server Inizializza a **null**.</span><span class="sxs-lookup"><span data-stu-id="cecb1-107">In this example, the stub passes the server a unique pointer, which the server initializes to **NULL**.</span></span> <span data-ttu-id="cecb1-108">Il server alloca quindi un blocco di barre, imposta il puntatore, imposta l'argomento size e restituisce.</span><span class="sxs-lookup"><span data-stu-id="cecb1-108">The server then allocates a block of BARs, sets the pointer, sets the size argument and returns.</span></span> <span data-ttu-id="cecb1-109">Si noti che per fare in modo che il server abbia effetto sul chiamante, è necessario passare \[ un \] puntatore Ref a un \[ [](/windows/desktop/Midl/unique) \] puntatore univoco ai dati.</span><span class="sxs-lookup"><span data-stu-id="cecb1-109">Note that in order for the server to have an effect on the caller you must pass a \[ref\] pointer to a \[[**unique**](/windows/desktop/Midl/unique)\] pointer to your data.</span></span> <span data-ttu-id="cecb1-110">Si noti anche che la virgola \[ [**\_ è**](/windows/desktop/Midl/size-is)(, \* psize) \] , che indica che il puntatore di primo livello non è un puntatore di dimensione, ma che il puntatore di livello inferiore è.</span><span class="sxs-lookup"><span data-stu-id="cecb1-110">Also note the comma in \[[**size\_is**](/windows/desktop/Midl/size-is)( , \*pSize )\], which indicates that the top-level pointer is not a sized pointer, but that the lower-level pointer is.</span></span>

<span data-ttu-id="cecb1-111">Sul lato client lo stub imposta ppBar su \* **null** prima di chiamare la procedura remota.</span><span class="sxs-lookup"><span data-stu-id="cecb1-111">On the client side, the stub sets \*ppBar to **NULL** before calling the remote procedure.</span></span> <span data-ttu-id="cecb1-112">Lo stub alloca quindi ed esegue l'unmarshalling del Arry degli oggetti barra.</span><span class="sxs-lookup"><span data-stu-id="cecb1-112">The stub then allocates and unmarshals the arry of BAR objects.</span></span> <span data-ttu-id="cecb1-113">L'argomento size indica le dimensioni del blocco e il numero di barre di cui è stato effettuato l'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="cecb1-113">The size argument indicates the size of the block (and the number of unmarshaled BARs).</span></span> <span data-ttu-id="cecb1-114">Il client deve liberare la matrice di oggetti barra restituita quando non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="cecb1-114">The client must free the returned array of BAR objects when it is no longer required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cecb1-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cecb1-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cecb1-116">**dimensioni \_**</span><span class="sxs-lookup"><span data-stu-id="cecb1-116">**size\_is**</span></span>](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 