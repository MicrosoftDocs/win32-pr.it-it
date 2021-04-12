---
title: Porting di sfere
description: Quando si trasferiscono le sfere a OpenGL, tenere presenti i punti seguenti
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Porting di IRIS GL, sfere
- porting da IRIS GL, sfere
- porting in OpenGL da IRIS GL, sfere
- Porting OpenGL da IRIS GL, sfere
- funzioni di disegno, sfere
- sfere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396326"
---
# <a name="porting-spheres"></a><span data-ttu-id="2f6d1-109">Porting di sfere</span><span class="sxs-lookup"><span data-stu-id="2f6d1-109">Porting Spheres</span></span>

<span data-ttu-id="2f6d1-110">Quando si trasferiscono le sfere a OpenGL, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2f6d1-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="2f6d1-111">Non è possibile controllare il tipo di primitive usato per creare la sfera.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="2f6d1-112">È possibile controllare la precisione del disegno in un altro modo: usare i parametri slices e stacks.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="2f6d1-113">Le sezioni sono longitudinali; gli stack sono latitudinali.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="2f6d1-114">Le sfere vengono disegnate al centro dell'origine.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="2f6d1-115">Anziché specificare il percorso, come avviene con la funzione **sphdraw** di Iris GL, prima di una chiamata alla funzione Glu [**gluSphere**](glusphere.md) con una traduzione.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="2f6d1-116">La libreria Sphere non è ancora disponibile per OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="2f6d1-117">La tabella seguente elenca le funzioni di IRIS GL per la creazione di sfere e le relative funzioni GLU equivalenti, ove disponibili.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="2f6d1-118">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="2f6d1-118">IRIS GL function</span></span> | <span data-ttu-id="2f6d1-119">GLU (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f6d1-119">GLU function</span></span>                                 | <span data-ttu-id="2f6d1-120">Significato</span><span class="sxs-lookup"><span data-stu-id="2f6d1-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="2f6d1-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-121">**sphobj**</span></span>       | [<span data-ttu-id="2f6d1-122">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="2f6d1-123">Crea un nuovo oggetto Sphere.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="2f6d1-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-124">**sphfree**</span></span>      | [<span data-ttu-id="2f6d1-125">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="2f6d1-126">Elimina l'oggetto Sphere e la memoria libera utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="2f6d1-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-127">**sphdraw**</span></span>      | [<span data-ttu-id="2f6d1-128">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="2f6d1-129">Disegna una sfera.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="2f6d1-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="2f6d1-131">Imposta gli attributi della sfera.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="2f6d1-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="2f6d1-133">Controlla l'orientamento della sfera.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="2f6d1-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="2f6d1-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="2f6d1-135">Restituisce il numero di poligoni nella sfera corrente.</span><span class="sxs-lookup"><span data-stu-id="2f6d1-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="2f6d1-136">??</span><span class="sxs-lookup"><span data-stu-id="2f6d1-136">??</span></span>

 

 




