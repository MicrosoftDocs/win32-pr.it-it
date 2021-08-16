---
title: Divisione in riquadri di buffer
description: Una risorsa buffer è suddivisa in riquadri da 64 KB, con spazio vuoto nell'ultimo riquadro se le dimensioni non sono un multiplo di 64 KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734243"
---
# <a name="buffer-tiling"></a>Divisione in riquadri di buffer

Una [risorsa buffer](overviews-direct3d-11-resources-buffers.md) è suddivisa in riquadri da 64 KB, con spazio vuoto nell'ultimo riquadro se le dimensioni non sono un multiplo di 64 KB.

I buffer strutturati non devono avere vincoli sullo stride da affiancare. Tuttavia, le possibili ottimizzazioni delle prestazioni nell'hardware per l'uso di [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) possono essere sacrificate rendendole affiancate in primo luogo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come viene affiancata l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 