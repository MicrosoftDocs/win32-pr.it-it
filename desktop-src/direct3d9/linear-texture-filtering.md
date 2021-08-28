---
description: Direct3D usa una forma di filtro trame lineare denominato filtro bilineare.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtro trame lineari (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5177af653c74383ef87468dbb43167fa2962cd093410a6a63f85da2233e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628531"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtro trame lineari (Direct3D 9)

Direct3D usa una forma di filtro trame lineare denominato filtro bilineare. Come il campionamento in punti più vicini [(Direct3D 9),](nearest-point-sampling.md)il filtro trame bilineari calcola innanzitutto un indirizzo texel, che in genere non è un indirizzo intero. Il filtro bilineare trova quindi il texel il cui indirizzo intero è più vicino all'indirizzo calcolato. Inoltre, il modulo di rendering Direct3D calcola una media ponderata dei texel immediatamente sopra, sotto, a sinistra di e a destra del punto di campionamento più vicino.

Selezionare il filtro trame bilineare richiamando il [**metodo IDirect3DDevice9::SetSamplerState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Impostare il valore del primo parametro sul numero di indice intero (0-7) della trama per cui si sta selezionando un metodo di filtro trame. Passare D3DSAMP \_ MAGFILTER, D3DSAMP MINFILTER o D3DSAMP MIPFILTER per il secondo parametro per impostare il \_ \_ filtro di ingrandimento, minificazione o mipmapping. Passare D3DTEXF \_ LINEAR nel terzo parametro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro trame](texture-filtering.md)
</dt> </dl>

 

 
