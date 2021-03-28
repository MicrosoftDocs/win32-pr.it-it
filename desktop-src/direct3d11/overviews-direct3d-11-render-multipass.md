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
# <a name="multiple-pass-rendering"></a>Rendering Multiple-Pass

Il rendering a più passaggi è un processo in cui un'applicazione attraversa più volte il grafico della scena per produrre un output per il rendering sullo schermo. Il rendering a più passaggi migliora le prestazioni perché suddivide le scene complesse in attività che possono essere eseguite simultaneamente.

Per eseguire il rendering a più passaggi, è necessario creare un contesto posticipato e un elenco di comandi per ogni passaggio aggiuntivo. Mentre l'applicazione attraversa il grafico della scena, registra i comandi (ad esempio, il rendering di comandi come il [**disegno**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)) in un contesto posticipato. Al termine dell'attraversamento, l'applicazione chiama il metodo [**FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) sul contesto posticipato. Infine, l'applicazione chiama il metodo [**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) nel contesto immediato per eseguire i comandi in ogni elenco di comandi.

Nello pseudocodice seguente viene illustrato come eseguire il rendering a più passaggi:

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
> Il contesto immediato modifica una risorsa, che è associata al contesto immediato come visualizzazione della destinazione di rendering (RTV); al contrario, ogni contesto posticipato utilizza semplicemente la risorsa, associata al contesto posticipato come visualizzazione risorse dello shader (SRV). Per ulteriori informazioni sui contesti immediati e posticipati, vedere [rendering immediato e posticipato](overviews-direct3d-11-render-multi-thread-render.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




