---
title: Unioni RPC
description: Unioni incapsulate e non incapsulate e relativo formato con RPC (Remote Procedure Call).
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f35f0ff23132705330bf1f8566443ac8aa81d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473163"
---
# <a name="rpc-unions"></a><span data-ttu-id="833ff-103">Unioni RPC</span><span class="sxs-lookup"><span data-stu-id="833ff-103">RPC unions</span></span>

<span data-ttu-id="833ff-104">Sia le unioni incapsulate che quelle non incapsulate condividono un \_ selettore di Unione ARM comune \_<> formato:</span><span class="sxs-lookup"><span data-stu-id="833ff-104">Both encapsulated and nonencapsulated unions share a common union\_arm\_selector<> format:</span></span>

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

<span data-ttu-id="833ff-105">Il \_ campo Union arms<2> è costituito da due parti.</span><span class="sxs-lookup"><span data-stu-id="833ff-105">The union\_arms<2> field consists of two parts.</span></span> <span data-ttu-id="833ff-106">Se l'Unione è un'Unione di stile MIDL 1,0, i 4 bit superiori contengono l'allineamento del ARM di Unione (allineamento del braccio allineato più grande).</span><span class="sxs-lookup"><span data-stu-id="833ff-106">If the union is a MIDL 1.0 style union, the upper 4 bits contain the alignment of the union arm (alignment of greatest aligned arm).</span></span> <span data-ttu-id="833ff-107">In caso contrario, i 4 bit superiori sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="833ff-107">Otherwise the upper 4 bits are zero.</span></span> <span data-ttu-id="833ff-108">I 12 bit inferiori contengono il numero di bracci nell'Unione.</span><span class="sxs-lookup"><span data-stu-id="833ff-108">The lower 12 bits contain the number of arms in the union.</span></span> <span data-ttu-id="833ff-109">In altre parole:</span><span class="sxs-lookup"><span data-stu-id="833ff-109">In other words:</span></span>

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

<span data-ttu-id="833ff-110">La descrizione dell'offset \_ a \_ ARM \_<2> i campi contengono un offset con segno relativo alla descrizione del tipo del ARM.</span><span class="sxs-lookup"><span data-stu-id="833ff-110">The offset\_to\_arm\_description<2> fields contain a relative signed offset to the arm's type description.</span></span> <span data-ttu-id="833ff-111">Tuttavia, il campo è sovraccarico con ottimizzazione per i tipi semplici.</span><span class="sxs-lookup"><span data-stu-id="833ff-111">However, the field is overloaded with optimization for simple types.</span></span> <span data-ttu-id="833ff-112">Per questi, il byte superiore di questo campo offset è FC \_ Magic \_ Union \_ byte (0x80) e il byte più basso di short è il tipo di carattere di formato effettivo del ARM.</span><span class="sxs-lookup"><span data-stu-id="833ff-112">For these, the upper byte of this offset field is FC\_MAGIC\_UNION\_BYTE (0x80) and the lower byte of the short is the actual format character type of the arm.</span></span> <span data-ttu-id="833ff-113">Di conseguenza, sono disponibili due intervalli per i valori di offset: "80 *XX*" significa che *XX* è una stringa di formato del tipo. e tutto il resto entro l'intervallo (80 FF...</span><span class="sxs-lookup"><span data-stu-id="833ff-113">As such, there are two ranges for the offset values: "80 *xx*" means that *xx* is a type format string; and everything else within range (80 FF ..</span></span> <span data-ttu-id="833ff-114">7F FF) indica un offset effettivo.</span><span class="sxs-lookup"><span data-stu-id="833ff-114">7f FF) means an actual offset.</span></span> <span data-ttu-id="833ff-115">Questa operazione rende gli offset dall'intervallo <80 00.</span><span class="sxs-lookup"><span data-stu-id="833ff-115">This makes offsets from range <80 00 ..</span></span> <span data-ttu-id="833ff-116">80 FF non > disponibili come offset.</span><span class="sxs-lookup"><span data-stu-id="833ff-116">80 FF > unavailable as offsets.</span></span> <span data-ttu-id="833ff-117">Il compilatore verifica che a partire da MIDL versione 5.1.164.</span><span class="sxs-lookup"><span data-stu-id="833ff-117">The compiler checks that as of MIDL version 5.1.164.</span></span>

<span data-ttu-id="833ff-118">Il \_ campo Default ARM \_ Description<2> indica il tipo di ARM Union per l'ARM predefinito, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="833ff-118">The default\_arm\_description<2> field indicates the type of union arm for the default arm, if any.</span></span> <span data-ttu-id="833ff-119">Se non è specificato un ARM predefinito per l'Unione, la descrizione predefinita di \_ arm \_<2> campo è 0xFFFF e viene generata un'eccezione se il \_ valore dell'opzione non corrisponde ad alcuno dei valori del case ARM.</span><span class="sxs-lookup"><span data-stu-id="833ff-119">If there is no default arm specified for the union then the default\_arm\_description<2> field is 0xFFFF and an exception is raised if the switch\_is value does not match any of the arm case values.</span></span> <span data-ttu-id="833ff-120">Se il ARM predefinito è specificato ma vuoto, il campo Default \_ ARM \_ Description<2> è zero.</span><span class="sxs-lookup"><span data-stu-id="833ff-120">If the default arm is specified but empty, then the default\_arm\_description<2> field is zero.</span></span> <span data-ttu-id="833ff-121">In caso contrario \_ , il campo Default ARM \_ Description<2> ha la stessa semantica dell'offset \_ a \_ arm \_ Description<2> Fields.</span><span class="sxs-lookup"><span data-stu-id="833ff-121">Otherwise the default\_arm\_description<2> field has the same semantics as the offset\_to\_arm\_description<2> fields.</span></span>

<span data-ttu-id="833ff-122">Di seguito è riportato un riepilogo:</span><span class="sxs-lookup"><span data-stu-id="833ff-122">The following is a summary:</span></span>

-   <span data-ttu-id="833ff-123">0: valore predefinito vuoto</span><span class="sxs-lookup"><span data-stu-id="833ff-123">0 - empty default</span></span>
-   <span data-ttu-id="833ff-124">FFFF-nessun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="833ff-124">FFFF - no default</span></span>
-   <span data-ttu-id="833ff-125">80xx-tipo semplice</span><span class="sxs-lookup"><span data-stu-id="833ff-125">80xx - simple type</span></span>
-   <span data-ttu-id="833ff-126">altro offset relativo</span><span class="sxs-lookup"><span data-stu-id="833ff-126">other - relative offset</span></span>

## <a name="encapsulated-unions"></a><span data-ttu-id="833ff-127">Unioni incapsulate</span><span class="sxs-lookup"><span data-stu-id="833ff-127">Encapsulated Unions</span></span>

<span data-ttu-id="833ff-128">Un'Unione incapsulata deriva da una speciale sintassi di Unione in IDL.</span><span class="sxs-lookup"><span data-stu-id="833ff-128">An encapsulated union comes from a special union syntax in IDL.</span></span> <span data-ttu-id="833ff-129">In realtà, un'Unione incapsulata è una struttura di aggregazione con un campo discriminante all'inizio della struttura e l'Unione come unico altro membro.</span><span class="sxs-lookup"><span data-stu-id="833ff-129">Effectively, an encapsulated union is a bundle structure with a discriminant field at the beginning of the structure and the union as the only other member.</span></span>

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

<span data-ttu-id="833ff-130">Il tipo di opzione di un'Unione incapsulata \_<1> campo è costituito da due parti.</span><span class="sxs-lookup"><span data-stu-id="833ff-130">An encapsulated union's switch\_type<1> field has two parts.</span></span> <span data-ttu-id="833ff-131">Il morso inferiore fornisce il tipo di Commuter effettivo e il bocconcino superiore fornisce l'incremento della memoria per eseguire un'istruzione/routine che indica che il puntatore di memoria deve essere incrementato per saltare oltre l'opzione \_ è Field, che include la spaziatura interna tra il \_ campo switch is () della struttura costruita dallo stub e il campo Union effettivo.</span><span class="sxs-lookup"><span data-stu-id="833ff-131">The lower nibble provides the actual switch type, and the upper nibble provides the memory increment to step over that is an amount that the memory pointer must be incremented to skip past the switch\_is field, which includes any padding between the switch\_is() field of the stub-constructed structure and the actual union field.</span></span>

<span data-ttu-id="833ff-132">Le \_ dimensioni della memoria<2> campo sono solo le dimensioni dell'Unione ed è identica alle unioni non incapsulate.</span><span class="sxs-lookup"><span data-stu-id="833ff-132">The memory\_size<2> field is the size of the union only, and is identical to nonencapsulated unions.</span></span> <span data-ttu-id="833ff-133">Per ottenere la dimensione totale della struttura che contiene l'Unione, aggiungere la dimensione della memoria \_<2> all'incremento della memoria per eseguire un'istruzione/routine, ovvero al morso superiore del tipo di commutere \_<1 campo> e quindi allinearlo in base all'allineamento corrispondente all'incremento.</span><span class="sxs-lookup"><span data-stu-id="833ff-133">To obtain the total size of the structure that contains the union, add memory\_size<2> to memory increment to step over, that is to the upper nibble of the switch\_type<1> field, then align by the alignment corresponding to the increment.</span></span>

## <a name="nonencapsulated-unions"></a><span data-ttu-id="833ff-134">Unioni non incapsulate</span><span class="sxs-lookup"><span data-stu-id="833ff-134">Nonencapsulated Unions</span></span>

<span data-ttu-id="833ff-135">Un'Unione non incapsulata è una situazione tipica in cui un'Unione è un argomento o un campo e l'opzione è un altro argomento o campo, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="833ff-135">A nonencapsulated union is a typical situation where a union is one argument or field and the switch is another argument or field, respectively.</span></span>

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

<span data-ttu-id="833ff-136">Dove:</span><span class="sxs-lookup"><span data-stu-id="833ff-136">Where:</span></span>

<span data-ttu-id="833ff-137">Il \_ tipo di opzione<1> campo è un carattere di formato per discriminante.</span><span class="sxs-lookup"><span data-stu-id="833ff-137">The switch\_type<1> field is a format character for the discriminant.</span></span>

<span data-ttu-id="833ff-138">L'opzione \_ è \_ descrittore<> campo è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="833ff-138">The switch\_is\_descriptor<> field is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="833ff-139">Tuttavia, per l'opzione \_ è \_ Description<>, se l'Unione è incorporata in una struttura, il campo offset dell'opzione \_ è \_ Description<> è l'offset per l'opzione \_ è il campo dalla posizione dell'Unione nella struttura (non dall'inizio della struttura).</span><span class="sxs-lookup"><span data-stu-id="833ff-139">However, for the switch\_is\_description<>, if the union is embedded in a structure, the offset field of the switch\_is\_description<> is the offset to the switch\_is field from the union's position in the structure (not from the beginning of the structure).</span></span>

<span data-ttu-id="833ff-140">Il \_ campo offset \_ per \_ size \_ e \_ Descrizione ARM<2> fornisce l'offset alle dimensioni dell'Unione e alla descrizione ARM, che è identica a quella per le unioni incapsulate e viene condivisa da tutte le unioni non incapsulate dello stesso tipo:</span><span class="sxs-lookup"><span data-stu-id="833ff-140">The offset\_to\_size\_and\_arm\_description<2> field gives the offset to the union's size and arm description, which is identical to that for encapsulated unions and is shared by all nonencapsulated unions of the same type :</span></span>

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 