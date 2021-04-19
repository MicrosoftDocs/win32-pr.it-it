---
title: Matrici (RPC) (TFS)
description: Le categorie di matrici RPC (Remote Procedure Call) includono dimensioni fisse, conformi, variabili conformi, variabili e complesse.
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d564a2dfd838006be1667343b14a57bdaf4b07
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106388813"
---
# <a name="arrays-rpc"></a><span data-ttu-id="b0b65-103">Matrici (RPC)</span><span class="sxs-lookup"><span data-stu-id="b0b65-103">Arrays (RPC)</span></span>

<span data-ttu-id="b0b65-104">Sono state definite diverse categorie di matrici in base alle relative caratteristiche di prestazioni, soprattutto se la matrice può essere copiata in blocchi.</span><span class="sxs-lookup"><span data-stu-id="b0b65-104">Several array categories have been defined based on their performance characteristics, primarily whether the array can be block-copied.</span></span>

<span data-ttu-id="b0b65-105">Per alcune categorie, ad esempio una matrice di dimensioni fisse, esistono due tipi di descrittori di matrici. sono indicati da una correzione nel nome del token FC principale.</span><span class="sxs-lookup"><span data-stu-id="b0b65-105">For some categories, such as a fixed-size array, two types of array descriptors exist; they are indicated by an in-fix in the name of the leading FC token.</span></span>



| <span data-ttu-id="b0b65-106">Formato carattere</span><span class="sxs-lookup"><span data-stu-id="b0b65-106">Format character</span></span> | <span data-ttu-id="b0b65-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0b65-107">Description</span></span>                                                           |
|------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b0b65-108">SM</span><span class="sxs-lookup"><span data-stu-id="b0b65-108">SM</span></span>               | <span data-ttu-id="b0b65-109">Le dimensioni totali del tipo possono essere rappresentate in un int senza segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="b0b65-109">The type's total size can be represented in a 16-bit unsigned int.</span></span>    |
| <span data-ttu-id="b0b65-110">LG</span><span class="sxs-lookup"><span data-stu-id="b0b65-110">LG</span></span>               | <span data-ttu-id="b0b65-111">La dimensione totale del tipo richiede una lunghezza senza segno a 32 bit per essere rappresentata.</span><span class="sxs-lookup"><span data-stu-id="b0b65-111">The type's total size needs a 32-bit unsigned long to be represented.</span></span> |



 

<span data-ttu-id="b0b65-112">Campi comuni alle matrici:</span><span class="sxs-lookup"><span data-stu-id="b0b65-112">Fields common to arrays:</span></span>

-   <span data-ttu-id="b0b65-113">\_dimensioni totali</span><span class="sxs-lookup"><span data-stu-id="b0b65-113">total\_size</span></span>

    <span data-ttu-id="b0b65-114">Dimensioni totali della matrice in memoria, in byte.</span><span class="sxs-lookup"><span data-stu-id="b0b65-114">Total size of the array in memory, in bytes.</span></span> <span data-ttu-id="b0b65-115">Corrisponde alla dimensione del Wire dopo l'allineamento.</span><span class="sxs-lookup"><span data-stu-id="b0b65-115">This is the same as wire size after alignment.</span></span> <span data-ttu-id="b0b65-116">La dimensione totale viene calcolata per le categorie per le quali non esiste un problema di riempimento e le dimensioni sono effettive della matrice.</span><span class="sxs-lookup"><span data-stu-id="b0b65-116">The total size is calculated for categories for which the padding issue does not exist and the size is actual array size.</span></span>

-   <span data-ttu-id="b0b65-117">\_dimensioni elemento</span><span class="sxs-lookup"><span data-stu-id="b0b65-117">element\_size</span></span>

    <span data-ttu-id="b0b65-118">Dimensioni totali in memoria di un singolo elemento della matrice, inclusa la spaziatura interna (questo può verificarsi solo per matrici complesse).</span><span class="sxs-lookup"><span data-stu-id="b0b65-118">Total size in memory of a single element of the array, including padding (this may happen for complex arrays only).</span></span>

-   <span data-ttu-id="b0b65-119">\_Descrizione elemento</span><span class="sxs-lookup"><span data-stu-id="b0b65-119">element\_description</span></span>

    <span data-ttu-id="b0b65-120">Descrizione del tipo di elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="b0b65-120">Description of the array element type.</span></span>

-   <span data-ttu-id="b0b65-121">\_layout puntatore</span><span class="sxs-lookup"><span data-stu-id="b0b65-121">pointer\_layout</span></span>

    <span data-ttu-id="b0b65-122">Per ulteriori informazioni, vedere l'argomento relativo al [layout del puntatore](pointer-layout-tfs.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b65-122">See the [Pointer Layout](pointer-layout-tfs.md) topic for more information.</span></span>

## <a name="fixed-sized-arrays"></a><span data-ttu-id="b0b65-123">Matrici a dimensione fissa</span><span class="sxs-lookup"><span data-stu-id="b0b65-123">Fixed-sized Arrays</span></span>

<span data-ttu-id="b0b65-124">Una stringa di formato di matrice a dimensione fissa viene generata per le matrici con una dimensione nota e pertanto può essere copiata in blocchi nel buffer di marshalling.</span><span class="sxs-lookup"><span data-stu-id="b0b65-124">A fixed-sized array format string is generated for arrays that have a known size, and therefore may be block-copied to the marshaling buffer.</span></span> <span data-ttu-id="b0b65-125">I due formati di descrittori di matrici fisse sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0b65-125">The two fixed array descriptor formats are as follows.</span></span>

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

<span data-ttu-id="b0b65-126">e</span><span class="sxs-lookup"><span data-stu-id="b0b65-126">and</span></span>

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a><span data-ttu-id="b0b65-127">Matrice conforme</span><span class="sxs-lookup"><span data-stu-id="b0b65-127">Conformant Array</span></span>

<span data-ttu-id="b0b65-128">Una matrice conforme può essere copiata in blocco una volta che la dimensione della matrice è nota.</span><span class="sxs-lookup"><span data-stu-id="b0b65-128">A conformant array can be block-copied once the size of the array is known.</span></span>

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b0b65-129">La descrizione della conformità \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="b0b65-129">The conformance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="conformant-varying-array"></a><span data-ttu-id="b0b65-130">Matrice a variazione conforme</span><span class="sxs-lookup"><span data-stu-id="b0b65-130">Conformant Varying Array</span></span>

<span data-ttu-id="b0b65-131">Una matrice a variazione conforme può anche essere copiata in blocchi.</span><span class="sxs-lookup"><span data-stu-id="b0b65-131">A conformant varying array can also be block-copied.</span></span>

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b0b65-132">La descrizione della conformità \_<> e la descrizione della varianza \_<> è un descrittore di correlazione e include 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="b0b65-132">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

## <a name="varying-array"></a><span data-ttu-id="b0b65-133">Matrice variabile</span><span class="sxs-lookup"><span data-stu-id="b0b65-133">Varying Array</span></span>

<span data-ttu-id="b0b65-134">Le matrici variabili hanno due possibilità a seconda della dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="b0b65-134">The varying arrays have two possibilities depending on the size of the array.</span></span>

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

<span data-ttu-id="b0b65-135">La descrizione della varianza \_<> è un descrittore di correlazione e ha 4 o 6 byte a seconda del [**/robust**](/windows/desktop/Midl/-robust) in uso.</span><span class="sxs-lookup"><span data-stu-id="b0b65-135">The variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on the [**/robust**](/windows/desktop/Midl/-robust) being used.</span></span>

<span data-ttu-id="b0b65-136">Per matrici variabili incorporate all'interno di una struttura, il campo Offset<2> della descrizione della varianza \_<> è un offset relativo dalla posizione della matrice variabile nella struttura al campo varianza descrittiva.</span><span class="sxs-lookup"><span data-stu-id="b0b65-136">For varying arrays embedded inside of a structure, the offset<2> field of the variance\_description<> is a relative offset from the varying array's position in the structure to the variance describing field.</span></span> <span data-ttu-id="b0b65-137">L'offset è in genere relativo all'inizio della struttura.</span><span class="sxs-lookup"><span data-stu-id="b0b65-137">The offset is typically relative to the beginning of the structure.</span></span>

## <a name="complex-arrays"></a><span data-ttu-id="b0b65-138">Matrici complesse</span><span class="sxs-lookup"><span data-stu-id="b0b65-138">Complex Arrays</span></span>

<span data-ttu-id="b0b65-139">Una matrice complessa è una matrice con un elemento che impedisce che venga copiata in blocco e, di conseguenza, deve essere eseguita un'azione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="b0b65-139">A complex array is any array with an element that prevents it from being block-copied, and as such, additional action needs to be taken.</span></span> <span data-ttu-id="b0b65-140">Questi elementi rendono un array complesso:</span><span class="sxs-lookup"><span data-stu-id="b0b65-140">These elements make an array complex:</span></span>

-   <span data-ttu-id="b0b65-141">tipi semplici: ENUM16, \_ \_ INT3264 (solo su piattaforme a 64 bit), un integrale con \[ [ **intervallo**](/windows/desktop/Midl/range)\]</span><span class="sxs-lookup"><span data-stu-id="b0b65-141">simple types: ENUM16, \_\_INT3264 (on 64-bit platforms only), an integral with \[[**range**](/windows/desktop/Midl/range)\]</span></span>
-   <span data-ttu-id="b0b65-142">puntatori di riferimento e interfaccia (tutti i puntatori sulle piattaforme a 64 bit)</span><span class="sxs-lookup"><span data-stu-id="b0b65-142">reference and interface pointers (all pointers on 64-bit platforms)</span></span>
-   <span data-ttu-id="b0b65-143">unioni</span><span class="sxs-lookup"><span data-stu-id="b0b65-143">unions</span></span>
-   <span data-ttu-id="b0b65-144">strutture complesse (per un elenco completo dei motivi per cui una struttura è complessa), vedere l'argomento relativo alla descrizione della struttura complessa.</span><span class="sxs-lookup"><span data-stu-id="b0b65-144">complex structures (see the Complex Structure Description topic for a full list of reasons for a structure to be complex)</span></span>
-   <span data-ttu-id="b0b65-145">elementi definiti con \[ [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) \] , \[ [**\_ marshalling utente**](/windows/desktop/Midl/user-marshal)\]</span><span class="sxs-lookup"><span data-stu-id="b0b65-145">elements defined with \[[**transmit\_as**](/windows/desktop/Midl/transmit-as)\], \[[**user\_marshal**](/windows/desktop/Midl/user-marshal)\]</span></span>
-   <span data-ttu-id="b0b65-146">Tutte le matrici multidimensionali con almeno una dimensione conforme e/o variabile sono complesse indipendentemente dal tipo di elemento sottostante.</span><span class="sxs-lookup"><span data-stu-id="b0b65-146">All multidimensional arrays with at least one conformant and/or varying dimension are complex regardless of the underlying element type.</span></span>

<span data-ttu-id="b0b65-147">La descrizione della matrice complessa è la seguente:</span><span class="sxs-lookup"><span data-stu-id="b0b65-147">The complex array description is as follows:</span></span>

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

<span data-ttu-id="b0b65-148">Il numero \_ di \_ elementi<2> campo è zero se la matrice è conforme.</span><span class="sxs-lookup"><span data-stu-id="b0b65-148">The number\_of\_elements<2> field is zero if the array is conformant.</span></span>

<span data-ttu-id="b0b65-149">La descrizione della conformità \_<> e la descrizione della varianza \_<> è un descrittore di correlazione e include 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="b0b65-149">The conformance\_description<> and variance\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="b0b65-150">Se la matrice ha una conformità e/o una varianza, la descrizione della conformità \_<> e/o la descrizione della varianza \_<> campo/i hanno descrizioni valide, in caso contrario i primi 4 byte del descrittore di correlazione vengono impostati su 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="b0b65-150">If the array has conformance and/or variance then the conformance\_description<> and/or variance\_description<> field(s) have valid descriptions, otherwise the first 4 bytes of the correlation descriptor are set to 0xFFFFFFFF.</span></span> <span data-ttu-id="b0b65-151">I flag, quando presenti, vengono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="b0b65-151">The flags, when present, are set to zero.</span></span>

 

 
