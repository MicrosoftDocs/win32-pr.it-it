---
title: Uso degli elenchi di visualizzazione
description: Uso degli elenchi di visualizzazione
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, elenchi di visualizzazione
- visualizzazione degli elenchi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855817"
---
# <a name="using-display-lists"></a><span data-ttu-id="58227-105">Uso degli elenchi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="58227-105">Using Display Lists</span></span>

<span data-ttu-id="58227-106">Un elenco di visualizzazione è un gruppo di funzioni OpenGL che è stato archiviato per l'esecuzione successiva.</span><span class="sxs-lookup"><span data-stu-id="58227-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="58227-107">La funzione [**glNewList**](glnewlist.md) inizia la creazione di un elenco di visualizzazione e [**glEndList**](glendlist.md) lo termina.</span><span class="sxs-lookup"><span data-stu-id="58227-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="58227-108">Con poche eccezioni, le funzioni OpenGL chiamate tra **glNewList** e **glEndList** vengono aggiunte all'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="58227-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="58227-109">Per un elenco delle funzioni che non è possibile archiviare ed eseguire dall'interno di un elenco di visualizzazione, vedere **glNewList** . Per attivare l'esecuzione di un elenco o di un set di elenchi, utilizzare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) e specificare il numero di identificazione di un elenco o di elenchi specifici.</span><span class="sxs-lookup"><span data-stu-id="58227-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="58227-110">È possibile gestire gli indici usati per identificare gli elenchi di visualizzazione con [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)e l' [**elenco a pagina.**](glislist.md)</span><span class="sxs-lookup"><span data-stu-id="58227-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="58227-111">Per eliminare un set di elenchi di visualizzazione, usare [**glDeleteLists**](gldeletelists.md).</span><span class="sxs-lookup"><span data-stu-id="58227-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58227-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58227-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58227-113">Riferimenti a elenchi di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="58227-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




