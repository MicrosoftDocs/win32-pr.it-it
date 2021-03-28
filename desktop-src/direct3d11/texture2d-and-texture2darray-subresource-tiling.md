---
title: Divisione in riquadri di sottorisorse Texture2D e Texture2DArray
description: In queste tabelle viene illustrato come affiancare le sottorisorse Texture2D e Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399352"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Divisione in riquadri di sottorisorse Texture2D e Texture2DArray

In queste tabelle viene illustrato come affiancare le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) . I valori in queste tabelle non contano la compressione della parte finale MIP.

Questa tabella mostra il modo in cui vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con conteggi multicampionamento pari a 1.



| Bits/pixel (1 campione/pixel) | Dimensioni riquadro (pixel, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | con dimensioni 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128x64                        |
| 128                         | 64x64                         |
| BC1, 4                       | 512x256                       |
| BC2, 3, 5, 6, 7                 | 256x256                       |



 

I conteggi dei bit di formato non supportati con le risorse affiancate sono formati di 96 BPP, formati video, \_ formato DXGI \_ R1 \_ UNORM, \_ formato DXGI \_ R8G8 B8G8 UNORM \_ \_ e \_ formato DXGI \_ \_ \_ R8R8 G8B8 UNORM.

Questa tabella mostra il modo in cui vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con diversi conteggi multicampionamento.



| Conteggio multicampionamento           | Dividere le dimensioni del riquadro sopra per (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Solo i conteggi dei campioni 1 e 4 sono obbligatori (e consentiti) per essere supportati con le risorse affiancate. Le risorse affiancate non supportano attualmente 2, 8 e 16 anche se sono visualizzate.

Le implementazioni possono scegliere di supportare 2, 8 e/o 16 modalità di anti-aliasing di esempio multisample (MSAA) per le risorse non affiancate, anche se la risorsa affiancata non le supporta.

Le risorse affiancate con conteggi di esempio maggiori di 1 non possono usare formati di 128 BPP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come affiancare l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 