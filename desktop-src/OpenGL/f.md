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
# <a name="f-opengl"></a>F (OpenGL)

[A](a.md) [B](b.md) [C](c.md) [d](d.md) [E](e.md) F [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_face"></span><span id="OPENGL_FACE"></span>**faccia**
</dt> <dd>

Un lato di un poligono. Ogni poligono è costituito da due visi: una faccia anteriore e una faccia posteriore. Nella finestra è sempre visibile solo una faccia. Se il retro o il quadrante anteriore è visibile è effettivamente determinato dopo che il poligono è stato proiettato nella finestra. Dopo questa proiezione, se i bordi del poligono sono diretti in senso orario, una delle facce è visibile; Se viene indirizzato in senso antiorario, l'altra faccia è visibile. Il programmatore OpenGL è determinato dal programmatore OpenGL, che indica se il valore in senso orario corrisponde a front o back (e in senso antiorario corrisponde a back o front

</dd> <dt>

<span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**ombreggiatura flat**
</dt> <dd>

Si riferisce alla colorazione di una primitiva con un singolo colore costante nell'extent, anziché l'interpolazione uniforme dei colori attraverso la primitiva. Vedere [ombreggiatura Gouraud](g.md).

</dd> <dt>

<span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**nebbia**
</dt> <dd>

Una tecnica di rendering che può essere usata per simulare gli effetti atmosferici come Haze, fog e smog dissolvendo i colori degli oggetti in un colore di sfondo in base alla distanza del visualizzatore. La nebbia contribuisce anche alla percezione della distanza dal visualizzatore, fornendo un segnale di profondità. Vedere anche la pagina relativa alla [profondità](d.md).

</dd> <dt>

<span id="opengl_font"></span><span id="OPENGL_FONT"></span>**carattere**
</dt> <dd>

Gruppo di rappresentazioni di caratteri grafici utilizzati generalmente per visualizzare le stringhe di testo. I caratteri possono essere lettere romane, simboli matematici, degli ideogrammi asiatici, geroglifici egiziani e così via.

</dd> <dt>

<span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**frammento**
</dt> <dd>

Dati grafici generati dalla rasterizzazione delle primitive. Ogni frammento corrisponde a un singolo pixel e include i valori di colore, profondità e talvolta di coordinate di trama.

</dd> <dt>

<span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**buffer frame**
</dt> <dd>

Stack di bitplane. Tutti i buffer di una finestra o di un contesto specifico. In alcuni casi include tutta la memoria pixel dell'acceleratore hardware grafica. Vedere anche [bitplane](b.md).

</dd> <dt>

<span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**faccia anteriore**
</dt> <dd>

Vedere Face.

</dd> <dt>

<span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**tronco**
</dt> <dd>

Volume di visualizzazione distorto da prospettiva divisione.

</dd> </dl>

 

 




