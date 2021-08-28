---
description: Il test di forbice culla i pixel esterni al rettangolo di forbice, una sottosezioni rettangolare definita dall'utente della destinazione di rendering.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Test di scissor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d44b7670d67e7944e9d6e2587ed0011a6244eecef509495b90c71ff0753073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746517"
---
# <a name="scissor-test-direct3d-9"></a>Test di scissor (Direct3D 9)

Il test di forbice culla i pixel esterni al rettangolo di forbice, una sottosezioni rettangolare definita dall'utente della destinazione di rendering.

Il rettangolo di forbice può essere usato per indicare l'area della destinazione di rendering in cui viene disegnato il mondo del gioco. L'area esterna al rettangolo è culled e può essere dedicata all'interfaccia utente grafica di un gioco. Il test di forbice non può eliminare aree non rettangolari.

I rettangoli di forbice non possono essere impostati più grandi della destinazione di rendering, ma possono essere impostati più grandi del viewport.

Il rettangolo di forbice è gestito da uno stato di rendering del dispositivo. Un test di scissor viene abilitato o disabilitato impostando renderstate su **TRUE** o **FALSE.** Questo test viene eseguito dopo il calcolo del colore del frammento, ma prima del test alfa. [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) reimposta il rettangolo di forbice sulla destinazione di rendering completa, analogamente alla reimpostazione del viewport. [**IDirect3DDevice9::SetScissorRect**](/windows/desktop/api) viene registrato da stateblocks e [**IDirect3DDevice9::CreateStateBlock con**](/windows/desktop/api) l'impostazione all state (valore D3DSBT \_ ALL in [**D3DSTATEBLOCKTYPE).**](./d3dstateblocktype.md) Il test di scissor influisce anche [**sull'operazione IDirect3DDevice9::Clear del**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) dispositivo.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



Il rettangolo di forbice predefinito è il riquadro di visualizzazione completo.

Il test dello scissor viene eseguito subito dopo il completamento dell'elaborazione pixel da un pixel shader o dalla pipeline di funzioni fisse, come illustrato nel diagramma seguente.

![diagramma del momento in cui viene eseguito il test delle forbici rispetto ad altri passaggi](images/scissor-test.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pixel Pipeline](pixel-pipeline.md)
</dt> </dl>

 

 
