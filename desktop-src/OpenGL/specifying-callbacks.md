---
title: Specifica di callback
description: È possibile specificare fino a cinque funzioni di callback per uno schema a mosaico.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilità OpenGL (GLU), che specifica le funzioni di callback
- GLU (utilità OpenGL), specifica di funzioni di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516030"
---
# <a name="specifying-callbacks"></a><span data-ttu-id="3e476-105">Specifica di callback</span><span class="sxs-lookup"><span data-stu-id="3e476-105">Specifying Callbacks</span></span>

<span data-ttu-id="3e476-106">È possibile specificare fino a cinque funzioni di callback per uno schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="3e476-106">You can specify up to five callback functions for a tessellation.</span></span> <span data-ttu-id="3e476-107">Tutte le funzioni non specificate non vengono chiamate durante la suddivisione a mosaico e non vengono restituite informazioni che potrebbero essere state restituite.</span><span class="sxs-lookup"><span data-stu-id="3e476-107">Any functions that you do not specify are not called during the tessellation, and you do not get any information they might have returned.</span></span> <span data-ttu-id="3e476-108">Si specificano le funzioni di callback con [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="3e476-108">You specify the callback functions with [*gluTessCallback*](glutess.md).</span></span>

<span data-ttu-id="3e476-109">La funzione **gluTessCallback** associa la funzione di callback *FN* al *tessobj* dell'oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="3e476-109">The **gluTessCallback** function associates the callback function *fn* with the tessellation object *tessobj*.</span></span> <span data-ttu-id="3e476-110">Il tipo del callback è determinato dal *tipo* di parametro, che può essere **Glu \_ Begin**, **Glu \_ Edge \_ flag**, **Glu \_ Vertex**, **Glu \_ end** o **Glu \_ Error**.</span><span class="sxs-lookup"><span data-stu-id="3e476-110">The type of the callback is determined by the parameter *type*, which can be **GLU\_BEGIN**, **GLU\_EDGE\_FLAG**, **GLU\_VERTEX**, **GLU\_END**, or **GLU\_ERROR**.</span></span> <span data-ttu-id="3e476-111">Le cinque funzioni di callback possibili includono i prototipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e476-111">The five possible callback functions have the following prototypes.</span></span>



| <span data-ttu-id="3e476-112">Funzione di callback</span><span class="sxs-lookup"><span data-stu-id="3e476-112">Callback function</span></span>   | <span data-ttu-id="3e476-113">Prototipo</span><span class="sxs-lookup"><span data-stu-id="3e476-113">Prototype</span></span>                                    |
|---------------------|----------------------------------------------|
| <span data-ttu-id="3e476-114">**\_inizio Glu**</span><span class="sxs-lookup"><span data-stu-id="3e476-114">**GLU\_BEGIN**</span></span>      | <span data-ttu-id="3e476-115">**void** **Begin**(\**GLEnum \* \* \* tipo* );</span><span class="sxs-lookup"><span data-stu-id="3e476-115">**void** **begin**(\**GLenum\*\*\*type* );</span></span>       |
| <span data-ttu-id="3e476-116">**\_flag di Edge Glu \_**</span><span class="sxs-lookup"><span data-stu-id="3e476-116">**GLU\_EDGE\_FLAG**</span></span> | <span data-ttu-id="3e476-117">**void** **EdgeFlag**(\**GLboolean \* \* \* flag* );</span><span class="sxs-lookup"><span data-stu-id="3e476-117">**void** **edgeFlag**(\**GLboolean\*\*\*flag* );</span></span> |
| <span data-ttu-id="3e476-118">**\_vertice Glu**</span><span class="sxs-lookup"><span data-stu-id="3e476-118">**GLU\_VERTEX**</span></span>     | <span data-ttu-id="3e476-119">**void** **Vertex**(\**void \* \* \* \* Data* );</span><span class="sxs-lookup"><span data-stu-id="3e476-119">**void** **vertex**(\**void \*\*\*\*data* );</span></span>     |
| <span data-ttu-id="3e476-120">**\_estremità Glu**</span><span class="sxs-lookup"><span data-stu-id="3e476-120">**GLU\_END**</span></span>        | <span data-ttu-id="3e476-121">**void** **end**( *void* );</span><span class="sxs-lookup"><span data-stu-id="3e476-121">**void** **end**( *void* );</span></span>                  |
| <span data-ttu-id="3e476-122">**\_errore Glu**</span><span class="sxs-lookup"><span data-stu-id="3e476-122">**GLU\_ERROR**</span></span>      | <span data-ttu-id="3e476-123"> **errore** void \(**GLEnum\ *\ *\ * errno* );</span><span class="sxs-lookup"><span data-stu-id="3e476-123">**void** **error**(\**GLenum\*\*\*errno* );</span></span>      |



 

<span data-ttu-id="3e476-124">Per modificare una funzione di callback, chiamare [*gluTessCallback*](glutess.md) con la nuova funzione.</span><span class="sxs-lookup"><span data-stu-id="3e476-124">To change a callback function, call [*gluTessCallback*](glutess.md) with the new function.</span></span> <span data-ttu-id="3e476-125">Per eliminare una funzione di callback senza sostituirla con una nuova, passare **gluTessCallback** un puntatore null per la funzione appropriata.</span><span class="sxs-lookup"><span data-stu-id="3e476-125">To eliminate a callback function without replacing it with a new one, pass **gluTessCallback** a null pointer for the appropriate function.</span></span>

<span data-ttu-id="3e476-126">Quando si procede a mosaico, le funzioni di callback vengono chiamate in modo analogo al modo in cui si usano le funzioni OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)e [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3e476-126">As tessellation proceeds, the callback functions are called in a manner similar to the way you would use the OpenGL functions [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md), and [**glEnd**](glend.md).</span></span>

<span data-ttu-id="3e476-127">La funzione **Glu \_ Begin** callback viene richiamata con uno dei tre parametri possibili:</span><span class="sxs-lookup"><span data-stu-id="3e476-127">The **GLU\_BEGIN** callback function is invoked with one of three possible parameters:</span></span>

-   <span data-ttu-id="3e476-128">\_ventola del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="3e476-128">GL\_TRIANGLE\_FAN</span></span>
-   <span data-ttu-id="3e476-129">\_striscia del triangolo GL \_</span><span class="sxs-lookup"><span data-stu-id="3e476-129">GL\_TRIANGLE\_STRIP</span></span>
-   <span data-ttu-id="3e476-130">triangoli GL \_</span><span class="sxs-lookup"><span data-stu-id="3e476-130">GL\_TRIANGLES</span></span>

<span data-ttu-id="3e476-131">Dopo aver chiamato la funzione **Glu \_ Begin** callback e prima di chiamare la funzione di callback associata a **Glu \_ end**, viene richiamata una combinazione del **\_ \_ flag di Edge Glu** e dei callback del **\_ vertice Glu** .</span><span class="sxs-lookup"><span data-stu-id="3e476-131">After calling the **GLU\_BEGIN** callback function, and before calling the callback function associated with **GLU\_END**, some combination of the **GLU\_EDGE\_FLAG** and **GLU\_VERTEX** callbacks is invoked.</span></span> <span data-ttu-id="3e476-132">I vertici e i flag perimetrali associati vengono interpretati esattamente come sono in OpenGL tra **glBegin**( \_ ventola del triangolo GL \_ ), **glBegin**(striscia del \_ triangolo GL \_ ) o **GlBegin**( \_ triangoli GL **)** e l'oggetto **glEnd** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3e476-132">The associated vertices and edge flags are interpreted exactly as they are in OpenGL between **glBegin**(GL\_TRIANGLE\_FAN), **glBegin**(GL\_TRIANGLE\_STRIP), or **glBegin**(GL\_TRIANGLES **)** and the matching **glEnd**.</span></span>

<span data-ttu-id="3e476-133">Poiché i flag perimetrali non hanno senso in una ventola a triangolo o in una striscia di triangolo, se è presente una funzione di callback associata al **\_ \_ flag di Edge di Glu**, il callback di **Glu \_ Begin** viene chiamato solo con **\_ triangoli GL**.</span><span class="sxs-lookup"><span data-stu-id="3e476-133">Because edge flags make no sense in a triangle fan or triangle strip, if there is a callback function associated with **GLU\_EDGE\_FLAG**, the **GLU\_BEGIN** callback is called only with **GL\_TRIANGLES**.</span></span> <span data-ttu-id="3e476-134">La funzione di callback di **Glu \_ Edge \_ flag** funziona in modo analogo alla funzione [glEdgeFlag](gledgeflag-functions.md) di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3e476-134">The **GLU\_EDGE\_FLAG** callback function works analogously to the OpenGL [glEdgeFlag](gledgeflag-functions.md) function.</span></span>

<span data-ttu-id="3e476-135">Se si verifica un errore durante il mosaico, viene richiamata la funzione di callback degli errori.</span><span class="sxs-lookup"><span data-stu-id="3e476-135">If there is an error during the tessellation, the error callback function is invoked.</span></span> <span data-ttu-id="3e476-136">Alla funzione di callback di errore viene passato un numero di errore GLU.</span><span class="sxs-lookup"><span data-stu-id="3e476-136">The error callback function is passed a GLU error number.</span></span> <span data-ttu-id="3e476-137">È possibile ottenere una stringa di caratteri che descrive l'errore con la funzione [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="3e476-137">You can obtain a character string describing the error with the [**gluErrorString**](gluerrorstring.md) function.</span></span>

 

 




