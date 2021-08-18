---
description: Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa da fare è impostare lo stato dell'effetto nel dispositivo.
ms.assetid: b6c88fa1-53d4-40dc-803d-5d1cdfe4777b
title: Applicare una tecnica (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4c920cbc7323ba42f3b099688a962674e3f5c2305746df7a56d1e158330919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128413"
---
# <a name="apply-a-technique-direct3d-10"></a>Applicare una tecnica (Direct3D 10)

Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa da fare è impostare lo stato dell'effetto nel dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Impostare lo stato non shader nel dispositivo

Alcuni stati della pipeline non sono impostati da un effetto. Ad esempio, la cancellazione di una destinazione di rendering prepara la destinazione di rendering per i dati. Prima di impostare lo stato dell'effetto nel dispositivo, ecco un esempio di cancellazione dei buffer di output.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D10RenderTargetView* pRTV = DXUTGetD3D10RenderTargetView();
    pd3dDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D10DepthStencilView* pDSV = DXUTGetD3D10DepthStencilView();
    pd3dDevice->ClearDepthStencilView( pDSV, D3D10_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Impostare lo stato dell'effetto nel dispositivo

L'impostazione dello stato dell'effetto viene eseguita applicando lo stato dell'effetto all'interno del ciclo di rendering. Questa operazione viene eseguita dall'esterno in . Ovvero, selezionare una tecnica e quindi impostare lo stato per ogni passaggio (a seconda del risultato desiderato).


```
    D3D10_TECHNIQUE_DESC techDesc;
    pRenderTechnique->GetDesc( &techDesc );
    for( UINT p = 0; p < techDesc.Passes; ++p )
    {
        }
            ....
            pRenderTechnique->GetPassByIndex( p )->Apply(0);
            pd3dDevice->DrawIndexed( (UINT)pSubset->IndexCount, 0,  
                 (UINT)pSubset->VertexStart );
        }
    }
```



Un effetto non esegue il rendering di alcun elemento, ma imposta semplicemente lo stato dell'effetto sul dispositivo. Il codice di rendering viene chiamato dopo che lo stato dell'effetto aggiorna lo stato del dispositivo. In questo esempio la chiamata DrawIndexed esegue il rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



