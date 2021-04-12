---
title: T (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera T.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: effb170b-fea3-4954-9f9c-3bc1aa829bc0
keywords:
- tassellatura
- Texel
- trama
- mapping trama
- matrice trama
- trasformazioni
- triangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1cb324179137dbf9f9046c0c19acfffdf7394e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118762"
---
# <a name="t-opengl"></a><span data-ttu-id="694c8-110">T (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="694c8-110">T (OpenGL)</span></span>

<span data-ttu-id="694c8-111">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="694c8-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="694c8-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**tassellatura**</span><span class="sxs-lookup"><span data-stu-id="694c8-112"><span id="opengl_tessellation"></span><span id="OPENGL_TESSELLATION"></span>**tessellation**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-113">Riduzione di una parte di una superficie analitica a una mesh di poligoni o di una parte di una curva analitica a una sequenza di righe.</span><span class="sxs-lookup"><span data-stu-id="694c8-113">Reduction of a portion of an analytic surface to a mesh of polygons, or of a portion of an analytic curve to a sequence of lines.</span></span>

</dd> <dt>

<span data-ttu-id="694c8-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**Texel**</span><span class="sxs-lookup"><span data-stu-id="694c8-114"><span id="opengl_texel"></span><span id="OPENGL_TEXEL"></span>**texel**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-115">Elemento texture.</span><span class="sxs-lookup"><span data-stu-id="694c8-115">A texture element.</span></span> <span data-ttu-id="694c8-116">Un Texel viene ottenuto dalla memoria della trama e rappresenta il colore della trama da applicare a un frammento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="694c8-116">A texel is obtained from texture memory and represents the color of the texture to be applied to a corresponding fragment.</span></span> <span data-ttu-id="694c8-117">Vedere anche [Fragment](f.md).</span><span class="sxs-lookup"><span data-stu-id="694c8-117">See also [fragment](f.md).</span></span>

</dd> <dt>

<span data-ttu-id="694c8-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**trama**</span><span class="sxs-lookup"><span data-stu-id="694c8-118"><span id="opengl_texture"></span><span id="OPENGL_TEXTURE"></span>**texture**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-119">Immagine a una o bidimensionale utilizzata per modificare il colore dei frammenti prodotti dalla rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="694c8-119">A one- or two-dimensional image used to modify the color of fragments produced by rasterization.</span></span> <span data-ttu-id="694c8-120">Vedere anche [rasterizzare](r.md).</span><span class="sxs-lookup"><span data-stu-id="694c8-120">See also [rasterize](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="694c8-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**mapping trama**</span><span class="sxs-lookup"><span data-stu-id="694c8-121"><span id="opengl_texture_mapping"></span><span id="OPENGL_TEXTURE_MAPPING"></span>**texture mapping**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-122">Processo di applicazione di un'immagine (trama) a una primitiva.</span><span class="sxs-lookup"><span data-stu-id="694c8-122">The process of applying an image (the texture) to a primitive.</span></span> <span data-ttu-id="694c8-123">Il mapping di trama viene spesso usato per aggiungere realismo a una scena.</span><span class="sxs-lookup"><span data-stu-id="694c8-123">Texture mapping is often used to add realism to a scene.</span></span> <span data-ttu-id="694c8-124">Ad esempio, è possibile applicare un'immagine di una facciata di compilazione a un poligono che rappresenta una parete.</span><span class="sxs-lookup"><span data-stu-id="694c8-124">For example, you could apply a picture of a building facade to a polygon representing a wall.</span></span> <span data-ttu-id="694c8-125">Vedere anche texture.</span><span class="sxs-lookup"><span data-stu-id="694c8-125">See also texture.</span></span>

</dd> <dt>

<span data-ttu-id="694c8-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**matrice trama**</span><span class="sxs-lookup"><span data-stu-id="694c8-126"><span id="opengl_texture_matrix"></span><span id="OPENGL_TEXTURE_MATRIX"></span>**texture matrix**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-127">Matrice 4x4 che trasforma le coordinate di trama dalle coordinate specificate in alle coordinate utilizzate per l'interpolazione e la ricerca della trama.</span><span class="sxs-lookup"><span data-stu-id="694c8-127">The 4x4 matrix that transforms texture coordinates from the coordinates that they're specified in to the coordinates that are used for interpolation and texture lookup.</span></span>

</dd> <dt>

<span data-ttu-id="694c8-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**trasformazione**</span><span class="sxs-lookup"><span data-stu-id="694c8-128"><span id="opengl_transformation"></span><span id="OPENGL_TRANSFORMATION"></span>**transformation**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-129">Distorsione dello spazio.</span><span class="sxs-lookup"><span data-stu-id="694c8-129">A warping of space.</span></span> <span data-ttu-id="694c8-130">In OpenGL le trasformazioni sono limitate alle trasformazioni proiettivi che includono qualsiasi elemento che può essere rappresentato da una matrice 4x4.</span><span class="sxs-lookup"><span data-stu-id="694c8-130">In OpenGL, transformations are limited to projective transformations that include anything that can be represented by a 4x4 matrix.</span></span> <span data-ttu-id="694c8-131">Tali trasformazioni includono le rotazioni, le conversioni, le proporzioni non uniformi lungo gli assi delle coordinate, le trasformazioni della prospettiva e le combinazioni di questi.</span><span class="sxs-lookup"><span data-stu-id="694c8-131">Such transformations include rotations, translations, (nonuniform) scalings along the coordinate axes, perspective transformations, and combinations of these.</span></span>

</dd> <dt>

<span data-ttu-id="694c8-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**triangolo**</span><span class="sxs-lookup"><span data-stu-id="694c8-132"><span id="opengl_triangle"></span><span id="OPENGL_TRIANGLE"></span>**triangle**</span></span>
</dt> <dd>

<span data-ttu-id="694c8-133">Poligono con tre bordi.</span><span class="sxs-lookup"><span data-stu-id="694c8-133">A polygon with three edges.</span></span> <span data-ttu-id="694c8-134">I triangoli sono sempre convessi.</span><span class="sxs-lookup"><span data-stu-id="694c8-134">Triangles are always convex.</span></span>

</dd> </dl>

 

 




