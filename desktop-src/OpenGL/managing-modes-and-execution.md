---
title: Gestione di modalità ed esecuzione
description: Gestione di modalità ed esecuzione
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298054"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="370ed-104">Gestione di modalità ed esecuzione</span><span class="sxs-lookup"><span data-stu-id="370ed-104">Managing Modes and Execution</span></span>

<span data-ttu-id="370ed-105">L'effetto di molte funzioni OpenGL dipende dal fatto che sia attiva una modalità specifica.</span><span class="sxs-lookup"><span data-stu-id="370ed-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="370ed-106">Le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) impostano tali modalità; [**glIsEnabled**](glisenabled.md) determina se è impostata una modalità specifica.</span><span class="sxs-lookup"><span data-stu-id="370ed-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="370ed-107">È possibile controllare l'esecuzione delle funzioni OpenGL precedentemente rilasciate con [**glFinish**](glfinish.md), che impone il completamento di tutte le funzioni di questo tipo, o [**glFlush**](glflush.md), che garantisce che tutte queste funzioni verranno completate in un intervallo di tempo limitato.</span><span class="sxs-lookup"><span data-stu-id="370ed-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="370ed-108">In una particolare implementazione di OpenGL, potrebbe essere possibile controllare determinati comportamenti con hint usando [**glHint**](glhint.md).</span><span class="sxs-lookup"><span data-stu-id="370ed-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="370ed-109">Questi comportamenti sono la qualità dell'interpolazione delle coordinate di trama e colore; accuratezza dei calcoli di nebbia; e la qualità di campionamento di punti, linee o poligoni con alias.</span><span class="sxs-lookup"><span data-stu-id="370ed-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="370ed-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="370ed-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="370ed-111">Modalità e riferimento all'esecuzione</span><span class="sxs-lookup"><span data-stu-id="370ed-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




