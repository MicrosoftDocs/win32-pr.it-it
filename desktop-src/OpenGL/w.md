---
title: W (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera W.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7f8235a3-ea48-40eb-8957-e7a55a5778af
keywords:
- windows
- allineato alla finestra
- Coordinate finestra
- wireframe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f6f1897af46c85ed48171d251ebe1b2de8c5e1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739274"
---
# <a name="w-opengl"></a><span data-ttu-id="ef672-107">W (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="ef672-107">W (OpenGL)</span></span>

<span data-ttu-id="ef672-108">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="ef672-108">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) W [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="ef672-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**finestra**</span><span class="sxs-lookup"><span data-stu-id="ef672-109"><span id="opengl_window"></span><span id="OPENGL_WINDOW"></span>**window**</span></span>
</dt> <dd>

<span data-ttu-id="ef672-110">Area secondaria del framebuffer, in genere rettangolare, i cui pixel hanno tutti la stessa configurazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="ef672-110">A subregion of the framebuffer, usually rectangular, whose pixels all have the same buffer configuration.</span></span> <span data-ttu-id="ef672-111">Un contesto OpenGL viene sottoposta a rendering in una finestra alla volta.</span><span class="sxs-lookup"><span data-stu-id="ef672-111">An OpenGL context renders to one window at a time.</span></span>

</dd> <dt>

<span data-ttu-id="ef672-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**allineato alla finestra**</span><span class="sxs-lookup"><span data-stu-id="ef672-112"><span id="opengl_window_aligned"></span><span id="OPENGL_WINDOW_ALIGNED"></span>**window-aligned**</span></span>
</dt> <dd>

<span data-ttu-id="ef672-113">Quando si fa riferimento ai segmenti di linea o ai bordi del poligono, significa che questi sono paralleli ai limiti della finestra.</span><span class="sxs-lookup"><span data-stu-id="ef672-113">When referring to line segments or polygon edges, implies that these are parallel to the window boundaries.</span></span> <span data-ttu-id="ef672-114">(In OpenGL la finestra è rettangolare, con bordi orizzontali e verticali).</span><span class="sxs-lookup"><span data-stu-id="ef672-114">(In OpenGL, the window is rectangular, with horizontal and vertical edges).</span></span> <span data-ttu-id="ef672-115">Quando si fa riferimento a un modello poligono, significa che il criterio è fisso rispetto all'origine della finestra.</span><span class="sxs-lookup"><span data-stu-id="ef672-115">When referring to a polygon pattern, implies that the pattern is fixed relative to the window origin.</span></span>

</dd> <dt>

<span data-ttu-id="ef672-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**Coordinate finestra**</span><span class="sxs-lookup"><span data-stu-id="ef672-116"><span id="opengl_window_coordinates"></span><span id="OPENGL_WINDOW_COORDINATES"></span>**window coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="ef672-117">Sistema di coordinate di una finestra.</span><span class="sxs-lookup"><span data-stu-id="ef672-117">The coordinate system of a window.</span></span> <span data-ttu-id="ef672-118">È importante distinguere tra i nomi dei pixel, che sono discreti, e il sistema di coordinate della finestra, che è continuo.</span><span class="sxs-lookup"><span data-stu-id="ef672-118">It's important to distinguish between the names of pixels, which are discrete, and the window-coordinate system, which is continuous.</span></span> <span data-ttu-id="ef672-119">Ad esempio, il pixel nell'angolo inferiore sinistro di una finestra è pixel (0,0); le coordinate della finestra del centro del pixel sono (0,5, 0,5, z).</span><span class="sxs-lookup"><span data-stu-id="ef672-119">For example, the pixel at the lower-left corner of a window is pixel (0, 0); the window coordinates of the center of this pixel are (0.5, 0.5, z).</span></span> <span data-ttu-id="ef672-120">Si noti che le coordinate della finestra includono un componente Depth, o z, e che anche questo componente è continuo.</span><span class="sxs-lookup"><span data-stu-id="ef672-120">Note that window coordinates include a depth, or z, component, and that this component is continuous as well.</span></span>

</dd> <dt>

<span data-ttu-id="ef672-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span><span class="sxs-lookup"><span data-stu-id="ef672-121"><span id="opengl_wireframe"></span><span id="OPENGL_WIREFRAME"></span>**wireframe**</span></span>
</dt> <dd>

<span data-ttu-id="ef672-122">Rappresentazione di un oggetto che contiene solo segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="ef672-122">A representation of an object that contains line segments only.</span></span> <span data-ttu-id="ef672-123">In genere, i segmenti di linea indicano i bordi del poligono.</span><span class="sxs-lookup"><span data-stu-id="ef672-123">Typically, the line segments indicate polygon edges.</span></span>

</dd> </dl>

 

 




