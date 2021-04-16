---
description: Direct3D usa un tipo di filtro di trama lineare denominato filtro bilineare.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtro di trama lineare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521929"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtro di trama lineare (Direct3D 9)

Direct3D usa un tipo di filtro di trama lineare denominato filtro bilineare. Analogamente al [campionamento dei punti più vicini (Direct3D 9)](nearest-point-sampling.md), il filtro di trama bilineare prima calcola un indirizzo Texel, che in genere non è un indirizzo Integer. Filtraggio bilineare trova quindi il Texel il cui indirizzo Integer è più vicino all'indirizzo calcolato. Il modulo di rendering Direct3D, inoltre, calcola una media ponderata dei Texel che si trovano immediatamente sopra, sotto, a sinistra di e a destra del punto di campionamento più vicino.

Selezionare filtro di trama bilineare richiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Impostare il valore del primo parametro sul numero di indice Integer (0-7) della trama per cui si seleziona un metodo di filtro della trama. Passare D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER o D3DSAMP \_ MIPFILTER per il secondo parametro per impostare il filtro di ingrandimento, minification o mapping MIP. Passare D3DTEXF \_ Linear nel terzo parametro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtraggio trama](texture-filtering.md)
</dt> </dl>

 

 
