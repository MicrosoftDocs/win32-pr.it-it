---
title: A (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: e583610f-37da-47bb-bbd6-41d353b88244
keywords:
- Aliasing
- alpha
- animazione
- anti-aliasing
- ritaglio specifico dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb69307f869031bb9fd176ec85dd20eac5d543ef3e7f63086c6ea0801d1b8b8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128371"
---
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U](t.md) [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**Aliasing**
</dt> <dd>

Tecnica di rendering che assegna ai pixel il colore della primitiva di cui viene eseguito il rendering, indipendentemente dal fatto che la primitiva ricopre l'intera area del pixel o in parte. L'aliasing comporta bordi frastagliati o jaggies. Vedere anche [jaggies.](jk.md)

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**
</dt> <dd>

Quarto componente di colore usato in genere per controllare la fusione dei colori. Il componente alfa non viene mai visualizzato direttamente. Per convenzione, OpenGL alpha indica opacità e trasparenza su una scala da 0,0 a 1,0. Un valore alfa pari a 1,0 implica opacità completa, un valore alfa pari a 0,0 implica trasparenza completa.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**Animazione**
</dt> <dd>

La generazione di rendering ripetuti di una scena abbastanza rapidamente, con un punto di vista o posizioni degli oggetti in continua evoluzione, che consente di ottenere l'effetto di movimento. L'animazione OpenGL usa quasi sempre il doppio buffer.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**Antialias**
</dt> <dd>

Tecnica di rendering che assegna colori ai pixel in base alla frazione dell'area pixel coperta dalla primitiva di cui viene eseguito il rendering. Il rendering con antialias riduce o elimina i jaggie risultanti dal rendering con alias. Vedere anche [jaggies,](jk.md) [rendering di](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**ritaglio specifico dell'applicazione** 
</dt> <dd>

Ritaglio di primitive su piani in coordinate oculare. I piani vengono specificati dall'applicazione usando [**glClipPlane.**](glclipplane.md) Vedere anche [coordinate oculare.](e.md)

</dd> </dl>

 

 




