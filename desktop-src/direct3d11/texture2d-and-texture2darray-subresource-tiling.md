---
title: Divisione in riquadri di sottorisorse Texture2D e Texture2DArray
description: Queste tabelle illustrano come vengono affiancate le sottorisorse Texture2D e Texture2DArray.
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ee7cc181845785ab978dc5d58b1e131a7f32c34a6d04006af1ac8034f089ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530436"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Divisione in riquadri di sottorisorse Texture2D e Texture2DArray

Queste tabelle illustrano come vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray.**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) I valori in queste tabelle non contano i mip pack della parte finale.

Questa tabella illustra come vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con conteggi multicampionamento di 1.



| Bit/Pixel (1 campione/pixel) | Dimensioni del riquadro (pixel, WxH) |
|-----------------------------|-------------------------------|
| 8                           | 256x256                       |
| 16                          | 256x128                       |
| 32                          | 128x128                       |
| 64                          | 128x64                        |
| 128                         | 64x64                         |
| BC1,4                       | 512x256                       |
| BC2,3,5,6,7                 | 256x256                       |



 

I conteggi di bit di formato non supportati con le risorse affiancate sono formati di 96 bpp, formati video, DXGI \_ \_ FORMAT R1 \_ UNORM, DXGI \_ FORMAT \_ \_ R8G8 B8G8 UNORM e \_ DXGI \_ FORMAT \_ R8R8 \_ G8B8 \_ UNORM.

Questa tabella illustra come vengono affiancate le sottorisorse [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) con vari conteggi multicampionamento.



| Conteggio multicampionamento           | Dividere le dimensioni del riquadro sopra per (WxH) |
|-----------------------------|-------------------------------|
| 1                           | 1x1                           |
| 2                           | 2x1                           |
| 4                           | 2x2                           |
| 8                           | 4x2                           |
| 16                          | 4x4                           |



 

Solo i conteggi dei campioni 1 e 4 sono necessari (e consentiti) per essere supportati con le risorse affiancate. Le risorse affiancate non supportano attualmente 2, 8 e 16, anche se vengono visualizzate.

Le implementazioni possono scegliere di supportare la modalità di antialiasing multicampionamento di esempio 2, 8 e/o 16 per le risorse non affiancate anche se le risorse affiancate non le supportano.

Le risorse affiancate con conteggi di campioni maggiori di 1 non possono usare formati bpp di 128.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come viene affiancata l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 