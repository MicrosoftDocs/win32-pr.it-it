---
title: C (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- computer client
- memoria client
- coordinate di ritaglio
- area di visualizzazione
- indice dei colori
- modalità di indicizzazione dei colori
- mappe colori
- components
- contesti
- Convesso
- struttura convessa
- sistema di coordinate
- Abbattimento
- matrice corrente
- posizione raster corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39007e4719e1f4507555bf5aafa3187a897756d1d33580e9facc8fa0f6d8fa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675991"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) J [K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) T [U](t.md) [V](u-v.md) [W](w.md) X Y [Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computer client**
</dt> <dd>

Computer da cui vengono emessi i comandi OpenGL. Il computer che esegue i comandi OpenGL può essere connesso tramite una rete a un computer diverso che esegue i comandi oppure i comandi possono essere eseguiti ed eseguiti nello stesso computer. Vedere anche [server](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria client**
</dt> <dd>

Memoria principale (in cui sono archiviate le variabili di programma) del computer client.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordinate di ritaglio**
</dt> <dd>

Sistema di coordinate che segue la trasformazione in base alla matrice di proiezione e precede la divisione prospettica. Il ritaglio del volume di visualizzazione viene eseguito in coordinate di ritaglio, mentre il ritaglio specifico dell'applicazione non lo è. Vedere anche [ritaglio specifico dell'applicazione.](a.md)

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Ritaglio**
</dt> <dd>

Eliminazione della parte di una primitiva geometrica esterna al mezzo spazio definito da un piano di ritaglio. I punti vengono semplicemente rifiutati se all'esterno. La parte di una linea o di un poligono che si trova all'esterno del mezzo spazio viene eliminata e vengono generati vertici aggiuntivi in base alle esigenze per completare la primitiva all'interno del mezzo spazio di ritaglio. Le primitive geometriche e la posizione raster corrente (se specificata) vengono sempre ritagliate rispetto ai sei semi spazi definiti dai piani sinistro, destro, inferiore, superiore, vicino e lontano del volume di visualizzazione. Le applicazioni possono specificare piani di ritaglio specifici dell'applicazione facoltativi da applicare nelle coordinate oculare.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**indice dei colori**
</dt> <dd>

Singolo valore che rappresenta un colore in base al nome, anziché in base al valore. Gli indici di colore OpenGL vengono considerati come valori continui (ad esempio, numeri a virgola mobile) mentre su di essi vengono eseguite operazioni come l'interpolazione e il dithering. Tuttavia, gli indici dei colori archiviati nel buffer dei frame sono sempre valori interi. Gli indici a virgola mobile vengono convertiti in numeri interi arrotondando al valore integer più vicino.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modalità di indicizzazione dei colori**
</dt> <dd>

Modalità di un contesto OpenGL in cui i buffer dei colori archiviano gli indici dei colori, anziché i componenti di colore rosso, verde, blu e alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mappa colori**
</dt> <dd>

Tabella di mapping da indice a RGB a cui l'hardware di visualizzazione accede. Ogni indice dei colori viene letto dal buffer dei colori, convertito in una tripla RGB tramite ricerca nella mappa colori e inviato al monitor.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Componente**
</dt> <dd>

Singolo valore continuo (ad esempio, a virgola mobile) che rappresenta un'intensità o una quantità. In genere, un valore del componente pari a zero rappresenta il valore minimo o l'intensità e un valore componente pari a uno rappresenta il valore massimo o l'intensità, anche se a volte vengono usate altre normalizzazioni. Poiché i valori dei componenti vengono interpretati in un intervallo normalizzato, vengono specificati indipendentemente dalla risoluzione effettiva. Ad esempio, il triplo RGB (1, 1, 1) è bianco, indipendentemente dal fatto che i buffer dei colori archivino 4, 8 o 12 bit ciascuno. I componenti non in intervallo vengono in genere troncate all'intervallo normalizzato, non troncate o interpretate in altro modo. Ad esempio, la tripla RGB (1.4, 1.5, 0.9) viene fissata a (1.0, 1.0, 0.9) prima di essere usata per aggiornare il buffer dei colori. Rosso, verde, blu, alfa e profondità vengono sempre considerati come componenti, mai come indici.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Contesto**
</dt> <dd>

Set completo di variabili di stato OpenGL. Si noti che il contenuto di framebuffer non fa parte dello stato OpenGL, ma la configurazione di framebuffer è .

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**Convesso**
</dt> <dd>

Condizione di un poligono in cui nessuna linea retta nel piano del poligono interseca il poligono più di due volte.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**scafo convesso**
</dt> <dd>

Area convessa più piccola che racchiude un gruppo specificato di punti. In due dimensioni, la carena convessa si trova concettualmente estendendo una banda di gomito intorno ai punti in modo che tutti i punti si trovano all'interno della banda.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema di coordinate**
</dt> <dd>

Nello spazio n-dimensionale, set di n vettori linearmente indipendenti ancorati a un punto, definito origine. Un gruppo di coordinate specifica un punto nello spazio nello spazio n-dimensionale, un set di n vettori indipendenti linearmente ancorati a un punto (denominato origine). Un gruppo di coordinate specifica un punto nello spazio (o un vettore dall'origine) indicando la distanza da percorrere lungo ogni vettore per raggiungere il punto (o punta del vettore). (o un vettore dall'origine) indicando quanto deve essere percorso lungo ogni vettore per raggiungere il punto (o la punta del vettore).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**Abbattimento**
</dt> <dd>

Processo di eliminazione di una faccia anteriore o posteriore di un poligono in modo che il viso non sia disegnato.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matrice corrente**
</dt> <dd>

Matrice che trasforma le coordinate di un sistema di coordinate in coordinate di un altro sistema. OpenGL contiene tre matrici correnti: la matrice della visualizzazione modello, che trasforma le coordinate degli oggetti (coordinate specificate dal programmatore) in coordinate oculare; matrice prospettica, che trasforma le coordinate oculare in coordinate di ritaglio; e la matrice di trame, che trasforma le coordinate di trama specificate o generate come descritto dalla matrice. Ogni matrice corrente è l'elemento principale in uno stack di matrici. Ognuno dei tre stack può essere modificato con i comandi di manipolazione della matrice OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posizione raster corrente**
</dt> <dd>

Posizione delle coordinate della finestra che specifica la posizione di una primitiva di immagine quando è rasterizzata. La posizione raster corrente e altri parametri raster correnti vengono aggiornati quando viene chiamato glRasterpos.

</dd> </dl>

 

 




