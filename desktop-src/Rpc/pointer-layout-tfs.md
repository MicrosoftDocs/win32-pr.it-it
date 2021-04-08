---
title: Layout puntatore
description: Il layout del puntatore descrive i puntatori di una struttura o di una matrice.
ms.assetid: 1a4984c1-97b9-4e95-a17e-851b67fa94a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f26a6639b0c4b56c911be1e688995aaf3fb9d2d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856638"
---
# <a name="pointer-layout"></a><span data-ttu-id="f46bb-103">Layout puntatore</span><span class="sxs-lookup"><span data-stu-id="f46bb-103">Pointer Layout</span></span>

<span data-ttu-id="f46bb-104">Il layout del puntatore descrive i puntatori di una struttura o di una matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-104">Pointer layout describes pointers of a structure or an array.</span></span>

## <a name="pointer_layout"></a><span data-ttu-id="f46bb-105">\_<> layout puntatore</span><span class="sxs-lookup"><span data-stu-id="f46bb-105">pointer\_layout<></span></span>

<span data-ttu-id="f46bb-106">Il \_ layout di un puntatore<> campo è costituito dai caratteri di formato FC \_ PP FC \_ , seguiti da una o più descrizioni del puntatore, come descritto più avanti e termina con un \_ carattere di formato finale FC:</span><span class="sxs-lookup"><span data-stu-id="f46bb-106">A pointer\_layout<> field consists of the format characters FC\_PP FC\_PAD followed by one or more pointer descriptions, as described later, and terminating with an FC\_END format character:</span></span>

``` syntax
FC_PP
FC_PAD
{ pointer_instance_layout<> }*
FC_END
```

<span data-ttu-id="f46bb-107">Il \_ \_ layout di un'istanza del puntatore<> campo è una stringa di formato che descrive una o più istanze di puntatori.</span><span class="sxs-lookup"><span data-stu-id="f46bb-107">A pointer\_instance\_layout<> field is a format string describing single or multiple instances of pointers.</span></span> <span data-ttu-id="f46bb-108">Nei descrittori vengono usati i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f46bb-108">The following fields are used in these descriptors:</span></span>

-   <span data-ttu-id="f46bb-109">offset \_ in \_ memoria</span><span class="sxs-lookup"><span data-stu-id="f46bb-109">offset\_in\_memory</span></span>

    <span data-ttu-id="f46bb-110">Offset con segno sulla posizione in memoria del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-110">The signed offset to the pointer's location in memory.</span></span> <span data-ttu-id="f46bb-111">Per un puntatore che si trova in una struttura, questo offset è un offset negativo rispetto alla fine della struttura (la fine della parte non conforme delle strutture conformi); per le matrici, l'offset è dall'inizio della matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-111">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures); for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="f46bb-112">offset \_ nel \_ buffer</span><span class="sxs-lookup"><span data-stu-id="f46bb-112">offset\_in\_buffer</span></span>

    <span data-ttu-id="f46bb-113">Offset con segno sulla posizione del puntatore nel buffer.</span><span class="sxs-lookup"><span data-stu-id="f46bb-113">The signed offset to the pointer's location in the buffer.</span></span> <span data-ttu-id="f46bb-114">Per un puntatore che si trova in una struttura, questo offset è un offset negativo rispetto alla fine della struttura (la fine della parte non conforme di strutture conformi): per le matrici, l'offset è dall'inizio della matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-114">For a pointer residing in a structure, this offset is a negative offset from the end of the structure (the end of the nonconformant portion of conformant structures): for arrays, the offset is from the beginning of the array.</span></span>

-   <span data-ttu-id="f46bb-115">offset \_ alla \_ matrice</span><span class="sxs-lookup"><span data-stu-id="f46bb-115">offset\_to\_array</span></span>

    <span data-ttu-id="f46bb-116">Offset da una struttura di inclusione alla matrice incorporata di cui vengono gestiti i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f46bb-116">Offset from an enclosing structure to the embedded array whose pointers are being handled.</span></span> <span data-ttu-id="f46bb-117">Per le matrici di primo livello, questo campo sarà sempre zero.</span><span class="sxs-lookup"><span data-stu-id="f46bb-117">For top-level arrays, this field will always be zero.</span></span>

-   <span data-ttu-id="f46bb-118">iterazioni</span><span class="sxs-lookup"><span data-stu-id="f46bb-118">iterations</span></span>

    <span data-ttu-id="f46bb-119">Numero totale di puntatori con lo stesso layout<> descritti.</span><span class="sxs-lookup"><span data-stu-id="f46bb-119">Total number of pointers that have the same layout<> described.</span></span>

-   <span data-ttu-id="f46bb-120">increment</span><span class="sxs-lookup"><span data-stu-id="f46bb-120">increment</span></span>

    <span data-ttu-id="f46bb-121">Incremento tra puntatori successivi durante la ripetizione.</span><span class="sxs-lookup"><span data-stu-id="f46bb-121">Increment between successive pointers during a REPEAT.</span></span>

-   <span data-ttu-id="f46bb-122">numero \_ di \_ puntatori</span><span class="sxs-lookup"><span data-stu-id="f46bb-122">number\_of\_pointers</span></span>

    <span data-ttu-id="f46bb-123">Numero di puntatori diversi in un'istanza di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="f46bb-123">Number of different pointers in a repeat instance.</span></span>

-   <span data-ttu-id="f46bb-124">Descrizione indicatore di misura \_</span><span class="sxs-lookup"><span data-stu-id="f46bb-124">pointer\_description</span></span>

    <span data-ttu-id="f46bb-125">Descrizione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-125">Pointer description.</span></span>

<span data-ttu-id="f46bb-126">Tutti i layout dell'istanza del puntatore utilizzano la seguente istanza a puntatore singolo \_<8>:</span><span class="sxs-lookup"><span data-stu-id="f46bb-126">All pointer instance layouts use the following single pointer\_instance<8>:</span></span>

``` syntax
offset_to_pointer_in_memory<2> 
offset_to_pointer_in_buffer<2> 
pointer_description<4>
```

<span data-ttu-id="f46bb-127">Di seguito sono riportati i descrittori di istanza:</span><span class="sxs-lookup"><span data-stu-id="f46bb-127">The following are instance descriptors:</span></span>

<span data-ttu-id="f46bb-128">**Singola istanza di un puntatore a un tipo semplice:**</span><span class="sxs-lookup"><span data-stu-id="f46bb-128">**Single instance of a pointer to a simple type:**</span></span>

``` syntax
FC_NO_REPEAT FC_PAD 
pointer_instance<8>
```

<span data-ttu-id="f46bb-129">**Puntatore di ripetizione fisso:**</span><span class="sxs-lookup"><span data-stu-id="f46bb-129">**Fixed repeat pointer:**</span></span>

``` syntax
FC_FIXED_REPEAT FC_PAD 
iterations<2> 
increment<2> 
offset_to_array<2> 
number_of_pointers<2>
{ pointer_instance<8> }*
```

<span data-ttu-id="f46bb-130">**Puntatore di ripetizione della variabile:**</span><span class="sxs-lookup"><span data-stu-id="f46bb-130">**Variable repeat pointer:**</span></span>

``` syntax
FC_VARIABLE_REPEAT (FC_FIXED_OFFSET | FC_VARIABLE_OFFSET) 
increment<2> 
offset_to_array<2> 
number_of_pointers<2> 
{ pointer_instance<8> }*
```

<span data-ttu-id="f46bb-131">Per le istanze di ripetizione fissa e di ripetizione del puntatore variabile è presente un set di descrizioni offset e puntatore per ogni puntatore nell'istanza di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="f46bb-131">For fixed repeat and variable repeat pointer instances there is a set of offset and pointer descriptions for each pointer in the repeat instance.</span></span>

## <a name="pointers-layout-design-issues"></a><span data-ttu-id="f46bb-132">Problemi di progettazione del layout dei puntatori</span><span class="sxs-lookup"><span data-stu-id="f46bb-132">Pointers Layout Design Issues</span></span>

<span data-ttu-id="f46bb-133">In questa sezione vengono illustrati i problemi relativi all'elaborazione di strutture conformi e puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="f46bb-133">This section addresses issues related to processing conformant structures and embedded pointers.</span></span> <span data-ttu-id="f46bb-134">Il problema è che il compilatore genera layout di puntatore per strutture e matrici con una certa ridondanza.</span><span class="sxs-lookup"><span data-stu-id="f46bb-134">The issue is that the compiler generates pointer layouts for structures and arrays with some redundancy.</span></span> <span data-ttu-id="f46bb-135">Questa operazione è utile perché le informazioni sono utili e, ad esempio, una struttura conforme può esaminare un layout di puntatore per servire tutti i puntatori dalla struttura e dalla matrice conforme che fanno parte della struttura conforme.</span><span class="sxs-lookup"><span data-stu-id="f46bb-135">This is beneficial, because the information is useful and as such, for example, a conformant structure can walk one pointer layout to service all the pointers from the structure and from the conformant array being part of the conformant structure.</span></span> <span data-ttu-id="f46bb-136">Tuttavia, esistono alcune situazioni incorporate che richiedono al motore di NDR di eseguire ulteriori operazioni per elaborare tutti i layout del puntatore nella sequenza corretta, elaborando ogni puntatore esattamente una volta.</span><span class="sxs-lookup"><span data-stu-id="f46bb-136">However, some embedded situations exist that require the NDR engine to perform additional work to process all the pointer layouts in the proper sequence, processing each pointer exactly once.</span></span>

## <a name="what-the-compiler-generates"></a><span data-ttu-id="f46bb-137">Cosa genera il compilatore</span><span class="sxs-lookup"><span data-stu-id="f46bb-137">What the Compiler Generates</span></span>

<span data-ttu-id="f46bb-138">Ogni oggetto illustrato in questa sezione include puntatori, ad esempio una struttura conforme ha puntatori nella parte della struttura e negli elementi della matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-138">Every object discussed in this section has pointers, so for example, a conformant structure has pointers in the structure part as well as in the array elements.</span></span> <span data-ttu-id="f46bb-139">L'elemento è una struttura semplice con un puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-139">The element is a simple structure with a pointer.</span></span>

1.  <span data-ttu-id="f46bb-140">Struttura conforme, singolo livello</span><span class="sxs-lookup"><span data-stu-id="f46bb-140">Conformant structure, single level</span></span>

    <span data-ttu-id="f46bb-141">Il descrittore conforme ha una parte PP in cui vengono descritti tutti i puntatori, sia dalla struttura che dalla matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-141">The conformant descriptor has a PP part where all the pointers are described, both from the structure and from the array.</span></span> <span data-ttu-id="f46bb-142">L'elenco dei membri ha \_ un FC lungo invece di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-142">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="f46bb-143">Il descrittore della matrice CARRAy contiene elementi tramite l'uso di un oggetto \_ complesso incorporato senza descrittori di puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-143">The CARRAY array descriptor has elements through the use of an embedded\_complex and no pointer descriptors at all.</span></span> <span data-ttu-id="f46bb-144">L'elemento ha ancora il descrittore del puntatore singolo.</span><span class="sxs-lookup"><span data-stu-id="f46bb-144">The element still has its single pointer descriptor.</span></span> <span data-ttu-id="f46bb-145">Il layout del puntatore precede il layout del membro in una struttura conforme e descrittori di struttura semplici.</span><span class="sxs-lookup"><span data-stu-id="f46bb-145">Pointer layout precedes the member layout in a conformant structure and simple structure descriptors.</span></span>

2.  <span data-ttu-id="f46bb-146">Struttura conforme, due o più livelli</span><span class="sxs-lookup"><span data-stu-id="f46bb-146">Conformant structure, two or more levels</span></span>

    <span data-ttu-id="f46bb-147">La descrizione PP contiene puntatori di tutti i livelli.</span><span class="sxs-lookup"><span data-stu-id="f46bb-147">The PP description has pointers from all levels.</span></span> <span data-ttu-id="f46bb-148">Riutilizza la stessa descrizione della matrice della struttura conforme interna.</span><span class="sxs-lookup"><span data-stu-id="f46bb-148">It reuses the same array description as the internal conformant structure.</span></span> <span data-ttu-id="f46bb-149">L'elenco dei membri ha \_ un FC lungo invece di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-149">The member list has FC\_LONG in lieu of a pointer.</span></span> <span data-ttu-id="f46bb-150">Una struttura incorporata passa attraverso l'uso di un complesso incorporato.</span><span class="sxs-lookup"><span data-stu-id="f46bb-150">An embedded structure comes through the use of an embedded complex.</span></span> <span data-ttu-id="f46bb-151">Il descrittore di struttura conforme viene riusato così com'è.</span><span class="sxs-lookup"><span data-stu-id="f46bb-151">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="f46bb-152">Anche le dimensioni della parte piatta della struttura sono state completate, vale a dire che la dimensione della struttura di primo livello includerà le dimensioni flat della struttura incorporata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-152">The size of the flat portion of the structure comes out complete as well, meaning that the top-level structure size would include embedded structure's flat size.</span></span>

3.  <span data-ttu-id="f46bb-153">Struttura complessa, a singolo livello</span><span class="sxs-lookup"><span data-stu-id="f46bb-153">Complex structure, single level</span></span>

    <span data-ttu-id="f46bb-154">I membri del puntatore sono contrassegnati dal \_ puntatore FC.</span><span class="sxs-lookup"><span data-stu-id="f46bb-154">Pointer members are marked by FC\_POINTER.</span></span> <span data-ttu-id="f46bb-155">Il layout del puntatore è semplificato in modo da disporre di un descrittore del puntatore (4 byte) per ogni voce del puntatore FC nell' \_ elenco.</span><span class="sxs-lookup"><span data-stu-id="f46bb-155">Pointer layout is simplified such that there is a pointer descriptor (4 bytes) for each FC\_POINTER entry on the list.</span></span> <span data-ttu-id="f46bb-156">Il layout del puntatore viene camminato in parallelo con una passeggiata del membro, ovvero un \_ puntatore FC causa l'elaborazione della descrizione del puntatore successiva.</span><span class="sxs-lookup"><span data-stu-id="f46bb-156">Pointer layout is walked in parallel with a member walk, that is, an FC\_POINTER causes the next pointer description to be processed.</span></span> <span data-ttu-id="f46bb-157">La matrice CARRAy presenta il layout del puntatore con tutti i descrittori della matrice e quindi l'elemento, tramite l'uso di un complesso incorporato.</span><span class="sxs-lookup"><span data-stu-id="f46bb-157">The CARRAY array has pointer layout with all the descriptors of the array, and then element, through the use of an embedded complex.</span></span> <span data-ttu-id="f46bb-158">Il descrittore dell'elemento viene riutilizzato.</span><span class="sxs-lookup"><span data-stu-id="f46bb-158">The element descriptor is reused.</span></span> <span data-ttu-id="f46bb-159">Le dimensioni della parte piana della struttura vengono completate. in altre parole, le dimensioni flat della struttura di livello superiore includono le dimensioni flat della struttura incorporata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-159">The size of the flat portion of the structure comes out complete; in other words, the top-level structure's flat size includes the embedded structure's flat size.</span></span> <span data-ttu-id="f46bb-160">Il layout del membro precede il layout del puntatore per le strutture complesse.</span><span class="sxs-lookup"><span data-stu-id="f46bb-160">The member layout precedes the pointer layout for complex structures.</span></span>

    <span data-ttu-id="f46bb-161">Di conseguenza, la generazione della descrizione della matrice conforme è diversa a seconda che si tratti di una matrice all'interno di una struttura conforme o all'interno di una struttura complessa.</span><span class="sxs-lookup"><span data-stu-id="f46bb-161">Hence, the conformant array description generation is different depending on whether it is an array inside of a conformant structure or inside a complex structure.</span></span>

4.  <span data-ttu-id="f46bb-162">Struttura complessa, 2 o più livelli, complesso in complesso</span><span class="sxs-lookup"><span data-stu-id="f46bb-162">Complex structure, 2 or more levels, complex in complex</span></span>

    <span data-ttu-id="f46bb-163">La struttura complessa di primo livello presenta i puntatori ai membri, la struttura complessa incorporata presenta i puntatori ai membri.</span><span class="sxs-lookup"><span data-stu-id="f46bb-163">Top-level complex structure has its member pointers, embedded complex structure has its member pointers.</span></span> <span data-ttu-id="f46bb-164">Il descrittore di struttura conforme viene riutilizzato.</span><span class="sxs-lookup"><span data-stu-id="f46bb-164">The conformant structure descriptor is reused.</span></span> <span data-ttu-id="f46bb-165">Il descrittore della matrice dalla parte superiore è la matrice riutilizzata dalla struttura incorporata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-165">The array descriptor from the top is the reused array from the embedded structure.</span></span>

5.  <span data-ttu-id="f46bb-166">Struttura complessa con una struttura conforme incorporata</span><span class="sxs-lookup"><span data-stu-id="f46bb-166">Complex structure with an embedded conformant structure</span></span>

    <span data-ttu-id="f46bb-167">Top = la struttura conforme al livello ha i puntatori dei membri.</span><span class="sxs-lookup"><span data-stu-id="f46bb-167">Top=level conformant structure has its member pointers.</span></span> <span data-ttu-id="f46bb-168">Il descrittore di struttura conforme viene riusato così com'è.</span><span class="sxs-lookup"><span data-stu-id="f46bb-168">The conformant structure descriptor is reused as-is.</span></span> <span data-ttu-id="f46bb-169">Il descrittore della matrice viene riutilizzato dalla struttura conforme incorporata; in altre parole, non ha alcun puntatore al descrittore della matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-169">The array descriptor is reused from the embedded conformant structure; in other words, it does not have any pointers at the array descriptor.</span></span> <span data-ttu-id="f46bb-170">Il descrittore dell'elemento è relativo al puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-170">The element has its pointer descriptor.</span></span>

6.  <span data-ttu-id="f46bb-171">Matrici di strutture con puntatori</span><span class="sxs-lookup"><span data-stu-id="f46bb-171">Arrays of structures with pointers</span></span>

    <span data-ttu-id="f46bb-172">Una matrice di strutture semplici con puntatori viene generata come SMFARRAY o CARRAy a seconda che la matrice sia ridimensionata, ma in entrambi i casi dispone di un layout del puntatore completato ( \_ ripetizione fissa o ripetizione della variabile \_ ).</span><span class="sxs-lookup"><span data-stu-id="f46bb-172">An array of simple structures with pointers is generated as an SMFARRAY or CARRAY depending whether the array is sized, but in both cases it has a pointer layout that is complete (FIXED\_REPEAT or VARIABLE\_REPEAT).</span></span> <span data-ttu-id="f46bb-173">Il layout del puntatore precede il layout del membro.</span><span class="sxs-lookup"><span data-stu-id="f46bb-173">The pointer layout comes before the member layout.</span></span>

    <span data-ttu-id="f46bb-174">Una matrice di strutture complesse con puntatori viene generata come matrice FASULLa \_ , indipendentemente dal fatto che sia fissa o ridimensionata, e in entrambi i casi non disponga di un layout di puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-174">An array of complex structures with pointers is generated as BOGUS\_ARRAY regardless whether it is fixed or sized, and in both cases, does not have any pointer layout.</span></span>

## <a name="what-the-ndr-engine-does"></a><span data-ttu-id="f46bb-175">Funzione del motore di NDR</span><span class="sxs-lookup"><span data-stu-id="f46bb-175">What the NDR Engine Does</span></span>

<span data-ttu-id="f46bb-176">In questa sezione viene descritto il comportamento del motore NDR.</span><span class="sxs-lookup"><span data-stu-id="f46bb-176">This section describes the NDR engine behavior.</span></span>

<span data-ttu-id="f46bb-177">**Passaggio di marshalling**</span><span class="sxs-lookup"><span data-stu-id="f46bb-177">**The marshaling pass**</span></span>

1.  <span data-ttu-id="f46bb-178">Strutture conformi e struttura conforme incorporata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-178">Conformant structures and embedded conformant structure.</span></span>

    <span data-ttu-id="f46bb-179">La struttura di livello superiore si comporta come una struttura a un solo livello.</span><span class="sxs-lookup"><span data-stu-id="f46bb-179">The top-level structure behaves like a single-level structure.</span></span>

2.  <span data-ttu-id="f46bb-180">Struttura complessa incorporata con matrice conforme</span><span class="sxs-lookup"><span data-stu-id="f46bb-180">Embedded complex structure with conformant array</span></span>

    <span data-ttu-id="f46bb-181">Qualsiasi struttura complessa forza la struttura esterna a essere una struttura complessa.</span><span class="sxs-lookup"><span data-stu-id="f46bb-181">Any complex structure forces the outer structure to be a complex structure.</span></span> <span data-ttu-id="f46bb-182">La struttura incorporata non esegue mai il marshalling della relativa matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-182">Embedded structure never marshals its array.</span></span> <span data-ttu-id="f46bb-183">Ogni struttura passa sempre attraverso puntatori incorporati semplicemente effettuando il marshalling dei membri e un membro che sta per essere un \_ puntatore FC.</span><span class="sxs-lookup"><span data-stu-id="f46bb-183">Every structure always goes through embedded pointers by simply marshaling members and a member happening to be an FC\_POINTER.</span></span>

3.  <span data-ttu-id="f46bb-184">Struttura complessa con struttura conforme</span><span class="sxs-lookup"><span data-stu-id="f46bb-184">Complex structure with conformant structure</span></span>

    <span data-ttu-id="f46bb-185">La struttura più in alto conforme incorporata esegue il marshalling della matrice conforme e di tutti i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f46bb-185">The top-most embedded conformant structure marshals the conformant array and all the pointees.</span></span> <span data-ttu-id="f46bb-186">Il motore di mancato recapito non scende mai a strutture conformi annidate più approfondite, se presenti; in questo modo la soluzione viene semplificata perché una struttura conforme è un oggetto foglia per quanto riguarda il marshalling degli oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="f46bb-186">The NDR engine never descends to deeper nested conformant structures if there are any; this simplifies the solution, as a conformant structure is a leaf object as far as the marshaling of embedded objects is concerned.</span></span> <span data-ttu-id="f46bb-187">La struttura complessa di primo livello ignora il marshalling della matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-187">The top-level complex structure skips the array marshaling.</span></span>

<span data-ttu-id="f46bb-188">**Unmarshaling, bufsizing e Free Pass**</span><span class="sxs-lookup"><span data-stu-id="f46bb-188">**Unmarshaling, bufsizing and freeing passes**</span></span>

<span data-ttu-id="f46bb-189">L'unmarshalling è simmetrico al marshalling; la prima operazione eseguita per le strutture complesse consiste nel trovare la posizione dei puntatori nel buffer per mezzo della chiamata alla funzione **NdrComplexStructBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="f46bb-189">Unmarshaling is symmetrical to marshaling; the first operation it performs for complex structures is to find out the pointees' location in the buffer by means of calling the **NdrComplexStructBufferSize** function.</span></span> <span data-ttu-id="f46bb-190">Esegue quindi l'unmarshalling dei puntatori in parallelo, abilitando lo stesso schema per l'unmarshalling dei puntatori correttamente da usare.</span><span class="sxs-lookup"><span data-stu-id="f46bb-190">It then unmarshals pointees in parallel, enabling the same scheme for unmarshaling the pointees correctly to be used.</span></span> <span data-ttu-id="f46bb-191">Non dovrebbero esserci confusione sugli oggetti e le unioni di dimensioni; l'immagine di memoria non deve essere utilizzata per gli oggetti e le unioni di dimensioni, solo per il contenuto del buffer.</span><span class="sxs-lookup"><span data-stu-id="f46bb-191">There should be no confusion about sized objects and unions; the memory image should not be used for sized objects and unions, just for the buffer contents.</span></span>

<span data-ttu-id="f46bb-192">I flag usati per eseguire correttamente il marshalling e l'unmarshalling vengono usati nello stesso modo in bufsizing e liberando per assicurarsi che i puntatori vengano passati esattamente una volta.</span><span class="sxs-lookup"><span data-stu-id="f46bb-192">The flags used to perform marshaling and unmarshaling correctly are used in the same way in bufsizing and freeing to make sure that pointees are walked exactly once.</span></span>

<span data-ttu-id="f46bb-193">**Superamento della sessione**</span><span class="sxs-lookup"><span data-stu-id="f46bb-193">**Endianess pass**</span></span>

<span data-ttu-id="f46bb-194">In primo luogo, il passaggio dell'oggetto è analogo al marshalling e all'unmarshalling; per elaborare strutture complesse sono necessarie due sessioni.</span><span class="sxs-lookup"><span data-stu-id="f46bb-194">At first, the endianess pass is somewhat similar to marshaling/unmarshaling; two passes are required to process complex structures.</span></span> <span data-ttu-id="f46bb-195">Il primo passaggio converte la parte flat e trova la posizione dei puntatori nel buffer in modo analogo a come bufsizing esegue questa operazione per l'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="f46bb-195">First pass converts the flat part and finds the pointees' location in the buffer similar to how bufsizing performs this operation for unmarshaling.</span></span> <span data-ttu-id="f46bb-196">Il secondo passaggio converte quindi i puntatori.</span><span class="sxs-lookup"><span data-stu-id="f46bb-196">The second pass then converts the pointees.</span></span>

<span data-ttu-id="f46bb-197">I passaggi di registrazione variano in modo analogo al seguente: ogni struttura e ogni membro deve essere rientrata fino a quando il membro foglia o l'elemento non è un tipo semplice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-197">Endianess passes differ in the following manner: every structure and every member has to be stepped until the leaf member or element is a simple type.</span></span> <span data-ttu-id="f46bb-198">Questa operazione è diversa dall'unmarshalling; Quando si esegue l'unmarshalling, ad esempio, non è mai necessario elaborare le strutture conformi incorporate in strutture conformi o qualsiasi membro della struttura conforme, a tale proposito.</span><span class="sxs-lookup"><span data-stu-id="f46bb-198">This is different from unmarshaling; in unmarshaling, for example, there is never a need to process conformant structures embedded in conformant structures, or any member of the conformant structure, for that matter.</span></span> <span data-ttu-id="f46bb-199">Un altro problema è rappresentato dal fatto che la conversione non è un'operazione idempotente, di conseguenza il passaggio di unmarshalling può ripetere l'unmarshalling di alcune parti senza danni, mentre la conversione deve essere eseguita in base a un tipo rigorosamente singolo.</span><span class="sxs-lookup"><span data-stu-id="f46bb-199">Another issue is that the conversion is not an idempotent operation—hence the unmarshaling pass could redo unmarshaling of some pieces without harm, while conversion has to be performed on a strictly once-per-any-simple-type basis.</span></span>

<span data-ttu-id="f46bb-200">Di conseguenza, è possibile riepilogare l'algoritmo delle opzioni come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="f46bb-200">Hence, the endianess algorithm can be summarized as the following.</span></span> <span data-ttu-id="f46bb-201">NDR presenta una nozione di struttura conforme di primo livello e un flag per contrassegnare questo, a seconda dei casi.</span><span class="sxs-lookup"><span data-stu-id="f46bb-201">NDR has a notion of the top-level conformant structure and a flag to mark that, as appropriate.</span></span> <span data-ttu-id="f46bb-202">Quando si esegue la prima volta, ad esempio per convertire la parte piatta e ottenere la posizione dei puntatori, questa nozione non verrà usata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-202">When walking the first time, such as to convert the flat portion and to obtain the location of the pointees, this notion would not be used.</span></span> <span data-ttu-id="f46bb-203">Il rapporto di mancato recapito attraverso le parti piane di tutti i livelli di strutture e mai venture nell'elaborazione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-203">NDR would descend through the flat parts of all levels of structures and never venture into pointer processing.</span></span> <span data-ttu-id="f46bb-204">Infine, il rapporto di MANCAto consiste nella conversione flat della matrice al livello superiore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-204">Finally, NDR would flat convert the array at the top-level.</span></span>

<span data-ttu-id="f46bb-205">Quando si esamina la seconda volta, il flag viene usato per contrassegnare il passaggio del puntatore incorporato per evitare di immettere livelli più profondi delle strutture conformi, quindi la struttura più in alto.</span><span class="sxs-lookup"><span data-stu-id="f46bb-205">When walking the second time, the flag would be used to mark the embedded pointer's pass to avoid entering deeper levels of the conformant structures, then the top-most conformant structure.</span></span> <span data-ttu-id="f46bb-206">In questo modo, il flag forza il comportamento comune di marshalling/unmarshalling, che consente di evitare decrescente in livelli più profondi di strutture conformi.</span><span class="sxs-lookup"><span data-stu-id="f46bb-206">In this way, the flag would force the common marshaling/unmarshaling behavior, which is to avoid descending into deeper levels of conformant structures.</span></span>

<span data-ttu-id="f46bb-207">Il secondo passaggio per le strutture complesse con matrici conformi funziona nel modo seguente: le strutture complesse funzionano in modo comune; il che significa che i livelli più profondi non dovrebbero mai esaminare o ignorare le dimensioni conformi o le matrici conformi ed è piuttosto semplice scorrere i membri senza toccare la matrice.</span><span class="sxs-lookup"><span data-stu-id="f46bb-207">The second pass for complex structures with conformant arrays works as follows: the complex structures work the common way; which means deeper levels would never look at or skip their conformant size or their conformant arrays, and would rather simply walk their members without touching the array.</span></span>

<span data-ttu-id="f46bb-208">Per le strutture complesse con strutture conformi, la struttura conforme deve essere in grado di riconoscere se è di primo livello e se si trova in una struttura complessa.</span><span class="sxs-lookup"><span data-stu-id="f46bb-208">For complex structures with conformant structures, the conformant structure must be aware whether it is top level, and whether it is in a complex structure.</span></span> <span data-ttu-id="f46bb-209">La parte piatta della matrice viene elaborata dalla struttura conforme più in alto.</span><span class="sxs-lookup"><span data-stu-id="f46bb-209">The flat portion of the array is processed by the top-most conformant structure.</span></span> <span data-ttu-id="f46bb-210">Al secondo passaggio, la struttura più in alto conforme ignora la parte piatta e passa attraverso il layout del puntatore e restituisce il risultato.</span><span class="sxs-lookup"><span data-stu-id="f46bb-210">On the second pass, the top-most conformant structure would skip the flat portion and go through the pointer layout and return.</span></span> <span data-ttu-id="f46bb-211">La struttura più alta più complessa ignora la parte piatta e ignora anche il layout del puntatore.</span><span class="sxs-lookup"><span data-stu-id="f46bb-211">The top-most complex structure would skip its flat portion, and would also skip the pointer layout.</span></span>

<span data-ttu-id="f46bb-212">**Il solido aspetto dei percorsi di un'esercitazione**</span><span class="sxs-lookup"><span data-stu-id="f46bb-212">**The robust aspect of the endianess walks**</span></span>

<span data-ttu-id="f46bb-213">Il percorso di inserimento controlla le normali condizioni di esaurimento del buffer ed esegue altri controlli su una natura non correlata.</span><span class="sxs-lookup"><span data-stu-id="f46bb-213">The endianess walk checks for the usual out-of-the-buffer conditions and performs other checks of an uncorrelated nature.</span></span> <span data-ttu-id="f46bb-214">I controlli destinati a valori correlati, ad esempio l'argomento di ridimensionamento rispetto alla dimensione conforme, non possono essere eseguiti con questo passaggio. vengono eseguite in un secondo momento, durante l'unmarshalling.</span><span class="sxs-lookup"><span data-stu-id="f46bb-214">The checks aimed at correlated values (such as the sizing argument versus the conformant size) cannot be performed using this step; they are performed later, when unmarshaling.</span></span>

 

 




