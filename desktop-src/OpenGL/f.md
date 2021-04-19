---
title: F (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- ombreggiatura flat
- nebbia
- font
- fragments
- framebuffer
- faccia anteriore
- tronco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300826"
---
# <a name="f-opengl"></a><span data-ttu-id="02e25-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="02e25-111">F (OpenGL)</span></span>

<span data-ttu-id="02e25-112">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) F [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="02e25-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="02e25-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**faccia**</span><span class="sxs-lookup"><span data-stu-id="02e25-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-114">Un lato di un poligono.</span><span class="sxs-lookup"><span data-stu-id="02e25-114">One side of a polygon.</span></span> <span data-ttu-id="02e25-115">Ogni poligono è costituito da due visi: una faccia anteriore e una faccia posteriore.</span><span class="sxs-lookup"><span data-stu-id="02e25-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="02e25-116">Nella finestra è sempre visibile solo una faccia.</span><span class="sxs-lookup"><span data-stu-id="02e25-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="02e25-117">Se il retro o il quadrante anteriore è visibile è effettivamente determinato dopo che il poligono è stato proiettato nella finestra.</span><span class="sxs-lookup"><span data-stu-id="02e25-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="02e25-118">Dopo questa proiezione, se i bordi del poligono sono diretti in senso orario, una delle facce è visibile; Se viene indirizzato in senso antiorario, l'altra faccia è visibile.</span><span class="sxs-lookup"><span data-stu-id="02e25-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="02e25-119">Il programmatore OpenGL è determinato dal programmatore OpenGL, che indica se il valore in senso orario corrisponde a front o back (e in senso antiorario corrisponde a back o front</span><span class="sxs-lookup"><span data-stu-id="02e25-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="02e25-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**ombreggiatura flat**</span><span class="sxs-lookup"><span data-stu-id="02e25-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-121">Si riferisce alla colorazione di una primitiva con un singolo colore costante nell'extent, anziché l'interpolazione uniforme dei colori attraverso la primitiva.</span><span class="sxs-lookup"><span data-stu-id="02e25-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="02e25-122">Vedere [ombreggiatura Gouraud](g.md).</span><span class="sxs-lookup"><span data-stu-id="02e25-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="02e25-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**nebbia**</span><span class="sxs-lookup"><span data-stu-id="02e25-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-124">Una tecnica di rendering che può essere usata per simulare gli effetti atmosferici come Haze, fog e smog dissolvendo i colori degli oggetti in un colore di sfondo in base alla distanza del visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="02e25-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="02e25-125">La nebbia contribuisce anche alla percezione della distanza dal visualizzatore, fornendo un segnale di profondità.</span><span class="sxs-lookup"><span data-stu-id="02e25-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="02e25-126">Vedere anche la pagina relativa alla [profondità](d.md).</span><span class="sxs-lookup"><span data-stu-id="02e25-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="02e25-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**carattere**</span><span class="sxs-lookup"><span data-stu-id="02e25-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-128">Gruppo di rappresentazioni di caratteri grafici utilizzati generalmente per visualizzare le stringhe di testo.</span><span class="sxs-lookup"><span data-stu-id="02e25-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="02e25-129">I caratteri possono essere lettere romane, simboli matematici, degli ideogrammi asiatici, geroglifici egiziani e così via.</span><span class="sxs-lookup"><span data-stu-id="02e25-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="02e25-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**frammento**</span><span class="sxs-lookup"><span data-stu-id="02e25-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-131">Dati grafici generati dalla rasterizzazione delle primitive.</span><span class="sxs-lookup"><span data-stu-id="02e25-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="02e25-132">Ogni frammento corrisponde a un singolo pixel e include i valori di colore, profondità e talvolta di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="02e25-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="02e25-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**buffer frame**</span><span class="sxs-lookup"><span data-stu-id="02e25-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-134">Stack di bitplane.</span><span class="sxs-lookup"><span data-stu-id="02e25-134">A stack of bitplanes.</span></span> <span data-ttu-id="02e25-135">Tutti i buffer di una finestra o di un contesto specifico.</span><span class="sxs-lookup"><span data-stu-id="02e25-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="02e25-136">In alcuni casi include tutta la memoria pixel dell'acceleratore hardware grafica.</span><span class="sxs-lookup"><span data-stu-id="02e25-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="02e25-137">Vedere anche [bitplane](b.md).</span><span class="sxs-lookup"><span data-stu-id="02e25-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="02e25-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**faccia anteriore**</span><span class="sxs-lookup"><span data-stu-id="02e25-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-139">Vedere Face.</span><span class="sxs-lookup"><span data-stu-id="02e25-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="02e25-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**tronco**</span><span class="sxs-lookup"><span data-stu-id="02e25-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="02e25-141">Volume di visualizzazione distorto da prospettiva divisione.</span><span class="sxs-lookup"><span data-stu-id="02e25-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




