---
title: Applicare una tecnica (Direct3D 11)
description: Informazioni su come impostare lo stato dell'effetto nel dispositivo per Direct3D 11 dopo la dichiarazione e l'inizializzazione delle costanti, delle trame e dello shader.
ms.assetid: 16001913-7ae2-4629-a625-eb850e29fc77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b53eb5f60c80baf69199885f8036a9e92ac1572fe8339bd6d4a96454adb0121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792041"
---
# <a name="apply-a-technique-direct3d-11"></a>Applicare una tecnica (Direct3D 11)

Con le costanti, le trame e lo stato dello shader dichiarati e inizializzati, l'unica cosa da fare è impostare lo stato dell'effetto nel dispositivo.

## <a name="set-non-shader-state-in-the-device"></a>Impostare lo stato non shader nel dispositivo

Uno stato della pipeline non è impostato da un effetto. Ad esempio, la cancellazione di una destinazione di rendering prepara la destinazione di rendering per i dati. Prima di impostare lo stato dell'effetto nel dispositivo, ecco un esempio di cancellazione dei buffer di output.


```
    // Clear the render target and depth stencil
    float ClearColor[4] = { 0.0f, 0.25f, 0.25f, 0.55f };
    ID3D11RenderTargetView* pRTV = DXUTGetD3D11RenderTargetView();
    pD3DDevice->ClearRenderTargetView( pRTV, ClearColor );
    ID3D11DepthStencilView* pDSV = DXUTGetD3D11DepthStencilView();
    pD3DDevice->ClearDepthStencilView( pDSV, D3D11_CLEAR_DEPTH, 1.0, 0 );
```



## <a name="set-effect-state-in-the-device"></a>Impostare lo stato dell'effetto nel dispositivo

L'impostazione dello stato dell'effetto viene eseguita applicando lo stato dell'effetto all'interno del ciclo di rendering. Questa operazione viene eseguita dall'esterno di . Ovvero, selezionare una tecnica e quindi impostare lo stato per ogni passaggio (a seconda del risultato desiderato).


```
    D3D11_TECHNIQUE_DESC techDesc;
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



Un effetto non esegue il rendering di alcun elemento, ma imposta semplicemente lo stato dell'effetto sul dispositivo. Il codice di rendering viene chiamato dopo che lo stato dell'effetto aggiorna lo stato del dispositivo. In questo esempio, la chiamata DrawIndexed esegue il rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 




