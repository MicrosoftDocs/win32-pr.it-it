---
title: Porting degli elenchi di visualizzazione
description: L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni in OpenGL non è possibile modificare gli elenchi di visualizzazione una volta creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.
ms.assetid: 617e19ff-6a55-4f7c-b229-075cdee8f1cf
keywords:
- Porting di IRIS GL, elenchi di visualizzazione
- porting da IRIS GL, elenchi di visualizzazione
- porting in OpenGL da IRIS GL, elenchi di visualizzazione
- Porting OpenGL da IRIS GL, elenchi di visualizzazione
- visualizzare elenchi, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461000e6d785f0d03bbbc8f738eba60768bc5d74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328820"
---
# <a name="porting-display-lists"></a><span data-ttu-id="8b7d7-108">Porting degli elenchi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="8b7d7-108">Porting Display Lists</span></span>

<span data-ttu-id="8b7d7-109">L'implementazione OpenGL degli elenchi di visualizzazione è simile all'implementazione di IRIS GL, con due eccezioni: in OpenGL non è possibile modificare gli elenchi di visualizzazione una volta creati e non è possibile chiamare funzioni dall'interno degli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-109">The OpenGL implementation of display lists is similar to the IRIS GL implementation, with two exceptions: in OpenGL you can't edit display lists once you've created them and you can't call functions from within display lists.</span></span>

<span data-ttu-id="8b7d7-110">Poiché non è possibile modificare o chiamare funzioni dall'interno degli elenchi di visualizzazione, queste funzioni di IRIS GL non hanno equivalenti in OpenGL:</span><span class="sxs-lookup"><span data-stu-id="8b7d7-110">Because you can't edit or call functions from within display lists, these IRIS GL functions have no equivalent in OpenGL:</span></span>

-   <span data-ttu-id="8b7d7-111">**editobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-111">**editobj**</span></span>
-   <span data-ttu-id="8b7d7-112">**objdelete**, **objinsert** e **objreplace**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-112">**objdelete**, **objinsert**, and **objreplace**</span></span>
-   <span data-ttu-id="8b7d7-113">**maketag**, **Gentag**, **ISTAG** e **DeltaG**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-113">**maketag**, **gentag**, **istag**, and **deltag**</span></span>
-   <span data-ttu-id="8b7d7-114">**callfunc**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-114">**callfunc**</span></span>

<span data-ttu-id="8b7d7-115">In IRIS GL usare le funzioni **makeobj** e **closeobj** per creare elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-115">In IRIS GL, you use the **makeobj** and **closeobj** functions to create display lists.</span></span> <span data-ttu-id="8b7d7-116">In OpenGL si usano [**glNewList**](glnewlist.md) e [**glEndList**](glendlist.md).</span><span class="sxs-lookup"><span data-stu-id="8b7d7-116">In OpenGL, you use [**glNewList**](glnewlist.md) and [**glEndList**](glendlist.md).</span></span>

<span data-ttu-id="8b7d7-117">La tabella seguente elenca le funzioni dell'elenco di visualizzazione di IRIS GL con le funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-117">The following table lists the IRIS GL display list functions with their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="8b7d7-118">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="8b7d7-118">IRIS GL function</span></span> | <span data-ttu-id="8b7d7-119">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-119">OpenGL function</span></span>                                                      | <span data-ttu-id="8b7d7-120">Significato</span><span class="sxs-lookup"><span data-stu-id="8b7d7-120">Meaning</span></span>                                                       |
|------------------|----------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8b7d7-121">**makeobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-121">**makeobj**</span></span>      | <span data-ttu-id="8b7d7-122">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-122">**glNewList**</span></span>                                                        | <span data-ttu-id="8b7d7-123">Crea un nuovo elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-123">Creates a new display list.</span></span>                                   |
| <span data-ttu-id="8b7d7-124">**closeobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-124">**closeobj**</span></span>     | <span data-ttu-id="8b7d7-125">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-125">**glEndList**</span></span>                                                        | <span data-ttu-id="8b7d7-126">Segnala la fine dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-126">Signals end of display list.</span></span>                                  |
| <span data-ttu-id="8b7d7-127">**callobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-127">**callobj**</span></span>      | <span data-ttu-id="8b7d7-128">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="8b7d7-128">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="8b7d7-129">Esegue l'elenco o gli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-129">Executes display list or lists.</span></span>                               |
| <span data-ttu-id="8b7d7-130">**isobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-130">**isobj**</span></span>        | [<span data-ttu-id="8b7d7-131">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-131">**glIsList**</span></span>](glislist.md)                                         | <span data-ttu-id="8b7d7-132">Verifica l'esistenza dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-132">Tests for display list existence.</span></span>                             |
| <span data-ttu-id="8b7d7-133">**DELOBJ**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-133">**delobj**</span></span>       | [<span data-ttu-id="8b7d7-134">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-134">**glDeleteLists**</span></span>](gldeletelists.md)                               | <span data-ttu-id="8b7d7-135">Elimina il gruppo contiguo di elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-135">Deletes contiguous group of display lists.</span></span>                    |
| <span data-ttu-id="8b7d7-136">**genobj**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-136">**genobj**</span></span>       | [<span data-ttu-id="8b7d7-137">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="8b7d7-137">**glGenLists**</span></span>](glgenlists.md)                                     | <span data-ttu-id="8b7d7-138">Genera il numero specificato di elenchi di visualizzazione vuoti contigui.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-138">Generates the given number of contiguous empty display lists.</span></span> |



 

<span data-ttu-id="8b7d7-139">Questo argomento include informazioni sui seguenti elementi.</span><span class="sxs-lookup"><span data-stu-id="8b7d7-139">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="8b7d7-140">Porting della funzione bbox2</span><span class="sxs-lookup"><span data-stu-id="8b7d7-140">Porting the bbox2 Function</span></span>](porting-the-bbox2-function.md)
-   [<span data-ttu-id="8b7d7-141">Porting degli elenchi di visualizzazione modificati</span><span class="sxs-lookup"><span data-stu-id="8b7d7-141">Porting Edited Display Lists</span></span>](porting-edited-display-lists.md)
-   [<span data-ttu-id="8b7d7-142">Una porta di esempio di un elenco di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="8b7d7-142">A Sample Port of a Display List</span></span>](a-sample-port-of-a-display-list.md)

 

 




