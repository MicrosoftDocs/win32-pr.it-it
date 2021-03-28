---
title: Funzioni (riferimento HLSL)
description: Funzioni incapsulano le istruzioni HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335660"
---
# <a name="functions-hlsl-reference"></a><span data-ttu-id="673a6-103">Funzioni (riferimento HLSL)</span><span class="sxs-lookup"><span data-stu-id="673a6-103">Functions (HLSL reference)</span></span>

<span data-ttu-id="673a6-104">Funzioni incapsulano le istruzioni HLSL.</span><span class="sxs-lookup"><span data-stu-id="673a6-104">Functions encapsulate HLSL statements.</span></span> <span data-ttu-id="673a6-105">In questo modo è possibile eseguire il debug di un set di funzioni e riutilizzarle in shader o effetti.</span><span class="sxs-lookup"><span data-stu-id="673a6-105">This enables you to debug a set of functions and then reuse them across shaders or effects.</span></span> <span data-ttu-id="673a6-106">Potrebbe essere necessario creare una funzione che incapsula la funzionalità di un vertex shader, pixel shader o trama shader.</span><span class="sxs-lookup"><span data-stu-id="673a6-106">You may want to create a function that encapsulates the functionality of a vertex shader, pixel shader or texture shader.</span></span> <span data-ttu-id="673a6-107">In altri casi, è possibile scrivere una funzione helper che esegue un'attività di uso comune e quindi chiamare tale funzione di supporto dalla funzione shader.</span><span class="sxs-lookup"><span data-stu-id="673a6-107">Other times, you may want to write a helper function that performs some commonly used task, and then call that helper function from your shader function.</span></span> <span data-ttu-id="673a6-108">Le regole per la scrittura di funzioni shader per HLSL sono molto simili alla scrittura di funzioni C.</span><span class="sxs-lookup"><span data-stu-id="673a6-108">The rules for writing shader functions for HLSL are very similar to writing C functions.</span></span>

-   [<span data-ttu-id="673a6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="673a6-109">Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
-   [<span data-ttu-id="673a6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="673a6-110">Parameters</span></span>](dx-graphics-hlsl-function-parameters.md)
-   [<span data-ttu-id="673a6-111">Istruzione Return</span><span class="sxs-lookup"><span data-stu-id="673a6-111">Return Statement</span></span>](dx-graphics-hlsl-return.md)
-   [<span data-ttu-id="673a6-112">Firme</span><span class="sxs-lookup"><span data-stu-id="673a6-112">Signatures</span></span>](dx-graphics-hlsl-signatures.md)

<span data-ttu-id="673a6-113">HLSL include anche una serie di [**funzioni intrinseche predefinite (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="673a6-113">HLSL also has a number of built-in [**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md).</span></span> <span data-ttu-id="673a6-114">Poiché tutte le funzioni intrinseche sono testate e le prestazioni sono ottimizzate, è consigliabile usare una funzione intrinseca laddove possibile anziché creare una funzione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="673a6-114">Because all intrinsic functions are tested and performance optimized, it is good practice to use an intrinsic function where possible instead of creating your own function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="673a6-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="673a6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="673a6-116">Sintassi del linguaggio (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="673a6-116">Language Syntax (DirectX HLSL)</span></span>](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




