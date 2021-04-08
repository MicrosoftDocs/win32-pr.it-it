---
title: Utilizzo di funzioni di callback
description: Le funzioni di callback GLU, gluBeginPolygon, gluTessVertex, gluNextContour e gluEndPolygon, sono simili alle funzioni Polygon di OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilità OpenGL (GLU), funzioni di callback
- GLU (utilità OpenGL), funzioni di callback
- Utilità OpenGL (GLU), a mosaico
- GLU (utilità OpenGL), mosaico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855818"
---
# <a name="using-callback-functions"></a><span data-ttu-id="9e692-107">Utilizzo di funzioni di callback</span><span class="sxs-lookup"><span data-stu-id="9e692-107">Using Callback Functions</span></span>

<span data-ttu-id="9e692-108">Le funzioni di callback GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), sono simili alle funzioni Polygon di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9e692-108">The GLU callback functions, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), are similar to the OpenGL polygon functions.</span></span>

<span data-ttu-id="9e692-109">In genere salvano i dati per i triangoli, le mesh triangolari e le ventole triangolo nelle strutture di dati definite dall'utente o negli elenchi di visualizzazione OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9e692-109">They typically save the data for the triangles, triangle meshes, and triangle fans in user-defined data structures or in OpenGL display lists.</span></span> <span data-ttu-id="9e692-110">Per eseguire il rendering dei poligoni, altro codice attraversa le strutture dei dati o chiama gli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9e692-110">To render the polygons, other code traverses the data structures or calls the display lists.</span></span> <span data-ttu-id="9e692-111">Sebbene le funzioni di callback possano chiamare funzioni OpenGL per visualizzare i poligoni direttamente, questa operazione non viene in genere eseguita, perché la suddivisione a mosaico può comportare un utilizzo intensivo di risorse di calcolo.</span><span class="sxs-lookup"><span data-stu-id="9e692-111">Although the callback functions could call OpenGL functions to display polygons directly, this is usually not done, as tessellation can be computationally resource-intensive.</span></span> <span data-ttu-id="9e692-112">È consigliabile salvare i dati se è possibile che si desideri visualizzarli nuovamente.</span><span class="sxs-lookup"><span data-stu-id="9e692-112">It's a good idea to save the data if there is any chance that you want to display it again.</span></span> <span data-ttu-id="9e692-113">Le funzioni di suddivisione a mosaico di GLU non restituiscono mai alcun nuovo vertice, quindi l'interpolazione di vertici, coordinate di trama o colori non è mai necessaria.</span><span class="sxs-lookup"><span data-stu-id="9e692-113">The GLU tessellation functions are guaranteed never to return any new vertices, so interpolation of vertices, texture coordinates, or colors is never required.</span></span>

 

 




