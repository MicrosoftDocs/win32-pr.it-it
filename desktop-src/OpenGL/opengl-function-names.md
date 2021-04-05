---
title: Nomi di funzioni OpenGL
description: Molte funzioni OpenGL sono varianti tra loro, in particolare per quanto riguarda i tipi di dati degli argomenti.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomi di funzione
- nomi di funzione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710606"
---
# <a name="opengl-function-names"></a><span data-ttu-id="6bb04-105">Nomi di funzioni OpenGL</span><span class="sxs-lookup"><span data-stu-id="6bb04-105">OpenGL Function Names</span></span>

<span data-ttu-id="6bb04-106">Molte funzioni OpenGL sono varianti tra loro, in particolare per quanto riguarda i tipi di dati degli argomenti.</span><span class="sxs-lookup"><span data-stu-id="6bb04-106">Many OpenGL functions are variations of each other, differing mostly in the data types of their arguments.</span></span> <span data-ttu-id="6bb04-107">Alcune funzioni differiscono per il numero di argomenti correlati e se tali argomenti possono essere specificati come vettore o devono essere specificati separatamente in un elenco.</span><span class="sxs-lookup"><span data-stu-id="6bb04-107">Some functions differ in the number of related arguments and whether those arguments can be specified as a vector or must be specified separately in a list.</span></span> <span data-ttu-id="6bb04-108">Se ad esempio si usa la funzione **glVertex2f** , è necessario fornire le coordinate x e y come numeri a virgola mobile a 32 bit; con **glVertex3sv**, è necessario fornire una matrice di tre valori integer brevi (a 16 bit) per x, y e z.</span><span class="sxs-lookup"><span data-stu-id="6bb04-108">For example, if you use the **glVertex2f** function, you need to supply x- and y-coordinates as 32-bit floating-point numbers; with **glVertex3sv**, you must supply an array of three short (16-bit) integer values for x, y, and z.</span></span> <span data-ttu-id="6bb04-109">Negli argomenti seguenti viene utilizzato solo il nome di base della funzione.</span><span class="sxs-lookup"><span data-stu-id="6bb04-109">Only the base name of the function is used in the topics that follow.</span></span> <span data-ttu-id="6bb04-110">Un asterisco indica che il nome effettivo della funzione può essere maggiore di quello visualizzato.</span><span class="sxs-lookup"><span data-stu-id="6bb04-110">An asterisk indicates that there may be more to the actual function name than is shown.</span></span> <span data-ttu-id="6bb04-111">Ad esempio, [glVertex \*](glvertex-functions.md) sta per tutte le varianti della funzione usata per specificare i vertici: **glVertex2d**, **glVertex2f**, **glVertex2i** e così via.</span><span class="sxs-lookup"><span data-stu-id="6bb04-111">For example, [glVertex\*](glvertex-functions.md) stands for all the variations of the function you use to specify vertices: **glVertex2d**, **glVertex2f**, **glVertex2i**, and so on.</span></span>

<span data-ttu-id="6bb04-112">L'effetto di una funzione OpenGL può variare a seconda che determinate modalità siano abilitate.</span><span class="sxs-lookup"><span data-stu-id="6bb04-112">The effect of an OpenGL function can vary depending on whether certain modes are enabled.</span></span> <span data-ttu-id="6bb04-113">Ad esempio, è necessario abilitare l'illuminazione se le funzioni correlate all'illuminazione devono produrre un oggetto illuminato correttamente.</span><span class="sxs-lookup"><span data-stu-id="6bb04-113">For example, you need to enable lighting if the lighting-related functions are to produce a properly lit object.</span></span> <span data-ttu-id="6bb04-114">Per abilitare una particolare modalità, usare la funzione [**glEnable**](glenable.md) e fornire la costante appropriata per identificare la modalità (ad esempio, l' \_ illuminazione GL).</span><span class="sxs-lookup"><span data-stu-id="6bb04-114">To enable a particular mode, use the [**glEnable**](glenable.md) function and supply the appropriate constant to identify the mode (for example, GL\_LIGHTING).</span></span> <span data-ttu-id="6bb04-115">Per disabilitare una modalità, usare [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="6bb04-115">To disable a mode, use [**glDisable**](gldisable.md).</span></span> <span data-ttu-id="6bb04-116">Vedere **glEnable** per un elenco completo delle modalità che è possibile abilitare.</span><span class="sxs-lookup"><span data-stu-id="6bb04-116">See **glEnable** for a complete list of the modes that can be enabled.</span></span>

 

 




