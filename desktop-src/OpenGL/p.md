---
title: P (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parametri
- Divisione prospettiva
- pixel
- punti
- poligoni
- Primitives
- matrici di proiezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963677"
---
# <a name="p-opengl"></a><span data-ttu-id="a0a56-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="a0a56-110">P (OpenGL)</span></span>

<span data-ttu-id="a0a56-111">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="a0a56-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="a0a56-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parametro**</span><span class="sxs-lookup"><span data-stu-id="a0a56-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-113">Valore passato come argomento a un comando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a0a56-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="a0a56-114">A volte uno dei valori passati per riferimento a un comando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a0a56-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**Divisione prospettiva**</span><span class="sxs-lookup"><span data-stu-id="a0a56-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-116">Divisione di x, y e z per w, eseguita nelle coordinate di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a0a56-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="a0a56-117">Vedere anche [coordinate di ritaglio](c.md).</span><span class="sxs-lookup"><span data-stu-id="a0a56-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span><span class="sxs-lookup"><span data-stu-id="a0a56-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-119">Elemento Picture.</span><span class="sxs-lookup"><span data-stu-id="a0a56-119">Picture element.</span></span> <span data-ttu-id="a0a56-120">I bit nella posizione (x, y) di tutti i bitplane nel framebuffer costituiscono il singolo pixel (x, y).</span><span class="sxs-lookup"><span data-stu-id="a0a56-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="a0a56-121">In un'immagine in memoria client, un pixel è un gruppo di elementi.</span><span class="sxs-lookup"><span data-stu-id="a0a56-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="a0a56-122">Nelle coordinate della finestra OpenGL ogni pixel corrisponde a un'area dello schermo 1.0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="a0a56-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="a0a56-123">Le coordinate dell'angolo inferiore sinistro dei nomi di pixel x, y sono (x, y) e l'angolo superiore destro è (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="a0a56-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**punto**</span><span class="sxs-lookup"><span data-stu-id="a0a56-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-125">Posizione esatta nello spazio, di cui viene eseguito il rendering come punto di diametro finito.</span><span class="sxs-lookup"><span data-stu-id="a0a56-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**poligono**</span><span class="sxs-lookup"><span data-stu-id="a0a56-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-127">Una superficie quasi piana delimitata da spigoli specificati dai vertici.</span><span class="sxs-lookup"><span data-stu-id="a0a56-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="a0a56-128">Ogni triangolo di una mesh triangolare è un poligono, così come ogni quadrilatero di una mesh quadrangolare.</span><span class="sxs-lookup"><span data-stu-id="a0a56-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="a0a56-129">Anche il rettangolo specificato da glRect è un poligono.</span><span class="sxs-lookup"><span data-stu-id="a0a56-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitivi**</span><span class="sxs-lookup"><span data-stu-id="a0a56-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-131">Una forma, ad esempio un punto, una linea, un poligono, una bitmap o un'immagine, che può essere disegnata, archiviata e modificata come entità discreta; elementi da cui vengono create le progettazioni grafiche di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a0a56-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="a0a56-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**matrice di proiezione**</span><span class="sxs-lookup"><span data-stu-id="a0a56-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="a0a56-133">Matrice 4x4 che trasforma punti, linee, poligoni e posizioni raster dalle coordinate oculari per ritagliare le coordinate.</span><span class="sxs-lookup"><span data-stu-id="a0a56-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




