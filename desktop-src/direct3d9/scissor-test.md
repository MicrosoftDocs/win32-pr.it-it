---
description: Il test a forbice esegue il ritaglio dei pixel esterni al rettangolo della forbice, una sottosezione rettangolare definita dall'utente della destinazione di rendering.
ms.assetid: deff4f54-4a2f-4d9a-98a7-a69d5fc0853d
title: Test a forbice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66c4298182ab2bb6302c19111e2970d23cef311d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304376"
---
# <a name="scissor-test-direct3d-9"></a>Test a forbice (Direct3D 9)

Il test a forbice esegue il ritaglio dei pixel esterni al rettangolo della forbice, una sottosezione rettangolare definita dall'utente della destinazione di rendering.

Il rettangolo a forbice può essere usato per indicare l'area della destinazione di rendering in cui viene disegnato il mondo del gioco. L'area esterna al rettangolo viene abbattuti e potrebbe essere dedicata all'interfaccia utente grafica del gioco. Il test a forbice non può eliminare aree non rettangolari.

I rettangoli a forbice non possono essere impostati su un numero maggiore rispetto alla destinazione di rendering, ma possono essere impostati su un numero maggiore rispetto al viewport.

Il rettangolo a forbice è gestito da uno stato di rendering del dispositivo. Un test a forbice viene abilitato o disabilitato impostando RenderState su **true** o **false**. Questo test viene eseguito dopo il calcolo del colore del frammento ma prima del test alfa. [**IDirect3DDevice9:: SetRenderTarget**](/windows/desktop/api) Reimposta il rettangolo della forbice sulla destinazione di rendering completa, analoga alla reimpostazione del viewport. [**IDirect3DDevice9:: SetScissorRect**](/windows/desktop/api) viene registrato da Stateblocks e [**IDirect3DDevice9:: CreateStateBlock**](/windows/desktop/api) con l'impostazione All State (D3DSBT \_ All value in [**D3DSTATEBLOCKTYPE**](./d3dstateblocktype.md)). Il test a forbice influisca anche sull'operazione [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) del dispositivo.


```
// Methods
HRESULT IDirect3DDevice9::SetScissorRect(CONST RECT* pRect); 
HRESULT IDirect3DDevice9::GetScissorRect(RECT* pRect); 

// New RenderState, values are TRUE or FALSE 
D3DRS_SCISSORTESTENABLE 

// New hardware cap 
D3D9CAPS.RasterCaps -> D3DPRASTERCAPS_SCISSORTEST;
```



Il rettangolo a forbice predefinito è il viewport completo.

Il test a forbice viene eseguito subito dopo il completamento dell'elaborazione dei pixel da parte di un pixel shader o della pipeline della funzione fissa, come illustrato nella figura seguente.

![diagramma del momento in cui viene eseguito il test a forbice rispetto ad altri passaggi](images/scissor-test.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 
