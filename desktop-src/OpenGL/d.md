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
# <a name="d-opengl"></a>D (OpenGL)

[A](a.md) [B](b.md) [C](c.md) d [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_depth"></span><span id="OPENGL_DEPTH"></span>**profondità**
</dt> <dd>

In genere si riferisce alla coordinata z della finestra.

</dd> <dt>

<span id="opengl_depth_cueing"></span><span id="OPENGL_DEPTH_CUEING"></span>**Cue di profondità**
</dt> <dd>

Una tecnica di rendering che assegna il colore in base alla distanza dal punto di vista.

</dd> <dt>

<span id="opengl_display_list"></span><span id="OPENGL_DISPLAY_LIST"></span>**elenco di visualizzazione**
</dt> <dd>

Elenco denominato di comandi OpenGL. Gli elenchi di visualizzazione vengono sempre archiviati nel server, pertanto è possibile utilizzare gli elenchi di visualizzazione per ridurre il traffico di rete in ambienti client/server. Il contenuto di un elenco di visualizzazione può essere pre-elaborato e potrebbe quindi essere eseguito in modo più efficiente rispetto allo stesso set di comandi OpenGL eseguiti in modalità immediata. Questa pre-elaborazione è particolarmente importante per il calcolo di comandi con utilizzo intensivo, ad esempio [**glTexImage**](glteximage1d.md).

</dd> <dt>

<span id="opengl_dithering"></span><span id="OPENGL_DITHERING"></span>**dithering**
</dt> <dd>

Una tecnica per aumentare l'intervallo di colori percepito in un'immagine al costo della risoluzione spaziale. Ai pixel adiacenti vengono assegnati valori di colore diversi. Quando vengono visualizzati da una distanza, questi colori sembrano fondersi in un singolo colore intermedio. La tecnica è simile a quella usata per le pubblicazioni in bianco e nero per ottenere sfumature di grigio.

</dd> <dt>

<span id="opengl_double_buffering"></span><span id="OPENGL_DOUBLE_BUFFERING"></span>**doppio buffer**
</dt> <dd>

Uso di contesti OpenGL in cui i buffer dei colori di primo e indietro sono con doppio buffer. L'animazione uniforme viene eseguita eseguendo il rendering solo nel buffer nascosto (che non viene visualizzato), causando lo scambio dei buffer di primo e indietro.

</dd> </dl>

 

 




