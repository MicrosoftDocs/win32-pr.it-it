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
# <a name="c-opengl"></a><span data-ttu-id="a7f21-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="a7f21-118">C (OpenGL)</span></span>

<span data-ttu-id="a7f21-119">[A](a.md) [B](b.md) C [d](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="a7f21-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="a7f21-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computer client**</span><span class="sxs-lookup"><span data-stu-id="a7f21-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-121">Computer da cui vengono eseguiti i comandi di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a7f21-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="a7f21-122">Il computer che rilascia i comandi OpenGL può essere connesso tramite una rete a un computer diverso che esegue i comandi oppure i comandi possono essere emessi ed eseguiti nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="a7f21-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="a7f21-123">Vedere anche [Server](s.md).</span><span class="sxs-lookup"><span data-stu-id="a7f21-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memoria client**</span><span class="sxs-lookup"><span data-stu-id="a7f21-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-125">Memoria principale (in cui sono archiviate le variabili di programma) del computer client.</span><span class="sxs-lookup"><span data-stu-id="a7f21-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**ritagliare le coordinate**</span><span class="sxs-lookup"><span data-stu-id="a7f21-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-127">Sistema di coordinate che segue la trasformazione in base alla matrice di proiezione e precede la divisione prospettica.</span><span class="sxs-lookup"><span data-stu-id="a7f21-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="a7f21-128">Visualizzazione: il ritaglio del volume viene eseguito nelle coordinate di ritaglio, ma il ritaglio specifico dell'applicazione non lo è.</span><span class="sxs-lookup"><span data-stu-id="a7f21-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="a7f21-129">Vedere anche [ritaglio specifico dell'applicazione](a.md).</span><span class="sxs-lookup"><span data-stu-id="a7f21-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**ritaglio**</span><span class="sxs-lookup"><span data-stu-id="a7f21-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-131">Eliminazione della parte di una primitiva geometrica esterna alla metà dello spazio definita da un piano di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a7f21-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="a7f21-132">I punti vengono semplicemente rifiutati se esterni a.</span><span class="sxs-lookup"><span data-stu-id="a7f21-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="a7f21-133">La parte di una linea o di un poligono che si trova all'esterno della metà dello spazio viene eliminata e vengono generati altri vertici necessari per completare la primitiva all'interno della metà dello spazio di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="a7f21-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="a7f21-134">Le primitive geometriche e la posizione raster corrente (se specificata) vengono sempre ritagliate in base ai sei spazi a sinistra, a destra, in basso, in alto, in prossimità e ai piani del volume di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a7f21-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="a7f21-135">Le applicazioni possono specificare piani di ritaglio specifici dell'applicazione facoltativi da applicare alle coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="a7f21-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**indice colori**</span><span class="sxs-lookup"><span data-stu-id="a7f21-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-137">Un singolo valore che rappresenta un colore per nome, anziché per valore.</span><span class="sxs-lookup"><span data-stu-id="a7f21-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="a7f21-138">Gli indici di colore OpenGL vengono considerati come valori continui, ad esempio numeri a virgola mobile, mentre vengono eseguite operazioni quali l'interpolazione e la dithering.</span><span class="sxs-lookup"><span data-stu-id="a7f21-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="a7f21-139">Tuttavia, gli indici dei colori archiviati nel buffer del frame sono sempre valori interi.</span><span class="sxs-lookup"><span data-stu-id="a7f21-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="a7f21-140">Gli indici a virgola mobile vengono convertiti in numeri interi arrotondando al valore intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="a7f21-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modalità di indicizzazione colori**</span><span class="sxs-lookup"><span data-stu-id="a7f21-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-142">Modalità di un contesto OpenGL in cui i buffer dei colori archiviano gli indici di colore, anziché i componenti di colore rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="a7f21-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mappa colori**</span><span class="sxs-lookup"><span data-stu-id="a7f21-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-144">Tabella di mapping da indice a RGB a cui è possibile accedere dall'hardware di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="a7f21-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="a7f21-145">Ogni indice di colore viene letto dal buffer dei colori, convertito in una tripla RGB mediante ricerca nella mappa colori e inviato al monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="a7f21-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="a7f21-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-147">Singolo valore continuo (ad esempio, a virgola mobile) che rappresenta un'intensità o una quantità.</span><span class="sxs-lookup"><span data-stu-id="a7f21-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="a7f21-148">In genere, un valore di componente pari a zero rappresenta il valore o l'intensità minima e il valore di un componente rappresenta il valore o l'intensità massima, sebbene vengano talvolta utilizzate altre normalizzazioni.</span><span class="sxs-lookup"><span data-stu-id="a7f21-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="a7f21-149">Poiché i valori dei componenti vengono interpretati in un intervallo normalizzato, vengono specificati indipendentemente dalla risoluzione effettiva.</span><span class="sxs-lookup"><span data-stu-id="a7f21-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="a7f21-150">Ad esempio, la tripla RGB (1, 1, 1) è bianca, indipendentemente dal fatto che i buffer dei colori memorizzino ognuno 4, 8 o 12 bit.</span><span class="sxs-lookup"><span data-stu-id="a7f21-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="a7f21-151">I componenti out-of-range vengono in genere fissati all'intervallo normalizzato, non troncato o interpretato in altro modo.</span><span class="sxs-lookup"><span data-stu-id="a7f21-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="a7f21-152">Ad esempio, la tripla RGB (1,4, 1,5, 0,9) viene fissata a (1,0, 1,0, 0,9) prima di essere utilizzata per aggiornare il buffer di colore.</span><span class="sxs-lookup"><span data-stu-id="a7f21-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="a7f21-153">Red, Green, Blue, Alpha e Depth vengono sempre considerati componenti, mai come indici.</span><span class="sxs-lookup"><span data-stu-id="a7f21-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**contesto**</span><span class="sxs-lookup"><span data-stu-id="a7f21-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-155">Set completo di variabili di stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a7f21-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="a7f21-156">Si noti che il contenuto del framebuffer non fa parte dello stato OpenGL, ma che la configurazione del framebuffer è.</span><span class="sxs-lookup"><span data-stu-id="a7f21-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**struttura convessa**</span><span class="sxs-lookup"><span data-stu-id="a7f21-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-158">Condizione di un poligono in cui nessuna linea retta nel piano del poligono interseca il poligono più di due volte.</span><span class="sxs-lookup"><span data-stu-id="a7f21-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**struttura convessa**</span><span class="sxs-lookup"><span data-stu-id="a7f21-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-160">Area convessa più piccola che racchiude un gruppo di punti specificato.</span><span class="sxs-lookup"><span data-stu-id="a7f21-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="a7f21-161">In due dimensioni, la struttura convessa viene trovata concettualmente allungando una striscia di gomma intorno ai punti in modo che tutti i punti si trovino all'interno della banda.</span><span class="sxs-lookup"><span data-stu-id="a7f21-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema di coordinate**</span><span class="sxs-lookup"><span data-stu-id="a7f21-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-163">Nello spazio n-dimensionale, set di n vettori linearmente indipendenti ancorati a un punto, definito origine.</span><span class="sxs-lookup"><span data-stu-id="a7f21-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="a7f21-164">Un gruppo di coordinate specifica un punto nello spazio n-dimensionale, un set di n vettori linearmente indipendenti ancorati a un punto (denominato origine).</span><span class="sxs-lookup"><span data-stu-id="a7f21-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="a7f21-165">Un gruppo di coordinate specifica un punto nello spazio (o un vettore dall'origine) indicando la distanza da percorrere lungo ogni vettore per raggiungere il punto (o punta del vettore).</span><span class="sxs-lookup"><span data-stu-id="a7f21-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="a7f21-166">(o un vettore dall'origine) indicando la distanza di spostamento lungo ogni vettore per raggiungere il punto (o la punta del vettore).</span><span class="sxs-lookup"><span data-stu-id="a7f21-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**selezione**</span><span class="sxs-lookup"><span data-stu-id="a7f21-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-168">Processo di eliminazione di un front-end o di un back-end di un poligono in modo che la faccia non venga disegnata.</span><span class="sxs-lookup"><span data-stu-id="a7f21-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matrice corrente**</span><span class="sxs-lookup"><span data-stu-id="a7f21-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-170">Matrice che trasforma le coordinate in un sistema di coordinate in coordinate di un altro sistema.</span><span class="sxs-lookup"><span data-stu-id="a7f21-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="a7f21-171">In OpenGL sono disponibili tre matrici correnti: la matrice Modelview, che trasforma le coordinate degli oggetti (coordinate specificate dal programmatore) in coordinate oculari; matrice prospettiva, che trasforma le coordinate oculari per ritagliare le coordinate; e la matrice di trama, che trasforma le coordinate di trama specificate o generate come descritto dalla matrice.</span><span class="sxs-lookup"><span data-stu-id="a7f21-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="a7f21-172">Ogni matrice corrente è l'elemento principale in uno stack di matrici.</span><span class="sxs-lookup"><span data-stu-id="a7f21-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="a7f21-173">Ognuno dei tre stack può essere modificato con i comandi di manipolazione della matrice OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a7f21-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="a7f21-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posizione raster corrente**</span><span class="sxs-lookup"><span data-stu-id="a7f21-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="a7f21-175">Posizione della coordinata della finestra che specifica la posizione di una primitiva di immagine quando viene rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="a7f21-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="a7f21-176">La posizione raster corrente e altri parametri raster correnti vengono aggiornati quando viene chiamato glRasterpos.</span><span class="sxs-lookup"><span data-stu-id="a7f21-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




