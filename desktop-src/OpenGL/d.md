---
title: D (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f97470e7-a500-47d7-84f0-b3045d04b8fc
keywords:
- depth
- Cue di profondità
- elenchi di visualizzazione
- dithering
- doppio buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cb068f06135c6ba29e8a61f472d98907090a78
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739498"
---
# <a name="d-opengl"></a><span data-ttu-id="a39a3-108">D (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="a39a3-108">D (OpenGL)</span></span>

<span data-ttu-id="a39a3-109">[A](a.md) [B](b.md) [C](c.md) d [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="a39a3-109">[A](a.md) [B](b.md) [C](c.md) D [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="a39a3-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**profondità**</span><span class="sxs-lookup"><span data-stu-id="a39a3-110"><span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**depth**</span></span>
</dt> <dd>

<span data-ttu-id="a39a3-111">In genere si riferisce alla coordinata z della finestra.</span><span class="sxs-lookup"><span data-stu-id="a39a3-111">Generally refers to the z window coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="a39a3-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**Cue di profondità**</span><span class="sxs-lookup"><span data-stu-id="a39a3-112"><span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**depth cueing**</span></span>
</dt> <dd>

<span data-ttu-id="a39a3-113">Una tecnica di rendering che assegna il colore in base alla distanza dal punto di vista.</span><span class="sxs-lookup"><span data-stu-id="a39a3-113">A rendering technique that assigns color based on distance from the viewpoint.</span></span>

</dd> <dt>

<span data-ttu-id="a39a3-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**elenco di visualizzazione**</span><span class="sxs-lookup"><span data-stu-id="a39a3-114"><span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**display list**</span></span>
</dt> <dd>

<span data-ttu-id="a39a3-115">Elenco denominato di comandi OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a39a3-115">A named list of OpenGL commands.</span></span> <span data-ttu-id="a39a3-116">Gli elenchi di visualizzazione vengono sempre archiviati nel server, pertanto è possibile utilizzare gli elenchi di visualizzazione per ridurre il traffico di rete in ambienti client/server.</span><span class="sxs-lookup"><span data-stu-id="a39a3-116">Display lists are always stored on the server, so display lists can be used to reduce the network traffic in client/server environments.</span></span> <span data-ttu-id="a39a3-117">Il contenuto di un elenco di visualizzazione può essere pre-elaborato e potrebbe quindi essere eseguito in modo più efficiente rispetto allo stesso set di comandi OpenGL eseguiti in modalità immediata.</span><span class="sxs-lookup"><span data-stu-id="a39a3-117">The contents of a display list may be preprocessed, and might therefore execute more efficiently than the same set of OpenGL commands executed in immediate mode.</span></span> <span data-ttu-id="a39a3-118">Questa pre-elaborazione è particolarmente importante per il calcolo di comandi con utilizzo intensivo, ad esempio [**glTexImage**](glteximage1d.md).</span><span class="sxs-lookup"><span data-stu-id="a39a3-118">Such preprocessing is especially important for computing intensive commands such as [**glTexImage**](glteximage1d.md).</span></span>

</dd> <dt>

<span data-ttu-id="a39a3-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span><span class="sxs-lookup"><span data-stu-id="a39a3-119"><span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**</span></span>
</dt> <dd>

<span data-ttu-id="a39a3-120">Una tecnica per aumentare l'intervallo di colori percepito in un'immagine al costo della risoluzione spaziale.</span><span class="sxs-lookup"><span data-stu-id="a39a3-120">A technique for increasing the perceived range of colors in an image at the cost of spatial resolution.</span></span> <span data-ttu-id="a39a3-121">Ai pixel adiacenti vengono assegnati valori di colore diversi.</span><span class="sxs-lookup"><span data-stu-id="a39a3-121">Adjacent pixels are assigned differing color values.</span></span> <span data-ttu-id="a39a3-122">Quando vengono visualizzati da una distanza, questi colori sembrano fondersi in un singolo colore intermedio.</span><span class="sxs-lookup"><span data-stu-id="a39a3-122">When viewed from a distance, these colors seem to blend into a single intermediate color.</span></span> <span data-ttu-id="a39a3-123">La tecnica è simile a quella usata per le pubblicazioni in bianco e nero per ottenere sfumature di grigio.</span><span class="sxs-lookup"><span data-stu-id="a39a3-123">The technique is similar to the half-toning used in black-and-white publications to achieve shades of gray.</span></span>

</dd> <dt>

<span data-ttu-id="a39a3-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**doppio buffer**</span><span class="sxs-lookup"><span data-stu-id="a39a3-124"><span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**double buffering**</span></span>
</dt> <dd>

<span data-ttu-id="a39a3-125">Uso di contesti OpenGL in cui i buffer dei colori di primo e indietro sono con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="a39a3-125">Using OpenGL contexts in which both front and back color buffers are double-buffered.</span></span> <span data-ttu-id="a39a3-126">L'animazione uniforme viene eseguita eseguendo il rendering solo nel buffer nascosto (che non viene visualizzato), causando lo scambio dei buffer di primo e indietro.</span><span class="sxs-lookup"><span data-stu-id="a39a3-126">Smooth animation is accomplished by rendering into only the back buffer (which isn't displayed), then causing the front and back buffers to be swapped.</span></span>

</dd> </dl>

 

 




