---
title: Puntatori (RPC)
description: Informazioni su un puntatore comune RPC, definito come qualsiasi elemento diverso da puntatori a interfaccia e puntatori al conteggio dei byte.
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119706"
---
# <a name="pointers-rpc"></a><span data-ttu-id="12efe-103">Puntatori (RPC)</span><span class="sxs-lookup"><span data-stu-id="12efe-103">Pointers (RPC)</span></span>

## <a name="common-pointers"></a><span data-ttu-id="12efe-104">Puntatori comuni</span><span class="sxs-lookup"><span data-stu-id="12efe-104">Common Pointers</span></span>

<span data-ttu-id="12efe-105">Un puntatore comune è definito come qualsiasi elemento diverso da puntatori a interfaccia e puntatori al conteggio dei byte.</span><span class="sxs-lookup"><span data-stu-id="12efe-105">A common pointer is defined as everything other than interface pointers and byte count pointers.</span></span>

<span data-ttu-id="12efe-106">Esistono due possibili layout per la descrizione:</span><span class="sxs-lookup"><span data-stu-id="12efe-106">There are two possible layouts for the description:</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

<span data-ttu-id="12efe-107">–oppure–</span><span class="sxs-lookup"><span data-stu-id="12efe-107">–or–</span></span>

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

<span data-ttu-id="12efe-108">Il primo formato viene usato se il puntatore è un puntatore a un tipo semplice o a un puntatore di stringa non di tipo grande.</span><span class="sxs-lookup"><span data-stu-id="12efe-108">The first format is used if the pointer is a pointer to a simple type or a nonsized string pointer.</span></span> <span data-ttu-id="12efe-109">Il secondo formato viene usato per i puntatori a tutti gli altri tipi.</span><span class="sxs-lookup"><span data-stu-id="12efe-109">The second format is used for pointers to all other types.</span></span> <span data-ttu-id="12efe-110">Gli attributi del puntatore indicano il layout della descrizione con il \_ flag FC SIMPLE \_ POINTER.</span><span class="sxs-lookup"><span data-stu-id="12efe-110">Pointer attributes indicate which description layout it is with the FC\_SIMPLE\_POINTER flag.</span></span>

<span data-ttu-id="12efe-111">Il \_ tipo di<1> è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="12efe-111">pointer\_type<1> is one of the following.</span></span>



| <span data-ttu-id="12efe-112">Formatta carattere</span><span class="sxs-lookup"><span data-stu-id="12efe-112">Format character</span></span> | <span data-ttu-id="12efe-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12efe-113">Description</span></span>                              |
|------------------|------------------------------------------|
| <span data-ttu-id="12efe-114">FC \_ RP</span><span class="sxs-lookup"><span data-stu-id="12efe-114">FC\_RP</span></span>           | <span data-ttu-id="12efe-115">Puntatore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="12efe-115">A reference pointer.</span></span>                     |
| <span data-ttu-id="12efe-116">FC \_ UP</span><span class="sxs-lookup"><span data-stu-id="12efe-116">FC\_UP</span></span>           | <span data-ttu-id="12efe-117">Puntatore univoco.</span><span class="sxs-lookup"><span data-stu-id="12efe-117">A unique pointer.</span></span>                        |
| <span data-ttu-id="12efe-118">FC \_ FP</span><span class="sxs-lookup"><span data-stu-id="12efe-118">FC\_FP</span></span>           | <span data-ttu-id="12efe-119">Puntatore completo.</span><span class="sxs-lookup"><span data-stu-id="12efe-119">A full pointer.</span></span>                          |
| <span data-ttu-id="12efe-120">FC \_ OP</span><span class="sxs-lookup"><span data-stu-id="12efe-120">FC\_OP</span></span>           | <span data-ttu-id="12efe-121">Puntatore univoco in un'interfaccia oggetto.</span><span class="sxs-lookup"><span data-stu-id="12efe-121">A unique pointer in an object interface.</span></span> |



 

<span data-ttu-id="12efe-122">Il motivo per distinguere FC OP è semantico: nelle interfacce oggetto, un puntatore in uscita deve essere liberato prima di eseguire \_ l'unmarsshaling di un nuovo oggetto e assegnare un nuovo valore del \[ \] puntatore.</span><span class="sxs-lookup"><span data-stu-id="12efe-122">The reason to distinguish FC\_OP is semantic: in object interfaces, an \[in,out\] pointer should be freed before unmarshaling a new object and assigning a new pointer value.</span></span>

<span data-ttu-id="12efe-123">Gli \_ attributi<1> possono avere uno qualsiasi dei flag illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="12efe-123">Pointer\_attributes<1> can have any of the flags shown in the following table.</span></span>



| <span data-ttu-id="12efe-124">Attributo</span><span class="sxs-lookup"><span data-stu-id="12efe-124">Attribute</span></span> | <span data-ttu-id="12efe-125">Flag</span><span class="sxs-lookup"><span data-stu-id="12efe-125">Flag</span></span>              | <span data-ttu-id="12efe-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12efe-126">Description</span></span>                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12efe-127">01</span><span class="sxs-lookup"><span data-stu-id="12efe-127">01</span></span>   | <span data-ttu-id="12efe-128">FC \_ ALLOCATE \_ ALL \_ NODES</span><span class="sxs-lookup"><span data-stu-id="12efe-128">FC\_ALLOCATE\_ALL\_NODES</span></span> | <span data-ttu-id="12efe-129">Il puntatore fa parte di uno schema di allocazione allocate(tutti \_ i nodi).</span><span class="sxs-lookup"><span data-stu-id="12efe-129">The pointer is a part of an allocate(all\_nodes) allocation scheme.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="12efe-130">02</span><span class="sxs-lookup"><span data-stu-id="12efe-130">02</span></span>   | <span data-ttu-id="12efe-131">FC \_ DONT \_ FREE</span><span class="sxs-lookup"><span data-stu-id="12efe-131">FC\_DONT\_FREE</span></span>           | <span data-ttu-id="12efe-132">Puntatore allocate(don't \_ free).</span><span class="sxs-lookup"><span data-stu-id="12efe-132">An allocate(dont\_free) pointer.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="12efe-133">04</span><span class="sxs-lookup"><span data-stu-id="12efe-133">04</span></span>   | <span data-ttu-id="12efe-134">FC \_ ALLOCED \_ ON \_ STACK</span><span class="sxs-lookup"><span data-stu-id="12efe-134">FC\_ALLOCED\_ON\_STACK</span></span>   | <span data-ttu-id="12efe-135">Puntatore il cui riferimento viene allocato nello stack dello stub.</span><span class="sxs-lookup"><span data-stu-id="12efe-135">A pointer whose referent is allocated on the stub's stack.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="12efe-136">08</span><span class="sxs-lookup"><span data-stu-id="12efe-136">08</span></span>   | <span data-ttu-id="12efe-137">PUNTATORE \_ FC \_ SEMPLICE</span><span class="sxs-lookup"><span data-stu-id="12efe-137">FC\_SIMPLE\_POINTER</span></span>      | <span data-ttu-id="12efe-138">Puntatore a un tipo semplice o a una stringa non conforme.</span><span class="sxs-lookup"><span data-stu-id="12efe-138">A pointer to a simple type or nonsized conformant string.</span></span> <span data-ttu-id="12efe-139">Questo flag impostato indica il layout della descrizione del puntatore come layout del puntatore semplice descritto in precedenza. In caso contrario, viene indicato il formato del descrittore con l'offset.</span><span class="sxs-lookup"><span data-stu-id="12efe-139">This flag being set indicates layout of the pointer description as the simple pointer layout described above, otherwise the descriptor format with the offset is indicated.</span></span> |
| <span data-ttu-id="12efe-140">10</span><span class="sxs-lookup"><span data-stu-id="12efe-140">10</span></span>   | <span data-ttu-id="12efe-141">DEREF \_ \_ PUNTATORE FC</span><span class="sxs-lookup"><span data-stu-id="12efe-141">FC\_POINTER\_DEREF</span></span>       | <span data-ttu-id="12efe-142">Puntatore che deve essere dereferenziato prima di gestire il riferimento del puntatore.</span><span class="sxs-lookup"><span data-stu-id="12efe-142">A pointer that must be dereferenced before handling the pointer's referent.</span></span>                                                                                                                                                           |



 

<span data-ttu-id="12efe-143">I puntatori con size \_ is(), max \_ is(), length \_ is(), last \_ is() e/o first is() applicati hanno descrizioni di stringa di formato identiche a un puntatore a una matrice del tipo appropriato \_ (ad esempio, \_ \_ una matrice conforme se size is() viene applicato, una matrice variabile conforme se size is() e length viene \_ applicato).</span><span class="sxs-lookup"><span data-stu-id="12efe-143">Pointers that have size\_is(), max\_is(), length\_is(), last\_is(), and/or first\_is() applied to them have format string descriptions identical to a pointer to an array of the appropriate type (for example, a conformant array if size\_is() is applied, a conformant varying array if size\_is() and length\_is are applied).</span></span>

## <a name="interface-pointers"></a><span data-ttu-id="12efe-144">Puntatori a interfaccia</span><span class="sxs-lookup"><span data-stu-id="12efe-144">Interface Pointers</span></span>

<span data-ttu-id="12efe-145">Una stringa di formato del puntatore a interfaccia a oggetti ha uno dei due formati seguenti, a seconda che l'IID corrispondente sia noto al compilatore.</span><span class="sxs-lookup"><span data-stu-id="12efe-145">An object interface pointer format string has one of two formats, depending on whether the corresponding IID is known to the compiler.</span></span>

<span data-ttu-id="12efe-146">Un puntatore a interfaccia con un IID costante ha la descrizione seguente:</span><span class="sxs-lookup"><span data-stu-id="12efe-146">An interface pointer with a constant IID has the following description:</span></span>

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

<span data-ttu-id="12efe-147">L'iid<16> parte è l'IID effettivo per il puntatore di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="12efe-147">The iid<16> part is the actual IID for the interface pointer.</span></span> <span data-ttu-id="12efe-148">L'iid viene scritto nella stringa di formato in un formato identico alla struttura dei dati GUID: long, short, short, char \[ 8 \] .</span><span class="sxs-lookup"><span data-stu-id="12efe-148">The iid is written to the format string in a format identical to the GUID data structure: long, short, short, char \[8\].</span></span>

<span data-ttu-id="12efe-149">La descrizione di un puntatore a interfaccia con iid \_ is() applicata è:</span><span class="sxs-lookup"><span data-stu-id="12efe-149">The description of an interface pointer with iid\_is() applied to it is:</span></span>

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

<span data-ttu-id="12efe-150">La descrizione iid<> descrittore di correlazione e ha 4 o 6 byte a seconda che \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno utilizzato.</span><span class="sxs-lookup"><span data-stu-id="12efe-150">The iid\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span> <span data-ttu-id="12efe-151">Il valore calcolato dalla **funzione NdrComputeConformance** è il puntatore IID.</span><span class="sxs-lookup"><span data-stu-id="12efe-151">The value calculated by the **NdrComputeConformance** function is the IID pointer.</span></span>

## <a name="byte-count-pointers"></a><span data-ttu-id="12efe-152">Puntatori di conteggio byte</span><span class="sxs-lookup"><span data-stu-id="12efe-152">Byte Count Pointers</span></span>

<span data-ttu-id="12efe-153">I puntatori al conteggio dei byte sono correlati a uno speciale attributo di ottimizzazione denominato \[ **byte \_ count** \] .</span><span class="sxs-lookup"><span data-stu-id="12efe-153">Byte count pointers relate to a special optimization attribute called \[**byte\_count**\].</span></span> <span data-ttu-id="12efe-154">Vengono usati i formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="12efe-154">The following formats are used:</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

<span data-ttu-id="12efe-155">–and:</span><span class="sxs-lookup"><span data-stu-id="12efe-155">–and –</span></span>

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<span data-ttu-id="12efe-156">La descrizione del<> byte è un descrittore di correlazione e ha 4 o 6 byte a seconda che \_ \_ [**/robust**](/windows/desktop/Midl/-robust) sia o meno utilizzato.</span><span class="sxs-lookup"><span data-stu-id="12efe-156">The byte\_count\_description<> is a correlation descriptor and has 4 or 6 bytes depending on whether [**/robust**](/windows/desktop/Midl/-robust) is used.</span></span>

<span data-ttu-id="12efe-157">La descrizione \_<> pointee è una descrizione del tipo pointee.</span><span class="sxs-lookup"><span data-stu-id="12efe-157">The pointee\_description<> is a description of the pointee type.</span></span>

 

 
