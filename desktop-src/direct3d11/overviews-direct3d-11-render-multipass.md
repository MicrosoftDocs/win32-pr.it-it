---
title: Rendering Multiple-Pass
description: Il rendering a più passaggi è un processo in cui un'applicazione attraversa più volte il grafico della scena per produrre un output per il rendering sullo schermo.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70fcf7f3f04bd641fdf82c9cf317e8a2ec99e85c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330804"
---
# <a name="multiple-pass-rendering"></a><span data-ttu-id="397e3-103">Rendering Multiple-Pass</span><span class="sxs-lookup"><span data-stu-id="397e3-103">Multiple-Pass Rendering</span></span>

<span data-ttu-id="397e3-104">Il rendering a più passaggi è un processo in cui un'applicazione attraversa più volte il grafico della scena per produrre un output per il rendering sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="397e3-104">Multiple-pass rendering is a process in which an application traverses its scene graph multiple times in order to produce an output to render to the display.</span></span> <span data-ttu-id="397e3-105">Il rendering a più passaggi migliora le prestazioni perché suddivide le scene complesse in attività che possono essere eseguite simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="397e3-105">Multiple-pass rendering improves performance because it breaks up complex scenes into tasks that can run concurrently.</span></span>

<span data-ttu-id="397e3-106">Per eseguire il rendering a più passaggi, è necessario creare un contesto posticipato e un elenco di comandi per ogni passaggio aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="397e3-106">To perform multiple-pass rendering, you create a deferred context and command list for each additional pass.</span></span> <span data-ttu-id="397e3-107">Mentre l'applicazione attraversa il grafico della scena, registra i comandi (ad esempio, il rendering di comandi come il [**disegno**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) in un contesto posticipato.</span><span class="sxs-lookup"><span data-stu-id="397e3-107">While the application traverses the scene graph, it records commands (for example, rendering commands such as [**Draw**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) into a deferred context.</span></span> <span data-ttu-id="397e3-108">Al termine dell'attraversamento, l'applicazione chiama il metodo [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) sul contesto posticipato.</span><span class="sxs-lookup"><span data-stu-id="397e3-108">After the application finishes the traversal, it calls the [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) method on the deferred context.</span></span> <span data-ttu-id="397e3-109">Infine, l'applicazione chiama il metodo [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) nel contesto immediato per eseguire i comandi in ogni elenco di comandi.</span><span class="sxs-lookup"><span data-stu-id="397e3-109">Finally, the application calls the [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) method on the immediate context to execute the commands in each command list.</span></span>

<span data-ttu-id="397e3-110">Nello pseudocodice seguente viene illustrato come eseguire il rendering a più passaggi:</span><span class="sxs-lookup"><span data-stu-id="397e3-110">The following pseudocode shows how to perform multiple-pass rendering:</span></span>

``` syntax
{
 ImmCtx->SetRenderTarget( pRTViewOfResourceX );
 DefCtx1->SetTexture( pSRView1OfResourceX );
 DefCtx2->SetTexture( pSRView2OfResourceX );

 for () // Traverse the scene graph.
  {
    ImmCtx->Draw(); // Pass 0: immediate context renders primitives into resource X.

    // The following texturing by the deferred contexts occurs after the 
    // immediate context makes calls to ExecuteCommandList. 
    // Resource X is then comletely updated by the immediate context. 
    DefCtx1->Draw(); // Pass 1: deferred context 1 performs texturing from resource X.
    DefCtx2->Draw(); // Pass 2: deferred context 2 performs texturing from resource X.
      }

  // Create command lists and record commands into them.
  DefCtx1->FinishCommandList( &pCL1 ); 
  DefCtx2->FinishCommandList( &pCL2 );

  ImmCtx->ExecuteCommandList( pCL1 ); // Execute pass 1.
  ImmCtx->ExecuteCommandList( pCL2 ); // Exeucte pass 2.
}
```

> [!Note]  
> <span data-ttu-id="397e3-111">Il contesto immediato modifica una risorsa, che è associata al contesto immediato come visualizzazione della destinazione di rendering (RTV); al contrario, ogni contesto posticipato utilizza semplicemente la risorsa, associata al contesto posticipato come visualizzazione risorse dello shader (SRV).</span><span class="sxs-lookup"><span data-stu-id="397e3-111">The immediate context modifies a resource, which is bound to the immediate context as a render target view (RTV); in contrast, each deferred context simply uses the resource, which is bound to the deferred context as a shader resource view (SRV).</span></span> <span data-ttu-id="397e3-112">Per ulteriori informazioni sui contesti immediati e posticipati, vedere [rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="397e3-112">For more information about immediate and deferred contexts, see [Immediate and Deferred Rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="397e3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="397e3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="397e3-114">Rendering</span><span class="sxs-lookup"><span data-stu-id="397e3-114">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




