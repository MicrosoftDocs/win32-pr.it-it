---
title: C (OpenGL)
description: Definizioni dei termini OpenGL che iniziano con la lettera C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- computer client
- memoria client
- ritagliare le coordinate
- area di visualizzazione
- indice colori
- modalità di indicizzazione colori
- Mappe colori
- components
- contesti
- struttura convessa
- struttura convessa
- sistema di coordinate
- selezione
- matrice corrente
- posizione raster corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047756"
---
# <a name="c-opengl"></a>C (OpenGL)

[A](a.md) [B](b.md) C [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computer client**
</dt> <dd>

Computer da cui vengono eseguiti i comandi di OpenGL. Il computer che rilascia i comandi OpenGL può essere connesso tramite una rete a un computer diverso che esegue i comandi oppure i comandi possono essere emessi ed eseguiti nello stesso computer. Vedere anche [Server](s.md).

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria client**
</dt> <dd>

Memoria principale (in cui sono archiviate le variabili di programma) del computer client.

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**ritagliare le coordinate**
</dt> <dd>

Sistema di coordinate che segue la trasformazione in base alla matrice di proiezione e precede la divisione prospettica. Visualizzazione: il ritaglio del volume viene eseguito nelle coordinate di ritaglio, ma il ritaglio specifico dell'applicazione non lo è. Vedere anche [ritaglio specifico dell'applicazione](a.md).

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**ritaglio**
</dt> <dd>

Eliminazione della parte di una primitiva geometrica esterna alla metà dello spazio definita da un piano di ritaglio. I punti vengono semplicemente rifiutati se esterni a. La parte di una linea o di un poligono che si trova all'esterno della metà dello spazio viene eliminata e vengono generati altri vertici necessari per completare la primitiva all'interno della metà dello spazio di ritaglio. Le primitive geometriche e la posizione raster corrente (se specificata) vengono sempre ritagliate in base ai sei spazi a sinistra, a destra, in basso, in alto, in prossimità e ai piani del volume di visualizzazione. Le applicazioni possono specificare piani di ritaglio specifici dell'applicazione facoltativi da applicare alle coordinate oculari.

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**indice colori**
</dt> <dd>

Un singolo valore che rappresenta un colore per nome, anziché per valore. Gli indici di colore OpenGL vengono considerati come valori continui, ad esempio numeri a virgola mobile, mentre vengono eseguite operazioni quali l'interpolazione e la dithering. Tuttavia, gli indici dei colori archiviati nel buffer del frame sono sempre valori interi. Gli indici a virgola mobile vengono convertiti in numeri interi arrotondando al valore intero più vicino.

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modalità di indicizzazione colori**
</dt> <dd>

Modalità di un contesto OpenGL in cui i buffer dei colori archiviano gli indici di colore, anziché i componenti di colore rosso, verde, blu e alfa.

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mappa colori**
</dt> <dd>

Tabella di mapping da indice a RGB a cui è possibile accedere dall'hardware di visualizzazione. Ogni indice di colore viene letto dal buffer dei colori, convertito in una tripla RGB mediante ricerca nella mappa colori e inviato al monitoraggio.

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**componente**
</dt> <dd>

Singolo valore continuo (ad esempio, a virgola mobile) che rappresenta un'intensità o una quantità. In genere, un valore di componente pari a zero rappresenta il valore o l'intensità minima e il valore di un componente rappresenta il valore o l'intensità massima, sebbene vengano talvolta utilizzate altre normalizzazioni. Poiché i valori dei componenti vengono interpretati in un intervallo normalizzato, vengono specificati indipendentemente dalla risoluzione effettiva. Ad esempio, la tripla RGB (1, 1, 1) è bianca, indipendentemente dal fatto che i buffer dei colori memorizzino ognuno 4, 8 o 12 bit. I componenti out-of-range vengono in genere fissati all'intervallo normalizzato, non troncato o interpretato in altro modo. Ad esempio, la tripla RGB (1,4, 1,5, 0,9) viene fissata a (1,0, 1,0, 0,9) prima di essere utilizzata per aggiornare il buffer di colore. Red, Green, Blue, Alpha e Depth vengono sempre considerati componenti, mai come indici.

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contesto**
</dt> <dd>

Set completo di variabili di stato OpenGL. Si noti che il contenuto del framebuffer non fa parte dello stato OpenGL, ma che la configurazione del framebuffer è.

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**struttura convessa**
</dt> <dd>

Condizione di un poligono in cui nessuna linea retta nel piano del poligono interseca il poligono più di due volte.

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**struttura convessa**
</dt> <dd>

Area convessa più piccola che racchiude un gruppo di punti specificato. In due dimensioni, la struttura convessa viene trovata concettualmente allungando una striscia di gomma intorno ai punti in modo che tutti i punti si trovino all'interno della banda.

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema di coordinate**
</dt> <dd>

Nello spazio n-dimensionale, set di n vettori linearmente indipendenti ancorati a un punto, definito origine. Un gruppo di coordinate specifica un punto nello spazio n-dimensionale, un set di n vettori linearmente indipendenti ancorati a un punto (denominato origine). Un gruppo di coordinate specifica un punto nello spazio (o un vettore dall'origine) indicando la distanza da percorrere lungo ogni vettore per raggiungere il punto (o punta del vettore). (o un vettore dall'origine) indicando la distanza di spostamento lungo ogni vettore per raggiungere il punto (o la punta del vettore).

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**selezione**
</dt> <dd>

Processo di eliminazione di un front-end o di un back-end di un poligono in modo che la faccia non venga disegnata.

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matrice corrente**
</dt> <dd>

Matrice che trasforma le coordinate in un sistema di coordinate in coordinate di un altro sistema. In OpenGL sono disponibili tre matrici correnti: la matrice Modelview, che trasforma le coordinate degli oggetti (coordinate specificate dal programmatore) in coordinate oculari; matrice prospettiva, che trasforma le coordinate oculari per ritagliare le coordinate; e la matrice di trama, che trasforma le coordinate di trama specificate o generate come descritto dalla matrice. Ogni matrice corrente è l'elemento principale in uno stack di matrici. Ognuno dei tre stack può essere modificato con i comandi di manipolazione della matrice OpenGL.

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posizione raster corrente**
</dt> <dd>

Posizione della coordinata della finestra che specifica la posizione di una primitiva di immagine quando viene rasterizzata. La posizione raster corrente e altri parametri raster correnti vengono aggiornati quando viene chiamato glRasterpos.

</dd> </dl>

 

 




