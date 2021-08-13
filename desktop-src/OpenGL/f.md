---
title: F (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- ombreggiatura piatta
- Nebbia
- font
- fragments
- buffer di frame
- front face
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 748eb0fade84ef76c133453165db53d8540326dae3111ac04f3b7a6819ae825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618186"
---
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U](t.md) [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**Faccia**
</dt> <dd>

Un lato di un poligono. Ogni poligono ha due visi: una faccia anteriore e una faccia posteriore. Nella finestra è sempre visibile un solo viso. La visibilità della faccia posteriore o anteriore viene determinata in modo efficace dopo che il poligono è stato proiettato nella finestra. Dopo questa proiezione, se i bordi del poligono sono diretti in senso orario, una delle facce è visibile; se indirizzato in senso antiorario, l'altro viso è visibile. Il programmatore OpenGL determina se corrisponde alla parte anteriore o posteriore (e in senso antiorario alla parte posteriore o anteriore).

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**ombreggiatura piatta**
</dt> <dd>

Si riferisce alla colorazione di una primitiva con un singolo colore costante nell'intera estensione, anziché interpolazione uniforme dei colori attraverso la primitiva. Vedere [Ombreggiatura gouraud.](g.md)

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**Nebbia**
</dt> <dd>

Tecnica di rendering che può essere usata per simulare gli effetti dell'emigrazione, ad esempio la conze, la lentezza e lo smog, impostando i colori degli oggetti su un colore di sfondo in base alla distanza dal visualizzatore. L'utente aiuta anche nella percezione della distanza dal visualizzatore, fornendo un segnale di profondità. Vedere anche [depth-cueing](d.md).

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**Carattere**
</dt> <dd>

Gruppo di rappresentazioni di caratteri grafici in genere utilizzate per visualizzare stringhe di testo. I caratteri possono essere lettere romane, simboli matematici, ideogrammi dell'Asia, hieroglyphs Disagi e così via.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**Frammento**
</dt> <dd>

Dati grafici generati dalla rasterizzazione delle primitive. Ogni frammento corrisponde a un singolo pixel e include valori di colore, profondità e talvolta coordinate della trama.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**Framebuffer**
</dt> <dd>

Stack di bitplan. Tutti i buffer di una determinata finestra o contesto. In alcuni casi include tutta la memoria in pixel dell'acceleratore hardware grafico. Vedere anche [bitplane.](b.md)

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**
</dt> <dd>

Vedere viso.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**
</dt> <dd>

Volume di visualizzazione di cui è stata scambiati i dati in base alla divisione prospettica.

</dd> </dl>

 

 




