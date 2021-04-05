---
title: Primitive e comandi
description: Primitive e comandi
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitive
- OpenGL, comandi
- primitive OpenGL
- comandi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709460"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="63558-107">Primitive e comandi</span><span class="sxs-lookup"><span data-stu-id="63558-107">Primitives and Commands</span></span>

<span data-ttu-id="63558-108">OpenGL disegna punti *primitivi* , segmenti di linea o polygonssubject a diverse modalità selezionabili.</span><span class="sxs-lookup"><span data-stu-id="63558-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="63558-109">È possibile controllare le modalità indipendentemente l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="63558-109">You can control modes independently of one another.</span></span> <span data-ttu-id="63558-110">Ciò significa che l'impostazione di una modalità non influisce sulla possibilità di impostare altre modalità (anche se molte modalità possono interagire per determinare la fine del buffer).</span><span class="sxs-lookup"><span data-stu-id="63558-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="63558-111">Per specificare le primitive, impostare le modalità ed eseguire altre operazioni OpenGL, è possibile eseguire i comandi sotto forma di chiamate di funzione.</span><span class="sxs-lookup"><span data-stu-id="63558-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="63558-112">Le primitive sono definite da un gruppo di uno o più *vertici*.</span><span class="sxs-lookup"><span data-stu-id="63558-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="63558-113">Un vertice definisce un punto, un endpoint di una linea o un angolo di un poligono in cui si incontrano due bordi.</span><span class="sxs-lookup"><span data-stu-id="63558-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="63558-114">I dati (costituiti da coordinate dei vertici, colori, normali, coordinate di trama e flag perimetrali) sono associati a un vertice e ogni vertice e i dati associati vengono elaborati in modo indipendente, nell'ordine e nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="63558-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="63558-115">Le uniche eccezioni a questa regola sono i casi in cui il gruppo di vertici deve essere ritagliato in modo che una particolare primitiva entri in un'area specificata.</span><span class="sxs-lookup"><span data-stu-id="63558-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="63558-116">In questo caso, i dati dei vertici possono essere modificati e nuovi vertici creati.</span><span class="sxs-lookup"><span data-stu-id="63558-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="63558-117">Il tipo di ritaglio dipende dalla primitiva rappresentata dal gruppo di vertici.</span><span class="sxs-lookup"><span data-stu-id="63558-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="63558-118">I comandi vengono sempre elaborati nell'ordine in cui vengono ricevuti, sebbene sia possibile che si verifichi un ritardo indeterminato prima che un comando venga applicato.</span><span class="sxs-lookup"><span data-stu-id="63558-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="63558-119">Ciò significa che ogni primitiva viene disegnata completamente prima che un comando successivo venga applicato.</span><span class="sxs-lookup"><span data-stu-id="63558-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="63558-120">Significa anche che i comandi di query di stato restituiscono dati coerenti con l'esecuzione completa di tutti i comandi OpenGL precedentemente rilasciati.</span><span class="sxs-lookup"><span data-stu-id="63558-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




