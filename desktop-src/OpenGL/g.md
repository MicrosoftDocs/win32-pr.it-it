---
title: G (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera G.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 588df117-d03c-4a1f-9666-84004cb3d97b
keywords:
- correzione di gamma
- modello geometrico
- oggetti geometrici
- primitive geometriche
- Ombreggiatura Gouraud
- groups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c369c5c2af949bed221d1afd5fb0c05aebf14849
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300824"
---
# <a name="g-opengl"></a><span data-ttu-id="82ba3-109">G (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="82ba3-109">G (OpenGL)</span></span>

<span data-ttu-id="82ba3-110">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) G [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="82ba3-110">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) G [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="82ba3-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**correzione gamma**</span><span class="sxs-lookup"><span data-stu-id="82ba3-111"><span id="opengl_gamma_correction"></span><span id="OPENGL_GAMMA_CORRECTION"></span>**gamma correction**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-112">Funzione applicata ai colori memorizzati nel buffer dei frame per correggere la risposta non lineare dell'occhio (e talvolta del monitoraggio) alle modifiche lineari nei valori di intensità del colore.</span><span class="sxs-lookup"><span data-stu-id="82ba3-112">A function applied to colors stored in the frame buffer to correct for the nonlinear response of the eye (and sometimes of the monitor) to linear changes in color-intensity values.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**modello geometrico**</span><span class="sxs-lookup"><span data-stu-id="82ba3-113"><span id="opengl_geometric_model"></span><span id="OPENGL_GEOMETRIC_MODEL"></span>**geometric model**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-114">I vertici e i parametri della coordinata oggetto che descrivono un oggetto.</span><span class="sxs-lookup"><span data-stu-id="82ba3-114">The object-coordinate vertices and parameters that describe an object.</span></span> <span data-ttu-id="82ba3-115">Si noti che OpenGL non definisce una sintassi per i modelli geometrici, bensì una sintassi e una semantica per il rendering dei modelli geometrici.</span><span class="sxs-lookup"><span data-stu-id="82ba3-115">Note that OpenGL doesn't define a syntax for geometric models, but rather a syntax and semantics for the rendering of geometric models.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**oggetto geometrico**</span><span class="sxs-lookup"><span data-stu-id="82ba3-116"><span id="opengl_geometric_object"></span><span id="OPENGL_GEOMETRIC_OBJECT"></span>**geometric object**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-117">Modello geometrico.</span><span class="sxs-lookup"><span data-stu-id="82ba3-117">A geometric model.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**primitiva geometrica**</span><span class="sxs-lookup"><span data-stu-id="82ba3-118"><span id="opengl_geometric_primitive"></span><span id="OPENGL_GEOMETRIC_PRIMITIVE"></span>**geometric primitive**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-119">Un punto, una linea o un poligono.</span><span class="sxs-lookup"><span data-stu-id="82ba3-119">A point, line, or polygon.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Ombreggiatura Gouraud**</span><span class="sxs-lookup"><span data-stu-id="82ba3-120"><span id="opengl_gouraud_shading"></span><span id="OPENGL_GOURAUD_SHADING"></span>**Gouraud shading**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-121">Interpolazione uniforme dei colori in un poligono o un segmento di linea.</span><span class="sxs-lookup"><span data-stu-id="82ba3-121">Smooth interpolation of colors across a polygon or line segment.</span></span> <span data-ttu-id="82ba3-122">I colori vengono assegnati ai vertici e interpolati linearmente attraverso la primitiva per produrre una variazione relativamente uniforme del colore.</span><span class="sxs-lookup"><span data-stu-id="82ba3-122">Colors are assigned at vertices and linearly interpolated across the primitive to produce a relatively smooth variation in color.</span></span> <span data-ttu-id="82ba3-123">Detto anche ombreggiatura uniforme.</span><span class="sxs-lookup"><span data-stu-id="82ba3-123">Also called smooth shading.</span></span>

</dd> <dt>

<span data-ttu-id="82ba3-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**gruppo**</span><span class="sxs-lookup"><span data-stu-id="82ba3-124"><span id="opengl_group"></span><span id="OPENGL_GROUP"></span>**group**</span></span>
</dt> <dd>

<span data-ttu-id="82ba3-125">Gruppo di uno, due, tre o quattro elementi che rappresenta ogni pixel di un'immagine nella memoria del client.</span><span class="sxs-lookup"><span data-stu-id="82ba3-125">A group of one, two, three, or four elements that represents each pixel of an image in client memory.</span></span> <span data-ttu-id="82ba3-126">Pertanto, nel contesto di un'immagine della memoria del client, un gruppo e un pixel sono la stessa cosa.</span><span class="sxs-lookup"><span data-stu-id="82ba3-126">Thus, in the context of a client memory image, a group and a pixel are the same thing.</span></span>

</dd> </dl>

 

 




