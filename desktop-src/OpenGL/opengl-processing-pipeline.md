---
title: Pipeline di elaborazione OpenGL
description: Pipeline di elaborazione OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline di elaborazione
- elaborazione della pipeline OpenGL
- OpenGL della pipeline
- framebuffer, pipeline di elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567942"
---
# <a name="opengl-processing-pipeline"></a><span data-ttu-id="1f49d-107">Pipeline di elaborazione OpenGL</span><span class="sxs-lookup"><span data-stu-id="1f49d-107">OpenGL Processing Pipeline</span></span>

<span data-ttu-id="1f49d-108">Molte funzioni OpenGL vengono usate in modo specifico per disegnare oggetti quali punti, linee, poligoni e bitmap.</span><span class="sxs-lookup"><span data-stu-id="1f49d-108">Many OpenGL functions are used specifically for drawing objects such as points, lines, polygons, and bitmaps.</span></span> <span data-ttu-id="1f49d-109">Alcune funzioni controllano il modo in cui si verificano alcuni di questi disegni, ad esempio quelli che abilitano l'anti-aliasing o la texturing.</span><span class="sxs-lookup"><span data-stu-id="1f49d-109">Some functions control the way that some of this drawing occurs (such as those that enable antialiasing or texturing).</span></span> <span data-ttu-id="1f49d-110">Altre funzioni sono specificamente interessate dalla manipolazione del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="1f49d-110">Other functions are specifically concerned with framebuffer manipulation.</span></span> <span data-ttu-id="1f49d-111">Negli argomenti di questa sezione viene descritto il funzionamento combinato di tutte le funzioni OpenGL per creare la pipeline di elaborazione OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1f49d-111">The topics in this section describe how all of the OpenGL functions work together to create the OpenGL processing pipeline.</span></span> <span data-ttu-id="1f49d-112">In questa sezione vengono inoltre esaminate in dettaglio le fasi in cui i dati vengono effettivamente elaborati e le fasi vengono legate alle funzioni OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1f49d-112">This section also takes a closer look at the stages in which data is actually processed, and ties these stages to OpenGL functions.</span></span>

<span data-ttu-id="1f49d-113">Il diagramma seguente illustra la pipeline di elaborazione OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1f49d-113">The following diagram details the OpenGL processing pipeline.</span></span> <span data-ttu-id="1f49d-114">Per la maggior parte della pipeline, è possibile visualizzare tre frecce verticali tra le fasi principali.</span><span class="sxs-lookup"><span data-stu-id="1f49d-114">For most of the pipeline, you can see three vertical arrows between the major stages.</span></span> <span data-ttu-id="1f49d-115">Queste frecce rappresentano i vertici e i due tipi di dati principali che possono essere associati ai vertici, ovvero i valori dei colori e le coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="1f49d-115">These arrows represent vertices and the two primary types of data that can be associated with vertices: color values and texture coordinates.</span></span> <span data-ttu-id="1f49d-116">Si noti inoltre che i vertici vengono assemblati in primitive, quindi in frammenti e infine in pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="1f49d-116">Also note that vertices are assembled into primitives, then into fragments, and finally into pixels in the framebuffer.</span></span> <span data-ttu-id="1f49d-117">Questa progressione viene discussa in modo più dettagliato in [vertici](vertices.md), [primitivi](primitives.md), [frammenti](fragments.md)e [pixel](pixels.md).</span><span class="sxs-lookup"><span data-stu-id="1f49d-117">This progression is discussed in more detail in [Vertices](vertices.md), [Primitives](primitives.md), [Fragments](fragments.md), and [Pixels](pixels.md).</span></span>

![Diagramma che illustra la pipeline di elaborazione OpenGL.](images/proc01.png)

 

 




