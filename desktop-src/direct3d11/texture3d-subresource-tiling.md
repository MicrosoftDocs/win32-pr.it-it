---
title: Divisione in riquadri di sottorisorse Texture3D
description: Questa tabella Mostra come affiancare le sottorisorse di Texture3D.
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993605"
---
# <a name="texture3d-subresource-tiling"></a>Divisione in riquadri di sottorisorse Texture3D

Questa tabella Mostra come affiancare le sottorisorse di [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) . I valori in questa tabella non contano la compressione della parte finale MIP.

Questa tabella prende il [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) di affiancamento e divide le dimensioni x/y di 4 ciascuna e aggiunge 16 livelli di profondità. Tutti i riquadri per il primo piano (piano 2D dei riquadri che definiscono i primi 16 livelli di profondità) vengono visualizzati prima dei piani successivi.

> [!Note]  
> Il supporto di [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) nelle risorse affiancate non viene esposto nell'implementazione iniziale delle risorse affiancate, ma le forme dei riquadri desiderate sono elencate qui perché il supporto potrebbe essere considerato in una versione futura.

 



| Bits/pixel (1 campione/pixel) | Dimensioni riquadro (pixel, LxAxP) |
|-----------------------------|---------------------------------|
| 8                           | 64x32x32                        |
| 16                          | 32x32x32                        |
| 32                          | 32x32x16                        |
| 64                          | 32x16x16                        |
| 128                         | 16x16x16                        |
| BC1, 4                       | 128x64x16                       |
| BC2, 3, 5, 6, 7                 | 64x64x16                        |



 

I conteggi dei bit di formato non supportati con le risorse affiancate sono formati di 96 BPP, formati video, \_ formato DXGI \_ R1 \_ UNORM, \_ formato DXGI \_ R8G8 B8G8 UNORM \_ \_ e \_ formato DXGI \_ \_ \_ R8R8 G8B8 UNORM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come affiancare l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 