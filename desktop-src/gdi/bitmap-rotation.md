---
description: Per copiare una bitmap in un parallelogramma; usare la funzione PlgBlt, che esegue un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un parallelogramma in un contesto di dispositivo di destinazione.
ms.assetid: fd5b3d9f-fdce-485e-bff8-464d96b8db34
title: Rotazione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c8711189182646c55aee414ef92409a6de20ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994120"
---
# <a name="bitmap-rotation"></a><span data-ttu-id="bd18f-103">Rotazione bitmap</span><span class="sxs-lookup"><span data-stu-id="bd18f-103">Bitmap Rotation</span></span>

<span data-ttu-id="bd18f-104">Per copiare una bitmap in un parallelogramma; usare la funzione [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) , che esegue un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un parallelogramma in un contesto di dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="bd18f-104">To copy a bitmap into a parallelogram; use the [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) function, which performs a bit-block transfer from a rectangle in a source device context into a parallelogram in a destination device context.</span></span> <span data-ttu-id="bd18f-105">Per ruotare la bitmap, un'applicazione deve fornire le coordinate, in unità di misura internazionali, da usare per gli angoli del parallelogramma.</span><span class="sxs-lookup"><span data-stu-id="bd18f-105">To rotate the bitmap, an application must provide the coordinates, in world units, to be used for the corners of the parallelogram.</span></span> <span data-ttu-id="bd18f-106">Per ulteriori informazioni sulla rotazione e sulle unità internazionali, vedere [Coordinate spazi e trasformazioni](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="bd18f-106">(For more information about rotation and world units, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).)</span></span>

 

 



