---
title: Strutture (RPC)
description: Descrizione dei vari tipi di strutture in RPC (Remote Procedure Call).
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047089"
---
# <a name="structures-rpc"></a><span data-ttu-id="96371-103">Strutture (RPC)</span><span class="sxs-lookup"><span data-stu-id="96371-103">Structures (RPC)</span></span>

<span data-ttu-id="96371-104">Esistono diverse categorie di strutture, progressivamente più complesse in termini di azioni necessarie per il marshalling.</span><span class="sxs-lookup"><span data-stu-id="96371-104">There are several categories of structures, progressively more complicated in terms of actions required for marshaling.</span></span> <span data-ttu-id="96371-105">Iniziano con una struttura semplice che può essere interamente copiata in blocchi e continuare a una struttura complessa che deve essere gestita campo per campo.</span><span class="sxs-lookup"><span data-stu-id="96371-105">They begin with a simple structure that can be block-copied as a whole, and continue to a complex structure that has to be serviced field by field.</span></span>

-   [<span data-ttu-id="96371-106">Struttura semplice</span><span class="sxs-lookup"><span data-stu-id="96371-106">Simple Structure</span></span>](#simple-structure)
-   [<span data-ttu-id="96371-107">Struttura semplice con puntatori</span><span class="sxs-lookup"><span data-stu-id="96371-107">Simple Structure with Pointers</span></span>](#simple-structure-with-pointers)
-   [<span data-ttu-id="96371-108">Struttura conforme</span><span class="sxs-lookup"><span data-stu-id="96371-108">Conformant Structure</span></span>](#conformant-structure)
-   [<span data-ttu-id="96371-109">Struttura conforme con puntatori</span><span class="sxs-lookup"><span data-stu-id="96371-109">Conformant Structure with Pointers</span></span>](#conformant-structure-with-pointers)
-   [<span data-ttu-id="96371-110">Struttura variabile conforme (con o senza puntatori)</span><span class="sxs-lookup"><span data-stu-id="96371-110">Conformant Varying Structure (with or without Pointers)</span></span>](#conformant-varying-structure-with-or-without-pointers)
-   [<span data-ttu-id="96371-111">Struttura hardware</span><span class="sxs-lookup"><span data-stu-id="96371-111">Hard Structure</span></span>](#hard-structure)
-   [<span data-ttu-id="96371-112">Struttura complessa</span><span class="sxs-lookup"><span data-stu-id="96371-112">Complex Structure</span></span>](#complex-structure)
-   [<span data-ttu-id="96371-113">Descrizione layout membri struttura</span><span class="sxs-lookup"><span data-stu-id="96371-113">Structure Member Layout Description</span></span>](#structure-member-layout-description)

> [!Note]  
> <span data-ttu-id="96371-114">Rispetto alle categorie di matrici, diventa chiaro che è possibile descrivere solo le strutture di dimensioni fino a 64K (le dimensioni sono per la parte piatta della struttura), ovvero non esiste alcun equivalente di matrici SM e LG.</span><span class="sxs-lookup"><span data-stu-id="96371-114">When compared to array categories, it becomes clear that only structures up to 64k in size can be described (the size is for the flat part of the structure), that is there is no equivalent of SM and LG arrays.</span></span>

 

<span data-ttu-id="96371-115">**Membri comuni alle strutture**</span><span class="sxs-lookup"><span data-stu-id="96371-115">**Members Common to Structures**</span></span>

-   <span data-ttu-id="96371-116">**allineamento**</span><span class="sxs-lookup"><span data-stu-id="96371-116">**alignment**</span></span>

    <span data-ttu-id="96371-117">Allineamento necessario del buffer prima dell'unmarshalling della struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-117">The necessary alignment of the buffer before unmarshaling the structure.</span></span> <span data-ttu-id="96371-118">I valori validi sono 0, 1, 3 e 7 (l'allineamento effettivo meno 1).</span><span class="sxs-lookup"><span data-stu-id="96371-118">Valid values are 0, 1, 3, and 7 (the actual alignment minus 1).</span></span>

-   <span data-ttu-id="96371-119">**\_Dimensioni memoria**</span><span class="sxs-lookup"><span data-stu-id="96371-119">**memory\_size**</span></span>

    <span data-ttu-id="96371-120">Dimensione della struttura in memoria in byte. per le strutture conformi questa dimensione non include la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="96371-120">Size of the structure in memory in bytes; for conformant structures this size does not include the array's size.</span></span>

-   <span data-ttu-id="96371-121">**offset \_ nella \_ Descrizione della matrice \_**</span><span class="sxs-lookup"><span data-stu-id="96371-121">**offset\_to\_array\_description**</span></span>

    <span data-ttu-id="96371-122">Offset dal puntatore della stringa di formato corrente alla descrizione della matrice conforme contenuta in una struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-122">Offset from the current format string pointer to the description of the conformant array contained in a structure.</span></span>

-   <span data-ttu-id="96371-123">**layout del membro \_**</span><span class="sxs-lookup"><span data-stu-id="96371-123">**member\_layout**</span></span>

    <span data-ttu-id="96371-124">Descrizione di ogni elemento della struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-124">Description of each element of the structure.</span></span> <span data-ttu-id="96371-125">Le routine NDR devono solo esaminare questa parte della stringa di formato di un tipo se è necessaria la trasformazione endian o se il tipo è una struttura complessa.</span><span class="sxs-lookup"><span data-stu-id="96371-125">The NDR routines only need to examine this portion of a type's format string if endian transformation is needed or if the type is a complex structure.</span></span>

-   <span data-ttu-id="96371-126">**\_layout puntatore**</span><span class="sxs-lookup"><span data-stu-id="96371-126">**pointer\_layout**</span></span>

    <span data-ttu-id="96371-127">Vedere la sezione del [layout del puntatore](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="96371-127">See the [Pointer Layout](pointer-layout-tfs.md) section.</span></span>

## <a name="simple-structure"></a><span data-ttu-id="96371-128">Struttura semplice</span><span class="sxs-lookup"><span data-stu-id="96371-128">Simple Structure</span></span>

<span data-ttu-id="96371-129">Una struttura semplice contiene solo tipi di base, matrici fisse e altre strutture semplici.</span><span class="sxs-lookup"><span data-stu-id="96371-129">A simple structure contains only base types, fixed arrays, and other simple structures.</span></span> <span data-ttu-id="96371-130">La caratteristica principale della struttura semplice è che può essere copiata in blocco nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="96371-130">The main feature of the simple structure is that it can be block-copied as a whole.</span></span>

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a><span data-ttu-id="96371-131">Struttura semplice con puntatori</span><span class="sxs-lookup"><span data-stu-id="96371-131">Simple Structure with Pointers</span></span>

<span data-ttu-id="96371-132">Una struttura semplice con puntatori contiene solo i tipi di base, i puntatori, le matrici fisse, le strutture semplici e altre strutture semplici con i puntatori.</span><span class="sxs-lookup"><span data-stu-id="96371-132">A simple structure with pointers contains only base types, pointers, fixed arrays, simple structures, and other simple structures with pointers.</span></span> <span data-ttu-id="96371-133">Poiché la<> del layout deve essere visitata solo quando si esegue una conversione di, viene inserita alla fine della descrizione.</span><span class="sxs-lookup"><span data-stu-id="96371-133">Because the layout<> will only have to be visited when doing an endianess conversion, it is placed at the end of the description.</span></span>

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a><span data-ttu-id="96371-134">Struttura conforme</span><span class="sxs-lookup"><span data-stu-id="96371-134">Conformant Structure</span></span>

<span data-ttu-id="96371-135">Una struttura conforme contiene solo tipi di base, matrici fisse e strutture semplici e deve contenere una stringa conforme o una matrice conforme.</span><span class="sxs-lookup"><span data-stu-id="96371-135">A conformant structure contains only base types, fixed arrays, and simple structures, and must contain either a conformant string or a conformant array.</span></span> <span data-ttu-id="96371-136">Questa matrice può essere effettivamente contenuta in un'altra struttura o struttura conforme con i puntatori incorporati nella struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-136">This array could actually be contained in another conformant structure or conformant structure with pointers which is embedded in this structure.</span></span>

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a><span data-ttu-id="96371-137">Struttura conforme con puntatori</span><span class="sxs-lookup"><span data-stu-id="96371-137">Conformant Structure with Pointers</span></span>

<span data-ttu-id="96371-138">Una struttura conforme con puntatori contiene solo i tipi di base, i puntatori, le matrici fisse, le strutture semplici e le strutture semplici con i puntatori; una struttura conforme deve contenere una matrice conforme.</span><span class="sxs-lookup"><span data-stu-id="96371-138">A conformant structure with pointers contains only base types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant structure must contain a conformant array.</span></span> <span data-ttu-id="96371-139">Questa matrice può essere effettivamente contenuta in un'altra struttura o struttura conforme con puntatori incorporati nella struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-139">This array could actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a><span data-ttu-id="96371-140">Struttura variabile conforme (con o senza puntatori)</span><span class="sxs-lookup"><span data-stu-id="96371-140">Conformant Varying Structure (with or without Pointers)</span></span>

<span data-ttu-id="96371-141">Una struttura a variazione conforme contiene solo tipi semplici, puntatori, matrici fisse, strutture semplici e strutture semplici con i puntatori; una struttura a variazione conforme deve contenere una stringa conforme o una matrice a variazione conforme.</span><span class="sxs-lookup"><span data-stu-id="96371-141">A conformant varying structure contains only simple types, pointers, fixed arrays, simple structures, and simple structures with pointers; a conformant varying structure must contain either a conformant string or a conformant-varying array.</span></span> <span data-ttu-id="96371-142">La stringa o la matrice conforme può essere effettivamente contenuta in un'altra struttura o struttura conforme con puntatori incorporati nella struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-142">The conformant string or array can actually be contained in another conformant structure or conformant structure with pointers that is embedded in this structure.</span></span>

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a><span data-ttu-id="96371-143">Struttura hardware</span><span class="sxs-lookup"><span data-stu-id="96371-143">Hard Structure</span></span>

<span data-ttu-id="96371-144">La struttura hardware era un concetto mirato a eliminare sanzioni ripide correlate all'elaborazione di strutture complesse.</span><span class="sxs-lookup"><span data-stu-id="96371-144">The hard structure was a concept aimed at eliminating steep penalties related to processing complex structures.</span></span> <span data-ttu-id="96371-145">Deriva da un'osservazione che una struttura complessa ha in genere solo una o due condizioni che impediscono la copia dei blocchi e pertanto ne danneggiano le prestazioni rispetto a una struttura semplice.</span><span class="sxs-lookup"><span data-stu-id="96371-145">It is derived from an observation that a complex structure typically has only one or two conditions that prevent block-copying, and therefore spoil its performance compared to a simple structure.</span></span> <span data-ttu-id="96371-146">I colpevoli sono in genere unioni o campi di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="96371-146">The culprits are usually unions or enumeration fields.</span></span>

<span data-ttu-id="96371-147">Una struttura rigida è una struttura con un enum16, un riempimento finale in memoria o un'Unione come ultimo membro.</span><span class="sxs-lookup"><span data-stu-id="96371-147">A hard structure is a structure that has an enum16, end-padding in memory, or a union as the last member.</span></span> <span data-ttu-id="96371-148">Questi tre elementi impediscono alla struttura di rientrare in una delle categorie di struttura precedenti, che sfruttano il sovraccarico dell'interpretazione di piccole dimensioni e il potenziale massimo di ottimizzazione, ma non forzano la categoria della struttura molto costosa.</span><span class="sxs-lookup"><span data-stu-id="96371-148">These three elements prevent the structure from falling into one of the previous structure categories, which enjoy small interpretation overhead and maximum optimization potential, but do not force it into the very costly complex structure category.</span></span>

<span data-ttu-id="96371-149">Il enum16 non deve causare differenze tra la memoria e le dimensioni dei cavi della struttura.</span><span class="sxs-lookup"><span data-stu-id="96371-149">The enum16 must not cause the memory and wire sizes of the structure to differ.</span></span> <span data-ttu-id="96371-150">La struttura non può contenere matrici conformi, né puntatori (a meno che non faccia parte dell'Unione); gli unici altri membri consentiti sono tipi di base, matrici fisse e strutture semplici.</span><span class="sxs-lookup"><span data-stu-id="96371-150">The structure cannot have any conformant array, nor any pointers (unless part of the union); the only other members allowed are base types, fixed arrays, and simple structures.</span></span>

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

<span data-ttu-id="96371-151">Il \_ campo Offset enum<2> fornisce l'offset dall'inizio della struttura in memoria a un enum16 se ne contiene uno; in caso contrario, l' \_ offset enum<2> campo è-1.</span><span class="sxs-lookup"><span data-stu-id="96371-151">The enum\_offset<2> field provides the offset from the beginning of the structure in memory to an enum16 if it contains one; otherwise the enum\_offset<2> field is –1.</span></span>

<span data-ttu-id="96371-152">Il \_ campo Copy size<2> fornisce il numero totale di byte nella struttura, che può essere copiato in un blocco nel/dal buffer.</span><span class="sxs-lookup"><span data-stu-id="96371-152">The copy\_size<2> field provides the total number of bytes in the structure, which may be block-copied into/from the buffer.</span></span> <span data-ttu-id="96371-153">Il totale non include alcuna unione finale né alcun riempimento finale nella memoria.</span><span class="sxs-lookup"><span data-stu-id="96371-153">This total does not include any trailing union nor any end-padding in memory.</span></span> <span data-ttu-id="96371-154">Questo valore rappresenta anche la quantità di incremento del puntatore del buffer dopo la copia.</span><span class="sxs-lookup"><span data-stu-id="96371-154">This value is also the amount the buffer pointer should be incremented following the copy.</span></span>

<span data-ttu-id="96371-155">Il \_ \_ campo incr<2> per la copia di MEM è il numero di byte che il puntatore di memoria deve incrementare dopo la copia di blocco prima di gestire qualsiasi unione finale.</span><span class="sxs-lookup"><span data-stu-id="96371-155">The mem\_copy\_incr<2> field is the number of bytes the memory pointer should be incremented following the block-copy before handling any trailing union.</span></span> <span data-ttu-id="96371-156">L'incremento in base a questa quantità (non in base alle dimensioni della copia \_<2> byte) restituisce un puntatore di memoria appropriato a qualsiasi unione finale.</span><span class="sxs-lookup"><span data-stu-id="96371-156">Incrementing by this amount (not by copy\_size<2> bytes) yields a proper memory pointer to any trailing union.</span></span>

## <a name="complex-structure"></a><span data-ttu-id="96371-157">Struttura complessa</span><span class="sxs-lookup"><span data-stu-id="96371-157">Complex Structure</span></span>

<span data-ttu-id="96371-158">Una struttura complessa è una struttura che contiene uno o più campi che impediscono la copia del blocco della struttura o per cui è necessario eseguire un controllo aggiuntivo durante il marshalling o l'unmarshalling, ad esempio i controlli associati in un'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="96371-158">A complex structure is any structure containing one or more fields that either prevent the structure from being block-copied, or for which additional checking must be performed during marshaling or unmarshaling (for example, bound checks on an enumeration).</span></span> <span data-ttu-id="96371-159">I tipi di NDR seguenti rientrino in questa categoria:</span><span class="sxs-lookup"><span data-stu-id="96371-159">The following NDR types fall in this category:</span></span>

-   <span data-ttu-id="96371-160">[tipi semplici](simple-types-tfs.md): ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), un integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="96371-160">[simple types](simple-types-tfs.md): ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="96371-161">riempimento allineamento alla fine della struttura</span><span class="sxs-lookup"><span data-stu-id="96371-161">alignment padding at the end of the structure</span></span>
-   <span data-ttu-id="96371-162">puntatori a interfaccia (utilizzano un complesso incorporato)</span><span class="sxs-lookup"><span data-stu-id="96371-162">interface pointers (they go using an embedded complex)</span></span>
-   <span data-ttu-id="96371-163">puntatori ignorati (correlati all'attributo \[ [**Ignore**](/windows/desktop/Midl/ignore) \] e al \_ token FC Ignore)</span><span class="sxs-lookup"><span data-stu-id="96371-163">ignored pointers (that is related to \[[**ignore**](/windows/desktop/Midl/ignore)\] attribute and FC\_IGNORE token)</span></span>
-   <span data-ttu-id="96371-164">matrici complesse, matrici variabili, matrici di stringhe</span><span class="sxs-lookup"><span data-stu-id="96371-164">complex arrays, varying arrays, string arrays</span></span>
-   <span data-ttu-id="96371-165">matrici conformi a più dimensioni con almeno una dimensione non fissa</span><span class="sxs-lookup"><span data-stu-id="96371-165">multidimensional conformant arrays with at least one nonfixed dimension</span></span>
-   <span data-ttu-id="96371-166">unioni</span><span class="sxs-lookup"><span data-stu-id="96371-166">unions</span></span>
-   <span data-ttu-id="96371-167">elementi definiti con \[ [**trasmissione \_ come**](/windows/desktop/Midl/transmit-as) \] , \[ [**rappresentano \_ come**](/windows/desktop/Midl/represent-as) \] , \[ [**\_ marshalling del Wire**](/windows/desktop/Midl/wire-marshal) \] , \[ [**\_ marshalling utente**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="96371-167">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**represent\_as**](/windows/desktop/Midl/represent-as)\], \[[**wire\_marshal**](/windows/desktop/Midl/wire-marshal)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="96371-168">strutture complesse incorporate</span><span class="sxs-lookup"><span data-stu-id="96371-168">embedded complex structures</span></span>
-   <span data-ttu-id="96371-169">riempimento alla fine della struttura</span><span class="sxs-lookup"><span data-stu-id="96371-169">padding at the end of the structure</span></span>

<span data-ttu-id="96371-170">Una struttura complessa presenta la descrizione del formato seguente:</span><span class="sxs-lookup"><span data-stu-id="96371-170">A complex structure has the following format description:</span></span>

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

<span data-ttu-id="96371-171">La \_ dimensione della memoria<2> campo corrisponde alla dimensione della struttura in memoria, in byte.</span><span class="sxs-lookup"><span data-stu-id="96371-171">The memory\_size<2> field is the size of the structure in memory, in bytes.</span></span>

<span data-ttu-id="96371-172">Se la struttura contiene una matrice conforme, l'offset \_ a una \_ Descrizione della matrice conforme \_ \_<2> campo fornisce l'offset alla descrizione della matrice conforme; in caso contrario, è zero.</span><span class="sxs-lookup"><span data-stu-id="96371-172">If the structure contains a conformant array, the offset\_to\_conformant\_array\_description<2> field provides the offset to the conformant array's description, otherwise it is zero.</span></span>

<span data-ttu-id="96371-173">Se la struttura dispone di puntatori, l'offset \_ al \_ layout del puntatore \_<2> campo fornisce l'offset oltre il layout della struttura al layout del puntatore, in caso contrario questo campo è zero.</span><span class="sxs-lookup"><span data-stu-id="96371-173">If the structure has pointers, the offset\_to\_pointer\_layout<2> field provides the offset past the structure's layout to the pointer layout, otherwise this field is zero.</span></span>

<span data-ttu-id="96371-174">Il layout del puntatore \_<> campo di una struttura complessa viene gestito in modo diverso rispetto alle altre strutture.</span><span class="sxs-lookup"><span data-stu-id="96371-174">The pointer\_layout<> field of a complex structure is handled somewhat differently than for other structures.</span></span> <span data-ttu-id="96371-175">Il layout del puntatore \_<> campo di una struttura complessa contiene solo le descrizioni dei campi del puntatore effettivi nella struttura stessa.</span><span class="sxs-lookup"><span data-stu-id="96371-175">The pointer\_layout<> field of a complex structure only contains descriptions of actual pointer fields in the structure itself.</span></span> <span data-ttu-id="96371-176">Tutti i puntatori contenuti all'interno di matrici, unioni o strutture incorporate non sono descritti nel campo di layout del puntatore della struttura complessa \_<> campo.</span><span class="sxs-lookup"><span data-stu-id="96371-176">Any pointers contained within any embedded arrays, unions, or structures are not described in the complex structure's pointer\_layout<> field.</span></span>

> [!Note]  
> <span data-ttu-id="96371-177">Questo si differenzia dalle altre strutture, che duplicano la descrizione di tutti i puntatori contenuti in matrici o strutture incorporate nel proprio layout di puntatore \_<> campo.</span><span class="sxs-lookup"><span data-stu-id="96371-177">This is in contrast to other structures, which duplicate the description of any pointers contained in embedded arrays or structures in their own pointer \_layout<> field as well.</span></span>

 

<span data-ttu-id="96371-178">Anche il formato del layout del puntatore di una struttura complessa è radicalmente diverso.</span><span class="sxs-lookup"><span data-stu-id="96371-178">The format of a complex structure's pointer layout is also radically different.</span></span> <span data-ttu-id="96371-179">Poiché contiene solo le descrizioni dei membri effettivi del puntatore e perché viene effettuato il marshalling di una struttura complessa e viene eseguito l'unmarshalling di un campo alla volta, il layout del puntatore \_<> campo contiene semplicemente la descrizione del puntatore di tutti i membri del puntatore.</span><span class="sxs-lookup"><span data-stu-id="96371-179">Because it only contains descriptions of actual pointer members and because a complex structure is marshaled and unmarshaled one field at a time, the pointer\_layout<> field simply contains the pointer description of all pointer members.</span></span> <span data-ttu-id="96371-180">Non è presente alcun inizio FC \_ PP e nessuno dei normali layout del puntatore \_<> informazioni.</span><span class="sxs-lookup"><span data-stu-id="96371-180">There is no beginning FC\_PP, and none of the usual pointer\_layout<> information.</span></span>

## <a name="structure-member-layout-description"></a><span data-ttu-id="96371-181">Descrizione layout membri struttura</span><span class="sxs-lookup"><span data-stu-id="96371-181">Structure Member Layout Description</span></span>

<span data-ttu-id="96371-182">La descrizione del layout di una struttura contiene uno o più dei caratteri di formato seguenti:</span><span class="sxs-lookup"><span data-stu-id="96371-182">A structure's layout description contains one or more of the following format characters:</span></span>

-   <span data-ttu-id="96371-183">Qualsiasi carattere di tipo di base, ad esempio FC \_ char e così via</span><span class="sxs-lookup"><span data-stu-id="96371-183">Any of the base type characters, like FC\_CHAR, and so on</span></span>
-   <span data-ttu-id="96371-184">Direttive di allineamento.</span><span class="sxs-lookup"><span data-stu-id="96371-184">Alignment directives.</span></span> <span data-ttu-id="96371-185">Sono disponibili tre caratteri di formato che specificano l'allineamento del puntatore di memoria: FC \_ ALIGNM2, FC \_ ALIGNM4 e FC \_ ALIGNM8.</span><span class="sxs-lookup"><span data-stu-id="96371-185">There are three format characters specifying alignment of the memory pointer: FC\_ALIGNM2, FC\_ALIGNM4, and FC\_ALIGNM8.</span></span>
    > [!Note]  
    > <span data-ttu-id="96371-186">Sono presenti anche token di allineamento del buffer, FC \_ ALIGNB2 tramite FC \_ ALIGNM8. questi non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="96371-186">There are also buffer alignment tokens, FC\_ALIGNB2 through FC\_ALIGNM8; these are not used.</span></span>

     

-   <span data-ttu-id="96371-187">Riempimento memoria.</span><span class="sxs-lookup"><span data-stu-id="96371-187">Memory padding.</span></span> <span data-ttu-id="96371-188">Questi si verificano solo alla fine della descrizione di una struttura e indicano il numero di byte di riempimento in memoria prima della matrice conforme nella struttura: FC \_ STRUCTPADn, dove n è il numero di byte di spaziatura interna.</span><span class="sxs-lookup"><span data-stu-id="96371-188">These occur only at the end of a structure's description and denote the number of bytes of padding in memory before the conformant array in the structure: FC\_STRUCTPADn, where n is the number of bytes of padding.</span></span>
-   <span data-ttu-id="96371-189">Qualsiasi tipo non di base incorporato (si noti, tuttavia, che una matrice conforme non si verifica mai nel layout della struttura).</span><span class="sxs-lookup"><span data-stu-id="96371-189">Any embedded nonbase type (note, however, that a conformant array never occurs in the structure layout).</span></span> <span data-ttu-id="96371-190">Questa operazione ha una descrizione di 4 byte:</span><span class="sxs-lookup"><span data-stu-id="96371-190">This has a 4-byte description:</span></span>

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    <span data-ttu-id="96371-191">Se non è garantito che l'offset sia allineato a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="96371-191">where the offset is not guaranteed to be 2-byte aligned.</span></span>

    <span data-ttu-id="96371-192">\_il riquadro memoria<1> è una spaziatura interna necessaria in memoria prima del campo complesso.</span><span class="sxs-lookup"><span data-stu-id="96371-192">memory\_pad<1> is a padding needed in memory before the complex field.</span></span>

    <span data-ttu-id="96371-193">offset \_ alla \_ Descrizione<2> è un offset di tipo relativo al tipo incorporato.</span><span class="sxs-lookup"><span data-stu-id="96371-193">offset\_to\_description<2> is a relative type offset to the embedded type.</span></span>

<span data-ttu-id="96371-194">Potrebbe anche essere presente un \_ Pad FC prima del termine FC di terminazione \_ , se necessario, per garantire che la stringa di formato venga allineata a un limite di 2 byte dopo l' \_ estremità FC.</span><span class="sxs-lookup"><span data-stu-id="96371-194">There may also be an FC\_PAD before the terminating FC\_END if needed to ensure that the format string will be aligned at a 2-byte boundary following the FC\_END.</span></span>

 

 