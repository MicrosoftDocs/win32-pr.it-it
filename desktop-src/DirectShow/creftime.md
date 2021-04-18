---
description: La classe CRefTime è una classe helper che consente di gestire i tempi di riferimento.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Classe CRefTime (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327926"
---
# <a name="creftime-class"></a><span data-ttu-id="89d02-103">Classe CRefTime</span><span class="sxs-lookup"><span data-stu-id="89d02-103">CRefTime class</span></span>

![gerarchia di classi creftime](images/cutil05.png)

<span data-ttu-id="89d02-105">La `CRefTime` classe è una classe helper per la gestione dei tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="89d02-105">The `CRefTime` class is a helper class for managing reference times.</span></span>

<span data-ttu-id="89d02-106">Un' *ora di riferimento* è un'unità di tempo rappresentata in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="89d02-106">A *reference time* is a unit of time represented in 100-nanosecond units.</span></span> <span data-ttu-id="89d02-107">Questa classe condivide lo stesso layout di dati del tipo di dati [**\_ time di riferimento**](reference-time.md) , ma aggiunge alcuni metodi e operatori che forniscono funzioni di confronto, conversione e aritmetica.</span><span class="sxs-lookup"><span data-stu-id="89d02-107">This class shares the same data layout as the [**REFERENCE\_TIME**](reference-time.md) data type, but adds some methods and operators that provide comparison, conversion, and arithmetic functions.</span></span> <span data-ttu-id="89d02-108">Per altre informazioni sui tempi di riferimento, vedere [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="89d02-108">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>



| <span data-ttu-id="89d02-109">Variabili membro pubblico</span><span class="sxs-lookup"><span data-stu-id="89d02-109">Public Member Variables</span></span>                                                 | <span data-ttu-id="89d02-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89d02-110">Description</span></span>                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="89d02-111">**\_ora m**</span><span class="sxs-lookup"><span data-stu-id="89d02-111">**m\_time**</span></span>](creftime-m-time.md)                                      | <span data-ttu-id="89d02-112">Specifica il valore dell' **\_ ora di riferimento** .</span><span class="sxs-lookup"><span data-stu-id="89d02-112">Specifies the **REFERENCE\_TIME** value.</span></span>              |
| <span data-ttu-id="89d02-113">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="89d02-113">Public Methods</span></span>                                                          | <span data-ttu-id="89d02-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89d02-114">Description</span></span>                                           |
| [<span data-ttu-id="89d02-115">**CRefTime**</span><span class="sxs-lookup"><span data-stu-id="89d02-115">**CRefTime**</span></span>](creftime-creftime.md)                                   | <span data-ttu-id="89d02-116">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="89d02-116">Constructor method.</span></span>                                   |
| [<span data-ttu-id="89d02-117">**Getunits**</span><span class="sxs-lookup"><span data-stu-id="89d02-117">**GetUnits**</span></span>](creftime-getunits.md)                                   | <span data-ttu-id="89d02-118">Recupera l'ora di riferimento in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="89d02-118">Retrieves the reference time in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="89d02-119">**Millisecondi**</span><span class="sxs-lookup"><span data-stu-id="89d02-119">**Millisecs**</span></span>](creftime-millisecs.md)                                 | <span data-ttu-id="89d02-120">Converte l'ora di riferimento in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="89d02-120">Converts the reference time to milliseconds.</span></span>          |
| <span data-ttu-id="89d02-121">Operatori</span><span class="sxs-lookup"><span data-stu-id="89d02-121">Operators</span></span>                                                               | <span data-ttu-id="89d02-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89d02-122">Description</span></span>                                           |
| [<span data-ttu-id="89d02-123">**tempo riferimento operatore \_ ()**</span><span class="sxs-lookup"><span data-stu-id="89d02-123">**operator REFERENCE\_TIME()**</span></span>](creftime-operator-reference-time-.md) | <span data-ttu-id="89d02-124">Esegue il cast dell'oggetto a un tipo di dati **\_ time di riferimento** .</span><span class="sxs-lookup"><span data-stu-id="89d02-124">Casts the object to a **REFERENCE\_TIME** data type.</span></span>  |
| [<span data-ttu-id="89d02-125">**operatore =**</span><span class="sxs-lookup"><span data-stu-id="89d02-125">**operator=**</span></span>](creftime-operator-assign.md)                           | <span data-ttu-id="89d02-126">Assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="89d02-126">Assigns a new reference time.</span></span>                         |
| [<span data-ttu-id="89d02-127">**operatore + =**</span><span class="sxs-lookup"><span data-stu-id="89d02-127">**operator+=**</span></span>](creftime-operator-plus-assign.md)                     | <span data-ttu-id="89d02-128">Aggiunge due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="89d02-128">Adds two reference times.</span></span>                             |
| [<span data-ttu-id="89d02-129">**operatore =**</span><span class="sxs-lookup"><span data-stu-id="89d02-129">**operator =**</span></span>](creftime-operator-minus-assign.md)                    | <span data-ttu-id="89d02-130">Sottrae un'ora di riferimento da un'altra.</span><span class="sxs-lookup"><span data-stu-id="89d02-130">Subtracts one reference time from another.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="89d02-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="89d02-131">Remarks</span></span>

<span data-ttu-id="89d02-132">È possibile che si verifichi un problema con l'utilizzo di questa classe.</span><span class="sxs-lookup"><span data-stu-id="89d02-132">There is a potential pitfall with using this class.</span></span> <span data-ttu-id="89d02-133">Se si applica l'operatore + = con un oggetto **CRefTime** come operando sinistro e una variabile di tipo **Long** come operando destro, il compilatore forza l'operando di destra in modo implicito in un oggetto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="89d02-133">If you apply the += operator with a **CRefTime** object as the left operand and a variable of type **LONG** as the right operand, the compiler will implicitly coerce the right operand into a **CRefTime** object.</span></span> <span data-ttu-id="89d02-134">Questa coercizione usa il costruttore **CRefTime** che converte i millisecondi in \_ unità di tempo di riferimento. di conseguenza, l'operando destro viene moltiplicato per 10.000:</span><span class="sxs-lookup"><span data-stu-id="89d02-134">This coercion uses the **CRefTime** constructor that converts milliseconds into REFERENCE\_TIME units; as a result, the right operand is multiplied by 10,000:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



<span data-ttu-id="89d02-135">Tuttavia, la stessa operazione non viene eseguita utilizzando l'operatore +:</span><span class="sxs-lookup"><span data-stu-id="89d02-135">However, the same thing does not happen using the + operator:</span></span>


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a><span data-ttu-id="89d02-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89d02-136">Requirements</span></span>



| <span data-ttu-id="89d02-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d02-137">Requirement</span></span> | <span data-ttu-id="89d02-138">Valore</span><span class="sxs-lookup"><span data-stu-id="89d02-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d02-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89d02-139">Header</span></span><br/>  | <dl> <span data-ttu-id="89d02-140"><dt>Reftime. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89d02-140"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89d02-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="89d02-141">Library</span></span><br/> | <dl> <span data-ttu-id="89d02-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="89d02-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




