---
title: Porting del codice in modalità MSINGLE
description: OpenGL non ha un equivalente per la modalità MSINGLE, a matrice singola.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Porting di IRIS GL, modalità MSINGLE
- porting da IRIS GL, modalità MSINGLE
- porting in OpenGL da IRIS GL, modalità MSINGLE
- Porting OpenGL da IRIS GL, modalità MSINGLE
- Modalità MSINGLE
- Porting di IRIS GL, modalità a matrice singola
- porting da IRIS GL, modalità a matrice singola
- porting in OpenGL da IRIS GL, modalità a matrice singola
- Porting OpenGL da IRIS GL, modalità a matrice singola
- modalità a matrice singola
- modalità a doppia matrice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396338"
---
# <a name="porting-msingle-mode-code"></a><span data-ttu-id="617c2-114">Porting del codice in modalità MSINGLE</span><span class="sxs-lookup"><span data-stu-id="617c2-114">Porting MSINGLE Mode Code</span></span>

<span data-ttu-id="617c2-115">OpenGL non ha un equivalente per la modalità **MSINGLE**, a matrice singola.</span><span class="sxs-lookup"><span data-stu-id="617c2-115">OpenGL has no equivalent for **MSINGLE**, single-matrix mode.</span></span> <span data-ttu-id="617c2-116">Anche se l'uso di questa modalità è stato sconsigliato, è l'impostazione predefinita per IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="617c2-116">Though use of this mode has been discouraged, it is the default for IRIS GL.</span></span> <span data-ttu-id="617c2-117">Se il programma IRIS GL usa la modalità a matrice singola, è necessario riscriverlo per usare solo la modalità a matrice doppia.</span><span class="sxs-lookup"><span data-stu-id="617c2-117">If your IRIS GL program uses the single-matrix mode, you need to rewrite it to use double-matrix mode only.</span></span> <span data-ttu-id="617c2-118">OpenGL è sempre in modalità a doppia matrice ed è inizialmente in modalità GL \_ MODELVIEW.</span><span class="sxs-lookup"><span data-stu-id="617c2-118">OpenGL is always in double-matrix mode, and is initially in GL\_MODELVIEW mode.</span></span>

<span data-ttu-id="617c2-119">La maggior parte del codice IRIS GL in modalità MSINGLE è simile a quanto segue:</span><span class="sxs-lookup"><span data-stu-id="617c2-119">Most IRIS GL code in MSINGLE mode looks like this:</span></span>

``` syntax
projectionmatrix();
```

<span data-ttu-id="617c2-120">dove *ProjectionMatrix* è uno dei seguenti: **Ortho**, **ortho2**, **Perspective** o **Window**.</span><span class="sxs-lookup"><span data-stu-id="617c2-120">where *projectionmatrix* is one of: **ortho**, **ortho2**, **perspective**, or **window**.</span></span> <span data-ttu-id="617c2-121">Per eseguire la porta in OpenGL, sostituire la funzione *ProjectionMatrix* in modalità **MSINGLE** con:</span><span class="sxs-lookup"><span data-stu-id="617c2-121">To port to OpenGL, replace the **MSINGLE** -mode *projectionmatrix* function with:</span></span>


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




