---
title: I (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera I.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2c78efce-9aed-4bcd-a254-7bff053b0acd
keywords:
- images
- primitive di immagini
- modalità immediata
- indice
- GL IRIS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe340cfbd7dbef3d93cc68ba310d863717225c0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517265"
---
# <a name="i-opengl"></a><span data-ttu-id="67987-108">I (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="67987-108">I (OpenGL)</span></span>

<span data-ttu-id="67987-109">[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) i [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="67987-109">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) I [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="67987-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**immagine**</span><span class="sxs-lookup"><span data-stu-id="67987-110"><span id="opengl_image"></span><span id="OPENGL_IMAGE"></span>**image**</span></span>
</dt> <dd>

<span data-ttu-id="67987-111">Matrice rettangolare di pixel, nella memoria del client o nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="67987-111">A rectangular array of pixels, either in client memory or in the framebuffer.</span></span>

</dd> <dt>

<span data-ttu-id="67987-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**primitiva immagine**</span><span class="sxs-lookup"><span data-stu-id="67987-112"><span id="opengl_image_primitive"></span><span id="OPENGL_IMAGE_PRIMITIVE"></span>**image primitive**</span></span> 
</dt> <dd>

<span data-ttu-id="67987-113">Bitmap o un'immagine.</span><span class="sxs-lookup"><span data-stu-id="67987-113">A bitmap or an image.</span></span>

</dd> <dt>

<span data-ttu-id="67987-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**modalità immediata**</span><span class="sxs-lookup"><span data-stu-id="67987-114"><span id="opengl_immediate_mode"></span><span id="OPENGL_IMMEDIATE_MODE"></span>**immediate mode**</span></span>
</dt> <dd>

<span data-ttu-id="67987-115">Modalità in cui un comando OpenGL viene chiamato direttamente, anziché da un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="67987-115">Mode in which an OpenGL command is called directly, rather than from a display list.</span></span> <span data-ttu-id="67987-116">Nessun bit in modalità immediata esistente. la modalità in modalità immediata si riferisce all'utilizzo di OpenGL, anziché a un bit specifico dello stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="67987-116">No immediate-mode bit exists; the mode in immediate mode refers to usage of OpenGL, rather than to a specific bit of OpenGL state.</span></span>

</dd> <dt>

<span data-ttu-id="67987-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**Indice**</span><span class="sxs-lookup"><span data-stu-id="67987-117"><span id="opengl_index"></span><span id="OPENGL_INDEX"></span>**index**</span></span>
</dt> <dd>

<span data-ttu-id="67987-118">Singolo valore interpretato come valore assoluto, anziché come valore normalizzato in un intervallo specificato (come un componente).</span><span class="sxs-lookup"><span data-stu-id="67987-118">A single value that is interpreted as an absolute value, rather than as a normalized value in a specified range (as is a component).</span></span> <span data-ttu-id="67987-119">Gli indici di colore sono i nomi dei colori, che vengono dereferenziati dall'hardware di visualizzazione usando la mappa colori.</span><span class="sxs-lookup"><span data-stu-id="67987-119">Color indexes are the names of colors, which are dereferenced by the display hardware using the color map.</span></span> <span data-ttu-id="67987-120">Gli indici vengono in genere mascherati, anziché clampati, quando non sono compresi nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="67987-120">Indexes are typically masked, rather than clamped, when out of range.</span></span> <span data-ttu-id="67987-121">Ad esempio, l'indice 0xf7 viene mascherato in 0x7 quando viene scritto in un buffer a 4 bit (colore o stencil).</span><span class="sxs-lookup"><span data-stu-id="67987-121">For example, the index 0xf7 is masked to 0x7 when written to a 4-bit buffer (color or stencil).</span></span> <span data-ttu-id="67987-122">Gli indici colore e gli indici stencil vengono sempre considerati come indici, mai come componenti.</span><span class="sxs-lookup"><span data-stu-id="67987-122">Color indexes and stencil indexes are always treated as indexes, never as components.</span></span>

</dd> <dt>

<span data-ttu-id="67987-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**GL IRIS**</span><span class="sxs-lookup"><span data-stu-id="67987-123"><span id="opengl_iris_gl"></span><span id="OPENGL_IRIS_GL"></span>**IRIS GL**</span></span>
</dt> <dd>

<span data-ttu-id="67987-124">Libreria grafica proprietaria di Silicon Graphics, sviluppata da 1982 a 1992.</span><span class="sxs-lookup"><span data-stu-id="67987-124">Silicon Graphics' proprietary graphics library, developed from 1982 through 1992.</span></span> <span data-ttu-id="67987-125">OpenGL è stato progettato con IRIS GL come punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="67987-125">OpenGL was designed with IRIS GL as a starting point.</span></span>

</dd> </dl>

 

 




