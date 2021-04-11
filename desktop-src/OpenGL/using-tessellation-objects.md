---
title: Uso di oggetti mosaico
description: Poiché viene descritto un poligono complesso e tassellati, sono necessari dati associati, ad esempio i vertici, i bordi e le funzioni di callback.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilità OpenGL (GLU), oggetti a mosaico
- GLU (utilità OpenGL), oggetti a mosaico
- oggetti a mosaico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329196"
---
# <a name="using-tessellation-objects"></a><span data-ttu-id="237e3-106">Uso di oggetti mosaico</span><span class="sxs-lookup"><span data-stu-id="237e3-106">Using Tessellation Objects</span></span>

<span data-ttu-id="237e3-107">Poiché viene descritto un poligono complesso e tassellati, sono necessari dati associati, ad esempio i vertici, i bordi e le funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="237e3-107">As a complex polygon is being described and tessellated, it requires associated data, such as the vertices, edges, and callback functions.</span></span> <span data-ttu-id="237e3-108">Tutti questi dati sono associati a un singolo oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="237e3-108">All this data is tied to a single tessellation object.</span></span> <span data-ttu-id="237e3-109">Per conteggiarla suddividerla un poligono, è necessario innanzitutto usare la funzione [**gluNewTess**](glunewtess.md) che crea un nuovo oggetto a mosaico e restituisce un puntatore.</span><span class="sxs-lookup"><span data-stu-id="237e3-109">To tessellate a polygon, you first use the [**gluNewTess**](glunewtess.md) function which creates a new tessellation object and returns a pointer to it.</span></span> <span data-ttu-id="237e3-110">Se la funzione ha esito negativo, viene restituito un puntatore null.</span><span class="sxs-lookup"><span data-stu-id="237e3-110">A null pointer is returned if the function fails.</span></span>

<span data-ttu-id="237e3-111">Se un oggetto a mosaico non è più necessario, è possibile eliminarlo e liberare tutta la memoria associata con [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="237e3-111">If you no longer need a tessellation object, you can delete it and free all associated memory with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="237e3-112">È possibile riutilizzare un unico oggetto a mosaico per tutti i tassellature.</span><span class="sxs-lookup"><span data-stu-id="237e3-112">You can reuse a single tessellation object for all your tessellations.</span></span> <span data-ttu-id="237e3-113">Questo oggetto è necessario solo perché le funzioni di libreria potrebbero dover eseguire la propria tassellature e devono essere in grado di eseguire questa operazione senza interferire con i mosaico eseguiti dal programma.</span><span class="sxs-lookup"><span data-stu-id="237e3-113">This object is required only because library functions may need to do their own tessellations, and they should be able to do so without interfering with any tessellation that your program is performing.</span></span> <span data-ttu-id="237e3-114">Sono inoltre utili più oggetti a mosaico se si desidera utilizzare set di callback diversi per tassellature diversi.</span><span class="sxs-lookup"><span data-stu-id="237e3-114">Multiple tessellation objects are also useful if you want to use different sets of callbacks for different tessellations.</span></span> <span data-ttu-id="237e3-115">In genere, tuttavia, si alloca un singolo oggetto a mosaico e lo si usa per tutti tassellature.</span><span class="sxs-lookup"><span data-stu-id="237e3-115">Typically, however, you allocate a single tessellation object and use it for all the tessellations.</span></span> <span data-ttu-id="237e3-116">Non è necessario liberarlo, perché usa una piccola quantità di memoria.</span><span class="sxs-lookup"><span data-stu-id="237e3-116">There's no real need to free it, because it uses a small amount of memory.</span></span> <span data-ttu-id="237e3-117">D'altra parte, se si sta scrivendo una funzione di libreria che usa il mosaico di GLU, prestare attenzione a liberare tutti gli oggetti a mosaico creati.</span><span class="sxs-lookup"><span data-stu-id="237e3-117">On the other hand, if you're writing a library function that uses GLU tessellation, be careful to free any tessellation objects you create.</span></span>

 

 




