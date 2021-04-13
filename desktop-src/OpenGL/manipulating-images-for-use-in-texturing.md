---
title: Manipolazione di immagini da utilizzare per la texturing
description: OpenGL Utility Library (GLU) fornisce funzioni di ridimensionamento delle immagini e mapping MIP automatiche per semplificare la specifica delle immagini di trama.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilità OpenGL (GLU), ridimensionamento delle immagini
- GLU (utilità OpenGL), ridimensionamento delle immagini
- Utilità OpenGL (GLU), mapping MIP automatico
- GLU (utilità OpenGL), mapping MIP automatico
- Utilità OpenGL (GLU), immagini di trama
- GLU (utilità OpenGL), immagini di trama
- Libreria GLU, immagini di trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329508"
---
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="ba590-110">Manipolazione di immagini da utilizzare per la texturing</span><span class="sxs-lookup"><span data-stu-id="ba590-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="ba590-111">OpenGL Utility Library (GLU) fornisce funzioni di ridimensionamento delle immagini e mapping MIP automatiche per semplificare la specifica delle immagini di trama.</span><span class="sxs-lookup"><span data-stu-id="ba590-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="ba590-112">La funzione [**gluScaleImage**](gluscaleimage.md) ridimensiona un'immagine specificata a una dimensione della trama accettata; è possibile passare l'immagine risultante a OpenGL come trama.</span><span class="sxs-lookup"><span data-stu-id="ba590-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="ba590-113">Le funzioni Automatic mapping MIP, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) e [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), creano immagini di trama mipmap da un'immagine specificata e le passano rispettivamente a [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="ba590-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 




