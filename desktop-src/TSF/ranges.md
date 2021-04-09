---
title: Intervalli
description: Intervalli
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Framework servizi di testo (TSF), intervalli
- TSF (Framework di servizi di testo), intervalli
- Servizi di testo, intervalli
- Applicazioni abilitate per TSF, intervalli
- ranges
- Framework servizi di testo (TSF), ancoraggi
- TSF (Framework di servizi di testo), ancoraggi
- Servizi di testo, ancoraggi
- Applicazioni abilitate per TSF, ancoraggi
- ancoraggi
- Framework servizi di testo (TSF), cloni
- TSF (Framework di servizi di testo), cloni
- Servizi di testo, cloni
- Applicazioni abilitate per TSF, cloni
- cloni
- Framework servizi di testo (TSF), backup
- TSF (Framework di servizi di testo), backup
- Servizi di testo, backup
- Applicazioni abilitate per TSF, backup
- backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955810"
---
# <a name="ranges"></a><span data-ttu-id="49578-123">Intervalli</span><span class="sxs-lookup"><span data-stu-id="49578-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="49578-124">Ancoraggi</span><span class="sxs-lookup"><span data-stu-id="49578-124">Anchors</span></span>

<span data-ttu-id="49578-125">Un intervallo è delimitato da due *ancoraggi*, un ancoraggio iniziale e un ancoraggio finale.</span><span class="sxs-lookup"><span data-stu-id="49578-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="49578-126">Un ancoraggio esiste in uno slot immaginario tra due caratteri.</span><span class="sxs-lookup"><span data-stu-id="49578-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="49578-127">L'ancoraggio iniziale si riferisce al testo che segue l'ancoraggio e l'ancoraggio finale è correlato al testo che precede l'ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="49578-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="49578-128">Entrambi gli ancoraggi di inizio e fine possono esistere nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="49578-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="49578-129">In questo caso, l'intervallo ha una lunghezza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="49578-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="49578-130">Ad esempio, iniziare con il testo seguente:</span><span class="sxs-lookup"><span data-stu-id="49578-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="49578-131">Applicare ora un intervallo al testo con entrambi gli ancoraggi iniziale e finale nella posizione 0.</span><span class="sxs-lookup"><span data-stu-id="49578-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="49578-132">Viene rappresentato visivamente come segue:</span><span class="sxs-lookup"><span data-stu-id="49578-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="49578-133">Gli ancoraggi non prendono spazio all'interno del testo stesso.</span><span class="sxs-lookup"><span data-stu-id="49578-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="49578-134">Si tratta di un intervallo di lunghezza zero e il testo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="49578-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="49578-135">A questo punto, spostare l'ancoraggio finale + 3 posizioni.</span><span class="sxs-lookup"><span data-stu-id="49578-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="49578-136">Viene rappresentato visivamente come segue:</span><span class="sxs-lookup"><span data-stu-id="49578-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="49578-137">L'ancoraggio iniziale è posizionato immediatamente prima del carattere nella posizione 0 e l'ancoraggio finale è posizionato subito dopo il carattere nella posizione 3 perché l'ancoraggio finale è stato spostato a destra di 3 posizioni.</span><span class="sxs-lookup"><span data-stu-id="49578-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="49578-138">L'intervallo di testo è ora "Thi".</span><span class="sxs-lookup"><span data-stu-id="49578-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="49578-139">Inoltre, l'ancoraggio iniziale non può essere eseguito per seguire l'ancoraggio finale e non è possibile fare in modo che preceda l'ancoraggio iniziale.</span><span class="sxs-lookup"><span data-stu-id="49578-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="49578-140">Gravità ancoraggio</span><span class="sxs-lookup"><span data-stu-id="49578-140">Anchor Gravity</span></span>

<span data-ttu-id="49578-141">Ogni ancoraggio ha un'impostazione di *gravità* che determina il modo in cui l'ancoraggio risponde quando il testo viene inserito nel flusso di testo nella posizione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="49578-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="49578-142">Quando viene eseguito un inserimento in corrispondenza della posizione di un ancoraggio, è necessario apportare una modifica nella posizione dell'ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="49578-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="49578-143">La gravità determina il modo in cui viene apportata la regolazione della posizione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="49578-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="49578-144">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="49578-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="49578-145">Se la parola "very" viene inserita nella posizione dell'intervallo, l'ancoraggio iniziale può essere posizionato prima o dopo la parola inserita:</span><span class="sxs-lookup"><span data-stu-id="49578-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="49578-146">\- oppure -</span><span class="sxs-lookup"><span data-stu-id="49578-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="49578-147">La gravità di ancoraggio specifica il modo in cui l'ancoraggio viene riposizionato quando viene eseguito un inserimento nella relativa posizione.</span><span class="sxs-lookup"><span data-stu-id="49578-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="49578-148">La gravità può essere *indietro* o *Avanti*.</span><span class="sxs-lookup"><span data-stu-id="49578-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="49578-149">Se l'ancoraggio presenta una gravità precedente, l'ancoraggio si sposta indietro rispetto al punto di inserimento, in caso di inserimento, in modo che il testo inserito segua l'ancoraggio:</span><span class="sxs-lookup"><span data-stu-id="49578-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="49578-150">Se l'ancoraggio ha una gravità in avanti, l'ancoraggio si sposta in avanti rispetto al punto di inserimento, in modo che il testo inserito preceda l'ancoraggio:</span><span class="sxs-lookup"><span data-stu-id="49578-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="49578-151">Cloni e backup</span><span class="sxs-lookup"><span data-stu-id="49578-151">Clones and Backups</span></span>

<span data-ttu-id="49578-152">Esistono due modi per creare una copia di un oggetto Range.</span><span class="sxs-lookup"><span data-stu-id="49578-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="49578-153">Il primo consiste nel creare un *Clone* dell'intervallo usando [ITfRange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span><span class="sxs-lookup"><span data-stu-id="49578-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="49578-154">Il secondo consiste nell'eseguire un *backup* dell'intervallo usando [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span><span class="sxs-lookup"><span data-stu-id="49578-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="49578-155">Un clone è una copia di un intervallo che non include dati statici.</span><span class="sxs-lookup"><span data-stu-id="49578-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="49578-156">Gli ancoraggi dell'intervallo vengono copiati, ma il clone copre ancora un intervallo di testo all'interno del contesto.</span><span class="sxs-lookup"><span data-stu-id="49578-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="49578-157">Un clone è un oggetto Range in tutti gli aspetti.</span><span class="sxs-lookup"><span data-stu-id="49578-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="49578-158">Ciò significa che il testo e le proprietà di un intervallo clonato sono dinamici e verranno modificati se il testo e/o le proprietà dell'intervallo coperto dal clone cambiano.</span><span class="sxs-lookup"><span data-stu-id="49578-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="49578-159">Un backup archivia il testo e le proprietà di un intervallo nel momento in cui il backup viene eseguito come dati statici.</span><span class="sxs-lookup"><span data-stu-id="49578-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="49578-160">Un backup clona anche l'intervallo originale in modo che sia possibile tenere traccia delle modifiche apportate alle dimensioni e alla posizione dell'intervallo originale.</span><span class="sxs-lookup"><span data-stu-id="49578-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="49578-161">Ciò significa che il testo e le proprietà di un intervallo di cui è stato eseguito il backup sono statici e non cambiano se il testo e/o le proprietà dell'intervallo coperto dal backup cambiano.</span><span class="sxs-lookup"><span data-stu-id="49578-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="49578-162">Ad esempio, l'intervallo seguente (pRange) all'interno del contesto:</span><span class="sxs-lookup"><span data-stu-id="49578-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="49578-163">A questo punto, creare un clone e un backup di questo intervallo:</span><span class="sxs-lookup"><span data-stu-id="49578-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="49578-164">A questo punto, gli oggetti contengono gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="49578-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="49578-165">Modificare ora il testo di pRange:</span><span class="sxs-lookup"><span data-stu-id="49578-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="49578-166">A questo punto, gli oggetti contengono gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="49578-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="49578-167">L'impostazione del testo ha causato la modifica del testo all'interno del contesto.</span><span class="sxs-lookup"><span data-stu-id="49578-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="49578-168">Ha anche causato la modifica dell'ancoraggio finale di pRange e pClone.</span><span class="sxs-lookup"><span data-stu-id="49578-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="49578-169">pClone contiene ora "altre parole" perché il testo è stato modificato nell'intervallo e le modifiche vengono rilevate da tutti gli intervalli.</span><span class="sxs-lookup"><span data-stu-id="49578-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="49578-170">Quando il testo coperto da pRange e pClone è stato modificato, anche il testo di pClone è cambiato.</span><span class="sxs-lookup"><span data-stu-id="49578-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="49578-171">Il testo in pBackup non è stato modificato rispetto al pRange originale perché i dati (testo e proprietà) nel backup non sono correlati al contesto e vengono archiviati separatamente.</span><span class="sxs-lookup"><span data-stu-id="49578-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="49578-172">Il clone contenuto all'interno del backup cambia effettivamente, ma i dati sono statici.</span><span class="sxs-lookup"><span data-stu-id="49578-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="49578-173">Quando si ripristina un backup, il backup può essere applicato al clone all'interno del backup o a un intervallo diverso.</span><span class="sxs-lookup"><span data-stu-id="49578-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="49578-174">Per applicare il backup al clone all'interno del backup, passare **null** a [ITfRangeBackup:: Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) , come illustrato nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="49578-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="49578-175">A questo punto, gli oggetti contengono gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="49578-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="49578-176">Per ripristinare il backup in un intervallo diverso, passare un puntatore all'oggetto intervallo quando si chiama **ITfRangeBackup:: Restore**.</span><span class="sxs-lookup"><span data-stu-id="49578-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="49578-177">Il testo e le proprietà di cui è stato eseguito il backup verranno applicati al nuovo intervallo.</span><span class="sxs-lookup"><span data-stu-id="49578-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="49578-178">Ad esempio, usando l'esempio precedente prima della chiamata di **ripristino** , Prange verrà modificato per illustrare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="49578-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="49578-179">A questo punto, gli oggetti contengono gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="49578-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="49578-180">Quando l'ancoraggio finale di pRange è stato spostato a sinistra di due punti, l'ancoraggio finale di pClone non è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="49578-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="49578-181">A questo punto, ripristinare il backup usando pRange con l'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="49578-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="49578-182">A questo punto, gli oggetti contengono gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="49578-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="49578-183">Il testo coperto da pRange è stato sostituito con "Text", una parte del testo analizzata da pClone è stata modificata e pBackup cambia per trovare la corrispondenza con pRange.</span><span class="sxs-lookup"><span data-stu-id="49578-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




