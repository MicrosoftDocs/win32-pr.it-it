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
# <a name="a-opengl"></a>A (OpenGL)

A [B](b.md) [C](c.md) [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_aliasing"></span><span id="OPENGL_ALIASING"></span>**aliasing**
</dt> <dd>

Una tecnica di rendering che assegna ai pixel il colore della primitiva di cui viene eseguito il rendering, indipendentemente dal fatto che la primitiva copra tutta o parte dell'area del pixel. L'aliasing genera bordi irregolari o irregolari. Vedere anche le [matrici](jk.md).

</dd> <dt>

<span id="opengl_alpha"></span><span id="OPENGL_ALPHA"></span>**Alfa**
</dt> <dd>

Componente di quarto colore usato in genere per controllare la fusione di colori. Il componente alfa non viene mai visualizzato direttamente. Per convenzione, OpenGL Alpha indica l'opacità e la trasparenza su una scala da 0,0 a 1,0. Un valore alfa di 1,0 implica l'opacità completa, un valore alfa pari a 0,0 implica la trasparenza completa.

</dd> <dt>

<span id="opengl_animation"></span><span id="OPENGL_ANIMATION"></span>**animazione**
</dt> <dd>

La generazione di rendering ripetuti di una scena in modo sufficientemente rapido, con posizioni del punto di vista o oggetto a modifica graduale, che l'illusione del movimento viene realizzata. L'animazione OpenGL usa quasi sempre il doppio buffering.

</dd> <dt>

<span id="opengl_antialiasing"></span><span id="OPENGL_ANTIALIASING"></span>**anti-aliasing**
</dt> <dd>

Tecnica di rendering che assegna colori ai pixel in base alla frazione dell'area dei pixel coperta dalla primitiva di cui viene eseguito il rendering. Il rendering con antialias riduce o Elimina le irregolarità derivanti dal rendering con alias. Vedere anche [Jaggi](jk.md), [rendering](r.md).

</dd> <dt>

<span id="opengl_application_specific_clipping"></span><span id="OPENGL_APPLICATION_SPECIFIC_CLIPPING"></span>**ritaglio specifico dell'applicazione** 
</dt> <dd>

Ritaglio delle primitive rispetto ai piani in coordinate oculari. I piani vengono specificati dall'applicazione usando [**glClipPlane**](glclipplane.md). Vedere anche [Coordinate oculari](e.md).

</dd> </dl>

 

 




