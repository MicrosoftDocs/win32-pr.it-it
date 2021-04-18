---
description: La classe COARefTime converte i tempi di riferimento tra i secondi e le unità 100-nanosecondi.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Classe COARefTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324471"
---
# <a name="coareftime-class"></a><span data-ttu-id="db61c-103">Classe COARefTime</span><span class="sxs-lookup"><span data-stu-id="db61c-103">COARefTime class</span></span>

![gerarchia di classi coareftime](images/cutil05.png)

<span data-ttu-id="db61c-105">La `COARefTime` classe converte i tempi di riferimento tra i secondi e le unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="db61c-105">The `COARefTime` class converts reference times between seconds and 100-nanosecond units.</span></span>

<span data-ttu-id="db61c-106">Questa classe esegue la conversione tra tempi di riferimento compatibili con l'automazione e i tempi di riferimento compatibili con C/C++.</span><span class="sxs-lookup"><span data-stu-id="db61c-106">This class converts between reference times that are compatible with Automation and reference times that are compatible with C/C++.</span></span> <span data-ttu-id="db61c-107">Le interfacce compatibili con l'automazione usano valori **doppi** per rappresentare il tempo in secondi.</span><span class="sxs-lookup"><span data-stu-id="db61c-107">Automation-compatible interfaces use **double** values to represent time in seconds.</span></span> <span data-ttu-id="db61c-108">Altre interfacce usano valori **LONGLONG** a 64 bit per rappresentare l'ora in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="db61c-108">Other interfaces use 64-bit **LONGLONG** values to represent time in 100-nanosecond units.</span></span> <span data-ttu-id="db61c-109">Per questi valori sono definiti i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="db61c-109">The following types are defined for these values:</span></span>

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

<span data-ttu-id="db61c-110">I filtri possono utilizzare la `COARefTime` classe per eseguire la conversione tra i due formati.</span><span class="sxs-lookup"><span data-stu-id="db61c-110">Filters can use the `COARefTime` class to convert between the two formats.</span></span> <span data-ttu-id="db61c-111">Questa classe è derivata dalla classe [**CRefTime**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="db61c-111">This class is derived from the [**CRefTime**](creftime.md) class.</span></span>



| <span data-ttu-id="db61c-112">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="db61c-112">Public Methods</span></span>                                          | <span data-ttu-id="db61c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db61c-113">Description</span></span>                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="db61c-114">**COARefTime**</span><span class="sxs-lookup"><span data-stu-id="db61c-114">**COARefTime**</span></span>](coareftime-coareftime.md)             | <span data-ttu-id="db61c-115">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="db61c-115">Constructor method.</span></span>                                                   |
| <span data-ttu-id="db61c-116">Operatori</span><span class="sxs-lookup"><span data-stu-id="db61c-116">Operators</span></span>                                               | <span data-ttu-id="db61c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db61c-117">Description</span></span>                                                           |
| [<span data-ttu-id="db61c-118">**doppio**</span><span class="sxs-lookup"><span data-stu-id="db61c-118">**double**</span></span>](coareftime-double.md)                     | <span data-ttu-id="db61c-119">Converte l'ora di riferimento in un valore **Double** .</span><span class="sxs-lookup"><span data-stu-id="db61c-119">Converts the reference time to a **double** value.</span></span>                    |
| [<span data-ttu-id="db61c-120">**\_ora riferimento**</span><span class="sxs-lookup"><span data-stu-id="db61c-120">**REFERENCE\_TIME**</span></span>](coareftime-reference-time.md)    | <span data-ttu-id="db61c-121">Esegue il cast dell'oggetto a un valore di **\_ ora di riferimento** .</span><span class="sxs-lookup"><span data-stu-id="db61c-121">Casts the object to a **REFERENCE\_TIME** value.</span></span>                      |
| [<span data-ttu-id="db61c-122">**operatore =**</span><span class="sxs-lookup"><span data-stu-id="db61c-122">**operator =**</span></span>](coareftime-operator-assign.md)        | <span data-ttu-id="db61c-123">Assegna una nuova ora di riferimento.</span><span class="sxs-lookup"><span data-stu-id="db61c-123">Assigns a new reference time.</span></span>                                         |
| [<span data-ttu-id="db61c-124">**operatore = =**</span><span class="sxs-lookup"><span data-stu-id="db61c-124">**operator ==**</span></span>](coareftime-operator-eq.md)           | <span data-ttu-id="db61c-125">Verifica l'uguaglianza tra due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="db61c-125">Tests for equality between two reference times.</span></span>                       |
| [<span data-ttu-id="db61c-126">**operatore! =**</span><span class="sxs-lookup"><span data-stu-id="db61c-126">**operator !=**</span></span>](cmediatype-operator-neq.md)          | <span data-ttu-id="db61c-127">Verifica la disuguaglianza tra due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="db61c-127">Tests for inequality between two reference times.</span></span>                     |
| [<span data-ttu-id="db61c-128">**operatore <**</span><span class="sxs-lookup"><span data-stu-id="db61c-128">**operator <**</span></span>](coareftime-operator-lt.md)         | <span data-ttu-id="db61c-129">Verifica se un tempo di riferimento è minore di un altro.</span><span class="sxs-lookup"><span data-stu-id="db61c-129">Tests if one reference time is less than another.</span></span>                     |
| [<span data-ttu-id="db61c-130">**operatore >**</span><span class="sxs-lookup"><span data-stu-id="db61c-130">**operator >**</span></span>](coareftime-operator-gt.md)         | <span data-ttu-id="db61c-131">Verifica se un tempo di riferimento è maggiore di un altro.</span><span class="sxs-lookup"><span data-stu-id="db61c-131">Tests if one reference time is greater than another.</span></span>                  |
| [<span data-ttu-id="db61c-132">**operatore <=**</span><span class="sxs-lookup"><span data-stu-id="db61c-132">**operator <=**</span></span>](coareftime-operator-lteq.md)      | <span data-ttu-id="db61c-133">Verifica se un'ora di riferimento è minore o uguale a un'altra.</span><span class="sxs-lookup"><span data-stu-id="db61c-133">Tests if one reference time is less than or equal to another.</span></span>         |
| [<span data-ttu-id="db61c-134">**operatore >=**</span><span class="sxs-lookup"><span data-stu-id="db61c-134">**operator >=**</span></span>](coareftime-operator-gteq.md)      | <span data-ttu-id="db61c-135">Verifica se un'ora di riferimento è maggiore o uguale a un'altra.</span><span class="sxs-lookup"><span data-stu-id="db61c-135">Tests if one reference time is greater than or equal to another.</span></span>      |
| [<span data-ttu-id="db61c-136">**operatore +**</span><span class="sxs-lookup"><span data-stu-id="db61c-136">**operator +**</span></span>](coareftime-operator-plus.md)          | <span data-ttu-id="db61c-137">Aggiunge due tempi di riferimento.</span><span class="sxs-lookup"><span data-stu-id="db61c-137">Adds two reference times.</span></span>                                             |
| [<span data-ttu-id="db61c-138">\* \* operatore \* \*</span><span class="sxs-lookup"><span data-stu-id="db61c-138">\*\*operator  \*\*</span></span>](coareftime-operator-minus.md)         | <span data-ttu-id="db61c-139">Sottrae un'ora di riferimento da un'altra.</span><span class="sxs-lookup"><span data-stu-id="db61c-139">Subtracts one reference time from another.</span></span>                            |
| [<span data-ttu-id="db61c-140">**operatore + =**</span><span class="sxs-lookup"><span data-stu-id="db61c-140">**operator +=**</span></span>](coareftime-operator-plus-assign.md)  | <span data-ttu-id="db61c-141">Aggiunge due tempi di riferimento e assegna il risultato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="db61c-141">Adds two reference times, and assigns the result to this object.</span></span>      |
| [<span data-ttu-id="db61c-142">**operatore =**</span><span class="sxs-lookup"><span data-stu-id="db61c-142">**operator  =**</span></span>](coareftime-operator-minus-assign.md) | <span data-ttu-id="db61c-143">Sottrae due tempi di riferimento e assegna il risultato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="db61c-143">Subtracts two reference times, and assigns the result to this object.</span></span> |
| [<span data-ttu-id="db61c-144">**operatore \***</span><span class="sxs-lookup"><span data-stu-id="db61c-144">**operator \***</span></span>](coareftime-operator-mult.md)         | <span data-ttu-id="db61c-145">Moltiplica un'ora di riferimento per un valore.</span><span class="sxs-lookup"><span data-stu-id="db61c-145">Multiplies a reference time by a value.</span></span>                               |
| [<span data-ttu-id="db61c-146">**operatore**</span><span class="sxs-lookup"><span data-stu-id="db61c-146">**operator /**</span></span>](coareftime-operator-div.md)           | <span data-ttu-id="db61c-147">Divide un'ora di riferimento per un valore.</span><span class="sxs-lookup"><span data-stu-id="db61c-147">Divides a reference time by a value.</span></span>                                  |



 

## <a name="requirements"></a><span data-ttu-id="db61c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db61c-148">Requirements</span></span>



| <span data-ttu-id="db61c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="db61c-149">Requirement</span></span> | <span data-ttu-id="db61c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="db61c-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db61c-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db61c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="db61c-152"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db61c-152"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db61c-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="db61c-153">Library</span></span><br/> | <dl> <span data-ttu-id="db61c-154"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="db61c-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




