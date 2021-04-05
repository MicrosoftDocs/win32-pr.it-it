---
title: Descrittori di correlazione
description: Un descrittore di correlazione è una stringa di formato che descrive un'espressione basata su un argomento correlato a un altro argomento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872894"
---
# <a name="correlation-descriptors"></a><span data-ttu-id="3cc30-103">Descrittori di correlazione</span><span class="sxs-lookup"><span data-stu-id="3cc30-103">Correlation Descriptors</span></span>

<span data-ttu-id="3cc30-104">Un descrittore di correlazione è una stringa di formato che descrive un'espressione basata su un argomento correlato a un altro argomento.</span><span class="sxs-lookup"><span data-stu-id="3cc30-104">A correlation descriptor is a format string that describes an expression based on one argument related to another argument.</span></span> <span data-ttu-id="3cc30-105">È necessario un descrittore di correlazione per la gestione della semantica relativa a attributi come \[ **size \_ is ()** \] , \[ **length \_ is ()** \] , \[ **Switch \_ is ()** \] ed \[ **IID \_ è ()** \] .</span><span class="sxs-lookup"><span data-stu-id="3cc30-105">A correlation descriptor is needed for handling semantics related to attributes like \[**size\_is()**\], \[**length\_is()**\], \[**switch\_is()**\] and \[**iid\_is()**\].</span></span> <span data-ttu-id="3cc30-106">I descrittori di correlazione vengono utilizzati con matrici, puntatori dimensionati, unioni e puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3cc30-106">Correlation descriptors are used with arrays, sized pointers, unions, and interface pointers.</span></span> <span data-ttu-id="3cc30-107">Il valore dell'espressione finale può essere una dimensione, una lunghezza, un discriminante di Unione o un puntatore a un IID, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="3cc30-107">The eventual expression value can be a size, a length, a union discriminant, or a pointer to an IID, respectively.</span></span> <span data-ttu-id="3cc30-108">In termini di stringhe di formato, i descrittori di correlazione vengono utilizzati con matrici, unioni e puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3cc30-108">In terms of format strings, correlation descriptors are used with arrays, unions, and interface pointers.</span></span> <span data-ttu-id="3cc30-109">Un puntatore ridimensionato viene descritto in formato stringhe come puntatore a una matrice.</span><span class="sxs-lookup"><span data-stu-id="3cc30-109">A sized pointer is described in format strings as a pointer to an array.</span></span>

<span data-ttu-id="3cc30-110">Sono disponibili due routine che eseguono i calcoli delle espressioni di base: NdrpComputeConformance viene usato per le dimensioni, i commutatori e l'IID \* mentre NdrpComputeVariance viene usato per lunghezze.</span><span class="sxs-lookup"><span data-stu-id="3cc30-110">There are two routines performing basic expression calculations: NdrpComputeConformance is used for sizes, switches and IID\* while NdrpComputeVariance is used for lengths.</span></span> <span data-ttu-id="3cc30-111">Esiste anche una singola routine per eseguire una convalida del valore di correlazione per la funzionalità di negazione di attacco.</span><span class="sxs-lookup"><span data-stu-id="3cc30-111">There is also a single routine to perform a correlation value validation for denial-of-attack functionality.</span></span>

<span data-ttu-id="3cc30-112">I descrittori di correlazione sono stati progettati per supportare solo espressioni molto limitate.</span><span class="sxs-lookup"><span data-stu-id="3cc30-112">Correlation descriptors have been designed to support only very limited expressions.</span></span> <span data-ttu-id="3cc30-113">Per situazioni complesse, il compilatore genera una routine di valutazione dell'espressione che verrà chiamata dal motore quando necessario.</span><span class="sxs-lookup"><span data-stu-id="3cc30-113">For complicated situations, the compiler generates an expression evaluation routine to be called by the engine when needed.</span></span>

<span data-ttu-id="3cc30-114">Un descrittore di correlazione ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="3cc30-114">A correlation descriptor has the following format:</span></span>

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

<span data-ttu-id="3cc30-115">Il tipo di correlazione del descrittore di correlazione \_<1> è costituito da due stuzzichini: i 4 bit superiori descrivono dove è possibile trovare l'espressione e i 4 bit inferiori descrivono il tipo del valore dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="3cc30-115">The correlation descriptor correlation\_type<1> consists of two nibbles: the upper 4 bits describe where the expression can be found and the lower 4 bits describe the type of the expression value.</span></span>

<span data-ttu-id="3cc30-116">Il bocconcino superiore può avere uno dei cinque valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cc30-116">The upper nibble can have one of these five values:</span></span>

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span data-ttu-id="3cc30-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_conformità normale \_ FC</span><span class="sxs-lookup"><span data-stu-id="3cc30-117"><span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC\_NORMAL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="3cc30-118">Un caso normale di conformità, ad esempio quello descritto in un campo di una struttura.</span><span class="sxs-lookup"><span data-stu-id="3cc30-118">A normal case of conformance, such as that described in a field of a structure.</span></span>

</dd> <dt>

<span data-ttu-id="3cc30-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>\_conformità del puntatore FC \_</span><span class="sxs-lookup"><span data-stu-id="3cc30-119"><span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC\_POINTER\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="3cc30-120">Per i puntatori con attributi (**size \_ è ()**, **length \_ è ()**) che sono campi in una struttura.</span><span class="sxs-lookup"><span data-stu-id="3cc30-120">For attributed pointers (**size\_is()**, **length\_is()**) which are fields in a structure.</span></span> <span data-ttu-id="3cc30-121">Ciò influiscono sul modo in cui viene impostato il puntatore di memoria di base.</span><span class="sxs-lookup"><span data-stu-id="3cc30-121">This affects the way the base memory pointer is set.</span></span>

</dd> <dt>

<span data-ttu-id="3cc30-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformità di \_ livello \_ superiore FC</span><span class="sxs-lookup"><span data-stu-id="3cc30-122"><span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC\_TOP\_LEVEL\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="3cc30-123">Per la conformità di primo livello descritta da un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="3cc30-123">For top-level conformance described by another parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3cc30-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_ \_ conformità MULTIlivello FC di primo livello \_ \_</span><span class="sxs-lookup"><span data-stu-id="3cc30-124"><span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC\_TOP\_LEVEL\_MULTID\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="3cc30-125">Per la conformità di primo livello di una matrice multidimensionale descritta da un altro parametro.</span><span class="sxs-lookup"><span data-stu-id="3cc30-125">For top-level conformance of a multidimensional array described by another parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3cc30-126">Le matrici e i puntatori di dimensioni multidimensionali attivano un'opzione a [**-Oicf**](/windows/desktop/Midl/-oi).</span><span class="sxs-lookup"><span data-stu-id="3cc30-126">Multidimensional sized arrays and pointers trigger a switch to [**–Oicf**](/windows/desktop/Midl/-oi).</span></span>

 

</dd> <dt>

<span data-ttu-id="3cc30-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>\_conformità costante \_ FC</span><span class="sxs-lookup"><span data-stu-id="3cc30-127"><span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC\_CONSTANT\_CONFORMANCE</span></span>
</dt> <dd>

<span data-ttu-id="3cc30-128">Per un valore costante.</span><span class="sxs-lookup"><span data-stu-id="3cc30-128">For a constant value.</span></span> <span data-ttu-id="3cc30-129">Il compilatore Precalcola il valore di un'espressione costante fornita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3cc30-129">The compiler precalculates the value from a constant expression supplied by the user.</span></span> <span data-ttu-id="3cc30-130">Quando questo è il caso, i 3 byte successivi nella descrizione della conformità contengono i 3 byte inferiori di un valore Long che descrive le dimensioni della conformità.</span><span class="sxs-lookup"><span data-stu-id="3cc30-130">When this is the case, the subsequent 3 bytes in the conformance description contain the lower 3 bytes of a long describing the conformance size.</span></span> <span data-ttu-id="3cc30-131">Non è necessario alcun calcolo ulteriore.</span><span class="sxs-lookup"><span data-stu-id="3cc30-131">No further computation is required.</span></span>

</dd> </dl>

<span data-ttu-id="3cc30-132">Il morso inferiore fornisce il tipo di valore che deve essere estratto dalla memoria:</span><span class="sxs-lookup"><span data-stu-id="3cc30-132">The lower nibble gives the type of the value that needs to be extracted from memory:</span></span>

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> <span data-ttu-id="3cc30-133">le espressioni a 64 bit non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="3cc30-133">64-bit expressions are not supported.</span></span> <span data-ttu-id="3cc30-134">FC \_ Hyper viene usato solo per **IID \_ è ()** su piattaforme a 64 bit per estrarre il valore del puntatore per IID \* .</span><span class="sxs-lookup"><span data-stu-id="3cc30-134">FC\_HYPER is used only for **iid\_is()** on 64-bit platforms to extract the pointer value for IID\*.</span></span>
>
> <span data-ttu-id="3cc30-135">Il compilatore imposta il tipo rosicchia su zero per i casi seguenti: espressione costante menzionata sopra e quando deve essere chiamata la routine dell'espressione di valutazione, ad esempio quando \_ vengono usati la conformità della costante FC \_ e il \_ callback FC.</span><span class="sxs-lookup"><span data-stu-id="3cc30-135">The compiler sets the type nibble to zero for the following cases: constant expression mentioned above and when evaluation expression routine needs to be called, for example, when FC\_CONSTANT\_CONFORMANCE and FC\_CALLBACK are used.</span></span>

 

<span data-ttu-id="3cc30-136">Il \_ campo dimensioni è \_ op<1> consente di applicare una delle operazioni seguenti alla variabile di conformità:</span><span class="sxs-lookup"><span data-stu-id="3cc30-136">The size\_is\_op<1> field allows for one of the following operations to be applied to the conformance variable:</span></span>

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

<span data-ttu-id="3cc30-137">La \_ costante di DEreferenziazione FC viene utilizzata per la correlazione di un puntatore, ad esempio per **\[ size \_ is ( \* pl) \]**.</span><span class="sxs-lookup"><span data-stu-id="3cc30-137">The FC\_DEREFERENCE constant is used for correlation being a pointee, like for **\[size\_is(\*pL)\]**.</span></span> <span data-ttu-id="3cc30-138">Gli operatori aritmetici usano solo la costante indicata.</span><span class="sxs-lookup"><span data-stu-id="3cc30-138">Arithmetic operators just use the indicated constant.</span></span> <span data-ttu-id="3cc30-139">La \_ costante di callback FC indica che deve essere chiamata una routine di valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="3cc30-139">The FC\_CALLBACK constant indicates that an expression evaluation routine needs to be called.</span></span>

<span data-ttu-id="3cc30-140">Il campo Offset<2> è in genere un offset relativo della memoria rispetto alla variabile dell'argomento Expression.</span><span class="sxs-lookup"><span data-stu-id="3cc30-140">The offset<2> field is typically a relative memory offset to the expression argument variable.</span></span> <span data-ttu-id="3cc30-141">Può anche essere un indice di routine di valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="3cc30-141">It can also be an expression evaluation–routine index.</span></span> <span data-ttu-id="3cc30-142">Come indicato in precedenza in questo documento, per le espressioni costanti è parte del valore dell'espressione finale effettivo.</span><span class="sxs-lookup"><span data-stu-id="3cc30-142">As mentioned previously in this document, for constant expressions it is a part of actual, final expression value.</span></span>

<span data-ttu-id="3cc30-143">L'interpretazione dell'offset<2> campo come offset della memoria dipende dalla complessità dell'espressione, dalla posizione della variabile di espressione e, nel caso di una matrice, se la matrice è effettivamente un puntatore con attributi.</span><span class="sxs-lookup"><span data-stu-id="3cc30-143">The interpretation of the offset<2> field as memory offset depends on the complexity of the expression, the location of the expression variable, and in the case of an array, whether the array is actually an attributed pointer.</span></span>

<span data-ttu-id="3cc30-144">Se la matrice è un puntatore con attributi e la variabile di conformità è un campo di una struttura, il campo Offset contiene l'offset dall'inizio della struttura al campo di conformità.</span><span class="sxs-lookup"><span data-stu-id="3cc30-144">If the array is an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the beginning of the structure to the conformance-describing field.</span></span> <span data-ttu-id="3cc30-145">Se la matrice non è un puntatore con attributi e la variabile di conformità è un campo di una struttura, il campo Offset contiene l'offset dalla fine della parte non conforme della struttura al campo descrittivo di conformità.</span><span class="sxs-lookup"><span data-stu-id="3cc30-145">If the array is not an attributed pointer and the conformance variable is a field in a structure, the offset field contains the offset from the end of the nonconformant part of the structure to the conformance-describing field.</span></span> <span data-ttu-id="3cc30-146">In genere, la matrice conforme è alla fine della struttura.</span><span class="sxs-lookup"><span data-stu-id="3cc30-146">Typically, the conformant array is at the end of the structure.</span></span>

<span data-ttu-id="3cc30-147">Per la conformità di primo livello, il campo Offset contiene l'offset dalla posizione del primo parametro dello stub nello stack al parametro che descrive la conformità.</span><span class="sxs-lookup"><span data-stu-id="3cc30-147">For top-level conformance, the offset field contains the offset from the stub's first parameter's location on the stack to the parameter that describes the conformance.</span></span> <span data-ttu-id="3cc30-148">Questa operazione non viene utilizzata in modalità **-sistema operativo** .</span><span class="sxs-lookup"><span data-stu-id="3cc30-148">This is not used in **–Os** mode.</span></span> <span data-ttu-id="3cc30-149">Esistono altre eccezioni all'interpretazione del campo offset. tali eccezioni sono descritte nella descrizione di tali tipi.</span><span class="sxs-lookup"><span data-stu-id="3cc30-149">There are other exceptions to the interpretation of the offset field; such exceptions are described in the description of those types.</span></span>

<span data-ttu-id="3cc30-150">Quando offset<2> viene usato con il \_ callback FC, contiene un indice nella tabella di routine di valutazione dell'espressione generata dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="3cc30-150">When offset<2> is used with FC\_CALLBACK, it contains an index in the expression evaluation routine table generated by the compiler.</span></span> <span data-ttu-id="3cc30-151">Il messaggio stub viene passato alla routine di valutazione, che quindi calcola il valore di conformità e lo assegna al campo MaxCount del messaggio stub.</span><span class="sxs-lookup"><span data-stu-id="3cc30-151">The stub message is passed to the evaluation routine, which then computes the conformance value and assigns it to the MaxCount field of the stub message.</span></span>

<span data-ttu-id="3cc30-152">\_È stato aggiunto il campo Solid flags<2> per Windows 2000 per il supporto di [**/robust**](/windows/desktop/Midl/-robust), ad esempio la funzionalità Denial of attacks.</span><span class="sxs-lookup"><span data-stu-id="3cc30-152">The robust\_flags<2> field has been added for Windows 2000 to support [**/robust**](/windows/desktop/Midl/-robust), such as the denial-of-attacks feature.</span></span> <span data-ttu-id="3cc30-153">Il primo byte definisce i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="3cc30-153">The following flags are defined on the first byte:</span></span>

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

<span data-ttu-id="3cc30-154">Il flag Early indica una correlazione anticipata rispetto alla latenza.</span><span class="sxs-lookup"><span data-stu-id="3cc30-154">The Early flag indicates early versus late correlation.</span></span> <span data-ttu-id="3cc30-155">Una correlazione anticipata è quando l'argomento dell'espressione precede l'argomento descritto, ad esempio un argomento di dimensione è precedente a un argomento del puntatore ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="3cc30-155">An early correlation is when the expression argument precedes the described argument, for example a size argument is before a sized pointer argument.</span></span> <span data-ttu-id="3cc30-156">Una correlazione tardiva si verifica quando l'argomento dell'espressione viene eseguito dopo l'argomento correlato.</span><span class="sxs-lookup"><span data-stu-id="3cc30-156">A late correlation is when the expression argument comes after the related argument.</span></span> <span data-ttu-id="3cc30-157">Il motore esegue immediatamente la convalida dei valori di correlazione anticipata, i valori di correlazione tardivi vengono archiviati per il controllo dopo che è stato eseguito l'annullamento del marshalling.</span><span class="sxs-lookup"><span data-stu-id="3cc30-157">The engine performs validation of early correlation values right away, the late correlation values are stored for checking after unmarshaling is done.</span></span>

<span data-ttu-id="3cc30-158">Il flag Split indica una suddivisione asincrona tra \[ gli \] argomenti in e \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="3cc30-158">The Split flag indicates an async split among \[in\] and \[out\] arguments.</span></span> <span data-ttu-id="3cc30-159">Un argomento di dimensione, ad esempio, può essere \[ in \] mentre il puntatore di dimensioni può essere \[ out \] .</span><span class="sxs-lookup"><span data-stu-id="3cc30-159">For example, a size argument may be \[in\] while the sized pointer may be \[out\].</span></span> <span data-ttu-id="3cc30-160">Nel contesto asincrono DCOM questi argomenti si trovano in stack diversi, quindi il motore deve essere a conoscenza di questo.</span><span class="sxs-lookup"><span data-stu-id="3cc30-160">In the DCOM async context, these arguments happen to be on different stacks, so the engine must be aware of this.</span></span>

<span data-ttu-id="3cc30-161">Il flag IsIidIs indica che la correlazione **IID \_ è ()** .</span><span class="sxs-lookup"><span data-stu-id="3cc30-161">The IsIidIs flag indicates an **iid\_is()** correlation.</span></span> <span data-ttu-id="3cc30-162">La routine NdrComputeConformance viene ingannata per ottenere un puntatore a IID come valore di espressione, ma la routine di convalida non può confrontare tali valori (si tratta di puntatori), quindi il flag indica che è necessario confrontare il IID effettivo.</span><span class="sxs-lookup"><span data-stu-id="3cc30-162">The NdrComputeConformance routine is tricked to obtain a pointer to IID as an expression value, but the validation routine cannot compare such values (they would be pointers) and so the flag indicates that actual IIDs need to be compared.</span></span>

### <a name="variance-description-and-other-array-attributes"></a><span data-ttu-id="3cc30-163">Descrizione della varianza e altri attributi di matrice</span><span class="sxs-lookup"><span data-stu-id="3cc30-163">Variance Description and Other Array Attributes</span></span>

<span data-ttu-id="3cc30-164">Il formato del campo della descrizione della varianza è identico al campo della descrizione della conformità.</span><span class="sxs-lookup"><span data-stu-id="3cc30-164">The variance description field format is identical to the conformance description field.</span></span> <span data-ttu-id="3cc30-165">La differenza consiste nel fatto che un campo di messaggio Stub diverso viene utilizzato dal motore di NDR come variabile temporanea.</span><span class="sxs-lookup"><span data-stu-id="3cc30-165">The difference is that a different stub message field is used by the NDR engine as a temporary variable.</span></span> <span data-ttu-id="3cc30-166">Nel caso della descrizione della varianza, è la lunghezza che viene valutata e il campo corrispondente è denominato ActualLength.</span><span class="sxs-lookup"><span data-stu-id="3cc30-166">In the case of variance description, it is the length that is evaluated and the corresponding field is called ActualLength.</span></span>

<span data-ttu-id="3cc30-167">Con la varianza, l'offset iniziale è in genere zero e il motore viene ottimizzato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="3cc30-167">With variance, the starting offset is typically zero and the engine is tuned accordingly.</span></span> <span data-ttu-id="3cc30-168">Se il **primo attributo \_ is ()** viene applicato a una matrice di variazione conforme, viene forzata una richiamata a una routine di valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="3cc30-168">If the **first\_is()** attribute is applied to a conformant varying array, a callback to an expression evaluation routine is forced.</span></span>

 

 