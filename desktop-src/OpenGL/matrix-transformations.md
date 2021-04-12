---
title: Trasformazioni matrice
description: I vertici e le normali sono trasformati dalle matrici Modelview e projection prima di essere usati per produrre un'immagine nel framebuffer.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline di elaborazione OpenGL, matrici
- matrici OpenGL
- matrice Modelview
- matrice di proiezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221330"
---
# <a name="matrix-transformations"></a><span data-ttu-id="00117-107">Trasformazioni matrice</span><span class="sxs-lookup"><span data-stu-id="00117-107">Matrix Transformations</span></span>

<span data-ttu-id="00117-108">I vertici e le normali sono trasformati dalle matrici Modelview e projection prima di essere usati per produrre un'immagine nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="00117-108">Vertices and normals are transformed by the modelview and projection matrices before they're used to produce an image in the framebuffer.</span></span> <span data-ttu-id="00117-109">Usare funzioni come [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**glTranslate \***](gltranslate.md)e [**glScale \***](glscale.md) per comporre le trasformazioni desiderate.</span><span class="sxs-lookup"><span data-stu-id="00117-109">Use functions such as [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix\***](glmultmatrix.md), [**glRotate\***](glrotate.md), [**glTranslate\***](gltranslate.md), and [**glScale\***](glscale.md) to compose the desired transformations.</span></span> <span data-ttu-id="00117-110">Oppure specificare matrici direttamente con [**glLoadMatrix \***](glloadmatrix.md) e [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="00117-110">Or specify matrices directly with [**glLoadMatrix\***](glloadmatrix.md) and [**glLoadIdentity**](glloadidentity.md).</span></span> <span data-ttu-id="00117-111">Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare Modelview e matrici di proiezione nei rispettivi stack.</span><span class="sxs-lookup"><span data-stu-id="00117-111">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore modelview and projection matrices on their respective stacks.</span></span>

 

 




