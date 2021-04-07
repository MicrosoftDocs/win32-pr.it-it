---
title: R (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ab0286f5-cad2-4537-aa98-be0fce55ff53
keywords:
- rasterizzazione
- rettangoli
- rendering
- RGBA
- Modalità RGBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b82a2db1bade12a0ff844006a1572cdc3b977dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873198"
---
# <a name="r-opengl"></a><span data-ttu-id="39285-108">R (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="39285-108">R (OpenGL)</span></span>

<span data-ttu-id="39285-109">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="39285-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) R [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="39285-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**Rasterizza**</span><span class="sxs-lookup"><span data-stu-id="39285-110"><span id="opengl_rasterize"></span><span id="OPENGL_RASTERIZE"></span>**rasterize**</span></span>
</dt> <dd>

<span data-ttu-id="39285-111">Per convertire un punto, una linea o un poligono proiettato, oppure i pixel di una bitmap o di un'immagine, in frammenti, ognuno corrispondente a un pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="39285-111">To convert a projected point, line, or polygon, or the pixels of a bitmap or image, to fragments, each corresponding to a pixel in the framebuffer.</span></span> <span data-ttu-id="39285-112">Si noti che tutte le primitive vengono rasterizzate, non solo punti, linee e poligoni</span><span class="sxs-lookup"><span data-stu-id="39285-112">Note that all primitives are rasterized, not just points, lines, and polygons</span></span>

</dd> <dt>

<span data-ttu-id="39285-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rettangolo**</span><span class="sxs-lookup"><span data-stu-id="39285-113"><span id="opengl_rectangle"></span><span id="OPENGL_RECTANGLE"></span>**rectangle**</span></span>
</dt> <dd>

<span data-ttu-id="39285-114">Un quadrilatero i cui spigoli alternativi sono paralleli tra loro nelle coordinate dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="39285-114">A quadrilateral whose alternate edges are parallel to each other in object coordinates.</span></span> <span data-ttu-id="39285-115">I poligoni specificati con glRect \* () sono sempre rettangoli. gli altri quadrilateri possono essere rettangoli.</span><span class="sxs-lookup"><span data-stu-id="39285-115">Polygons specified with glRect\*( ) are always rectangles; other quadrilaterals might be rectangles.</span></span>

</dd> <dt>

<span data-ttu-id="39285-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span><span class="sxs-lookup"><span data-stu-id="39285-116"><span id="opengl_rendering"></span><span id="OPENGL_RENDERING"></span>**rendering**</span></span>
</dt> <dd>

<span data-ttu-id="39285-117">Conversione di primitive specificate nelle coordinate dell'oggetto in un'immagine nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="39285-117">Conversion of primitives specified in object coordinates to an image in the framebuffer.</span></span> <span data-ttu-id="39285-118">Il rendering è il funzionamento principale di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="39285-118">Rendering is the primary operation of OpenGL.</span></span>

</dd> <dt>

<span data-ttu-id="39285-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span><span class="sxs-lookup"><span data-stu-id="39285-119"><span id="opengl_rgba"></span><span id="OPENGL_RGBA"></span>**RGBA**</span></span>
</dt> <dd>

<span data-ttu-id="39285-120">I componenti di colore rosso, verde, blu e alfa della modalità RGBA.</span><span class="sxs-lookup"><span data-stu-id="39285-120">The red, green, blue, and alpha color components of the RGBA mode.</span></span>

</dd> <dt>

<span data-ttu-id="39285-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**Modalità RGBA**</span><span class="sxs-lookup"><span data-stu-id="39285-121"><span id="opengl_rgba_mode"></span><span id="OPENGL_RGBA_MODE"></span>**RGBA mode**</span></span>
</dt> <dd>

<span data-ttu-id="39285-122">Contesto OpenGL in cui i buffer dei colori archiviano i componenti di colore rosso, verde, blu e alfa, anziché gli indici dei colori.</span><span class="sxs-lookup"><span data-stu-id="39285-122">An OpenGL context in which its color buffers store red, green, blue, and alpha color components, rather than color indexes.</span></span>

</dd> </dl>

 

 




