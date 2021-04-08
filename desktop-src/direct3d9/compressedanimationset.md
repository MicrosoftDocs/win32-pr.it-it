---
description: Contiene i dati del set di animazioni.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049252"
---
# <a name="compressedanimationset"></a>CompressedAnimationSet

Contiene i dati del set di animazioni.

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

Dove:

-   CompressedBlockSize: dimensioni totali, in byte, dei dati compressi nel buffer dei dati di animazione del fotogramma chiave compresso.
-   TicksPerSec: numero di cicli fotogrammi chiave di animazione che si verificano al secondo.
-   PlaybackType: tipo del ciclo di riproduzione del set di animazioni. Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).
-   BufferLength-dimensioni minime del buffer, in byte, necessarie per conservare i dati di animazione del fotogramma chiave compressi. Il valore è uguale a ((CompressedBlockSize + 3)/4).
-   CompressedData \[ bufferLength \] : matrice di valori di dati compressi.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[**XFILECOMPRESSEDANIMATIONSET**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
