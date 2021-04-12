---
title: Funzioni di porting v
description: In IRIS GL si usano le variazioni sulla funzione v per specificare i vertici. La funzione OpenGL equivalente è glVertex di seguito sono riportati esempi di glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Porting di IRIS GL, vertici
- porting da IRIS GL, vertici
- porting in OpenGL da IRIS GL, vertici
- Porting OpenGL da IRIS GL, vertici
- funzioni di disegno, vertici
- vertici, porting da IRIS GL
- Porting di IRIS GL, funzioni v
- porting da IRIS GL, v Functions
- porting in OpenGL dalle funzioni di IRIS GL, v
- Porting OpenGL dalle funzioni di IRIS GL, v
- funzioni di disegno, funzioni v
- funzioni v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329420"
---
# <a name="porting-v-functions"></a><span data-ttu-id="7ac36-116">Funzioni di porting v</span><span class="sxs-lookup"><span data-stu-id="7ac36-116">Porting v Functions</span></span>

<span data-ttu-id="7ac36-117">In IRIS GL si usano le variazioni sulla funzione **v** per specificare i vertici.</span><span class="sxs-lookup"><span data-stu-id="7ac36-117">In IRIS GL, you use variations on the **v** function to specify vertices.</span></span> <span data-ttu-id="7ac36-118">La funzione OpenGL equivalente è [glVertex](glvertex-functions.md): di seguito sono riportati alcuni esempi di **glVertex**.</span><span class="sxs-lookup"><span data-stu-id="7ac36-118">The equivalent OpenGL function is [glVertex](glvertex-functions.md): Below are examples of **glVertex**.</span></span>

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

<span data-ttu-id="7ac36-119">La funzione **glVertex** accetta suffissi allo stesso modo di altre chiamate di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7ac36-119">The **glVertex** function takes suffixes the same way other OpenGL calls do.</span></span> <span data-ttu-id="7ac36-120">Le versioni vettoriali della chiamata accettano matrici di dimensioni appropriate come argomenti.</span><span class="sxs-lookup"><span data-stu-id="7ac36-120">The vector versions of the call take arrays of the proper size as arguments.</span></span> <span data-ttu-id="7ac36-121">Nella versione 2D, z = 0 e w = 1.</span><span class="sxs-lookup"><span data-stu-id="7ac36-121">In the 2-D version, z=0 and w=1.</span></span> <span data-ttu-id="7ac36-122">Nella versione 3D, w = 1.</span><span class="sxs-lookup"><span data-stu-id="7ac36-122">In the 3-D version, w=1.</span></span>

 

 




