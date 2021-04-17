---
title: Tipi di la di base
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Eseguire la migrazione di pagine Web e applicazioni che si basano su la in SVG o su altri standard ampiamente supportati.
ms.assetid: 07c17e7b-5ac4-4a8d-a468-559307408d5b
keywords:
- Vector Markup Language (la), tipi di base
- LA (Vector Markup Language), tipi di base
- grafica vettoriale, tipi la di base
- Vector Markup Language (la), tipi
- LA (Vector Markup Language), tipi
- grafica vettoriale, tipi la
- tipi di la di base
- tipo Boolean
- tipo di frazione
- tipo ordinata
- tipo lunghezza
- tipo di misura
- tipo di angolo
- tipo di colore
- tipo di carattere
- tipo di bitmap
- Tipo vector
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f05b058c919496b608b875f96e6c03bbeb0d50e8
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104567100"
---
# <a name="basic-vml-types"></a><span data-ttu-id="d30b7-121">Tipi di la di base</span><span class="sxs-lookup"><span data-stu-id="d30b7-121">Basic VML Types</span></span>

<span data-ttu-id="d30b7-122">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d30b7-122">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d30b7-123">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d30b7-123">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d30b7-124">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d30b7-124">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d30b7-125">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-125">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d30b7-126">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d30b7-126">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d30b7-127">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d30b7-127">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d30b7-128">**Contents**</span><span class="sxs-lookup"><span data-stu-id="d30b7-128">**Contents**</span></span>

-   [<span data-ttu-id="d30b7-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d30b7-129">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="d30b7-130">boolean</span><span class="sxs-lookup"><span data-stu-id="d30b7-130">boolean</span></span>](#boolean)
-   [<span data-ttu-id="d30b7-131">frazione</span><span class="sxs-lookup"><span data-stu-id="d30b7-131">fraction</span></span>](#fraction)
-   [<span data-ttu-id="d30b7-132">coordinare</span><span class="sxs-lookup"><span data-stu-id="d30b7-132">ordinate</span></span>](#ordinate)
-   [<span data-ttu-id="d30b7-133">length</span><span class="sxs-lookup"><span data-stu-id="d30b7-133">length</span></span>](#length)
    -   [<span data-ttu-id="d30b7-134">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-134">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="d30b7-135">misura</span><span class="sxs-lookup"><span data-stu-id="d30b7-135">measure</span></span>](#measure)
    -   [<span data-ttu-id="d30b7-136">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-136">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="d30b7-137">angolo</span><span class="sxs-lookup"><span data-stu-id="d30b7-137">angle</span></span>](#angle)
    -   [<span data-ttu-id="d30b7-138">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-138">Alternative representations</span></span>](#alternative-representations)
-   [<span data-ttu-id="d30b7-139">color</span><span class="sxs-lookup"><span data-stu-id="d30b7-139">color</span></span>](#color)
    -   [<span data-ttu-id="d30b7-140">Unità colore</span><span class="sxs-lookup"><span data-stu-id="d30b7-140">Color units</span></span>](#color-units)
    -   [<span data-ttu-id="d30b7-141">Colori HTML</span><span class="sxs-lookup"><span data-stu-id="d30b7-141">HTML colors</span></span>](#html-colors)
    -   [<span data-ttu-id="d30b7-142">Colori dello schema</span><span class="sxs-lookup"><span data-stu-id="d30b7-142">Scheme colors</span></span>](#scheme-colors)
    -   [<span data-ttu-id="d30b7-143">Colori di sistema</span><span class="sxs-lookup"><span data-stu-id="d30b7-143">System colors</span></span>](#system-colors)
    -   [<span data-ttu-id="d30b7-144">Colori puri</span><span class="sxs-lookup"><span data-stu-id="d30b7-144">Pure colors</span></span>](#pure-colors)
    -   [<span data-ttu-id="d30b7-145">Regolazioni colori</span><span class="sxs-lookup"><span data-stu-id="d30b7-145">Color adjustments</span></span>](#color-adjustments)
-   [<span data-ttu-id="d30b7-146">carattere</span><span class="sxs-lookup"><span data-stu-id="d30b7-146">font</span></span>](#font)
-   [<span data-ttu-id="d30b7-147">bitmap</span><span class="sxs-lookup"><span data-stu-id="d30b7-147">bitmap</span></span>](#bitmap)
    -   [<span data-ttu-id="d30b7-148">Formati di file immagine</span><span class="sxs-lookup"><span data-stu-id="d30b7-148">Picture file formats</span></span>](#picture-file-formats)
-   [<span data-ttu-id="d30b7-149">vettore</span><span class="sxs-lookup"><span data-stu-id="d30b7-149">vector</span></span>](#vector)

## <a name="introduction"></a><span data-ttu-id="d30b7-150">Introduzione</span><span class="sxs-lookup"><span data-stu-id="d30b7-150">Introduction</span></span>

<span data-ttu-id="d30b7-151">Questa proposta usa un numero ridotto di tipi di base, elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-151">This proposal uses a small number of basic types, listed in the table below.</span></span>



| <span data-ttu-id="d30b7-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="d30b7-152">Type</span></span>                  | <span data-ttu-id="d30b7-153">Elemento</span><span class="sxs-lookup"><span data-stu-id="d30b7-153">Element</span></span>           | <span data-ttu-id="d30b7-154">Rappresentazione fondamentale</span><span class="sxs-lookup"><span data-stu-id="d30b7-154">Fundamental Representation</span></span> | <span data-ttu-id="d30b7-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-155">Description</span></span>                                                                                          |
|-----------------------|-------------------|----------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d30b7-156">boolean</span><span class="sxs-lookup"><span data-stu-id="d30b7-156">boolean</span></span>](#boolean)   |                   | <span data-ttu-id="d30b7-157">1 bit</span><span class="sxs-lookup"><span data-stu-id="d30b7-157">1 bit</span></span>                      | <span data-ttu-id="d30b7-158">Valore booleano: true o false.</span><span class="sxs-lookup"><span data-stu-id="d30b7-158">A boolean value: true or false.</span></span>                                                                      |
| [<span data-ttu-id="d30b7-159">frazione</span><span class="sxs-lookup"><span data-stu-id="d30b7-159">fraction</span></span>](#fraction) |                   | <span data-ttu-id="d30b7-160">numero 2 6</span><span class="sxs-lookup"><span data-stu-id="d30b7-160">number 2 6</span></span>                 | <span data-ttu-id="d30b7-161">Un valore numerico, ridimensionato di 2 6 (65536) e archiviato come intero con segno.</span><span class="sxs-lookup"><span data-stu-id="d30b7-161">A numeric value, scaled by 2 6 (65536) and stored as a signed integer.</span></span>                               |
| [<span data-ttu-id="d30b7-162">coordinare</span><span class="sxs-lookup"><span data-stu-id="d30b7-162">ordinate</span></span>](#ordinate) |                   | <span data-ttu-id="d30b7-163">segno più intero a 30 bit</span><span class="sxs-lookup"><span data-stu-id="d30b7-163">30-bit integer plus sign</span></span>   | <span data-ttu-id="d30b7-164">Parte di una coordinata (ad esempio, in un percorso), i valori definiti da Coord.</span><span class="sxs-lookup"><span data-stu-id="d30b7-164">Part of a coordinate (e.g., in a path ), the values defined by coord.</span></span>                                |
| [<span data-ttu-id="d30b7-165">length</span><span class="sxs-lookup"><span data-stu-id="d30b7-165">length</span></span>](#length)     |                   | [<span data-ttu-id="d30b7-166">UEM</span><span class="sxs-lookup"><span data-stu-id="d30b7-166">EMU</span></span>](#length)             | <span data-ttu-id="d30b7-167">Lunghezza fisica, ad esempio la larghezza di una riga o la dimensione di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d30b7-167">A physical length, such as the width of a line or the size of a font.</span></span>                                |
| [<span data-ttu-id="d30b7-168">misura</span><span class="sxs-lookup"><span data-stu-id="d30b7-168">measure</span></span>](#measure)   |                   | <span data-ttu-id="d30b7-169">EMU o numero 2 6</span><span class="sxs-lookup"><span data-stu-id="d30b7-169">EMU or number 2 6</span></span>          | <span data-ttu-id="d30b7-170">Lunghezza fisica, incluso un numero di pixel del dispositivo o una frazione di un'altra quantità.</span><span class="sxs-lookup"><span data-stu-id="d30b7-170">Either a physical length, including a number of device pixels, or a fraction of some other quantity.</span></span> |
| [<span data-ttu-id="d30b7-171">angolo</span><span class="sxs-lookup"><span data-stu-id="d30b7-171">angle</span></span>](#angle)       |                   | <span data-ttu-id="d30b7-172">gradi 2 6</span><span class="sxs-lookup"><span data-stu-id="d30b7-172">degrees 2 6</span></span>                | <span data-ttu-id="d30b7-173">Angolo; il positivo è in senso orario.</span><span class="sxs-lookup"><span data-stu-id="d30b7-173">An angle; positive is clockwise.</span></span>                                                                     |
| [<span data-ttu-id="d30b7-174">color</span><span class="sxs-lookup"><span data-stu-id="d30b7-174">color</span></span>](#color)       | [<span data-ttu-id="d30b7-175">c</span><span class="sxs-lookup"><span data-stu-id="d30b7-175">c</span></span>](#color)       | <span data-ttu-id="d30b7-176">complex</span><span class="sxs-lookup"><span data-stu-id="d30b7-176">complex</span></span>                    | <span data-ttu-id="d30b7-177">Elemento che consente la derivazione di un colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-177">An element that allows a color to be derived.</span></span>                                                        |
| [<span data-ttu-id="d30b7-178">carattere</span><span class="sxs-lookup"><span data-stu-id="d30b7-178">font</span></span>](#font)         | [<span data-ttu-id="d30b7-179">carattere</span><span class="sxs-lookup"><span data-stu-id="d30b7-179">font</span></span>](#font)     | <span data-ttu-id="d30b7-180">complex</span><span class="sxs-lookup"><span data-stu-id="d30b7-180">complex</span></span>                    | <span data-ttu-id="d30b7-181">Descrizione di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="d30b7-181">A description of a font.</span></span>                                                                             |
| [<span data-ttu-id="d30b7-182">bitmap</span><span class="sxs-lookup"><span data-stu-id="d30b7-182">bitmap</span></span>](#bitmap)     | [<span data-ttu-id="d30b7-183">bitmap</span><span class="sxs-lookup"><span data-stu-id="d30b7-183">bitmap</span></span>](#bitmap) | <span data-ttu-id="d30b7-184">href</span><span class="sxs-lookup"><span data-stu-id="d30b7-184">href</span></span>                       | <span data-ttu-id="d30b7-185">Riferimento a un file di immagine esterno.</span><span class="sxs-lookup"><span data-stu-id="d30b7-185">A reference to an external picture file.</span></span>                                                             |
| [<span data-ttu-id="d30b7-186">vettore</span><span class="sxs-lookup"><span data-stu-id="d30b7-186">vector</span></span>](#vector)     | [<span data-ttu-id="d30b7-187">v</span><span class="sxs-lookup"><span data-stu-id="d30b7-187">v</span></span>](#vector)      | <span data-ttu-id="d30b7-188">complex</span><span class="sxs-lookup"><span data-stu-id="d30b7-188">complex</span></span>                    | <span data-ttu-id="d30b7-189">Descrizione di un percorso vettoriale</span><span class="sxs-lookup"><span data-stu-id="d30b7-189">A description of a vector path</span></span>                                                                       |



 

<span data-ttu-id="d30b7-190">La "rappresentazione fondamentale" è la rappresentazione di precisione più elevata che la proposta richiede un'implementazione conforme per la manutenzione; i dati andranno persi se l'implementazione non è in grado di rappresentare i dati alla precisione richiesta.</span><span class="sxs-lookup"><span data-stu-id="d30b7-190">The "fundamental representation" is the highest precision representation that the proposal requires a conforming implementation to maintain; data will be lost if the implementation is not able to represent the data to the precision required.</span></span> <span data-ttu-id="d30b7-191">I tipi di colore, tipo di carattere e vettore corrispondono agli elementi che a loro volta hanno una struttura, in un certo senso, non sono tipi di base; Tuttavia, è opportuno trattarle come tali in questa proposta.</span><span class="sxs-lookup"><span data-stu-id="d30b7-191">The color, font, and vector types correspond to elements which themselves have structure -- in a sense, they are not basic types; however, it is convenient to treat them as such within this proposal.</span></span>

<span data-ttu-id="d30b7-192">A ogni tipo di base non complesso è associato un elemento con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d30b7-192">Each non-complex basic type has an associated element of the same name.</span></span> <span data-ttu-id="d30b7-193">Questi nomi di elemento sono riservati e non possono essere usati per altri scopi all'interno di estensioni, anche se l'uso si trova all'interno di un elemento di estensione OnView = "Skip".</span><span class="sxs-lookup"><span data-stu-id="d30b7-193">These element names are reserved and may not be used for any other purpose within extensions, even if the use is within an onview="skip" extension element.</span></span> <span data-ttu-id="d30b7-194">Per questo motivo, è possibile che un'implementazione riscontri codice XML sconosciuto per fornire un'archiviazione interna efficiente del codice XML sconosciuto, a condizione che i valori siano racchiusi negli elementi "Type".</span><span class="sxs-lookup"><span data-stu-id="d30b7-194">Because of this, it is possible for an implementation that encounters unknown XML to provide efficient internal storage of the unknown XML as long as the values are enclosed in the "type" elements.</span></span>


```HTML
<new:tag>1.578</new:tag>
<new:tag><v:fraction>1.578</v:fraction></new:tag>
```



<span data-ttu-id="d30b7-195">Nel primo esempio precedente, la stringa "1,578" deve essere archiviata come una sequenza di caratteri (l'implementazione non sa se si tratta di una stringa o di un numero). nel secondo esempio, l'elemento fraction indica che il contenuto è un numero, pertanto può essere convertito nella rappresentazione della frazione con precisione elevata.</span><span class="sxs-lookup"><span data-stu-id="d30b7-195">In the first example above, the string "1.578" must be stored as a sequence of characters (the implementation does not know whether it is a string or a number); in the second example, the fraction element indicates that the content is a number, thus it may be converted to the high precision fraction representation.</span></span>

<span data-ttu-id="d30b7-196">Ai tipi complessi (incluse bitmap) sono associati nomi di elementi utilizzati per delimitare il valore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-196">Complex types (including bitmap) have associated element names that are used to delimit the value.</span></span> <span data-ttu-id="d30b7-197">In questo modo si semplifica l'analisi assicurando che le attività di analisi più complesse siano associate ai tag degli elementi univoci.</span><span class="sxs-lookup"><span data-stu-id="d30b7-197">This simplifies parsing by ensuring that the more complex parsing tasks are associated with unique element tags.</span></span>

<span data-ttu-id="d30b7-198">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-198">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="boolean"></a><span data-ttu-id="d30b7-199">boolean</span><span class="sxs-lookup"><span data-stu-id="d30b7-199">boolean</span></span>


```HTML
boolean
<!entity % boolean "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-200">Un valore booleano è rappresentato come una parola chiave che indica lo stato del flag.</span><span class="sxs-lookup"><span data-stu-id="d30b7-200">A boolean value is represented as a keyword indicating the state of the flag.</span></span> <span data-ttu-id="d30b7-201">Sono definite le parole chiave seguenti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-201">The following keywords are defined.</span></span>



| <span data-ttu-id="d30b7-202">Valore per true</span><span class="sxs-lookup"><span data-stu-id="d30b7-202">Value for true</span></span> | <span data-ttu-id="d30b7-203">Valore per false</span><span class="sxs-lookup"><span data-stu-id="d30b7-203">Value for false</span></span> |
|----------------|-----------------|
| <span data-ttu-id="d30b7-204">true</span><span class="sxs-lookup"><span data-stu-id="d30b7-204">true</span></span>           | <span data-ttu-id="d30b7-205">false</span><span class="sxs-lookup"><span data-stu-id="d30b7-205">false</span></span>           |
| <span data-ttu-id="d30b7-206">sì</span><span class="sxs-lookup"><span data-stu-id="d30b7-206">yes</span></span>            | <span data-ttu-id="d30b7-207">no</span><span class="sxs-lookup"><span data-stu-id="d30b7-207">no</span></span>              |
| <span data-ttu-id="d30b7-208">in</span><span class="sxs-lookup"><span data-stu-id="d30b7-208">on</span></span>             | <span data-ttu-id="d30b7-209">spento</span><span class="sxs-lookup"><span data-stu-id="d30b7-209">off</span></span>             |
| <span data-ttu-id="d30b7-210">u</span><span class="sxs-lookup"><span data-stu-id="d30b7-210">t</span></span>              | <span data-ttu-id="d30b7-211">f</span><span class="sxs-lookup"><span data-stu-id="d30b7-211">f</span></span>               |
| <span data-ttu-id="d30b7-212">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-212">1</span></span>              | <span data-ttu-id="d30b7-213">0</span><span class="sxs-lookup"><span data-stu-id="d30b7-213">0</span></span>               |



 

<span data-ttu-id="d30b7-214">Un'implementazione può scrivere qualsiasi valore e deve riconoscere tutti i valori.</span><span class="sxs-lookup"><span data-stu-id="d30b7-214">An implementation may write any value and must recognize all values.</span></span> <span data-ttu-id="d30b7-215">Un'implementazione è gratuita per modificare i valori da una rappresentazione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="d30b7-215">An implementation is free to change values from one representation to another.</span></span>

<span data-ttu-id="d30b7-216">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-216">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="fraction"></a><span data-ttu-id="d30b7-217">frazione</span><span class="sxs-lookup"><span data-stu-id="d30b7-217">fraction</span></span>


```HTML
fraction
<!entity % fraction "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-218">Tutti i valori numerici, ad esempio i valori di quantità non dimensionabili, all'interno di questa proposta possono essere archiviati come numeri interi scalando i valori di 2 6 (65536).</span><span class="sxs-lookup"><span data-stu-id="d30b7-218">All numeric values (i.e., values of dimensionless quantities) within this proposal can be stored as integers by scaling them by 2  6 (65536).</span></span> <span data-ttu-id="d30b7-219">Un numero può essere specificato in questo formato, con il suffisso f o come numero decimale senza suffisso.</span><span class="sxs-lookup"><span data-stu-id="d30b7-219">A number may be given either in this form, with the suffix f or as a decimal number with no suffix.</span></span> <span data-ttu-id="d30b7-220">Pertanto, gli elementi ipotetici seguenti rappresentano lo stesso valore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-220">Thus, the following hypothetical elements represent the same value.</span></span>


```HTML
<fillwidth>0.25</fillwidth>
<fillwidth>16384f</fillwidth>
```



<span data-ttu-id="d30b7-221">Una quantità con il suffisso f deve essere un numero intero; i numeri frazionari non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-221">A quantity with the f suffix must be a whole number; fractional numbers are not permitted.</span></span> <span data-ttu-id="d30b7-222">Il valore integer risultante deve essere rappresentabile come numero con segno di complemento a 32 bit 2. Pertanto, l'intervallo effettivo della rappresentazione è 32768 (in effetti, minore di 32768 e maggiore o uguale a-32768).</span><span class="sxs-lookup"><span data-stu-id="d30b7-222">The resultant integer must be representable as a 32-bit 2's complement signed number; thus, the effective range of the representation is  32768 (in fact, less than 32768 and greater than or equal to -32768.)</span></span>

<span data-ttu-id="d30b7-223">Un'implementazione conforme è necessaria per mantenere i valori espressi come valori f.</span><span class="sxs-lookup"><span data-stu-id="d30b7-223">A conforming implementation is required to preserve values that are expressed as f values.</span></span> <span data-ttu-id="d30b7-224">I valori rappresentati come numeri decimali possono essere convertiti in un valore f e archiviati in questo modo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-224">Values represented as decimal numbers may be converted to an f value and stored that way.</span></span> <span data-ttu-id="d30b7-225">Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata; Tuttavia, un valore letto da un documento esistente deve essere mantenuto alla precisione originale completa oppure deve essere convertito in un valore f.</span><span class="sxs-lookup"><span data-stu-id="d30b7-225">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an f value.</span></span>

<span data-ttu-id="d30b7-226">Se l'implementazione non è in grado di eseguire questa operazione, è necessario avvisare l'utente che i dati potrebbero andare persi.</span><span class="sxs-lookup"><span data-stu-id="d30b7-226">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="d30b7-227">(È accettabile emettere tale avviso una volta quando vengono rilevati prima i dati generati dall'esterno).</span><span class="sxs-lookup"><span data-stu-id="d30b7-227">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="d30b7-228">Quando un valore decimale viene convertito in formato f, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetico; Tuttavia, un numero intero deve essere convertito esattamente nel formato f.</span><span class="sxs-lookup"><span data-stu-id="d30b7-228">When a decimal value is converted into f format, the implementation may use any arithmetic rounding mode; however, a whole number must be converted to the f format exactly.</span></span> <span data-ttu-id="d30b7-229">È consigliabile che le implementazioni convertano con l'arrotondamento a meno infinito e che la conversione sia sempre esatta.</span><span class="sxs-lookup"><span data-stu-id="d30b7-229">It is recommended that implementations convert by rounding to minus infinity and that the convertion always be exact.</span></span>

<span data-ttu-id="d30b7-230">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-230">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="ordinate"></a><span data-ttu-id="d30b7-231">coordinare</span><span class="sxs-lookup"><span data-stu-id="d30b7-231">ordinate</span></span>


```HTML
ordinate
<!entity % ordinate "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-232">Le unità del sistema di coordinate stabilito da Coord sono di tipo nominale, che viene definito ordinata.</span><span class="sxs-lookup"><span data-stu-id="d30b7-232">The units of the coordinate system established by coord are of some nominal type, which is referred to as ordinate.</span></span> <span data-ttu-id="d30b7-233">Si tratta di una misura di lunghezza, ma viene utilizzata solo in relazione al rettangolo stabilito da Coord.</span><span class="sxs-lookup"><span data-stu-id="d30b7-233">This is a measure of length, but it is only used in relation to the rectangle that coord establishes.</span></span> <span data-ttu-id="d30b7-234">Qualsiasi valore di tipo ordinate verrà ridimensionato in base ai valori *w* e *h* del Coord e al rapporto risultante usato per stabilire una misura reale sul dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="d30b7-234">Any value of type ordinate will be scaled by the *w* and *h* values of the coord and the resulting ratio used to establish a real measurement on the output device.</span></span>

<span data-ttu-id="d30b7-235">Un'implementazione conforme deve essere in grado di gestire valori ordinati fino a 30 bit più segno, ovvero un intero con segno a 31 bit, non un intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d30b7-235">A conforming implementation must be able to handle ordinate values of up to 30 bits plus sign (i.e., a 31-bit signed integer, not a 32-bit signed integer).</span></span> <span data-ttu-id="d30b7-236">Si consiglia, tuttavia, che le implementazioni tentino di produrre coordinate per il percorso e gli elementi simili con circa 16 bit di precisione.</span><span class="sxs-lookup"><span data-stu-id="d30b7-236">It is recommended, however, that implementations attempt to produce coordinates for path and similar elements that have about 16 bits of precision.</span></span> <span data-ttu-id="d30b7-237">In questo modo è possibile ridurre al minimo la possibilità di underflow o overflow in un'implementazione non conforme.</span><span class="sxs-lookup"><span data-stu-id="d30b7-237">This will minimize the chance of either underflow or overflow in a non-conforming implementation.</span></span>

<span data-ttu-id="d30b7-238">i valori delle coordinate sono sempre integrali.</span><span class="sxs-lookup"><span data-stu-id="d30b7-238">ordinate values are always integral.</span></span> <span data-ttu-id="d30b7-239">Un separatore decimale non può essere visualizzato in un valore di tipo ordinata.</span><span class="sxs-lookup"><span data-stu-id="d30b7-239">A decimal point may not appear in a value of type ordinate.</span></span> <span data-ttu-id="d30b7-240">Non è possibile aggiungere identificatori di unità a valori di tipo ordinate.</span><span class="sxs-lookup"><span data-stu-id="d30b7-240">No unit specifiers may be appended to values of type ordinate.</span></span>

<span data-ttu-id="d30b7-241">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-241">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="length"></a><span data-ttu-id="d30b7-242">length</span><span class="sxs-lookup"><span data-stu-id="d30b7-242">length</span></span>


```HTML
length
<!entity % length "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-243">Una lunghezza è una misura reale o, a volte, una misura in pixel del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-243">A length is a real-world measurement or, sometimes, a measurement in device pixels.</span></span> <span data-ttu-id="d30b7-244">È consigliabile evitare l'uso di Device pixel (px) per le implementazioni.</span><span class="sxs-lookup"><span data-stu-id="d30b7-244">It is recommended that implementations avoid the use of device pixels (px).</span></span>

<span data-ttu-id="d30b7-245">Tutti i qualificatori di unità [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) standard sono consentiti su lunghezza.</span><span class="sxs-lookup"><span data-stu-id="d30b7-245">All the standard [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) unit qualifiers are permitted on a length.</span></span> <span data-ttu-id="d30b7-246">Inoltre, è possibile utilizzare il qualificatore Emu.</span><span class="sxs-lookup"><span data-stu-id="d30b7-246">In addition, the qualifier emu may be used.</span></span> <span data-ttu-id="d30b7-247">Questo qualificatore fa riferimento a un'unità, ovvero l'UEM (unità metrica inglese), che è un denominatore comune delle quantità di misura in uso generalizzato nella grafica del computer.</span><span class="sxs-lookup"><span data-stu-id="d30b7-247">This qualifier refers to a unit -- the EMU (English Metric Unit) -- which is a common denominator of the measurement quantities in widespread use in computer graphics.</span></span> <span data-ttu-id="d30b7-248">Il EMU è in <sup>pollici</sup> /914400, ovvero sono presenti 914400 Emu per pollice.</span><span class="sxs-lookup"><span data-stu-id="d30b7-248">The EMU is <sup>inch</sup> / 914400, i.e., there are 914400 EMU per inch.</span></span> <span data-ttu-id="d30b7-249">La tabella seguente elenca il numero di emù in un numero ridotto di unità rilevate di frequente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-249">The following table lists the number of EMUs in a small number of commonly encountered units.</span></span>



| <span data-ttu-id="d30b7-250">Numero di emù</span><span class="sxs-lookup"><span data-stu-id="d30b7-250">Number of EMUs</span></span> | <span data-ttu-id="d30b7-251">Numero per pollice</span><span class="sxs-lookup"><span data-stu-id="d30b7-251">Number per Inch</span></span> | <span data-ttu-id="d30b7-252">Numero per millimetro</span><span class="sxs-lookup"><span data-stu-id="d30b7-252">Number per Millimeter</span></span> | <span data-ttu-id="d30b7-253">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-253">Description</span></span>             |
|----------------|-----------------|-----------------------|-------------------------|
| <span data-ttu-id="d30b7-254">360</span><span class="sxs-lookup"><span data-stu-id="d30b7-254">360</span></span>            |                 | <span data-ttu-id="d30b7-255">0.01</span><span class="sxs-lookup"><span data-stu-id="d30b7-255">0.01</span></span>                  | <span data-ttu-id="d30b7-256">HIMETRIC Win32</span><span class="sxs-lookup"><span data-stu-id="d30b7-256">Win32 HIMETRIC</span></span>          |
| <span data-ttu-id="d30b7-257">12700</span><span class="sxs-lookup"><span data-stu-id="d30b7-257">12700</span></span>          | <span data-ttu-id="d30b7-258">72</span><span class="sxs-lookup"><span data-stu-id="d30b7-258">72</span></span>              |                       | <span data-ttu-id="d30b7-259">punto</span><span class="sxs-lookup"><span data-stu-id="d30b7-259">"point"</span></span>                 |
| <span data-ttu-id="d30b7-260">635</span><span class="sxs-lookup"><span data-stu-id="d30b7-260">635</span></span>            | <span data-ttu-id="d30b7-261">1440</span><span class="sxs-lookup"><span data-stu-id="d30b7-261">1440</span></span>            |                       | <span data-ttu-id="d30b7-262">TWIP Win32</span><span class="sxs-lookup"><span data-stu-id="d30b7-262">Win32 TWIP</span></span>              |
| <span data-ttu-id="d30b7-263">762</span><span class="sxs-lookup"><span data-stu-id="d30b7-263">762</span></span>            | <span data-ttu-id="d30b7-264">1200</span><span class="sxs-lookup"><span data-stu-id="d30b7-264">1200</span></span>            |                       | <span data-ttu-id="d30b7-265">Stampante ad alta risoluzione</span><span class="sxs-lookup"><span data-stu-id="d30b7-265">High-resolution printer</span></span> |



 

<span data-ttu-id="d30b7-266">I numeri frazionari di emù non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-266">Fractional numbers of EMUs are not permitted.</span></span> <span data-ttu-id="d30b7-267">Qualsiasi misurazione deve essere rappresentabile come numero integrale con segno a 32 bit di emù, che limita la grandezza di una misurazione a 2348 centimetri, circa 59 metri o 65 iarde.</span><span class="sxs-lookup"><span data-stu-id="d30b7-267">Any measurement must be representable as a 32-bit signed integral number of EMUs -- this limits the magnitude of a measurement to 2348 inches -- about 59 meters or 65 yards.</span></span> <span data-ttu-id="d30b7-268">Poiché le misurazioni si riferiscono sempre alle dimensioni di un rendering in un dispositivo di output di dimensioni di schermo o di pagina nominalmente, saranno sempre comprese nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-268">Because the measurements always refer to the size of a rendering on a nominally screen- or page-sized output device, they will always be within this range.</span></span>

<span data-ttu-id="d30b7-269">Si noti, tuttavia, che la rappresentazione non è appropriata per le misurazioni reali e che dove vengono registrate, ad esempio per registrare le dimensioni reali di un percorso, è necessario usare un'altra rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="d30b7-269">Notice, however, that the representation is inappropriate for real-world measurements and that where these are recorded (for example, to record the real-world size of a path) some other representation must be used.</span></span>

<span data-ttu-id="d30b7-270">Un'implementazione conforme è necessaria per mantenere i valori che sono numeri esatti di emù.</span><span class="sxs-lookup"><span data-stu-id="d30b7-270">A conforming implementation is required to preserve values that are exact numbers of EMUs.</span></span> <span data-ttu-id="d30b7-271">I valori rappresentati in qualsiasi altro modo possono essere convertiti in un valore EMU e archiviati in questo modo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-271">Values represented in any other way may be converted to an EMU value and stored that way.</span></span> <span data-ttu-id="d30b7-272">Un'applicazione è autorizzata a registrare i valori generati internamente in qualsiasi unità appropriata; Tuttavia, un valore letto da un documento esistente deve essere mantenuto alla precisione originale completa oppure deve essere convertito in un valore EMU.</span><span class="sxs-lookup"><span data-stu-id="d30b7-272">An application is permitted to record internally generated values in any appropriate unit; however, a value read in from an existing document must either be maintained to the full original precision or must be converted into an EMU value.</span></span>

<span data-ttu-id="d30b7-273">Se l'implementazione non è in grado di eseguire questa operazione, è necessario avvisare l'utente che i dati potrebbero andare persi.</span><span class="sxs-lookup"><span data-stu-id="d30b7-273">If the implementation is unable to do this, it must warn the user that data may be lost.</span></span> <span data-ttu-id="d30b7-274">(È accettabile emettere tale avviso una volta quando vengono rilevati prima i dati generati dall'esterno).</span><span class="sxs-lookup"><span data-stu-id="d30b7-274">(It is acceptable to issue such a warning once when externally generated data is first encountered.)</span></span>

<span data-ttu-id="d30b7-275">In pratica, le lunghezze fisiche vengono usate per un numero relativamente ridotto di misure in questa proposta.</span><span class="sxs-lookup"><span data-stu-id="d30b7-275">In practice, physical lengths are used for relatively few measurements in this proposal.</span></span> <span data-ttu-id="d30b7-276">I dati che sono in genere più importanti sono i dati del percorso e questo oggetto è codificato nel sistema di coordinate definito, in base alla forma, da Coord.</span><span class="sxs-lookup"><span data-stu-id="d30b7-276">The data which is normally most important is the path data and this is encoded in the coordinate system defined, on a per-shape basis, by coord.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="d30b7-277">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-277">Alternative representations</span></span>

<span data-ttu-id="d30b7-278">Le rappresentazioni di lunghezza standard di HTML sono definite da [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-278">The standard length representations of HTML are defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span></span> <span data-ttu-id="d30b7-279">Le unità relative, ad eccezione del pixel, non sono significative nel contesto in cui le lunghezze vengono utilizzate in questa proposta e non devono essere utilizzate.</span><span class="sxs-lookup"><span data-stu-id="d30b7-279">Relative units, with the exception of the pixel, are not meaningful in the context within which lengths are used in this proposal and must not be used.</span></span> <span data-ttu-id="d30b7-280">Se il documento registra le dimensioni del pixel previste (destinazione), definisce la conversione dei pixel in EMU; in caso contrario, deve essere usato il valore predefinito di 90 dpi definito da [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-280">If the document records the intended (target) pixel size, this defines the translation of pixels into EMU; otherwise, the default of 90 dpi defined by [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#length-units) should be used.</span></span>

<span data-ttu-id="d30b7-281">Fatta eccezione per EMU, qualsiasi valore può essere specificato come frazione decimale.</span><span class="sxs-lookup"><span data-stu-id="d30b7-281">With the exception of emu, any value may be given as a decimal fraction.</span></span> <span data-ttu-id="d30b7-282">Quando un valore decimale viene convertito in EMU, l'implementazione può usare qualsiasi modalità di arrotondamento aritmetica.</span><span class="sxs-lookup"><span data-stu-id="d30b7-282">When a decimal value is converted to EMU, the implementation may use any arithmetic rounding mode.</span></span> <span data-ttu-id="d30b7-283">L'unico modo in cui un'applicazione di creazione può garantire un determinato risultato è specificarlo nell'UEM.</span><span class="sxs-lookup"><span data-stu-id="d30b7-283">(The only way for an authoring application to guarantee a particular result is to specify it in emu.)</span></span>

<span data-ttu-id="d30b7-284">Se non viene specificato alcun identificatore di unità in un valore length, l'implementazione deve presupporre Emu.</span><span class="sxs-lookup"><span data-stu-id="d30b7-284">If no unit specifier is given in a length value, the implementation must assume emu.</span></span>

<span data-ttu-id="d30b7-285">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-285">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="measure"></a><span data-ttu-id="d30b7-286">Misura</span><span class="sxs-lookup"><span data-stu-id="d30b7-286">measure</span></span>


```HTML
measure
<!entity % measure "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-287">Una misura è una quantità che può essere una [lunghezza](#length) o una [frazione](#fraction).</span><span class="sxs-lookup"><span data-stu-id="d30b7-287">A measure is a quantity that may be either a [length](#length) or a [fraction](#fraction).</span></span> <span data-ttu-id="d30b7-288">Questo è molto simile alle misure di lunghezza HTML e CSS, che in molti casi possono essere misurazioni fisiche o percentuali di altre quantità.</span><span class="sxs-lookup"><span data-stu-id="d30b7-288">This closely resembles the HTML and CSS length measurements, which can, in many cases, either be physical measurements or percentages of some other quantity.</span></span> <span data-ttu-id="d30b7-289">Se non viene specificato alcun identificatore di unità, il valore deve essere una frazione decimale (pertanto, questo comportamento viene ereditato dalla frazione, non dalla lunghezza).</span><span class="sxs-lookup"><span data-stu-id="d30b7-289">If no unit specifier is given, the value must be assumed to be a decimal fraction (thus, this behavior is inherited from fraction, not from length.)</span></span>

<span data-ttu-id="d30b7-290">A differenza della lunghezza, un valore in pixel ha un significato definito dal contesto, quindi la conversione in Emu non è normalmente appropriata.</span><span class="sxs-lookup"><span data-stu-id="d30b7-290">Unlike length, a pixel value has a context-defined meaning, so conversion to emu is normally inappropriate.</span></span> <span data-ttu-id="d30b7-291">Esistono tre possibili rappresentazioni fondamentali che l'implementazione deve gestire (ovvero una rappresentazione non può essere convertita in un'altra senza perdita di informazioni).</span><span class="sxs-lookup"><span data-stu-id="d30b7-291">There are three possible fundamental representations that the implementation must maintain (i.e., one representation cannot be converted into another without loss of information).</span></span>

1.  <span data-ttu-id="d30b7-292">Un valore frazionario deve essere mantenuto nel formato della [frazione](#fraction) (valore "f").</span><span class="sxs-lookup"><span data-stu-id="d30b7-292">A fractional value should be maintained in the [fraction](#fraction) format (an " f " value).</span></span>
2.  <span data-ttu-id="d30b7-293">È necessario mantenere una lunghezza fisica nell'UEM.</span><span class="sxs-lookup"><span data-stu-id="d30b7-293">A physical length should be maintained in EMU.</span></span>
3.  <span data-ttu-id="d30b7-294">Il valore di un pixel deve essere mantenuto come un numero intero di pixel.</span><span class="sxs-lookup"><span data-stu-id="d30b7-294">A pixel value should be maintained as a whole number of pixels.</span></span>

<span data-ttu-id="d30b7-295">Non sono consentiti numeri frazionari di pixel.</span><span class="sxs-lookup"><span data-stu-id="d30b7-295">Fractional numbers of pixels are not permitted.</span></span>

### <a name="alternative-representations"></a><span data-ttu-id="d30b7-296">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-296">Alternative representations</span></span>

<span data-ttu-id="d30b7-297">Sono consentite tutte le rappresentazioni alternative della [frazione](#fraction) e della [lunghezza](#length) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-297">All the alternate representations of both [fraction](#fraction) and [length](#length) are permitted.</span></span>

<span data-ttu-id="d30b7-298">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-298">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="angle"></a><span data-ttu-id="d30b7-299">angle</span><span class="sxs-lookup"><span data-stu-id="d30b7-299">angle</span></span>


```HTML
angle
<!entity % angle "#pcdata" -- or nmtoken in an attribute -- >
```



<span data-ttu-id="d30b7-300">La rappresentazione fondamentale di un angolo è un numero di gradi multipli di 2 6 (65536) e archiviati come Integer.</span><span class="sxs-lookup"><span data-stu-id="d30b7-300">The fundamental representation of an angle is a number of degrees multipled by 2 6 (65536) and stored as an integer.</span></span> <span data-ttu-id="d30b7-301">Poiché lo spazio delle coordinate viene invertito (l'asse y positivo è inattivo), un angolo in senso orario è positivo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-301">Because the coordinate space is inverted (positive y axis is down), a clockwise angle is positive.</span></span> <span data-ttu-id="d30b7-302">Un'implementazione conforme è necessaria per mantenere la precisione completa di tale valore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-302">A conforming implementation is required to preserve the full precision of such a value.</span></span>

<span data-ttu-id="d30b7-303">Un'implementazione può usare qualsiasi intervallo per gli angoli ed è consentito normalizzare un angolo, ad esempio da-180 a + 180 o da 0 a 360.</span><span class="sxs-lookup"><span data-stu-id="d30b7-303">An implementation is permitted to use any range for angles and is permitted to normalise an angle (for example to -180  to +180  or 0 to 360 ).</span></span> <span data-ttu-id="d30b7-304">Non è necessario che le implementazioni siano coerenti. Tuttavia, la rappresentazione integrale di un angolo non deve superare l'intervallo di un intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="d30b7-304">Implementations are not required to be consistent; however, the integral representation of an angle must not exceed the range of a 32-bit signed integer.</span></span>

<span data-ttu-id="d30b7-305">Il suffisso FD viene usato per identificare la rappresentazione di un angolo (grado frazionario).</span><span class="sxs-lookup"><span data-stu-id="d30b7-305">The suffix fd is used to identify this representation of an angle (fractional degree).</span></span> <span data-ttu-id="d30b7-306">Si noti che questo si distingue dal suffisso f per una frazione con dimensione, sebbene sia possibile usarlo per supportare un'aritmetica identica.</span><span class="sxs-lookup"><span data-stu-id="d30b7-306">Notice that this is distinguished from the f suffix for a dimensionless fraction although identical arithmetic can be used to support it.</span></span> <span data-ttu-id="d30b7-307">Il valore predefinito per un valore angolare è il grado semplice, ovvero un valore non scalato.</span><span class="sxs-lookup"><span data-stu-id="d30b7-307">The default for an angular value is simple degrees, i.e., an unscaled value.</span></span> <span data-ttu-id="d30b7-308">Questa operazione può anche essere segnalata con il suffisso "" (simbolo del grado); Tuttavia, l'uso di questa operazione dipende dalla presenza di una codifica dei documenti adatta, di conseguenza il suffisso deg viene definito anche come valore medio.</span><span class="sxs-lookup"><span data-stu-id="d30b7-308">This may also be signalled with the suffix " " (the degree symbol); however, use of this depends on having a suitable document encoding -- consequently, the suffix deg is also defined to mean degrees.</span></span> <span data-ttu-id="d30b7-309">Il set completo di possibili sufficiente è il seguente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-309">The full set of possible suffices are as follows.</span></span>



| <span data-ttu-id="d30b7-310">Suffisso</span><span class="sxs-lookup"><span data-stu-id="d30b7-310">Suffix</span></span>       | <span data-ttu-id="d30b7-311">Fattore di conversione</span><span class="sxs-lookup"><span data-stu-id="d30b7-311">Conversion Factor</span></span> | <span data-ttu-id="d30b7-312">Commenti</span><span class="sxs-lookup"><span data-stu-id="d30b7-312">Comments</span></span>                               |
|--------------|-------------------|----------------------------------------|
| <span data-ttu-id="d30b7-313">FD</span><span class="sxs-lookup"><span data-stu-id="d30b7-313">fd</span></span>           | <span data-ttu-id="d30b7-314">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-314">1</span></span>                 | <span data-ttu-id="d30b7-315">Rappresentazione interna a precisione elevata</span><span class="sxs-lookup"><span data-stu-id="d30b7-315">High-precision internal representation</span></span> |
| <span data-ttu-id="d30b7-316">nessuno, deg,</span><span class="sxs-lookup"><span data-stu-id="d30b7-316">none, deg,</span></span>   | <span data-ttu-id="d30b7-317">65536</span><span class="sxs-lookup"><span data-stu-id="d30b7-317">65536</span></span>             | <span data-ttu-id="d30b7-318">Degrees</span><span class="sxs-lookup"><span data-stu-id="d30b7-318">Degrees</span></span>                                |
| <span data-ttu-id="d30b7-319">rad</span><span class="sxs-lookup"><span data-stu-id="d30b7-319">rad</span></span>          | <span data-ttu-id="d30b7-320">65536pi/180</span><span class="sxs-lookup"><span data-stu-id="d30b7-320">65536pi/180</span></span>       | <span data-ttu-id="d30b7-321">Radians</span><span class="sxs-lookup"><span data-stu-id="d30b7-321">Radians</span></span>                                |



 

### <a name="alternative-representations"></a><span data-ttu-id="d30b7-322">Rappresentazioni alternative</span><span class="sxs-lookup"><span data-stu-id="d30b7-322">Alternative representations</span></span>

<span data-ttu-id="d30b7-323">La trasformazione ridimensionamento presenta discontinuità a multipli dispari di 45.</span><span class="sxs-lookup"><span data-stu-id="d30b7-323">The scaling transformation has discontinuities at odd multiples of 45 .</span></span> <span data-ttu-id="d30b7-324">È pertanto estremamente importante per la conversione di qualsiasi quantità inesatta per essere ben definita.</span><span class="sxs-lookup"><span data-stu-id="d30b7-324">It is, therefore, extremely important for the conversion of any inexact quantity to be well defined.</span></span> <span data-ttu-id="d30b7-325">Per questo motivo, l'aritmetica della conversione viene definita per essere arrotondata verso meno infinito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-325">For this reason, the arithmetic of conversion is defined to round towards minus infinity.</span></span>

<span data-ttu-id="d30b7-326">Poiché questo potrebbe essere difficile o impossibile da garantire in alcune implementazioni, l'utilizzo dei seguenti elementi viene definito come una funzionalità di livello 3:</span><span class="sxs-lookup"><span data-stu-id="d30b7-326">Because this may be difficult or impossible to guarantee in some implementations, the use of the following is defined to be a level 3 feature:</span></span>

1.  <span data-ttu-id="d30b7-327">Qualsiasi valore del grado frazionario.</span><span class="sxs-lookup"><span data-stu-id="d30b7-327">Any fractional degree value.</span></span>
2.  <span data-ttu-id="d30b7-328">Qualsiasi valore radiante</span><span class="sxs-lookup"><span data-stu-id="d30b7-328">Any radian value</span></span>

<span data-ttu-id="d30b7-329">Pertanto, i valori qualificati FD e i valori integrali non qualificati o i valori integrali qualificati deg o devono essere gestiti esattamente da un'implementazione di livello 0 conforme; non è necessario che altri valori.</span><span class="sxs-lookup"><span data-stu-id="d30b7-329">Thus, values qualified fd and unqualified integral values, or integral values qualified deg or   must be handled exactly by a conforming level 0 implementation; other values need not.</span></span> <span data-ttu-id="d30b7-330">È vivamente consigliabile che qualsiasi implementazione gestisca esattamente la conversione da un valore Degree frazionario a un valore Degree (FD) scalato.</span><span class="sxs-lookup"><span data-stu-id="d30b7-330">It is strongly recommended that any implementation handle the conversion from a fractional degree value to a scaled (fd) degree value exactly.</span></span> <span data-ttu-id="d30b7-331">Questa operazione può essere eseguita senza supporto a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="d30b7-331">This can be done without floating point support.</span></span>

<span data-ttu-id="d30b7-332">I requisiti più esatti per la conversione distinguono FD da f.</span><span class="sxs-lookup"><span data-stu-id="d30b7-332">The more exacting requirements for conversion distinguish fd from f.</span></span>

<span data-ttu-id="d30b7-333">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-333">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="color"></a><span data-ttu-id="d30b7-334">color</span><span class="sxs-lookup"><span data-stu-id="d30b7-334">color</span></span>


```HTML
c
<!element c  %color;>
```



<span data-ttu-id="d30b7-335">I colori sono una parte essenziale della grafica moderna del computer.</span><span class="sxs-lookup"><span data-stu-id="d30b7-335">Colors are an essential part of modern computer graphics.</span></span> <span data-ttu-id="d30b7-336">La proposta usa i metodi stabiliti per specificare i colori fissi.</span><span class="sxs-lookup"><span data-stu-id="d30b7-336">The proposal uses the established methods of specifying fixed colors.</span></span> <span data-ttu-id="d30b7-337">Tuttavia, i colori nei diagrammi sono raramente semplici colori statici; spesso derivano da altri elementi nel diagramma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-337">However, colors in diagrams are rarely simple static colors; they are often derived from other elements in the diagram.</span></span> <span data-ttu-id="d30b7-338">Gran parte di queste informazioni è molto specifica dell'applicazione, pertanto questa proposta fornisce due meccanismi di base per specificare tale comportamento:</span><span class="sxs-lookup"><span data-stu-id="d30b7-338">Much of this information is very application-specific, so this proposal provides two very basic mechanisms to specify such behavior:</span></span>

1.  <span data-ttu-id="d30b7-339">Un colore può derivare da un altro colore nella stessa forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-339">A color may be derived from another color in the same shape.</span></span>
2.  <span data-ttu-id="d30b7-340">Un numero ridotto di operazioni aritmetiche viene definito per la derivazione o la modifica di un colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-340">A small number of arithmetic operations are defined for deriving, or modifying, a color.</span></span>

<span data-ttu-id="d30b7-341">Il meccanismo di forma del prototipo integra questo oggetto consentendo la definizione dei prototipi da cui è possibile ereditare i colori.</span><span class="sxs-lookup"><span data-stu-id="d30b7-341">The prototype shape mechanism supplements this by allow prototypes to be defined from which colors can be inherited.</span></span>


```HTML
color
<!entity % color "( %color-unit; | pure | %color.adjustment; )*">
```



<span data-ttu-id="d30b7-342">Un valore di colore è un superset della [definizione di colore CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-342">A color value is a superset of the [CSS1 color definition](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span> <span data-ttu-id="d30b7-343">Le estensioni consentono di determinare il valore di colore RGB da altri colori all'interno della forma o da una combinazione di colori complessiva definita utilizzando CSS1.</span><span class="sxs-lookup"><span data-stu-id="d30b7-343">The extensions allow the RGB color value to be determined from other colors within the shape or from an overall color scheme defined using CSS1.</span></span>

<span data-ttu-id="d30b7-344">Se il valore di un elemento è definito come un colore, il *contenuto* di un elemento definisce il valore del colore per mezzo di un singolo token di colore modificato facoltativamente da un'operazione aritmetica sul colore RGB corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-344">If the value of an element is defined to be a color, the *content* of an element defines the color value by means of a single color token optionally modified by an arithmetic operation on the corresponding RGB color.</span></span>

<span data-ttu-id="d30b7-345">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-345">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-units"></a><span data-ttu-id="d30b7-346">Unità colore</span><span class="sxs-lookup"><span data-stu-id="d30b7-346">Color units</span></span>

<span data-ttu-id="d30b7-347">Il set completo di token di colore proviene da un'ampia gamma di origini: HTML, CSS1 e questa proposta.</span><span class="sxs-lookup"><span data-stu-id="d30b7-347">The full set of color tokens come from a variety of sources: HTML, CSS1, and this proposal.</span></span> <span data-ttu-id="d30b7-348">Sono definite come segue usando la notazione di [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) o la notazione XPointer definita per il collegamento XML.</span><span class="sxs-lookup"><span data-stu-id="d30b7-348">They are defined as follows using notation from [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1) or the XPointer notation defined for XML linking.</span></span>

<span data-ttu-id="d30b7-349">Nelle definizioni XPointer l'origine del percorso è l'elemento contenente il valore del colore e l'espressione fa riferimento all'intero set di elementi della forma come se tutti gli elementi del prototipo di base fossero stati Uniti con la forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-349">In the XPointer definitions, the location source is the element containing the color value, and the expression refers to the whole element set of the shape as though any base prototype elements had been merged with the shape.</span></span> <span data-ttu-id="d30b7-350">Quando l'elemento corrispondente non esiste, al suo posto viene utilizzato il valore predefinito di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-350">When the corresponding element does not exist, the default value for that element is used in its place.</span></span>



| <span data-ttu-id="d30b7-351">Colore</span><span class="sxs-lookup"><span data-stu-id="d30b7-351">Color</span></span>            | <span data-ttu-id="d30b7-352">Definizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-352">Definition</span></span>                                                                                                  | <span data-ttu-id="d30b7-353">Level</span><span class="sxs-lookup"><span data-stu-id="d30b7-353">Level</span></span> | <span data-ttu-id="d30b7-354">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-354">Description</span></span>                                                                                                                                                               |
|------------------|-------------------------------------------------------------------------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30b7-355">name</span><span class="sxs-lookup"><span data-stu-id="d30b7-355">name</span></span>             | <span data-ttu-id="d30b7-356">Vedere di seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-356">See below</span></span>                                                                                                   | <span data-ttu-id="d30b7-357">0</span><span class="sxs-lookup"><span data-stu-id="d30b7-357">0</span></span>     | <span data-ttu-id="d30b7-358">Nome del colore HTML, come elencato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-358">HTML color name, as listed in the table below.</span></span>                                                                                                                            |
| <span data-ttu-id="d30b7-359">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="d30b7-359">\#rr'gg'bb'</span></span>      | <span data-ttu-id="d30b7-360">\#rr'gg'bb'</span><span class="sxs-lookup"><span data-stu-id="d30b7-360">\#rr'gg'bb'</span></span>                                                                                                 | <span data-ttu-id="d30b7-361">0</span><span class="sxs-lookup"><span data-stu-id="d30b7-361">0</span></span>     | <span data-ttu-id="d30b7-362">Rappresentazione del colore CSS1/sRGB standard con valori compresi nell'intervallo 0.. 255 rappresentati con 2 cifre esadecimali ciascuna.</span><span class="sxs-lookup"><span data-stu-id="d30b7-362">Standard CSS1/sRGB color representation using values in the range 0..255 represented using 2 hexadecimal digits each.</span></span>                                                     |
| <span data-ttu-id="d30b7-363">\#RGB</span><span class="sxs-lookup"><span data-stu-id="d30b7-363">\#rgb</span></span>            | <span data-ttu-id="d30b7-364">\#RRGGBB</span><span class="sxs-lookup"><span data-stu-id="d30b7-364">\#rrggbb</span></span>                                                                                                    | <span data-ttu-id="d30b7-365">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-365">1</span></span>     | <span data-ttu-id="d30b7-366">Formato CSS1 abbreviato con solo tre cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d30b7-366">Shortened CSS1 form with only three hexadecimal digits.</span></span>                                                                                                                   |
| <span data-ttu-id="d30b7-367">RGB (r, g, b)</span><span class="sxs-lookup"><span data-stu-id="d30b7-367">rgb(r,g,b)</span></span>       | <span data-ttu-id="d30b7-368">\#r g b</span><span class="sxs-lookup"><span data-stu-id="d30b7-368">\#(r)(g)(b)</span></span>                                                                                                 | <span data-ttu-id="d30b7-369">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-369">1</span></span>     | <span data-ttu-id="d30b7-370">CSS1 formato RGB; gli elementi del valore RGB vengono convertiti come definito in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-370">CSS1 rgb form; the elements of the rgb value are converted as defined in [CSS1](https://www.w3.org/pub/WWW/TR/REC-CSS1#color-units) .</span></span>                                      |
| <span data-ttu-id="d30b7-371">fill</span><span class="sxs-lookup"><span data-stu-id="d30b7-371">fill</span></span>             | <span data-ttu-id="d30b7-372">predecessore (1, forma)</span><span class="sxs-lookup"><span data-stu-id="d30b7-372">ancestor(1,shape)</span></span><br/> <span data-ttu-id="d30b7-373">figlio (1, riempimento)</span><span class="sxs-lookup"><span data-stu-id="d30b7-373">child(1, fill)</span></span><br/> <span data-ttu-id="d30b7-374">figlio (1, colore)</span><span class="sxs-lookup"><span data-stu-id="d30b7-374">child(1, color)</span></span><br/>                           | <span data-ttu-id="d30b7-375">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-375">1</span></span>     | <span data-ttu-id="d30b7-376">Colore di riempimento in primo piano della forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-376">The foreground fill color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="d30b7-377">fillBack</span><span class="sxs-lookup"><span data-stu-id="d30b7-377">fillBack</span></span>         | <span data-ttu-id="d30b7-378">predecessore (1, forma)</span><span class="sxs-lookup"><span data-stu-id="d30b7-378">ancestor(1,shape)</span></span><br/> <span data-ttu-id="d30b7-379">figlio (1, riempimento)</span><span class="sxs-lookup"><span data-stu-id="d30b7-379">child(1, fill)</span></span><br/> <span data-ttu-id="d30b7-380">figlio (1, indietro)</span><span class="sxs-lookup"><span data-stu-id="d30b7-380">child(1, back)</span></span><br/> <span data-ttu-id="d30b7-381">figlio (1, colore)</span><span class="sxs-lookup"><span data-stu-id="d30b7-381">child(1, color)</span></span><br/> | <span data-ttu-id="d30b7-382">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-382">1</span></span>     | <span data-ttu-id="d30b7-383">Colore di sfondo del riempimento della forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-383">The background color of the shape fill.</span></span>                                                                                                                                   |
| <span data-ttu-id="d30b7-384">line</span><span class="sxs-lookup"><span data-stu-id="d30b7-384">line</span></span>             | <span data-ttu-id="d30b7-385">predecessore (1, forma)</span><span class="sxs-lookup"><span data-stu-id="d30b7-385">ancestor(1,shape)</span></span><br/> <span data-ttu-id="d30b7-386">figlio (1, riga)</span><span class="sxs-lookup"><span data-stu-id="d30b7-386">child(1, line)</span></span><br/> <span data-ttu-id="d30b7-387">figlio (1, colore)</span><span class="sxs-lookup"><span data-stu-id="d30b7-387">child(1, color)</span></span><br/>                           | <span data-ttu-id="d30b7-388">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-388">1</span></span>     | <span data-ttu-id="d30b7-389">Colore della linea di primo piano della forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-389">The foreground line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="d30b7-390">lineBack</span><span class="sxs-lookup"><span data-stu-id="d30b7-390">lineBack</span></span>         | <span data-ttu-id="d30b7-391">predecessore (1, forma)</span><span class="sxs-lookup"><span data-stu-id="d30b7-391">ancestor(1,shape)</span></span><br/> <span data-ttu-id="d30b7-392">figlio (1, riga)</span><span class="sxs-lookup"><span data-stu-id="d30b7-392">child(1, line)</span></span><br/> <span data-ttu-id="d30b7-393">figlio (1, indietro)</span><span class="sxs-lookup"><span data-stu-id="d30b7-393">child(1,back)</span></span> <br/> <span data-ttu-id="d30b7-394">figlio (1, colore)</span><span class="sxs-lookup"><span data-stu-id="d30b7-394">child(1, color)</span></span><br/> | <span data-ttu-id="d30b7-395">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-395">1</span></span>     | <span data-ttu-id="d30b7-396">Colore della linea di sfondo della forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-396">The background line color of the shape.</span></span>                                                                                                                                   |
| <span data-ttu-id="d30b7-397">lineOrFill</span><span class="sxs-lookup"><span data-stu-id="d30b7-397">lineOrFill</span></span>       | <span data-ttu-id="d30b7-398">riga, riempimento</span><span class="sxs-lookup"><span data-stu-id="d30b7-398">line, fill</span></span>                                                                                                  | <span data-ttu-id="d30b7-399">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-399">1</span></span>     | <span data-ttu-id="d30b7-400">Il valore della linea se non è impostato come predefinito; in caso contrario, il valore di riempimento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-400">The line value if not defaulted, otherwise the fill value.</span></span> <span data-ttu-id="d30b7-401">In questo modo viene restituito il colore che si trova al bordo della forma.</span><span class="sxs-lookup"><span data-stu-id="d30b7-401">This effectively returns the color that is at the edge of the shape.</span></span>                                           |
| <span data-ttu-id="d30b7-402">fillThenLine</span><span class="sxs-lookup"><span data-stu-id="d30b7-402">fillThenLine</span></span>     | <span data-ttu-id="d30b7-403">riempimento, riga</span><span class="sxs-lookup"><span data-stu-id="d30b7-403">fill, line</span></span>                                                                                                  | <span data-ttu-id="d30b7-404">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-404">1</span></span>     | <span data-ttu-id="d30b7-405">Il valore di riempimento se non è impostato come predefinito; in caso contrario, il valore della riga.</span><span class="sxs-lookup"><span data-stu-id="d30b7-405">The fill value if not defaulted, otherwise the line value.</span></span> <span data-ttu-id="d30b7-406">In questo modo viene restituito il colore della forma principale (se la forma non è riempita, il risultato sarà il colore della linea).</span><span class="sxs-lookup"><span data-stu-id="d30b7-406">This effectively returns the main shape color (if the shape is unfilled, the result will be the line color).</span></span>   |
| <span data-ttu-id="d30b7-407">shadow</span><span class="sxs-lookup"><span data-stu-id="d30b7-407">shadow</span></span>           | <span data-ttu-id="d30b7-408">predecessore (1, forma)</span><span class="sxs-lookup"><span data-stu-id="d30b7-408">ancestor(1,shape)</span></span><br/> <span data-ttu-id="d30b7-409">figlio (1, ombreggiatura)</span><span class="sxs-lookup"><span data-stu-id="d30b7-409">child(1, shadow)</span></span><br/> <span data-ttu-id="d30b7-410">figlio (1, colore)</span><span class="sxs-lookup"><span data-stu-id="d30b7-410">child(1, color)</span></span><br/>                         | <span data-ttu-id="d30b7-411">2</span><span class="sxs-lookup"><span data-stu-id="d30b7-411">2</span></span>     | <span data-ttu-id="d30b7-412">Il colore dell'ombreggiatura (si tratta di una funzionalità di livello 2).</span><span class="sxs-lookup"><span data-stu-id="d30b7-412">The color of the shadow (this is a level 2 feature).</span></span>                                                                                                                      |
| <span data-ttu-id="d30b7-413">scheme</span><span class="sxs-lookup"><span data-stu-id="d30b7-413">scheme</span></span>           | <span data-ttu-id="d30b7-414">Vedere di seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-414">See below</span></span>                                                                                                   | <span data-ttu-id="d30b7-415">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-415">1</span></span>     | <span data-ttu-id="d30b7-416">Colore dello schema dello schema definito per il documento; vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-416">A scheme color from the scheme defined for the document; see below.</span></span>                                                                                                       |
| <span data-ttu-id="d30b7-417">Schema (*Indice*)</span><span class="sxs-lookup"><span data-stu-id="d30b7-417">scheme(*index*)</span></span>  | <span data-ttu-id="d30b7-418">Vedere di seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-418">See below</span></span>                                                                                                   | <span data-ttu-id="d30b7-419">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-419">1</span></span>     | <span data-ttu-id="d30b7-420">*Indice* dei colori dello schema, a partire da 0; vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-420">Scheme color *index*, starting from 0; see below.</span></span>                                                                                                                         |
| <span data-ttu-id="d30b7-421">this</span><span class="sxs-lookup"><span data-stu-id="d30b7-421">this</span></span>             | <span data-ttu-id="d30b7-422">Implicita</span><span class="sxs-lookup"><span data-stu-id="d30b7-422">Implied</span></span>                                                                                                     | <span data-ttu-id="d30b7-423">2</span><span class="sxs-lookup"><span data-stu-id="d30b7-423">2</span></span>     | <span data-ttu-id="d30b7-424">L'operazione (riempimento di un percorso o disegno) viene definita in un altro modo (ad esempio, come bitmap) e il colore specifica una "modifica" ai colori in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-424">The operation (filling a path, or drawing it) is defined in some other way (for example, as a bitmap), and the color specifies a "modification" to the colors so implied.</span></span> |
| <span data-ttu-id="d30b7-425">tavolozza (*Indice*)</span><span class="sxs-lookup"><span data-stu-id="d30b7-425">palette(*index*)</span></span> | <span data-ttu-id="d30b7-426">Implicita</span><span class="sxs-lookup"><span data-stu-id="d30b7-426">Implied</span></span>                                                                                                     | <span data-ttu-id="d30b7-427">3</span><span class="sxs-lookup"><span data-stu-id="d30b7-427">3</span></span>     | <span data-ttu-id="d30b7-428">Si comporta in modo analogo a, ad eccezione del fatto che viene identificata esattamente una voce in una tabella dei colori bitmap.</span><span class="sxs-lookup"><span data-stu-id="d30b7-428">Behaves in the same way as this, except that exactly one entry in a bitmap color table is identified.</span></span> <span data-ttu-id="d30b7-429">Consentito solo se dichiarato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-429">Permitted only where explicitly stated.</span></span>                             |
| <span data-ttu-id="d30b7-430">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d30b7-430">none</span></span>             | \-                                                                                                          | <span data-ttu-id="d30b7-431">2</span><span class="sxs-lookup"><span data-stu-id="d30b7-431">2</span></span>     | <span data-ttu-id="d30b7-432">Indica l'assenza di un colore. può essere usato per annullare un'operazione di disegno che usa il colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-432">Indicates the absence of a color; may be used to cancel a drawing operation that uses the color.</span></span>                                                                          |
| <span data-ttu-id="d30b7-433">sistema</span><span class="sxs-lookup"><span data-stu-id="d30b7-433">system</span></span>           | <span data-ttu-id="d30b7-434">Vedere di seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-434">See below</span></span>                                                                                                   | <span data-ttu-id="d30b7-435">3</span><span class="sxs-lookup"><span data-stu-id="d30b7-435">3</span></span>     | <span data-ttu-id="d30b7-436">Colore definito dall'interfaccia utente del sistema.</span><span class="sxs-lookup"><span data-stu-id="d30b7-436">A color defined by the system user interface.</span></span>                                                                                                                             |



 

<span data-ttu-id="d30b7-437">Questo colore consente a un valore di colore di specificare una modifica a un colore derivato in altro modo; in particolare, è possibile specificare una singola operazione per tutti i colori di una bitmap.</span><span class="sxs-lookup"><span data-stu-id="d30b7-437">The this color allows a color value to specify a modification to a color which is derived in some other way; in particular, a single operation may be specified for all the colors in a bitmap.</span></span> <span data-ttu-id="d30b7-438">Il colore della tavolozza (*Indice*) identifica una voce specifica in una bitmap mappata alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="d30b7-438">The palette(*index*) color identifies a particular entry in a palette-mapped bitmap.</span></span> <span data-ttu-id="d30b7-439">L'utilizzo di questa proprietà viene definito solo per la registrazione di una voce di tabella dei colori da considerare trasparente in una bitmap di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-439">Use of this is only defined for recording a color table entry that should be regarded as transparent in such a bitmap.</span></span>

<span data-ttu-id="d30b7-440">La definizione di un valore di colore non deve fare riferimento a se stessa, direttamente o indirettamente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-440">The definition of a color value must not refer to itself, either directly or indirectly.</span></span> <span data-ttu-id="d30b7-441">Se viene rilevata una definizione di questo tipo, è consigliabile, ma non obbligatorio, che l'implementazione consideri come nero il valore non definito.</span><span class="sxs-lookup"><span data-stu-id="d30b7-441">If such a definition is encountered, it is recommended, but not required, that the implementation treat the undefined value as black.</span></span>

<span data-ttu-id="d30b7-442">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-442">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="html-colors"></a><span data-ttu-id="d30b7-443">Colori HTML</span><span class="sxs-lookup"><span data-stu-id="d30b7-443">HTML colors</span></span>

<span data-ttu-id="d30b7-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) definisce i seguenti sedici colori:</span><span class="sxs-lookup"><span data-stu-id="d30b7-444">[HTML](https://www.w3.org/TR/wd-html40-970708/types.mdl#type-color) defines the following sixteen color names:</span></span>



<span data-ttu-id="d30b7-445">Nomi dei colori e valori sRGB</span><span class="sxs-lookup"><span data-stu-id="d30b7-445">Color names and sRGB values</span></span>

![Esempio di colore nero.](images/black.gif)

<span data-ttu-id="d30b7-447">Nero = " \# 000000"</span><span class="sxs-lookup"><span data-stu-id="d30b7-447">Black = "\#000000"</span></span>

![Esempio di colore verde.](images/green.gif)

<span data-ttu-id="d30b7-449">Verde = " \# 008000"</span><span class="sxs-lookup"><span data-stu-id="d30b7-449">Green = "\#008000"</span></span>

![Esempio di colore Silver.](images/silver.gif)

<span data-ttu-id="d30b7-451">Silver = " \# C0C0C0"</span><span class="sxs-lookup"><span data-stu-id="d30b7-451">Silver = "\#C0C0C0"</span></span>

![Esempio di colore lime.](images/lime.gif)

<span data-ttu-id="d30b7-453">Lime = " \# 00FF00"</span><span class="sxs-lookup"><span data-stu-id="d30b7-453">Lime = "\#00FF00"</span></span>

![Esempio di colore grigio.](images/gray.gif)

<span data-ttu-id="d30b7-455">Grigio = " \# 808080"</span><span class="sxs-lookup"><span data-stu-id="d30b7-455">Gray = "\#808080"</span></span>

![Esempio di colore oliva.](images/olive.gif)

<span data-ttu-id="d30b7-457">Olive = " \# 808000"</span><span class="sxs-lookup"><span data-stu-id="d30b7-457">Olive = "\#808000"</span></span>

![Esempio di colore bianco.](images/white.gif)

<span data-ttu-id="d30b7-459">Bianco = " \# FFFFFF"</span><span class="sxs-lookup"><span data-stu-id="d30b7-459">White = "\#FFFFFF"</span></span>

![Esempio di colore ywllow.](images/yellow.gif)

<span data-ttu-id="d30b7-461">Yellow = " \# FFFF00"</span><span class="sxs-lookup"><span data-stu-id="d30b7-461">Yellow = "\#FFFF00"</span></span>

![Esempio di colore marrone.](images/maroon.gif)

<span data-ttu-id="d30b7-463">Maroon = " \# 800000"</span><span class="sxs-lookup"><span data-stu-id="d30b7-463">Maroon = "\#800000"</span></span>

![Esempio di colore navy.](images/navy.gif)

<span data-ttu-id="d30b7-465">Navy = " \# 000080"</span><span class="sxs-lookup"><span data-stu-id="d30b7-465">Navy = "\#000080"</span></span>

![Esempio di colore rosso.](images/red.gif)

<span data-ttu-id="d30b7-467">Rosso = " \# FF0000"</span><span class="sxs-lookup"><span data-stu-id="d30b7-467">Red = "\#FF0000"</span></span>

![Esempio di colore blu.](images/blue.gif)

<span data-ttu-id="d30b7-469">Blue = " \# 0000FF"</span><span class="sxs-lookup"><span data-stu-id="d30b7-469">Blue = "\#0000FF"</span></span>

![Esempio di colore viola.](images/purple.gif)

<span data-ttu-id="d30b7-471">Viola = " \# 800080"</span><span class="sxs-lookup"><span data-stu-id="d30b7-471">Purple = "\#800080"</span></span>

![Esempio di colore verde acqua.](images/teal.gif)

<span data-ttu-id="d30b7-473">Verde acqua = " \# 008080"</span><span class="sxs-lookup"><span data-stu-id="d30b7-473">Teal = "\#008080"</span></span>

![Esempio di colore fucsia.](images/fuchsia.gif)

<span data-ttu-id="d30b7-475">Fucsia = " \# FF00FF"</span><span class="sxs-lookup"><span data-stu-id="d30b7-475">Fuchsia = "\#FF00FF"</span></span>

![Esempio di colore Aqua.](images/aqua.gif)

<span data-ttu-id="d30b7-477">Aqua = " \# 00FFFF"</span><span class="sxs-lookup"><span data-stu-id="d30b7-477">Aqua = "\#00FFFF"</span></span>



 

<span data-ttu-id="d30b7-478">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-478">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="scheme-colors"></a><span data-ttu-id="d30b7-479">Colori dello schema</span><span class="sxs-lookup"><span data-stu-id="d30b7-479">Scheme colors</span></span>

<span data-ttu-id="d30b7-480">I colori dello schema a cui fa riferimento lo schema vengono definiti a livello di documento usando il tag meta con un attributo Name di "tema Color Scheme".</span><span class="sxs-lookup"><span data-stu-id="d30b7-480">The scheme colors referenced by scheme are defined at the document level using the meta tag with a name attribute of "Theme Color Scheme".</span></span>


```HTML
<meta name="Theme Color Scheme"
  content="rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb, rrggbb">
```



<span data-ttu-id="d30b7-481">Questo tag consente di definire un massimo di otto colori dello schema.</span><span class="sxs-lookup"><span data-stu-id="d30b7-481">This tag allows up to eight scheme colors to be defined.</span></span> <span data-ttu-id="d30b7-482">I colori non definiti devono essere impostati su nero.</span><span class="sxs-lookup"><span data-stu-id="d30b7-482">Undefined colors should default to black.</span></span> <span data-ttu-id="d30b7-483">I colori dello schema consentono di modificare la combinazione di colori utilizzata per un documento completo semplicemente modificando il contenuto della combinazione di colori del tema.</span><span class="sxs-lookup"><span data-stu-id="d30b7-483">The scheme colors allow the color scheme used for a complete document to be changed just by altering the Theme Color Scheme contents.</span></span> <span data-ttu-id="d30b7-484">Per garantire che la grafica importata da diverse applicazioni di creazione usi coerentemente i colori dello schema, vengono definite le interpretazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-484">To ensure that graphics imported from different authoring applications make consistent use of the scheme colors, the following interpretations are defined.</span></span> <span data-ttu-id="d30b7-485">"Usage" è una breve descrizione dello scopo e la colonna "Description" fornisce dettagli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d30b7-485">The "usage" is a short description of the purpose, and the "description" column provides additional details.</span></span>



| <span data-ttu-id="d30b7-486">Indice</span><span class="sxs-lookup"><span data-stu-id="d30b7-486">Index</span></span> | <span data-ttu-id="d30b7-487">Nome</span><span class="sxs-lookup"><span data-stu-id="d30b7-487">Name</span></span>              | <span data-ttu-id="d30b7-488">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d30b7-488">Usage</span></span>                         | <span data-ttu-id="d30b7-489">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-489">Description</span></span>                                                                                                              |
|-------|-------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30b7-490">0</span><span class="sxs-lookup"><span data-stu-id="d30b7-490">0</span></span>     | <span data-ttu-id="d30b7-491">Schema. sfondo</span><span class="sxs-lookup"><span data-stu-id="d30b7-491">scheme.background</span></span> | <span data-ttu-id="d30b7-492">Sfondo</span><span class="sxs-lookup"><span data-stu-id="d30b7-492">Background</span></span>                    | <span data-ttu-id="d30b7-493">Colore utilizzato per lo sfondo di un elemento grafico (e, di frequente, per la pagina intera).</span><span class="sxs-lookup"><span data-stu-id="d30b7-493">The color used for the background of a graphic (and, frequently, for the whole page).</span></span>                                    |
| <span data-ttu-id="d30b7-494">1</span><span class="sxs-lookup"><span data-stu-id="d30b7-494">1</span></span>     | <span data-ttu-id="d30b7-495">Schema. Text</span><span class="sxs-lookup"><span data-stu-id="d30b7-495">scheme.text</span></span>       | <span data-ttu-id="d30b7-496">Testo e righe</span><span class="sxs-lookup"><span data-stu-id="d30b7-496">Text and lines</span></span>                | <span data-ttu-id="d30b7-497">Colore del testo associato a una forma e al colore della linea standard.</span><span class="sxs-lookup"><span data-stu-id="d30b7-497">The color for text attached to a shape and the standard line color.</span></span>                                                      |
| <span data-ttu-id="d30b7-498">2</span><span class="sxs-lookup"><span data-stu-id="d30b7-498">2</span></span>     | <span data-ttu-id="d30b7-499">Schema. Shadow</span><span class="sxs-lookup"><span data-stu-id="d30b7-499">scheme.shadow</span></span>     | <span data-ttu-id="d30b7-500">Ombreggiature</span><span class="sxs-lookup"><span data-stu-id="d30b7-500">Shadows</span></span>                       | <span data-ttu-id="d30b7-501">Colore ombreggiatura standard: colore usato in genere per le ombreggiature delle forme.</span><span class="sxs-lookup"><span data-stu-id="d30b7-501">Standard shadow color -- the color typically used for shape shadows.</span></span>                                                     |
| <span data-ttu-id="d30b7-502">3</span><span class="sxs-lookup"><span data-stu-id="d30b7-502">3</span></span>     | <span data-ttu-id="d30b7-503">Schema. title</span><span class="sxs-lookup"><span data-stu-id="d30b7-503">scheme.title</span></span>      | <span data-ttu-id="d30b7-504">Testo titolo</span><span class="sxs-lookup"><span data-stu-id="d30b7-504">Title text</span></span>                    | <span data-ttu-id="d30b7-505">Il colore da utilizzare per l'intestazione o il testo del titolo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-505">The color to use for heading or title text.</span></span>                                                                              |
| <span data-ttu-id="d30b7-506">4</span><span class="sxs-lookup"><span data-stu-id="d30b7-506">4</span></span>     | <span data-ttu-id="d30b7-507">Schema. Fill</span><span class="sxs-lookup"><span data-stu-id="d30b7-507">scheme.fill</span></span>       | <span data-ttu-id="d30b7-508">Riempie</span><span class="sxs-lookup"><span data-stu-id="d30b7-508">Fills</span></span>                         | <span data-ttu-id="d30b7-509">Colore di riempimento standard: colore usato in genere per riempire le forme.</span><span class="sxs-lookup"><span data-stu-id="d30b7-509">Standard fill color -- the color typically used to fill shapes.</span></span>                                                          |
| <span data-ttu-id="d30b7-510">5</span><span class="sxs-lookup"><span data-stu-id="d30b7-510">5</span></span>     | <span data-ttu-id="d30b7-511">Schema. accento</span><span class="sxs-lookup"><span data-stu-id="d30b7-511">scheme.accent</span></span>     | <span data-ttu-id="d30b7-512">Accento</span><span class="sxs-lookup"><span data-stu-id="d30b7-512">Accent</span></span>                        | <span data-ttu-id="d30b7-513">Colore "Highlight" normale utilizzato per evidenziare un elemento importante di un elemento grafico.</span><span class="sxs-lookup"><span data-stu-id="d30b7-513">Normal "highlight" color used to emphasis an important element of a graphic.</span></span>                                             |
| <span data-ttu-id="d30b7-514">6</span><span class="sxs-lookup"><span data-stu-id="d30b7-514">6</span></span>     | <span data-ttu-id="d30b7-515">Schema. Hyperlink</span><span class="sxs-lookup"><span data-stu-id="d30b7-515">scheme.hyperlink</span></span>  | <span data-ttu-id="d30b7-516">Accento e collegamento ipertestuale</span><span class="sxs-lookup"><span data-stu-id="d30b7-516">Accent and hyperlink</span></span>          | <span data-ttu-id="d30b7-517">Colore di evidenziazione usato per i collegamenti ipertestuali.</span><span class="sxs-lookup"><span data-stu-id="d30b7-517">Highlight color used for hyperlinks.</span></span> <span data-ttu-id="d30b7-518">Può essere usato per altri scopi in cui il colore denota un collegamento ad altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d30b7-518">May be used for other purposes where the color denotes a link to other information.</span></span> |
| <span data-ttu-id="d30b7-519">7</span><span class="sxs-lookup"><span data-stu-id="d30b7-519">7</span></span>     | <span data-ttu-id="d30b7-520">Schema. seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-520">scheme.followed</span></span>   | <span data-ttu-id="d30b7-521">Accento e collegamento ipertestuale seguito</span><span class="sxs-lookup"><span data-stu-id="d30b7-521">Accent and followed hyperlink</span></span> | <span data-ttu-id="d30b7-522">Colore di evidenziazione per i collegamenti ipertestuali seguiti; appropriato anche per i collegamenti "indietro".</span><span class="sxs-lookup"><span data-stu-id="d30b7-522">Highlight color for followed hyperlinks; also appropriate for "backwards" links.</span></span>                                         |



 

<span data-ttu-id="d30b7-523">È possibile fare riferimento a un colore dello schema in base al nome o all'indice, pertanto schema. Fill e Scheme (4) hanno lo stesso colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-523">A scheme color may be referred to either by name or by index, thus scheme.fill and scheme(4) are the same color.</span></span>

<span data-ttu-id="d30b7-524">I colori dello schema non fanno parte dello schema predefinito se non si specifica un colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-524">Scheme colors do not participate in the defaulting scheme if a color is not specified.</span></span> <span data-ttu-id="d30b7-525">Un colore di riempimento non specificato deve essere sempre interpretato come bianco, indipendentemente dal colore del colore 4 dello schema.</span><span class="sxs-lookup"><span data-stu-id="d30b7-525">An unspecified fill color must always be interpreted as white, regardless of the color of scheme color 4.</span></span> <span data-ttu-id="d30b7-526">I colori "accento" devono essere contrapposti sia allo sfondo (0) sia ai colori di riempimento (4), mentre i colori del testo e del testo del titolo devono avere la stessa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d30b7-526">The "accent" colors should contrast with both the background (0) and the fill (4) colors, and text and title text colors should have the same property.</span></span> <span data-ttu-id="d30b7-527">Una tecnica standard consiste nel fare in modo che gli accenti siano colorati e il testo standard non venga colorato, in genere nero o bianco.</span><span class="sxs-lookup"><span data-stu-id="d30b7-527">One standard technique is to make the accents colored and the standard text uncolored (typically black or white).</span></span>

<span data-ttu-id="d30b7-528">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-528">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="system-colors"></a><span data-ttu-id="d30b7-529">Colori di sistema</span><span class="sxs-lookup"><span data-stu-id="d30b7-529">System colors</span></span>

<span data-ttu-id="d30b7-530">Le applicazioni talvolta registrano i colori in base alle impostazioni del sistema operativo all'interno della grafica.</span><span class="sxs-lookup"><span data-stu-id="d30b7-530">Applications sometimes record colors based on operating system settings within graphics.</span></span> <span data-ttu-id="d30b7-531">Normalmente questi sono temporanei e non devono essere scritti; le definizioni thesystemcolor sono disponibili solo per supportare questo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-531">Normally these are transient and need not be written out; thesystemcolor definitions exist solely to support this.</span></span> <span data-ttu-id="d30b7-532">Un colore di sistema viene introdotto definendo un tag appropriato in un nuovo spazio dei nomi e inserendo le informazioni appropriate nel contenuto dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-532">A system color is introduced by defining an appropriate tag in a new namespace and inserting the appropriate information in the element content.</span></span>

<span data-ttu-id="d30b7-533">Questa proposta definisce un tag di questo tipo per codificare i colori dell'interfaccia utente di Windows definiti nel file di intestazione Winuser. h.</span><span class="sxs-lookup"><span data-stu-id="d30b7-533">This proposal defines such a tag to encode the Windows user interface colors defined in the winuser.h header file.</span></span>


```HTML
win.color
<!element win.color #pcdata>
```



<span data-ttu-id="d30b7-534">Il contenuto dell'elemento è un singolo integer che contiene il valore del colore pertinente \_ definito da winuser. h.</span><span class="sxs-lookup"><span data-stu-id="d30b7-534">The content of the element is a single integer which contains the value of the relevant COLOR\_ define from winuser.h.</span></span> <span data-ttu-id="d30b7-535">È possibile adottare una tecnica simile per qualsiasi specifica di colore del sistema o dell'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="d30b7-535">A similar technique can be adopted for any system- or application-specific color specification.</span></span> <span data-ttu-id="d30b7-536">Si consiglia vivamente di utilizzare questa funzionalità solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-536">It is strongly recommended that this feature be used only for backward compatibility.</span></span>

<span data-ttu-id="d30b7-537">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-537">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="pure-colors"></a><span data-ttu-id="d30b7-538">Colori puri</span><span class="sxs-lookup"><span data-stu-id="d30b7-538">Pure colors</span></span>


```HTML
pure
<!elementpure empty>
```



<span data-ttu-id="d30b7-539">Se l'elemento <pure/> viene visualizzato in un valore di colore, è un suggerimento che il colore non dovrebbe essere approssimato da un modello di dithering.</span><span class="sxs-lookup"><span data-stu-id="d30b7-539">If the element <pure/> appears in a color value, it is a hint that the color should not be approximated by a dither pattern.</span></span> <span data-ttu-id="d30b7-540">Si tratta di una funzionalità di livello 1, che non deve essere rispettata da un'implementazione conforme.</span><span class="sxs-lookup"><span data-stu-id="d30b7-540">This is a level 1 feature, and a conforming implementation need not honor it.</span></span> <span data-ttu-id="d30b7-541">La designazione è importante per i grafici visualizzati sui dispositivi di risoluzione media, ad esempio le visualizzazioni video, in cui le funzionalità di piccole dimensioni (ad esempio le linee) potrebbero causare un alias non valido con i colori dichiarati.</span><span class="sxs-lookup"><span data-stu-id="d30b7-541">The designation is important for graphics displayed on medium-resolution devices, such as video displays, where small features (such as lines) may cause bad aliasing with dithered colors.</span></span> <span data-ttu-id="d30b7-542">Nei dispositivi, ad esempio stampanti, che in genere dipendono da tutti i colori, ad eccezione dei pochi colori completamente saturi, la dithering è in genere sufficiente per evitare questo problema.</span><span class="sxs-lookup"><span data-stu-id="d30b7-542">On devices such as printers, which normally dither all colors except for the few fully saturated colors, the dithering is normally sufficiently fine to avoid this problem.</span></span>

<span data-ttu-id="d30b7-543">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-543">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="color-adjustments"></a><span data-ttu-id="d30b7-544">Regolazioni colori</span><span class="sxs-lookup"><span data-stu-id="d30b7-544">Color adjustments</span></span>

<span data-ttu-id="d30b7-545">Il colore di base può essere regolato da operazioni aritmetiche sul valore RGB.</span><span class="sxs-lookup"><span data-stu-id="d30b7-545">The base color may be adjusted by arithmetic operations on the RGB value.</span></span> <span data-ttu-id="d30b7-546">Queste operazioni vengono definite utilizzando elementi aggiuntivi all'interno del valore del colore.</span><span class="sxs-lookup"><span data-stu-id="d30b7-546">These operations are defined using additional elements within the color value.</span></span> <span data-ttu-id="d30b7-547">Tali modifiche sono utili solo quando vengono applicate a colori derivati da altri elementi.</span><span class="sxs-lookup"><span data-stu-id="d30b7-547">Such adjustments are useful only when applied to colors derived from other elements.</span></span> <span data-ttu-id="d30b7-548">È possibile specificare tale regolazione su un valore di colore fisso. Tuttavia, un'implementazione di può ridurre questo valore al valore RGB corrispondente e archiviarlo anziché l'originale.</span><span class="sxs-lookup"><span data-stu-id="d30b7-548">It is valid to specify such an adjustment on a fixed color value; however, an implementation is permitted to reduce this to the corresponding RGB value and store that instead of the original.</span></span>

<span data-ttu-id="d30b7-549">Tutte le funzionalità di regolazione del colore descritte in questa sezione sono funzionalità di livello 1.</span><span class="sxs-lookup"><span data-stu-id="d30b7-549">All the color adjustment features described in this section are level 1 features.</span></span>


```HTML
color.adjustment
<!entity % color.adjustment  -- change to make to a color --
  "( %color.op; )?, ( %color.adj; )*"
>

color.op
<!entity % color.op          -- arithmetic operation --
  "( darken | lighten | add | subtract | reverseSubtract |
  blackWhite )"
>
<!element   darken           %color.parameter;>
<!element   lighten          %color.parameter;>
<!element   add              %color.parameter;>
<!element   subtract         %color.parameter;>
<!element   reversesubtract  %color.parameter;>
<!element   blackwhite       %color.parameter;>

color.parameter
<!entity % color.parameter  "#pcdata" >

color.adj
<!entity % color.adj          -- additional adjustment to color --
  "invert | invert128 | gray"
>
<!element   invert       empty>
<!element   INVERT128    empty>
<!element   gray         empty>
```



<span data-ttu-id="d30b7-550">Il parametro delle prime sei operazioni è un singolo valore numerico integrale compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="d30b7-550">The parameter of the first six operations is a single integral numeric value in the range 0 to 255.</span></span> <span data-ttu-id="d30b7-551">La regolazione viene eseguita sul valore RGB di 3x8bit come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d30b7-551">The adjustment is performed on the 3x8bit RGB value as follows:</span></span>

1.  <span data-ttu-id="d30b7-552">Se <gray/> si specifica, il valore RGB viene sostituito da yyy, dove y è il valore di luminanza (y) calcolato dal valore sRGB in seguito a ITU-r BT. 709.</span><span class="sxs-lookup"><span data-stu-id="d30b7-552">If <gray/> is specified, the RGB value is replaced by yyy, where y is the luminance (y') value calculated from the sRGB value in following the ITU-r BT.709.</span></span> <span data-ttu-id="d30b7-553">Il calcolo è il seguente:</span><span class="sxs-lookup"><span data-stu-id="d30b7-553">This calculation is:</span></span>
    ```HTML
    y = 0 2125xr + 0 7154xg + 0 0721xb
    ```

    

2.  <span data-ttu-id="d30b7-554">Se viene fornita una modifica di colore. op, ogni componente viene regolato separatamente in base alla tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-554">If a color.op modification is given, each component is separately adjusted according to the table below.</span></span> <span data-ttu-id="d30b7-555">c è il valore del componente e p è il valore Color. Parameter.</span><span class="sxs-lookup"><span data-stu-id="d30b7-555">c is the component value, and p is the color.parameter value.</span></span>

    | <span data-ttu-id="d30b7-556">Operazione</span><span class="sxs-lookup"><span data-stu-id="d30b7-556">Operation</span></span>       | <span data-ttu-id="d30b7-557">Formula</span><span class="sxs-lookup"><span data-stu-id="d30b7-557">Formula</span></span>                            |
    |-----------------|------------------------------------|
    | <span data-ttu-id="d30b7-558">Darken</span><span class="sxs-lookup"><span data-stu-id="d30b7-558">darken</span></span>          | <span data-ttu-id="d30b7-559">c: = CXP/255</span><span class="sxs-lookup"><span data-stu-id="d30b7-559">c := cxp/255</span></span>                       |
    | <span data-ttu-id="d30b7-560">schiarire</span><span class="sxs-lookup"><span data-stu-id="d30b7-560">lighten</span></span>         | <span data-ttu-id="d30b7-561">c: = 255-(255-c) XP/255</span><span class="sxs-lookup"><span data-stu-id="d30b7-561">c := 255 - (255-c)xp/255</span></span>           |
    | <span data-ttu-id="d30b7-562">add</span><span class="sxs-lookup"><span data-stu-id="d30b7-562">add</span></span>             | <span data-ttu-id="d30b7-563">c: = c + p</span><span class="sxs-lookup"><span data-stu-id="d30b7-563">c := c + p</span></span>                         |
    | <span data-ttu-id="d30b7-564">sottrarre</span><span class="sxs-lookup"><span data-stu-id="d30b7-564">subtract</span></span>        | <span data-ttu-id="d30b7-565">c: = c-p</span><span class="sxs-lookup"><span data-stu-id="d30b7-565">c := c - p</span></span>                         |
    | <span data-ttu-id="d30b7-566">reversesubtract</span><span class="sxs-lookup"><span data-stu-id="d30b7-566">reversesubtract</span></span> | <span data-ttu-id="d30b7-567">c: = p-c</span><span class="sxs-lookup"><span data-stu-id="d30b7-567">c := p - c</span></span>                         |
    | <span data-ttu-id="d30b7-568">BlackWhite</span><span class="sxs-lookup"><span data-stu-id="d30b7-568">blackwhite</span></span>      | <span data-ttu-id="d30b7-569">Se c < p thenc: = 0elsec: = 255</span><span class="sxs-lookup"><span data-stu-id="d30b7-569">if c < p thenc := 0elsec := 255</span></span> |

    

     

    <span data-ttu-id="d30b7-570">In ogni caso, se il valore del componente calcolato, c, supera 255, viene utilizzato 255 e se è minore di 0, viene utilizzato 0.</span><span class="sxs-lookup"><span data-stu-id="d30b7-570">In each case, if the calculated component value, c, exceeds 255, then 255 is used, and if it is less than 0, then 0 is used.</span></span>

3.  <span data-ttu-id="d30b7-571">Se <INVERT128/> viene specificato, il valore 128 viene sottratto o aggiunto a ogni componente a seconda che il componente sia minore di 128 o meno.</span><span class="sxs-lookup"><span data-stu-id="d30b7-571">If <INVERT128/> is given, the value 128 is subtracted or added to each component according to whether the component is less than 128 or not.</span></span>
    ```HTML
    if c < 128
        then
       c := c + 128
    else
       c := c - 128
    ```

    

4.  <span data-ttu-id="d30b7-572">Se <invert/> viene specificato, ogni componente viene sostituito da 255 meno il valore del componente.</span><span class="sxs-lookup"><span data-stu-id="d30b7-572">If <invert/> is given, each component is replaced by 255 minus the value of the component.</span></span>
    ```HTML
    c := 255-c
    ```

    

<span data-ttu-id="d30b7-573">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-573">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="font"></a><span data-ttu-id="d30b7-574">carattere</span><span class="sxs-lookup"><span data-stu-id="d30b7-574">font</span></span>


```HTML
font
<!element font any>
<!attlist font 
   style     cdata  #implied>
```



<span data-ttu-id="d30b7-575">Un tipo di carattere viene identificato usando un attributo di stile come definito nella [sezione CSS1 5,2 (proprietà del tipo di carattere)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span><span class="sxs-lookup"><span data-stu-id="d30b7-575">A font is identified using a style attribute as defined in [CSS1 section 5.2 (font properties)](https://www.w3.org/pub/WWW/TR/REC-CSS1#font-properties) .</span></span> <span data-ttu-id="d30b7-576">Il corpo dell'elemento del tipo di carattere è, al momento, non definito, ma può essere usato in futuro per codificare le informazioni standard sui tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="d30b7-576">The body of the font element is, at present, undefined but may be used in the future to encode standard font information.</span></span> <span data-ttu-id="d30b7-577">Le implementazioni iniziali di questa proposta devono mantenere ma non interpretare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="d30b7-577">Initial implementations of this proposal should preserve but not interpret the information.</span></span>

<span data-ttu-id="d30b7-578">È possibile che il supporto verrà aggiunto in futuro per informazioni sui tipi di carattere out-of-line (tipi di carattere scaricabili o risorse dei tipi di carattere condivise).</span><span class="sxs-lookup"><span data-stu-id="d30b7-578">It is conceivable that support will be added in the future for out-of-line font information (downloadable fonts, or shared font resources).</span></span> <span data-ttu-id="d30b7-579">Questa operazione verrà eseguita da un elemento di collegamento XML all'interno del contenuto dell'elemento font, assicurando compatbility precedenti con implementazioni iniziali.</span><span class="sxs-lookup"><span data-stu-id="d30b7-579">This will be done by an XML-link element within the content of the font element, ensuring backward compatbility with initial implementations.</span></span>

<span data-ttu-id="d30b7-580">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-580">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="bitmap"></a><span data-ttu-id="d30b7-581">bitmap</span><span class="sxs-lookup"><span data-stu-id="d30b7-581">bitmap</span></span>


```HTML
bitmap
<!element   bitmap   empty>
<!attlist   bitmap
   XML-link    cdata               #fixed "simple"
   href        cdata               #REQUIRED
   title       cdata               #implied
   behavior    cdata               #implied
   show        (embed|replace|new) #fixed "embed"
   inline      (true|false)        #fixed "true"
   actuate     (auto|user)         #fixed "auto"
>
```



<span data-ttu-id="d30b7-582">L'elemento bitmap consente di includere in un grafico un riferimento a una risorsa immagine out-of-line (normalmente una bitmap).</span><span class="sxs-lookup"><span data-stu-id="d30b7-582">The bitmap element allows a reference to an out-of-line picture resource (normally a bitmap) to be included in a graphic.</span></span>

<span data-ttu-id="d30b7-583">bitmap è una funzionalità di livello 1.</span><span class="sxs-lookup"><span data-stu-id="d30b7-583">bitmap is a level 1 feature.</span></span>

<span data-ttu-id="d30b7-584">L'attributo Behavior può essere usato per indicare il modo in cui la bitmap deve essere gestita da un'applicazione di modifica.</span><span class="sxs-lookup"><span data-stu-id="d30b7-584">The behavior attribute may be used to indicate how the bitmap should be handled by an editing application.</span></span> <span data-ttu-id="d30b7-585">Il valore può essere uno o entrambi i token seguenti.</span><span class="sxs-lookup"><span data-stu-id="d30b7-585">The value may be one or both of the following tokens.</span></span>



| <span data-ttu-id="d30b7-586">token</span><span class="sxs-lookup"><span data-stu-id="d30b7-586">Token</span></span>    | <span data-ttu-id="d30b7-587">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d30b7-587">Description</span></span>                                                                                                                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30b7-588">separato</span><span class="sxs-lookup"><span data-stu-id="d30b7-588">separate</span></span> | <span data-ttu-id="d30b7-589">Contrassegna la bitmap come entità separata, che non deve essere considerata parte integrante del documento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-589">Marks the bitmap as a separate entity, which should not be regarded as an integral part of the document.</span></span> <span data-ttu-id="d30b7-590">La bitmap non deve essere mantenuta nel documento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-590">The bitmap should not be kept with the document.</span></span> <span data-ttu-id="d30b7-591">Se il documento viene copiato, la bitmap non deve essere copiata; Se il documento viene spostato, la bitmap non deve essere spostata.</span><span class="sxs-lookup"><span data-stu-id="d30b7-591">If the document is copied, the bitmap should not be copied; if the document is moved, the bitmap should not be moved with it.</span></span> |
| <span data-ttu-id="d30b7-592">originale</span><span class="sxs-lookup"><span data-stu-id="d30b7-592">original</span></span> | <span data-ttu-id="d30b7-593">L'attributo title identifica il percorso originale della bitmap come URL; in caso contrario, il significato di title non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="d30b7-593">The title attribute identifies the original location of the bitmap as a URL; otherwise, the meaning of title is not specified.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="d30b7-594">Questi valori sono entrambi hint per il comportamento previsto.</span><span class="sxs-lookup"><span data-stu-id="d30b7-594">These values are both hints as to the expected behavior.</span></span> <span data-ttu-id="d30b7-595">L'opzione separato si riferisce al comportamento dei dati a cui viene fatto riferimento da href.</span><span class="sxs-lookup"><span data-stu-id="d30b7-595">The separate option refers to the behavior of the data referred to by href.</span></span> <span data-ttu-id="d30b7-596">Se vengono specificati sia un oggetto separato che un originale, l'applicazione deve ignorare l'URI href e rigenerare la bitmap dai dati originali.</span><span class="sxs-lookup"><span data-stu-id="d30b7-596">If both separate and original are given, the application is expected to disregard the href URI and regenerate the bitmap from the original data.</span></span> <span data-ttu-id="d30b7-597">Se viene specificato solo originale, l'applicazione deve usare l'URI href per trovare la bitmap ma può dare all'utente la possibilità di rigenerarla.</span><span class="sxs-lookup"><span data-stu-id="d30b7-597">If only original is given, the application is expected to use the href URI to find the bitmap but may give the user the option of regenerating it.</span></span>

<span data-ttu-id="d30b7-598">È possibile rendere l'URI href e l'attributo title lo stesso valore (lessicale), che è appropriato se la bitmap a cui viene fatto riferimento non è "archiviata con" il documento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-598">It is valid to make the href URI and the title attribute the same (lexical) value -- this is appropriate if the referenced bitmap is not "stored with" the document.</span></span> <span data-ttu-id="d30b7-599">È previsto (sebbene non necessario) che href venga usato per la copia personalizzata del documento, che può essere eliminato se le forme di riferimento vengono eliminate e tale titolo viene usato per indicare una copia condivisa.</span><span class="sxs-lookup"><span data-stu-id="d30b7-599">It is intended (though not required) that href be used for the document's own copy of the bitmap -- which may be deleted if the referencing shapes are deleted -- and that title be used to indicate a shared copy.</span></span> <span data-ttu-id="d30b7-600">Pertanto, se entrambi contengono lo stesso valore, non esiste alcuna copia specifica del documento.</span><span class="sxs-lookup"><span data-stu-id="d30b7-600">Thus, if both contain the same value there is no document-specific copy.</span></span>

<span data-ttu-id="d30b7-601">Le applicazioni possono ignorare l'hint se non si adatta al modello di archiviazione effettivo dei dati XML.</span><span class="sxs-lookup"><span data-stu-id="d30b7-601">Applications may disregard the hint if it does not fit in with the actual storage model of the XML data.</span></span>

<span data-ttu-id="d30b7-602">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-602">[![back to top](images/top.gif) Back to top](#top)</span></span>

### <a name="picture-file-formats"></a><span data-ttu-id="d30b7-603">Formati di file immagine</span><span class="sxs-lookup"><span data-stu-id="d30b7-603">Picture file formats</span></span>

<span data-ttu-id="d30b7-604">Nel contesto di questa proposta, i dati esterni sono invariabilmente una bitmap o un file usato per produrre una bitmap.</span><span class="sxs-lookup"><span data-stu-id="d30b7-604">Within the context of this proposal, external data is invariably either a bitmap or a file which is used to produce a bitmap.</span></span> <span data-ttu-id="d30b7-605">Al livello di rendering 0, non è necessario supportare alcun formato di bitmap esterno. i percorsi possono essere riempiti solo con colori a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="d30b7-605">At render level 0, no external bitmap format need be supported -- paths may only be filled with solid colors.</span></span> <span data-ttu-id="d30b7-606">Per eseguire il rendering del set completo di riempimenti di livello 1 di rendering, è necessario che le bitmap siano supportate.</span><span class="sxs-lookup"><span data-stu-id="d30b7-606">To render the full set of render level 1 fills, bitmaps need to be supported.</span></span> <span data-ttu-id="d30b7-607">Il livello di rendering 1 include (solo) i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="d30b7-607">Render level 1 includes (only) the following formats:</span></span>

1.  <span data-ttu-id="d30b7-608">JFIF, ad esempio i dati in formato ISO/IEC 10918 incorporati in un file con l'intestazione JFIF (che può essere considerata come un particolare marcatore APP0 dopo il creatore di SOI) e includendo (solo) la gamma di formati JPEG supportati dal codice IJG V6.</span><span class="sxs-lookup"><span data-stu-id="d30b7-608">JFIF, i.e. ISO/IEC 10918 format data embedded within a file with the JFIF header (which may be regarded as a particular APP0 marker after the SOI maker) and including (only) the range of JPEG formats supported by the IJG v6 code.</span></span>
2.  <span data-ttu-id="d30b7-609">PNG, come definito dalla specifica PNG versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="d30b7-609">PNG, as defined by the PNG version 1.0 specification.</span></span>

<span data-ttu-id="d30b7-610">Il livello di rendering 2 include anche il supporto per gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d30b7-610">Render level 2 also includes support for the following:</span></span>

-   <span data-ttu-id="d30b7-611">GIF, come definito dalla specifica GIF pubblicata da CompuServ in 1987 (normalmente denominata "GIF87a").</span><span class="sxs-lookup"><span data-stu-id="d30b7-611">GIF, as defined by the GIF specification published by CompuServ in 1987 (normally referred to as "GIF87a").</span></span> <span data-ttu-id="d30b7-612">GIF89a deve essere anche supportato a questo livello, soggetto alla restrizione che i dati non devono contenere alcun blocco di estensione che debba interpretare per visualizzare la bitmap diversa dal controllo grafico extensionswithouta requisito per l'input dell'utente o un ritardo.</span><span class="sxs-lookup"><span data-stu-id="d30b7-612">GIF89a must also be supported at this level, subject to the restriction that the data must not contain any extension blocks that need interpretation to display the bitmap other than graphics control extensionswithouta requirement for user input or a delay time.</span></span> <span data-ttu-id="d30b7-613">In questo modo è possibile includere i commenti, ma non l'estensione del testo normale.</span><span class="sxs-lookup"><span data-stu-id="d30b7-613">This allows comments to be included, but not the plain text extension.</span></span> <span data-ttu-id="d30b7-614">Un'applicazione può inserire le estensioni dell'applicazione (0x21, 0xFF) ma, usando la terminologia di questa proposta, deve contenere solo la modifica, non il rendering e i dati.</span><span class="sxs-lookup"><span data-stu-id="d30b7-614">An application may insert application (0x21, 0xFF) extensions but, using the terminology of this proposal, these must contain only editing, not rendering, data.</span></span>

<span data-ttu-id="d30b7-615">Tutti gli altri formati di dati usati nel grafico forzano tale grafico ad almeno modificare il livello 3 e possibilmente il livello di rendering 3 (se i dati sono necessari per eseguire il rendering dell'immagine).</span><span class="sxs-lookup"><span data-stu-id="d30b7-615">Any other data format used in the graphic forces that graphic to be at least editing level 3 and possibly rendering level 3 (if the data is necessary to render the graphic).</span></span> <span data-ttu-id="d30b7-616">È consigliabile pubblicare i formati supportati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d30b7-616">An application is encouraged to publish the formats which it supports.</span></span> <span data-ttu-id="d30b7-617">Ad esempio, Microsoft Office supporta i formati aggiuntivi seguenti in modo nativo e può quindi scrivere i dati di modifica in questo formato:</span><span class="sxs-lookup"><span data-stu-id="d30b7-617">For example, Microsoft Office supports the following additional formats natively and may therefore write editing data in this form:</span></span>

1.  <span data-ttu-id="d30b7-618">WMF--metafile Windows (formato Win 3,1)</span><span class="sxs-lookup"><span data-stu-id="d30b7-618">WMF -- Windows metafile (Win 3.1 format)</span></span>
2.  <span data-ttu-id="d30b7-619">EMF--metafile "Enhanced" di Windows (formato Win32)</span><span class="sxs-lookup"><span data-stu-id="d30b7-619">EMF -- Windows "enhanced" metafile (Win32 format)</span></span>
3.  <span data-ttu-id="d30b7-620">PICT--Mac OS file PICT di rinvio (tutte le versioni ma senza record QuickTime o altre estensioni)</span><span class="sxs-lookup"><span data-stu-id="d30b7-620">PICT -- Mac OS QuickDraw PICT file (all versions but with no QuickTime records or other extensions)</span></span>
4.  <span data-ttu-id="d30b7-621">BMP: formato di file bitmap di Windows, formati "OS/2" (BITMAPCORE), BITMAPINFO, BITMAPV4 e BITMAPV5</span><span class="sxs-lookup"><span data-stu-id="d30b7-621">BMP -- Windows bitmap file format, "os/2" (BITMAPCORE), BITMAPINFO, BITMAPV4, and BITMAPV5 formats</span></span>

<span data-ttu-id="d30b7-622">[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)</span><span class="sxs-lookup"><span data-stu-id="d30b7-622">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="vector"></a><span data-ttu-id="d30b7-623">vettore</span><span class="sxs-lookup"><span data-stu-id="d30b7-623">vector</span></span>


```HTML
v
<!element v "( #pcdata | p )*">
```



<span data-ttu-id="d30b7-624">Un percorso grafico vettoriale è codificato come PCDATA.</span><span class="sxs-lookup"><span data-stu-id="d30b7-624">A vector graphic path is encoded as pcdata.</span></span> <span data-ttu-id="d30b7-625">Il contenuto dell'elemento v è misto, contenente una descrizione del percorso vettoriale facoltativamente parametrizzata con gli elementi p.</span><span class="sxs-lookup"><span data-stu-id="d30b7-625">The content of the v element is mixed, containing a vector path description optionally parameterized with p elements.</span></span>

[<span data-ttu-id="d30b7-626">Torna alla panoramica di la</span><span class="sxs-lookup"><span data-stu-id="d30b7-626">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

