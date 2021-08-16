---
title: Multiple-Pass rendering
description: Il rendering a più passi è un processo in cui un'applicazione attraversa il grafico della scena più volte per produrre un output per il rendering sulla visualizzazione.
ms.assetid: 9a11686a-fd99-4d40-8b02-6f8ec18346e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242573dea2982f3525082187aad536a407e446c4ce59f116f53b8fa0d40fc582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124209"
---
# <a name="multiple-pass-rendering"></a>Multiple-Pass rendering

Il rendering a più passi è un processo in cui un'applicazione attraversa il grafico della scena più volte per produrre un output per il rendering sulla visualizzazione. Il rendering a più passi migliora le prestazioni perché suddivide scene complesse in attività che possono essere eseguite contemporaneamente.

Per eseguire il rendering a più passaggi, è necessario creare un contesto posticipato e un elenco di comandi per ogni passaggio aggiuntivo. Mentre l'applicazione attraversa il grafico della scena, registra i comandi (ad esempio, il rendering di comandi come [**Draw)**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)in un contesto posticipato. Al termine dell'attraversamento, l'applicazione chiama il [**metodo FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) sul contesto posticipato. Infine, l'applicazione chiama [**il metodo ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) sul contesto immediato per eseguire i comandi in ogni elenco di comandi.

Lo pseudocodice seguente illustra come eseguire il rendering a più passaggi:

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
> Il contesto immediato modifica una risorsa, associata al contesto immediato come visualizzazione di destinazione di rendering (RTV). Al contrario, ogni contesto posticipato usa semplicemente la risorsa , associata al contesto posticipato come visualizzazione di risorse shader (SRV). Per altre informazioni sui contesti immediati e posticimanti, vedere [Rendering immediato e posticipato.](overviews-direct3d-11-render-multi-thread-render.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering](overviews-direct3d-11-render.md)
</dt> </dl>

 

 




