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
# <a name="compressedanimationset"></a><span data-ttu-id="73874-103">CompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="73874-103">CompressedAnimationSet</span></span>

<span data-ttu-id="73874-104">Contiene i dati del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="73874-104">Contains animation set data.</span></span>

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

<span data-ttu-id="73874-105">Dove:</span><span class="sxs-lookup"><span data-stu-id="73874-105">Where:</span></span>

-   <span data-ttu-id="73874-106">CompressedBlockSize: dimensioni totali, in byte, dei dati compressi nel buffer dei dati di animazione del fotogramma chiave compresso.</span><span class="sxs-lookup"><span data-stu-id="73874-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="73874-107">TicksPerSec: numero di cicli fotogrammi chiave di animazione che si verificano al secondo.</span><span class="sxs-lookup"><span data-stu-id="73874-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="73874-108">PlaybackType: tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="73874-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="73874-109">Vedere [**D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="73874-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="73874-110">BufferLength-dimensioni minime del buffer, in byte, necessarie per conservare i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="73874-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="73874-111">Il valore è uguale a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="73874-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="73874-112">CompressedData \[ bufferLength \] : matrice di valori di dati compressi.</span><span class="sxs-lookup"><span data-stu-id="73874-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="73874-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73874-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73874-114">Modelli</span><span class="sxs-lookup"><span data-stu-id="73874-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="73874-115">**XFILECOMPRESSEDANIMATIONSET**</span><span class="sxs-lookup"><span data-stu-id="73874-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
