---
title: A (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- aliasing
- alpha
- animazione
- anti-aliasing
- ritaglio specifico dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d161832eb6d81738038e10564233f26920f0d60
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400146"
---
# <a name="a-opengl"></a><span data-ttu-id="0de4f-108">A (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="0de4f-108">A (OpenGL)</span></span>

<span data-ttu-id="0de4f-109">A [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="0de4f-109">A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="0de4f-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span><span class="sxs-lookup"><span data-stu-id="0de4f-110"><span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**</span></span>
</dt> <dd>

<span data-ttu-id="0de4f-111">Una tecnica di rendering che assegna ai pixel il colore della primitiva di cui viene eseguito il rendering, indipendentemente dal fatto che la primitiva copra tutta o parte dell'area del pixel.</span><span class="sxs-lookup"><span data-stu-id="0de4f-111">A rendering technique that assigns to pixels the color of the primitive being rendered, whether that primitive covers all or part of the pixel's area.</span></span> <span data-ttu-id="0de4f-112">L'aliasing genera bordi irregolari o irregolari.</span><span class="sxs-lookup"><span data-stu-id="0de4f-112">Aliasing results in jagged edges, or jaggies.</span></span> <span data-ttu-id="0de4f-113">Vedere anche le [matrici](jk.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-113">See also [jaggies](jk.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de4f-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**</span><span class="sxs-lookup"><span data-stu-id="0de4f-114"><span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**alpha**</span></span>
</dt> <dd>

<span data-ttu-id="0de4f-115">Componente di quarto colore usato in genere per controllare la fusione di colori.</span><span class="sxs-lookup"><span data-stu-id="0de4f-115">A fourth color component typically used to control color blending.</span></span> <span data-ttu-id="0de4f-116">Il componente alfa non viene mai visualizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="0de4f-116">The alpha component is never displayed directly.</span></span> <span data-ttu-id="0de4f-117">Per convenzione, OpenGL Alpha indica l'opacità e la trasparenza su una scala da 0,0 a 1,0.</span><span class="sxs-lookup"><span data-stu-id="0de4f-117">By convention, OpenGL alpha indicates opacity and transparency on a scale of 0.0 to 1.0.</span></span> <span data-ttu-id="0de4f-118">Un valore alfa di 1,0 implica l'opacità completa, un valore alfa pari a 0,0 implica la trasparenza completa.</span><span class="sxs-lookup"><span data-stu-id="0de4f-118">An alpha value of 1.0 implies complete opacity, an alpha value of 0.0 implies complete transparency.</span></span>

</dd> <dt>

<span data-ttu-id="0de4f-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animazione**</span><span class="sxs-lookup"><span data-stu-id="0de4f-119"><span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animation**</span></span>
</dt> <dd>

<span data-ttu-id="0de4f-120">La generazione di rendering ripetuti di una scena in modo sufficientemente rapido, con posizioni del punto di vista o oggetto a modifica graduale, che l'illusione del movimento viene realizzata.</span><span class="sxs-lookup"><span data-stu-id="0de4f-120">The generation of repeated renderings of a scene quickly enough, with smoothly changing viewpoint or object positions, that the illusion of motion is achieved.</span></span> <span data-ttu-id="0de4f-121">L'animazione OpenGL usa quasi sempre il doppio buffering.</span><span class="sxs-lookup"><span data-stu-id="0de4f-121">OpenGL animation almost always uses double-buffering.</span></span>

</dd> <dt>

<span data-ttu-id="0de4f-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**anti-aliasing**</span><span class="sxs-lookup"><span data-stu-id="0de4f-122"><span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**antialiasing**</span></span>
</dt> <dd>

<span data-ttu-id="0de4f-123">Tecnica di rendering che assegna colori ai pixel in base alla frazione dell'area dei pixel coperta dalla primitiva di cui viene eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="0de4f-123">A rendering technique that assigns colors to pixels based on the fraction of the pixel area that is covered by the primitive being rendered.</span></span> <span data-ttu-id="0de4f-124">Il rendering con antialias riduce o Elimina le irregolarità derivanti dal rendering con alias.</span><span class="sxs-lookup"><span data-stu-id="0de4f-124">Antialiased rendering reduces or eliminates the jaggies that result from aliased rendering.</span></span> <span data-ttu-id="0de4f-125">Vedere anche [Jaggi](jk.md), [rendering](r.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-125">See also [jaggies](jk.md), [rendering](r.md).</span></span>

</dd> <dt>

<span data-ttu-id="0de4f-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**ritaglio specifico dell'applicazione**</span><span class="sxs-lookup"><span data-stu-id="0de4f-126"><span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**application-specific clipping**</span></span> 
</dt> <dd>

<span data-ttu-id="0de4f-127">Ritaglio delle primitive rispetto ai piani in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="0de4f-127">Clipping of primitives against planes in eye coordinates.</span></span> <span data-ttu-id="0de4f-128">I piani vengono specificati dall'applicazione usando [**glClipPlane**](glclipplane.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-128">The planes are specified by the application using [**glClipPlane**](glclipplane.md).</span></span> <span data-ttu-id="0de4f-129">Vedere anche [Coordinate oculari](e.md).</span><span class="sxs-lookup"><span data-stu-id="0de4f-129">See also [eye coordinates](e.md).</span></span>

</dd> </dl>

 

 




