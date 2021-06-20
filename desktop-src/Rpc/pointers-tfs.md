---
title: Puntatori (RPC)
description: Informazioni su un puntatore comune RPC, definito come tutto ciò che è diverso da puntatori a interfaccia e puntatori di conteggio dei byte.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e41a0b6208745b543a9efe2fe22ab090046778
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406594"
---
# <a name="pointers-rpc"></a><span data-ttu-id="76d53-103">Puntatori (RPC)</span><span class="sxs-lookup"><span data-stu-id="76d53-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="76d53-104">Puntatori comuni</span><span class="sxs-lookup"><span data-stu-id="76d53-104">Common Pointers</span></span>

<span data-ttu-id="76d53-105">Un puntatore comune è definito come qualsiasi elemento diverso da puntatori a interfaccia e puntatori di conteggio dei byte.</span><span class="sxs-lookup"><span data-stu-id="76d53-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="76d53-106">Per la descrizione sono disponibili due layout possibili:</span><span class="sxs-lookup"><span data-stu-id="76d53-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="76d53-107">–oppure–</span><span class="sxs-lookup"><span data-stu-id="76d53-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="76d53-108">Il primo formato viene usato se il puntatore è un puntatore a un tipo semplice o a un puntatore di stringa non disized.</span><span class="sxs-lookup"><span data-stu-id="76d53-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="76d53-109">Il secondo formato viene usato per i puntatori a tutti gli altri tipi.</span><span class="sxs-lookup"><span data-stu-id="76d53-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="76d53-110">Gli attributi del puntatore indicano il layout della descrizione con il \_ flag FC SIMPLE \_ POINTER.</span><span class="sxs-lookup"><span data-stu-id="76d53-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="76d53-111">Il \_ tipo di<1> è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="76d53-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="76d53-112">Carattere di formattazione</span><span class="sxs-lookup"><span data-stu-id="76d53-112">Format character</span></span> | <span data-ttu-id="76d53-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76d53-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="76d53-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="76d53-114">FC\_RP</span></span>           | <span data-ttu-id="76d53-115">Puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="76d53-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="76d53-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="76d53-116">FC\_UP</span></span>           | <span data-ttu-id="76d53-117">Puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="76d53-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="76d53-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="76d53-118">FC\_FP</span></span>           | <span data-ttu-id="76d53-119">Puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="76d53-119">A full pointer.</span></span>                          |
| <span data-ttu-id="76d53-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="76d53-120">FC\_OP</span></span>           | <span data-ttu-id="76d53-121">Puntatore univoco in un'interfaccia a oggetti.</span><span class="sxs-lookup"><span data-stu-id="76d53-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="76d53-122">Il motivo per distinguere FC OP è semantico: nelle interfacce oggetto, un puntatore in,out deve essere liberato prima di annullare ilmarshaling di un nuovo oggetto e assegnare un nuovo valore \_ \[ del \] puntatore.</span><span class="sxs-lookup"><span data-stu-id="76d53-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="76d53-123">Gli attributi del<1> possono avere \_ uno qualsiasi dei flag illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="76d53-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="76d53-124">Flag</span><span class="sxs-lookup"><span data-stu-id="76d53-124">Flag</span></span> | <span data-ttu-id="76d53-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76d53-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76d53-126">01</span><span class="sxs-lookup"><span data-stu-id="76d53-126">01</span></span>   | <span data-ttu-id="76d53-127">FC \_ \_ ALLOCA TUTTI I \_ NODI</span><span class="sxs-lookup"><span data-stu-id="76d53-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="76d53-128">Il puntatore fa parte di uno schema di allocazione (tutti \_ i nodi).</span><span class="sxs-lookup"><span data-stu-id="76d53-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="76d53-129">02</span><span class="sxs-lookup"><span data-stu-id="76d53-129">02</span></span>   | <span data-ttu-id="76d53-130">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="76d53-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="76d53-131">Puntatore allocate(don't \_ free).</span><span class="sxs-lookup"><span data-stu-id="76d53-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="76d53-132">04</span><span class="sxs-lookup"><span data-stu-id="76d53-132">04</span></span>   | <span data-ttu-id="76d53-133">FC \_ ALLOCATO \_ NELLO \_ STACK</span><span class="sxs-lookup"><span data-stu-id="76d53-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="76d53-134">Puntatore il cui riferimento è allocato nello stack dello stub.</span><span class="sxs-lookup"><span data-stu-id="76d53-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="76d53-135">08</span><span class="sxs-lookup"><span data-stu-id="76d53-135">08</span></span>   | <span data-ttu-id="76d53-136">PUNTATORE SEMPLICE FC \_ \_</span><span class="sxs-lookup"><span data-stu-id="76d53-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="76d53-137">Puntatore a un tipo semplice o a una stringa conforme non di formato.</span><span class="sxs-lookup"><span data-stu-id="76d53-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="76d53-138">Questo flag impostato indica il layout della descrizione del puntatore come layout del puntatore semplice descritto in precedenza, in caso contrario viene indicato il formato del descrittore con l'offset.</span><span class="sxs-lookup"><span data-stu-id="76d53-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="76d53-139">10</span><span class="sxs-lookup"><span data-stu-id="76d53-139">10</span></span>   | <span data-ttu-id="76d53-140">DEREF \_ DEL \_ PUNTATORE FC</span><span class="sxs-lookup"><span data-stu-id="76d53-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="76d53-141">Puntatore che deve essere dereferenziato prima di gestire il riferimento del puntatore.</span><span class="sxs-lookup"><span data-stu-id="76d53-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="76d53-142">I puntatori con size \_ is(), max \_ is(), length \_ is(), last \_ is() e/o first is() applicati hanno descrizioni di stringa di formato identiche a un puntatore a una matrice del tipo appropriato \_ (ad esempio, \_ \_ una matrice conforme se size is() viene applicata, una matrice variabile conforme se size is() e length vengono \_ applicate).</span><span class="sxs-lookup"><span data-stu-id="76d53-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="76d53-143">Puntatori a interfaccia</span><span class="sxs-lookup"><span data-stu-id="76d53-143">Interface Pointers</span></span>

<span data-ttu-id="76d53-144">Una stringa di formato del puntatore a interfaccia a oggetti ha uno dei due formati, a seconda che l'IID corrispondente sia noto al compilatore.</span><span class="sxs-lookup"><span data-stu-id="76d53-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="76d53-145">Un puntatore a interfaccia con un IID costante ha la descrizione seguente:</span><span class="sxs-lookup"><span data-stu-id="76d53-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="76d53-146">L'iid<16> è l'IID effettivo per il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="76d53-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="76d53-147">L'iid viene scritto nella stringa di formato in un formato identico alla struttura dei dati GUID: long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="76d53-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="76d53-148">La descrizione di un puntatore a interfaccia con iid \_ is() applicata è:</span><span class="sxs-lookup"><span data-stu-id="76d53-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="76d53-149">La descrizione dell'iid<> descrittore di correlazione e ha 4 o 6 byte a seconda che \_ [**sia usato /robust.**](/windows/desktop/Midl/-robust)</span><span class="sxs-lookup"><span data-stu-id="76d53-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="76d53-150">Il valore calcolato dalla **funzione NdrComputeConformance** è il puntatore IID.</span><span class="sxs-lookup"><span data-stu-id="76d53-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="76d53-151">Puntatori di conteggio byte</span><span class="sxs-lookup"><span data-stu-id="76d53-151">Byte Count Pointers</span></span>

<span data-ttu-id="76d53-152">I puntatori di conteggio dei byte sono correlati a uno speciale attributo di ottimizzazione denominato \[ **byte \_ count** \] .</span><span class="sxs-lookup"><span data-stu-id="76d53-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="76d53-153">Vengono usati i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="76d53-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="76d53-154">–e -</span><span class="sxs-lookup"><span data-stu-id="76d53-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="76d53-155">La descrizione del<> byte è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno usato.</span><span class="sxs-lookup"><span data-stu-id="76d53-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="76d53-156">La descrizione \_ del<> pointee è una descrizione del tipo di puntato.</span><span class="sxs-lookup"><span data-stu-id="76d53-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
