---
title: Trasformazione in coordinate finestra
description: Prima che le coordinate della clip vengano convertite in coordinate della finestra, sono divise per il valore di w per restituire coordinate del dispositivo normalizzate.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline di elaborazione OpenGL, conversione in coordinate finestra
- conversione in coordinate della finestra OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713924"
---
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="80d15-105">Trasformazione in coordinate finestra</span><span class="sxs-lookup"><span data-stu-id="80d15-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="80d15-106">Prima che le coordinate della clip vengano convertite in coordinate della finestra, sono divise per il valore di *w* per restituire coordinate del dispositivo normalizzate.</span><span class="sxs-lookup"><span data-stu-id="80d15-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="80d15-107">La trasformazione viewport applicata a queste coordinate normalizzate genera le coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="80d15-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="80d15-108">Si controlla il viewport, che determina l'area della finestra sullo schermo che visualizza un'immagine, con [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).</span><span class="sxs-lookup"><span data-stu-id="80d15-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




