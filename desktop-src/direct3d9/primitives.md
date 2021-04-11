---
description: Una primitiva 3D è una raccolta di vertici che formano una singola entità 3D. La primitiva più semplice è costituita da una raccolta di punti in un sistema di coordinate 3D, denominato elenco di punti.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitive (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123432"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="83307-104">Primitive (grafica Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83307-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="83307-105">Una primitiva 3D è una raccolta di vertici che formano una singola entità 3D.</span><span class="sxs-lookup"><span data-stu-id="83307-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="83307-106">La primitiva più semplice è costituita da una raccolta di punti in un sistema di coordinate 3D, denominato elenco di punti.</span><span class="sxs-lookup"><span data-stu-id="83307-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="83307-107">Spesso le primitive 3D sono poligoni.</span><span class="sxs-lookup"><span data-stu-id="83307-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="83307-108">Un poligono è una figura 3D chiusa delimitata da almeno tre vertici.</span><span class="sxs-lookup"><span data-stu-id="83307-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="83307-109">Il poligono più semplice è un triangolo.</span><span class="sxs-lookup"><span data-stu-id="83307-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="83307-110">Microsoft Direct3D usa triangoli per comporre la maggior parte dei relativi poligoni perché tutti e tre i vertici in un triangolo sono sicuramente complanari.</span><span class="sxs-lookup"><span data-stu-id="83307-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="83307-111">Il rendering di vertici non pianificati non è efficiente.</span><span class="sxs-lookup"><span data-stu-id="83307-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="83307-112">È possibile combinare triangoli per formare poligoni e mesh complessi di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="83307-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="83307-113">Nella figura seguente viene illustrato un cubo.</span><span class="sxs-lookup"><span data-stu-id="83307-113">The following illustration shows a cube.</span></span> <span data-ttu-id="83307-114">Due triangoli formano ogni faccia del cubo.</span><span class="sxs-lookup"><span data-stu-id="83307-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="83307-115">L'intero set di triangoli costituisce una primitiva cubica.</span><span class="sxs-lookup"><span data-stu-id="83307-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="83307-116">È possibile applicare trame e materiali alle superfici delle primitive per fare in modo che vengano visualizzate come una singola forma a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="83307-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="83307-117">Per informazioni dettagliate, vedere [materiali (Direct3D 9)](materials.md) e [trame Direct3D (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="83307-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![illustrazione di un cubo con due triangoli in ogni viso](images/cube3d.png)

<span data-ttu-id="83307-119">È anche possibile usare triangoli per creare primitive le cui superfici sembrano essere curve smussate.</span><span class="sxs-lookup"><span data-stu-id="83307-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="83307-120">Nella figura seguente viene illustrato come una sfera può essere simulata con triangoli.</span><span class="sxs-lookup"><span data-stu-id="83307-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="83307-121">Dopo l'applicazione di un materiale, la sfera appare curva quando viene sottoposta a rendering.</span><span class="sxs-lookup"><span data-stu-id="83307-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="83307-122">Ciò è particolarmente vero se si usa l'ombreggiatura Gouraud.</span><span class="sxs-lookup"><span data-stu-id="83307-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="83307-123">Per informazioni dettagliate, vedere [ombreggiatura Gouraud](shading-modes.md).</span><span class="sxs-lookup"><span data-stu-id="83307-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![illustrazione di una sfera simulata usando triangoli](images/sphere3d.png)

<span data-ttu-id="83307-125">I dispositivi Direct3D possono creare e modificare i tipi di primitivi seguenti.</span><span class="sxs-lookup"><span data-stu-id="83307-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="83307-126">Elenchi di punti</span><span class="sxs-lookup"><span data-stu-id="83307-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="83307-127">Elenchi di righe</span><span class="sxs-lookup"><span data-stu-id="83307-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="83307-128">Strisce di linea</span><span class="sxs-lookup"><span data-stu-id="83307-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="83307-129">Elenchi di triangolo</span><span class="sxs-lookup"><span data-stu-id="83307-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="83307-130">Strisce triangolari</span><span class="sxs-lookup"><span data-stu-id="83307-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="83307-131">Ventilatori a triangolo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83307-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="83307-132">È possibile eseguire il rendering di tipi primitivi da un'applicazione C++ con uno dei metodi di rendering dell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="83307-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83307-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="83307-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83307-134">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="83307-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
