---
title: Divisione in riquadri di buffer
description: Una risorsa buffer è divisa in riquadri 64KB, con uno spazio vuoto nell'ultimo riquadro se la dimensione non è un multiplo di 64KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872585"
---
# <a name="buffer-tiling"></a>Divisione in riquadri di buffer

Una risorsa [buffer](overviews-direct3d-11-resources-buffers.md) è divisa in riquadri 64KB, con uno spazio vuoto nell'ultimo riquadro se la dimensione non è un multiplo di 64KB.

I buffer strutturati non devono avere vincoli sullo stride da affiancare. Tuttavia, le possibili ottimizzazioni delle prestazioni nell'hardware per l'uso di [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) possono essere sacrificate, rendendole in primo luogo affiancate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come affiancare l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 