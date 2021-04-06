---
title: Formato degli Appunti HTML
description: In questa sezione viene illustrato il formato degli Appunti HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Interfaccia utente di Windows, appunti
- Appunti, taglio di dati
- Appunti, copia di dati
- Appunti, incolla di dati
- Appunti, formati
- Appunti, formato HTML
- Appunti, taglio del testo HTML
- Appunti, incollare testo HTML
- Formato degli Appunti CF_HTML
- Appunti, formato CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044887"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="ad916-113">Formato degli Appunti HTML</span><span class="sxs-lookup"><span data-stu-id="ad916-113">HTML Clipboard Format</span></span>

<span data-ttu-id="ad916-114">I requisiti per il trasferimento del testo HTML per mezzo degli Appunti variano a seconda dello scenario.</span><span class="sxs-lookup"><span data-stu-id="ad916-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="ad916-115">In questo articolo si tratta di tagliare e incollare frammenti di un documento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="ad916-116">Potrebbero esserci requisiti per il trasferimento di interi documenti HTML tramite gli Appunti. Tuttavia, questo articolo è determinato da un requisito per trasferire frammenti del testo HTML selezionato.</span><span class="sxs-lookup"><span data-stu-id="ad916-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="ad916-117">Di conseguenza, un metodo che ha richiesto l'intero documento HTML da copiare negli Appunti viene considerato troppo pesante.</span><span class="sxs-lookup"><span data-stu-id="ad916-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="ad916-118">Il \_ formato degli Appunti HTML CF consente a un frammento di testo HTML non elaborato e del relativo contesto di essere archiviato negli Appunti come ASCII.</span><span class="sxs-lookup"><span data-stu-id="ad916-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="ad916-119">Questo consente il contesto del frammento HTML, che è costituito da tutti i tag circostanti precedenti, che devono essere esaminati da un'applicazione in modo che i tag circostanti del frammento HTML possano essere annotati con i relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="ad916-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="ad916-120">Sebbene le applicazioni decidano come interpretare tali frammenti, alcune linee guida di base sono incluse in questo articolo, in base alle implementazioni IE4/MSHTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="ad916-121">Il nome ufficiale degli Appunti (la stringa utilizzata da RegisterClipboardFormat) è formato HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="ad916-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad916-122">Description</span></span>](#description)
-   [<span data-ttu-id="ad916-123">Scenari</span><span class="sxs-lookup"><span data-stu-id="ad916-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="ad916-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad916-124">Description</span></span>

<span data-ttu-id="ad916-125">\_Il formato HTML CF è interamente formato da testo (per essere, tra le altre cose, nello spirito HTML e usa UTF-8) e include un `description` , un facoltativo `context` e, all'interno del contesto, il `fragment` .</span><span class="sxs-lookup"><span data-stu-id="ad916-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="ad916-126">Di seguito è riportato un esempio di uno degli Appunti:</span><span class="sxs-lookup"><span data-stu-id="ad916-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="ad916-127">La descrizione include il numero di versione e gli offset degli Appunti, che indicano dove il contesto e l'inizio e la fine del frammento.</span><span class="sxs-lookup"><span data-stu-id="ad916-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="ad916-128">La descrizione è un elenco di parole chiave di testo ASCII (min/Maj non è significativo) seguite da una stringa e separate da due punti (:).</span><span class="sxs-lookup"><span data-stu-id="ad916-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="ad916-129">**Versione**: il numero di versione degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ad916-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="ad916-130">La versione iniziale è 0,9.</span><span class="sxs-lookup"><span data-stu-id="ad916-130">Starting version is 0.9.</span></span>

<span data-ttu-id="ad916-131">**StartHTML**: GetByteCount dall'inizio degli Appunti all'inizio del contesto, oppure-1 se non è presente alcun contesto.</span><span class="sxs-lookup"><span data-stu-id="ad916-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="ad916-132">È possibile eseguire l' **indhtml**, dall'inizio degli Appunti alla fine del contesto oppure-1 se non è presente alcun contesto.</span><span class="sxs-lookup"><span data-stu-id="ad916-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="ad916-133">**StartFragment**: GetByteCount dall'inizio degli Appunti all'inizio del frammento.</span><span class="sxs-lookup"><span data-stu-id="ad916-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="ad916-134">**EndFragment**: GetByteCount dall'inizio degli Appunti alla fine del frammento.</span><span class="sxs-lookup"><span data-stu-id="ad916-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="ad916-135">**StartSelection**: GetByteCount dall'inizio degli Appunti all'inizio della selezione.</span><span class="sxs-lookup"><span data-stu-id="ad916-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="ad916-136">Di cui è possibile eseguire la **selezione, dall'** inizio degli Appunti alla fine della selezione.</span><span class="sxs-lookup"><span data-stu-id="ad916-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="ad916-137">Le parole chiave StartSelection e sono facoltative e devono essere omesse se non si vuole che l'applicazione generi queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ad916-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="ad916-138">Altre informazioni di questo tipo potrebbero essere aggiunte in un secondo momento, perché il codice HTML inizia in corrispondenza del StartHTMLoffset.</span><span class="sxs-lookup"><span data-stu-id="ad916-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="ad916-139">Ad esempio, è possibile aggiungere più coppie di StartFragment/EndFragment in un secondo momento per supportare la selezione non contigua dei frammenti.</span><span class="sxs-lookup"><span data-stu-id="ad916-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="ad916-140">Per praticità dei programmi che generano il valore di getbytecounts, è possibile lasciare gli zeri imbottiti.</span><span class="sxs-lookup"><span data-stu-id="ad916-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="ad916-141">Ad esempio, i programmi che generano l'oggetto GetByteCount possono influenzare arbitrariamente dieci (10) zeri per ogni parola chiave (StartHTML: 0000000000) e quindi, quando il valore esatto StartHTML GetByteCount è noto (ad esempio, 71), il programma può sostituire il numero appropriato di zeri con l'oggetto GetByteCount (StartHTML: 0000000071).</span><span class="sxs-lookup"><span data-stu-id="ad916-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="ad916-142">L'unico set di caratteri supportato dagli Appunti è Unicode nella codifica UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ad916-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="ad916-143">Poiché i primi caratteri di UTF-8 e ASCII corrispondono, la descrizione è sempre ASCII, ma i byte del contesto (a partire da StartHTML) potrebbero usare qualsiasi altro carattere codificato in UTF-8.</span><span class="sxs-lookup"><span data-stu-id="ad916-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="ad916-144">La fine delle righe nell'intestazione del formato degli Appunti può essere CR o CR/LF o LF.</span><span class="sxs-lookup"><span data-stu-id="ad916-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="ad916-145">Il frammento contiene un HTML puro e valido che rappresenta l'area selezionata dall'utente, ad esempio per la copia.</span><span class="sxs-lookup"><span data-stu-id="ad916-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="ad916-146">Contiene il testo selezionato più i tag di apertura e gli attributi di qualsiasi elemento con un tag di fine all'interno del testo selezionato e i tag di fine alla fine del frammento per qualsiasi tag di inizio incluso.</span><span class="sxs-lookup"><span data-stu-id="ad916-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="ad916-147">Si tratta di tutte le informazioni necessarie per incollare di base di un frammento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="ad916-148">Il frammento deve essere preceduto e seguito dai commenti HTML</span><span class="sxs-lookup"><span data-stu-id="ad916-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="ad916-149">e</span><span class="sxs-lookup"><span data-stu-id="ad916-149">and</span></span> <!--EndFragment--> <span data-ttu-id="ad916-150">non è consentito alcuno spazio tra il!--e il testo) per indicare facilmente la posizione in cui il frammento inizia e termina.</span><span class="sxs-lookup"><span data-stu-id="ad916-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="ad916-151">Pertanto, l'inizio e la fine del frammento sono indicate dalla presenza di questi commenti e dai conteggi dei byte StartFragment e EndFragment nella descrizione.</span><span class="sxs-lookup"><span data-stu-id="ad916-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="ad916-152">Si prevede che gli strumenti producano queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="ad916-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="ad916-153">Questa ridondanza è stata introdotta per poter trovare rapidamente l'inizio del frammento (dal numero di byte) e contrassegnare la posizione del frammento direttamente nell'albero HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="ad916-154">La selezione indica all'interno del frammento l'area HTML esatta selezionata dall'utente, ad esempio per la copia.</span><span class="sxs-lookup"><span data-stu-id="ad916-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="ad916-155">Verranno aggiunte altre informazioni al frammento indicando il testo selezionato esatto, senza i tag di apertura e i tag di fine che sono stati aggiunti per garantire che il frammento sia HTML ben formato.</span><span class="sxs-lookup"><span data-stu-id="ad916-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="ad916-156">La selezione è facoltativa, poiché nel frammento viene inclusa una quantità di informazioni sufficiente per l'incollatura di base.</span><span class="sxs-lookup"><span data-stu-id="ad916-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="ad916-157">Se la selezione non viene archiviata, i StartSelection e l'inclusione non vengono archiviati nell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="ad916-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="ad916-158">Il contesto è un documento HTML completo e valido.</span><span class="sxs-lookup"><span data-stu-id="ad916-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="ad916-159">Questo articolo contiene il frammento e tutti i tag circostanti (tag di inizio e di fine) che precedono rappresentano tutti i nodi padre del frammento fino al nodo HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="ad916-160">L'articolo contiene anche l'intestazione completa e consente di includere, ad esempio, gli elementi di BASE e titolo, in modo da poter ottenere queste informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="ad916-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="ad916-161">Un'applicazione che copia un frammento di codice HTML negli Appunti può scegliere di creare un elemento di BASE da includere nel contesto se tale elemento non è già presente, in modo da poter risolvere gli URL parziali nel frammento.</span><span class="sxs-lookup"><span data-stu-id="ad916-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="ad916-162">Il contesto è facoltativo, dal momento che nel frammento sono incluse informazioni sufficienti per l'incollamento di base di un frammento HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="ad916-163">Se il contesto non è archiviato, viene archiviato solo il frammento e StartHTML = dHTML =-1.</span><span class="sxs-lookup"><span data-stu-id="ad916-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="ad916-164">Scenari</span><span class="sxs-lookup"><span data-stu-id="ad916-164">Scenarios</span></span>

<span data-ttu-id="ad916-165">Negli scenari seguenti viene descritto il modo in cui l'editor HTML IE4/MSHTML gestisce le operazioni Taglia e Incolla HTML; è possibile che altre applicazioni non seguano questi scenari.</span><span class="sxs-lookup"><span data-stu-id="ad916-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="ad916-166">Il formato degli Appunti descritto di seguito ha lo scopo di consentire la flessibilità del modo in cui un'applicazione sceglie di funzionare.</span><span class="sxs-lookup"><span data-stu-id="ad916-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="ad916-167">Questi scenari mostrano solo codice HTML valido, ovvero nessun tag sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="ad916-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="ad916-168">Semplice frammento di codice HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="ad916-169">Testo HTML:</span><span class="sxs-lookup"><span data-stu-id="ad916-169">HTML text:</span></span>

            <span data-ttu-id="ad916-170"><BODY>Si tratta di una situazione normale in <B>grassetto </B>. si tratta di <I> <B> </B>un corsivo</I></BODY></span><span class="sxs-lookup"><span data-stu-id="ad916-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="ad916-171">Viene visualizzato come:</span><span class="sxs-lookup"><span data-stu-id="ad916-171">Appears as:</span></span>

            <span data-ttu-id="ad916-172">Si tratta di una situazione normale in **grassetto**. si tratta di un corsivo    \*    \*</span><span class="sxs-lookup"><span data-stu-id="ad916-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="ad916-173">Il testo tra \* \* è selezionato e copiato negli Appunti:</span><span class="sxs-lookup"><span data-stu-id="ad916-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="ad916-174">Si tratta di una **situazione normale in** \* \* **grassetto**    \*    . \* \*  questo è il corsivo</span><span class="sxs-lookup"><span data-stu-id="ad916-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="ad916-175">Questo è ciò che si troverà negli Appunti (si noti che si tratta dell'interpretazione di IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="ad916-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="ad916-176">Versione: 0.9</span><span class="sxs-lookup"><span data-stu-id="ad916-176">Version:0.9</span></span>

            <span data-ttu-id="ad916-177">StartHTML: 71</span><span class="sxs-lookup"><span data-stu-id="ad916-177">StartHTML:71</span></span>

            <span data-ttu-id="ad916-178">Con dHTML: 160</span><span class="sxs-lookup"><span data-stu-id="ad916-178">EndHTML:160</span></span>

            <span data-ttu-id="ad916-179">StartFragment: 130</span><span class="sxs-lookup"><span data-stu-id="ad916-179">StartFragment:130</span></span>

            <span data-ttu-id="ad916-180">EndFragment: 150</span><span class="sxs-lookup"><span data-stu-id="ad916-180">EndFragment:150</span></span>

            <span data-ttu-id="ad916-181">**StartSelection: 130**</span><span class="sxs-lookup"><span data-stu-id="ad916-181">**StartSelection:130**</span></span>

            <span data-ttu-id="ad916-182">**: 150**</span><span class="sxs-lookup"><span data-stu-id="ad916-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="ad916-183">**<B>grassetto</B><I><B>corsivo</B></I>**</span><span class="sxs-lookup"><span data-stu-id="ad916-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="ad916-184">In questo scenario solo il tag BODY e il tag HTML vengono visualizzati nel contesto, perché precede il frammento selezionato.</span><span class="sxs-lookup"><span data-stu-id="ad916-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="ad916-185">Si noti che i tag di inizio e di fine sono inclusi nel contesto.</span><span class="sxs-lookup"><span data-stu-id="ad916-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="ad916-186">La selezione, come delimitato da StartSelection e l'opzione di visualizzazione, viene visualizzata in grassetto.</span><span class="sxs-lookup"><span data-stu-id="ad916-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="ad916-187">Frammento di una tabella in HTML.</span><span class="sxs-lookup"><span data-stu-id="ad916-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="ad916-188">Testo HTML:</span><span class="sxs-lookup"><span data-stu-id="ad916-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="ad916-189">Head1</span><span class="sxs-lookup"><span data-stu-id="ad916-189">Head1</span></span></TH><TD><span data-ttu-id="ad916-190">Item 1</span><span class="sxs-lookup"><span data-stu-id="ad916-190">Item 1</span></span></TD><TD><span data-ttu-id="ad916-191">Elemento 2</span><span class="sxs-lookup"><span data-stu-id="ad916-191">Item 2</span></span></TD><TD><span data-ttu-id="ad916-192">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-192">Item 3</span></span></TD><TD><span data-ttu-id="ad916-193">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="ad916-194">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-194">Item 5</span></span></TD><TD><span data-ttu-id="ad916-195">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="ad916-195">Item 6</span></span></TD><TD><span data-ttu-id="ad916-196">Elemento 7</span><span class="sxs-lookup"><span data-stu-id="ad916-196">Item 7</span></span></TD><TD><span data-ttu-id="ad916-197">Elemento 8</span><span class="sxs-lookup"><span data-stu-id="ad916-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="ad916-198">Head2</span><span class="sxs-lookup"><span data-stu-id="ad916-198">Head2</span></span></TH><TD><span data-ttu-id="ad916-199">Elemento 9</span><span class="sxs-lookup"><span data-stu-id="ad916-199">Item 9</span></span></TD><TD><span data-ttu-id="ad916-200">Elemento 10</span><span class="sxs-lookup"><span data-stu-id="ad916-200">Item 10</span></span></TD><TD><span data-ttu-id="ad916-201">Elemento 11</span><span class="sxs-lookup"><span data-stu-id="ad916-201">Item 11</span></span></TD><TD><span data-ttu-id="ad916-202">Elemento 12</span><span class="sxs-lookup"><span data-stu-id="ad916-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="ad916-203">Viene visualizzato come: ></span><span class="sxs-lookup"><span data-stu-id="ad916-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="ad916-204">Head1</span><span class="sxs-lookup"><span data-stu-id="ad916-204">Head1</span></span></TH><TD><span data-ttu-id="ad916-205">Item 1</span><span class="sxs-lookup"><span data-stu-id="ad916-205">Item 1</span></span></TD><TD><span data-ttu-id="ad916-206">Elemento 2</span><span class="sxs-lookup"><span data-stu-id="ad916-206">Item 2</span></span></TD><TD><span data-ttu-id="ad916-207">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-207">Item 3</span></span></TD><TD><span data-ttu-id="ad916-208">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="ad916-209">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-209">Item 5</span></span></TD><TD><span data-ttu-id="ad916-210">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="ad916-210">Item 6</span></span></TD><TD><span data-ttu-id="ad916-211">Elemento 7</span><span class="sxs-lookup"><span data-stu-id="ad916-211">Item 7</span></span></TD><TD><span data-ttu-id="ad916-212">Elemento 8</span><span class="sxs-lookup"><span data-stu-id="ad916-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="ad916-213">Head2</span><span class="sxs-lookup"><span data-stu-id="ad916-213">Head2</span></span></TH><TD><span data-ttu-id="ad916-214">Elemento 9</span><span class="sxs-lookup"><span data-stu-id="ad916-214">Item 9</span></span></TD><TD><span data-ttu-id="ad916-215">Elemento 10</span><span class="sxs-lookup"><span data-stu-id="ad916-215">Item 10</span></span></TD><TD><span data-ttu-id="ad916-216">Elemento 11</span><span class="sxs-lookup"><span data-stu-id="ad916-216">Item 11</span></span></TD><TD><span data-ttu-id="ad916-217">Elemento 12</span><span class="sxs-lookup"><span data-stu-id="ad916-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="ad916-218"><. \[ CDATA\[\]\]></span><span class="sxs-lookup"><span data-stu-id="ad916-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="ad916-219">Gli elementi 6, Item7, Item 10 e Item 11 della tabella sono selezionati come blocchi e copiati negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ad916-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="ad916-220">Questo è ciò che si troverà negli Appunti (si noti che si tratta dell'interpretazione di IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="ad916-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="ad916-221">**<TR><TD>Elemento 6 </TD> <TD> elemento 7 elemento </TD> </TR> <TR> <TD> 10 elemento </TD> <TD> 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="ad916-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="ad916-222">Incollare un frammento di un elenco ordinato in testo normale.</span><span class="sxs-lookup"><span data-stu-id="ad916-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="ad916-223">Testo HTML:</span><span class="sxs-lookup"><span data-stu-id="ad916-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="ad916-224">Item 1</span><span class="sxs-lookup"><span data-stu-id="ad916-224">Item 1</span></span><LI><span data-ttu-id="ad916-225">Elemento 2</span><span class="sxs-lookup"><span data-stu-id="ad916-225">Item 2</span></span><LI><span data-ttu-id="ad916-226">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-226">Item 3</span></span><LI><span data-ttu-id="ad916-227">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-227">Item 4</span></span><LI><span data-ttu-id="ad916-228">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-228">Item 5</span></span><LI><span data-ttu-id="ad916-229">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="ad916-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="ad916-230">Viene visualizzato come:</span><span class="sxs-lookup"><span data-stu-id="ad916-230">Appears as:</span></span>
            1.  <span data-ttu-id="ad916-231">Item 1</span><span class="sxs-lookup"><span data-stu-id="ad916-231">Item 1</span></span>
            2.  <span data-ttu-id="ad916-232">Elemento 2</span><span class="sxs-lookup"><span data-stu-id="ad916-232">Item 2</span></span>
            3.  <span data-ttu-id="ad916-233">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-233">Item 3</span></span>
            4.  <span data-ttu-id="ad916-234">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-234">Item 4</span></span>
            5.  <span data-ttu-id="ad916-235">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-235">Item 5</span></span>
            6.  <span data-ttu-id="ad916-236">Elemento 6</span><span class="sxs-lookup"><span data-stu-id="ad916-236">Item 6</span></span>
        -   <span data-ttu-id="ad916-237">L'utente seleziona e copia gli elementi da 3 a 5 negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="ad916-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="ad916-238">Negli Appunti è riportato il codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="ad916-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="ad916-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="ad916-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="ad916-240">**<LI>Elemento 3 <LI> elemento 4 elemento <LI> 5**</span><span class="sxs-lookup"><span data-stu-id="ad916-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="ad916-241">La selezione, come delimitato da StartSelection e l'esposizione, viene visualizzata in grassetto.</span><span class="sxs-lookup"><span data-stu-id="ad916-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="ad916-242">Se questo frammento viene ora incollato in un documento vuoto, verrà creato il codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="ad916-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="ad916-243">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-243">Item 3</span></span><LI><span data-ttu-id="ad916-244">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-244">Item 4</span></span><LI><span data-ttu-id="ad916-245">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="ad916-246">Visualizzato come:</span><span class="sxs-lookup"><span data-stu-id="ad916-246">Appearing as:</span></span>
            1.  <span data-ttu-id="ad916-247">Elemento 3</span><span class="sxs-lookup"><span data-stu-id="ad916-247">Item 3</span></span>
            2.  <span data-ttu-id="ad916-248">Elemento 4</span><span class="sxs-lookup"><span data-stu-id="ad916-248">Item 4</span></span>
            3.  <span data-ttu-id="ad916-249">Elemento 5</span><span class="sxs-lookup"><span data-stu-id="ad916-249">Item 5</span></span>

4.  <span data-ttu-id="ad916-250">Incollare un'area parzialmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="ad916-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="ad916-251">Testo HTML:</span><span class="sxs-lookup"><span data-stu-id="ad916-251">HTML text:</span></span>

            <P> <span data-ttu-id="ad916-252">IE4/MSHTML è un editor WYSIWYG che supporta:</span><span class="sxs-lookup"><span data-stu-id="ad916-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="ad916-253">Taglia</span><span class="sxs-lookup"><span data-stu-id="ad916-253">Cut</span></span><LI><span data-ttu-id="ad916-254">Copia</span><span class="sxs-lookup"><span data-stu-id="ad916-254">Copy</span></span><LI><span data-ttu-id="ad916-255">Incolla</span><span class="sxs-lookup"><span data-stu-id="ad916-255">Paste</span></span></UL><P><span data-ttu-id="ad916-256">Si tratta di uno strumento straordinario.</span><span class="sxs-lookup"><span data-stu-id="ad916-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="ad916-257">Viene visualizzato come: IE4/MSHTML è un editor WYSIWYG che supporta:</span><span class="sxs-lookup"><span data-stu-id="ad916-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="ad916-258">Taglia</span><span class="sxs-lookup"><span data-stu-id="ad916-258">Cut</span></span>
                -   <span data-ttu-id="ad916-259">Copia</span><span class="sxs-lookup"><span data-stu-id="ad916-259">Copy</span></span>
                -   <span data-ttu-id="ad916-260">Incolla</span><span class="sxs-lookup"><span data-stu-id="ad916-260">Paste</span></span>

        -   <span data-ttu-id="ad916-261">L'utente seleziona da "WYSIWYG" fino a "Cop". Negli Appunti è riportato il codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="ad916-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="ad916-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="ad916-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="ad916-263">**Editor WYSIWYG, che supporta**</span><span class="sxs-lookup"><span data-stu-id="ad916-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="ad916-264">**<UL><LI>Taglia <LI> COP**</span><span class="sxs-lookup"><span data-stu-id="ad916-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="ad916-265">L'utente seleziona da "OPY" fino a "Great".</span><span class="sxs-lookup"><span data-stu-id="ad916-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="ad916-266">Negli Appunti è riportato il codice HTML seguente:</span><span class="sxs-lookup"><span data-stu-id="ad916-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="ad916-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="ad916-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="ad916-268">**OPY <LI> incollare </UL> <P> questo è un ottimo**</span><span class="sxs-lookup"><span data-stu-id="ad916-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="ad916-269">La selezione, come delimitato da StartSelection e l'opzione di visualizzazione, viene visualizzata in grassetto.</span><span class="sxs-lookup"><span data-stu-id="ad916-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




