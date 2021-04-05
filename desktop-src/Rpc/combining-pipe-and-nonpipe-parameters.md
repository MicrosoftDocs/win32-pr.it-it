---
title: Combinazione di parametri pipe e nonpipe
description: Combinazione di parametri pipe e non pipe in RPC (Remote Procedure Call).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872814"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="c64cb-103">Combinazione di parametri pipe e nonpipe</span><span class="sxs-lookup"><span data-stu-id="c64cb-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="c64cb-104">Quando si combinano i tipi di pipe e altri tipi in una chiamata di procedura remota, i dati vengono trasmessi in base alla direzione del parametro:</span><span class="sxs-lookup"><span data-stu-id="c64cb-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="c64cb-105">Nella direzione, i dati per tutti gli argomenti non pipe vengono trasmessi per primi, seguiti dai dati della pipe. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="c64cb-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="c64cb-106">Nella direzione di **\[ uscita \]** , il server invia prima i dati della pipe.</span><span class="sxs-lookup"><span data-stu-id="c64cb-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="c64cb-107">Dopo la restituzione della routine del Manager, il server trasmette i dati non pipe.</span><span class="sxs-lookup"><span data-stu-id="c64cb-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="c64cb-108">Quando ci sono **\[ in, gli \] argomenti di pipe in uscita** combinati con **\[ in, out \]** di argomenti non pipe, prima i dati di input vengono trasmessi integralmente, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c64cb-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="c64cb-109">I dati di output vengono quindi trasmessi come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c64cb-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="c64cb-110">La restrizione seguente si applica a questa implementazione (MIDL 3,0) delle pipe: quando si combinano i tipi di pipe e altri tipi in una singola chiamata di procedura remota, i parametri non pipe devono avere una dimensione ben definita per consentire al compilatore MIDL di calcolare la dimensione del buffer necessaria.</span><span class="sxs-lookup"><span data-stu-id="c64cb-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="c64cb-111">Non è ad esempio possibile combinare parametri pipe con un \[ [](/windows/desktop/Midl/unique) \] puntatore univoco o una struttura conforme, poiché non è possibile determinare le dimensioni in fase di compilazione.</span><span class="sxs-lookup"><span data-stu-id="c64cb-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c64cb-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c64cb-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c64cb-113">inviare tramite pipe</span><span class="sxs-lookup"><span data-stu-id="c64cb-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="c64cb-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="c64cb-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 