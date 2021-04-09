---
title: Puntatori (RPC)
description: Pointers
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cabf5109506bc1e194a39c809bfb43a8f952fbf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118758"
---
# <a name="pointers-rpc"></a><span data-ttu-id="bc8a8-103">Puntatori (RPC)</span><span class="sxs-lookup"><span data-stu-id="bc8a8-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="bc8a8-104">Puntatori comuni</span><span class="sxs-lookup"><span data-stu-id="bc8a8-104">Common Pointers</span></span>

<span data-ttu-id="bc8a8-105">Un puntatore comune è definito come tutto tranne i puntatori di interfaccia e i puntatori di conteggio dei byte.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="bc8a8-106">Esistono due possibili layout per la descrizione:</span><span class="sxs-lookup"><span data-stu-id="bc8a8-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="bc8a8-107">–oppure–</span><span class="sxs-lookup"><span data-stu-id="bc8a8-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="bc8a8-108">Il primo formato viene usato se il puntatore è un puntatore a un tipo semplice o a un puntatore di stringa non ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="bc8a8-109">Il secondo formato viene usato per i puntatori a tutti gli altri tipi.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="bc8a8-110">Gli attributi del puntatore indicano il layout della descrizione con il \_ flag del puntatore semplice FC \_ .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="bc8a8-111">\_il tipo di puntatore<1> è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="bc8a8-112">Formato carattere</span><span class="sxs-lookup"><span data-stu-id="bc8a8-112">Format character</span></span> | <span data-ttu-id="bc8a8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc8a8-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="bc8a8-114">\_RP FC</span><span class="sxs-lookup"><span data-stu-id="bc8a8-114">FC\_RP</span></span>           | <span data-ttu-id="bc8a8-115">Puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="bc8a8-116">FC \_ attivo</span><span class="sxs-lookup"><span data-stu-id="bc8a8-116">FC\_UP</span></span>           | <span data-ttu-id="bc8a8-117">Puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="bc8a8-118">\_FP FC</span><span class="sxs-lookup"><span data-stu-id="bc8a8-118">FC\_FP</span></span>           | <span data-ttu-id="bc8a8-119">Puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-119">A full pointer.</span></span>                          |
| <span data-ttu-id="bc8a8-120">\_op FC</span><span class="sxs-lookup"><span data-stu-id="bc8a8-120">FC\_OP</span></span>           | <span data-ttu-id="bc8a8-121">Puntatore univoco in un'interfaccia dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="bc8a8-122">Il motivo per distinguere FC \_ op è semantico: nelle interfacce oggetto, un \[ puntatore out \] deve essere liberato prima di eseguire l'unmarshalling di un nuovo oggetto e l'assegnazione di un nuovo valore del puntatore.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="bc8a8-123">Gli \_ attributi del puntatore<1> possono avere uno dei flag mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="bc8a8-124">Flag</span><span class="sxs-lookup"><span data-stu-id="bc8a8-124">Flag</span></span> | <span data-ttu-id="bc8a8-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc8a8-125">Description</span></span>              |                                                                                                                                                                                                                                       |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8a8-126">01</span><span class="sxs-lookup"><span data-stu-id="bc8a8-126">01</span></span>   | <span data-ttu-id="bc8a8-127">FC \_ allocare \_ tutti i \_ nodi</span><span class="sxs-lookup"><span data-stu-id="bc8a8-127">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="bc8a8-128">Il puntatore è parte di uno schema di allocazione (tutti i \_ nodi).</span><span class="sxs-lookup"><span data-stu-id="bc8a8-128">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="bc8a8-129">02</span><span class="sxs-lookup"><span data-stu-id="bc8a8-129">02</span></span>   | <span data-ttu-id="bc8a8-130">FC \_ non \_ disponibile</span><span class="sxs-lookup"><span data-stu-id="bc8a8-130">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="bc8a8-131">Puntatore allocate (non \_ gratuito).</span><span class="sxs-lookup"><span data-stu-id="bc8a8-131">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="bc8a8-132">04</span><span class="sxs-lookup"><span data-stu-id="bc8a8-132">04</span></span>   | <span data-ttu-id="bc8a8-133">\_allocati FC \_ nello \_ stack</span><span class="sxs-lookup"><span data-stu-id="bc8a8-133">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="bc8a8-134">Puntatore il cui referente viene allocato nello stack dello stub.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-134">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="bc8a8-135">08</span><span class="sxs-lookup"><span data-stu-id="bc8a8-135">08</span></span>   | <span data-ttu-id="bc8a8-136">\_puntatore semplice \_ FC</span><span class="sxs-lookup"><span data-stu-id="bc8a8-136">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="bc8a8-137">Puntatore a un tipo semplice o a una stringa conforme non dimensionata.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-137">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="bc8a8-138">Questo flag impostato indica il layout della descrizione del puntatore come il layout del puntatore semplice descritto in precedenza; in caso contrario, viene indicato il formato del descrittore con l'offset.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-138">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="bc8a8-139">10</span><span class="sxs-lookup"><span data-stu-id="bc8a8-139">10</span></span>   | <span data-ttu-id="bc8a8-140">\_Deref puntatore \_ FC</span><span class="sxs-lookup"><span data-stu-id="bc8a8-140">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="bc8a8-141">Puntatore che deve essere dereferenziato prima di gestire il referente del puntatore.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-141">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="bc8a8-142">I puntatori con dimensione \_ è (), il valore Max \_ è (), length \_ è (), Last \_ è () e/o First \_ is () viene applicato a tali stringhe di formato identico a un puntatore a una matrice del tipo appropriato (ad esempio, una matrice conforme se size \_ is () viene applicato, una matrice variabile conforme se size \_ è () e \_ viene applicata la lunghezza.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-142">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="bc8a8-143">Puntatori a interfaccia</span><span class="sxs-lookup"><span data-stu-id="bc8a8-143">Interface Pointers</span></span>

<span data-ttu-id="bc8a8-144">Una stringa di formato puntatore a interfaccia a oggetti presenta uno dei due formati, a seconda che l'IID corrispondente sia noto al compilatore.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-144">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="bc8a8-145">Un puntatore di interfaccia con un IID costante presenta la descrizione seguente:</span><span class="sxs-lookup"><span data-stu-id="bc8a8-145">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="bc8a8-146">L'IID<16> parte è l'IID effettivo per il puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-146">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="bc8a8-147">L'IID viene scritto nella stringa di formato in un formato identico alla struttura di dati GUID: Long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-147">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="bc8a8-148">Viene applicata la descrizione di un puntatore a interfaccia con IID \_ ():</span><span class="sxs-lookup"><span data-stu-id="bc8a8-148">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="bc8a8-149">La descrizione dell'IID \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-149">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="bc8a8-150">Il valore calcolato dalla funzione **NdrComputeConformance** è il puntatore IID.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-150">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="bc8a8-151">Puntatori conteggio byte</span><span class="sxs-lookup"><span data-stu-id="bc8a8-151">Byte Count Pointers</span></span>

<span data-ttu-id="bc8a8-152">I puntatori al numero di byte sono correlati a un attributo di ottimizzazione speciale denominato \[ **\_ conteggio byte** \] .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-152">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="bc8a8-153">Vengono usati i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc8a8-153">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="bc8a8-154">e</span><span class="sxs-lookup"><span data-stu-id="bc8a8-154">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="bc8a8-155">La descrizione del conteggio dei byte \_ \_<> è un descrittore di correlazione e ha 4 o 6 byte, a seconda che venga usato [**/robust**](/windows/desktop/Midl/-robust) .</span><span class="sxs-lookup"><span data-stu-id="bc8a8-155">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="bc8a8-156">La descrizione del puntatore \_<> è una descrizione del tipo di puntatore.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-156">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
