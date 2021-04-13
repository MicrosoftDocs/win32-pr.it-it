---
title: Selezione
description: Selection restituisce il contenuto corrente dello stack dei nomi, ovvero una matrice di nomi con valori interi.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modalità di selezione OpenGL
- selezione riscontri OpenGL
- hit record OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330671"
---
# <a name="selection"></a><span data-ttu-id="acd57-106">Selezione</span><span class="sxs-lookup"><span data-stu-id="acd57-106">Selection</span></span>

<span data-ttu-id="acd57-107">Selection restituisce il contenuto corrente dello stack dei nomi, ovvero una matrice di nomi con valori interi.</span><span class="sxs-lookup"><span data-stu-id="acd57-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="acd57-108">Assegnare i nomi e compilare lo stack dei nomi all'interno del codice di modellazione che specifica la geometria degli oggetti che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="acd57-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="acd57-109">Quindi, in modalità di selezione, ogni volta che una primitiva interseca il volume di clip, si verifica un riscontro di selezione.</span><span class="sxs-lookup"><span data-stu-id="acd57-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="acd57-110">Il record di hit, scritto nella matrice di selezione fornita con [**glSelectBuffer**](glselectbuffer.md), contiene informazioni sul contenuto dello stack dei nomi al momento del raggiungimento.</span><span class="sxs-lookup"><span data-stu-id="acd57-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="acd57-111">Chiamare [**glSelectBuffer**](glselectbuffer.md) prima di inserire OpenGL in modalità di selezione con [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="acd57-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="acd57-112">Non è garantito che l'intero contenuto dello stack dei nomi venga restituito fino a quando non si chiama **glRenderMode** per portare OpenGL fuori dalla modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="acd57-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="acd57-113">Modificare lo stack dei nomi con [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)e [**glPopName**](glpopname.md).</span><span class="sxs-lookup"><span data-stu-id="acd57-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="acd57-114">È anche possibile usare [**gluPickMatrix**](glupickmatrix.md) per la selezione.</span><span class="sxs-lookup"><span data-stu-id="acd57-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




