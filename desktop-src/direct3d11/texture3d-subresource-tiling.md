---
title: Divisione in riquadri di sottorisorse Texture3D
description: Questa tabella illustra come vengono affiancate le sottorisorse Texture3D.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46149fd82153bb062599fb1c4246970ea53012aa6134c46b42292f7befbeaf94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912765"
---
# <a name="texture3d-subresource-tiling"></a>Divisione in riquadri di sottorisorse Texture3D

Questa tabella illustra come vengono affiancate le sottorisorse [**Texture3D.**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) I valori in questa tabella non contano i mip pack della coda.

Questa tabella accetta [**l'affiancamento Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) e divide le dimensioni x/y per 4 e aggiunge 16 livelli di profondità. Tutti i riquadri per il primo piano (piano 2D di riquadri che definiscono i primi 16 livelli di profondità) vengono visualizzati prima dei piani successivi.

> [!Note]  
> [**Il supporto Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) nelle risorse affiancate non viene esposto nell'implementazione iniziale delle risorse affiancate, ma le forme del riquadro desiderate sono elencate qui perché il supporto potrebbe essere considerato in una versione futura.

 



| Bit/Pixel (1 campione/pixel) | Dimensioni del riquadro (pixel, WxHxD) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1,4                       | 128x64x16                       |
| BC2,3,5,6,7                 | 64x64x16                        |



 

I conteggi di bit di formato non supportati con le risorse affiancate sono formati di 96 bpp, formati video, DXGI \_ \_ FORMAT R1 \_ UNORM, DXGI \_ FORMAT \_ \_ R8G8 B8G8 UNORM e \_ DXGI \_ FORMAT \_ R8R8 \_ G8B8 \_ UNORM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come viene affiancata l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 