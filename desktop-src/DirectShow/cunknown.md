---
description: La classe CUnknown implementa l'interfaccia IUnknown. La maggior parte degli oggetti Component Object Model (COM) in DirectShow derivano da CUnknown.
ms.assetid: 9711d36b-6987-4fb0-a8df-eba94348dc7b
title: Classe CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4818a088119f7cba25ce8a470f63cab722998c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331444"
---
# <a name="cunknown-class"></a><span data-ttu-id="c136f-104">Classe CUnknown</span><span class="sxs-lookup"><span data-stu-id="c136f-104">CUnknown class</span></span>

![gerarchia di classi CUnknown](images/cbase01.png)

<span data-ttu-id="c136f-106">La classe **CUnknown** implementa l'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="c136f-106">The **CUnknown** class implements the **IUnknown** interface.</span></span> <span data-ttu-id="c136f-107">La maggior parte degli oggetti Component Object Model (COM) in DirectShow derivano da **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c136f-107">Most Component Object Model (COM) objects in DirectShow derive from **CUnknown**.</span></span>

<span data-ttu-id="c136f-108">Se si implementa un oggetto COM, potrebbe essere necessario derivarlo da **CUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c136f-108">If you implement a COM object, you might want to derive it from **CUnknown**.</span></span> <span data-ttu-id="c136f-109">La derivazione da **CUnknown** fornisce un'implementazione thread-safe e consente di evitare il problema di implementare **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c136f-109">Deriving from **CUnknown** provides a thread-safe implementation, and saves you the trouble of implementing **IUnknown**.</span></span>

<span data-ttu-id="c136f-110">Per una descrizione dettagliata di come usare questa classe di base, vedere [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="c136f-110">For a detailed discussion of how to use this base class, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span> <span data-ttu-id="c136f-111">Di seguito è riportato un breve riepilogo:</span><span class="sxs-lookup"><span data-stu-id="c136f-111">What follows is a brief summary:</span></span>

-   <span data-ttu-id="c136f-112">Includere la macro [**Declare \_ IUnknown**](declare-iunknown.md) nella sezione public della definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="c136f-112">Include the [**DECLARE\_IUNKNOWN**](declare-iunknown.md) macro in the public section of your class definition.</span></span> <span data-ttu-id="c136f-113">Questa macro dichiara i tre metodi dell'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="c136f-113">This macro declares the three methods of the **IUnknown** interface.</span></span>
-   <span data-ttu-id="c136f-114">Eseguire l'override del metodo [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) per supportare interfacce diverse da **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="c136f-114">Override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method to support interfaces other than **IUnknown**.</span></span> <span data-ttu-id="c136f-115">All'interno di questo metodo, chiamare la funzione [**GetInterface**](getinterface.md) per recuperare i puntatori di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c136f-115">Within this method, call the [**GetInterface**](getinterface.md) function to retrieve interface pointers.</span></span>
-   <span data-ttu-id="c136f-116">Nel costruttore della classe richiamare il metodo del costruttore **CUnknown** .</span><span class="sxs-lookup"><span data-stu-id="c136f-116">In your class constructor, invoke the **CUnknown** constructor method.</span></span>



| <span data-ttu-id="c136f-117">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="c136f-117">Protected Member Variables</span></span>                                                  | <span data-ttu-id="c136f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c136f-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c136f-119">**\_cref m**</span><span class="sxs-lookup"><span data-stu-id="c136f-119">**m\_cRef**</span></span>](cunknown-m-cref.md)                                          | <span data-ttu-id="c136f-120">Conteggio riferimenti.</span><span class="sxs-lookup"><span data-stu-id="c136f-120">Reference count.</span></span>                                                   |
| <span data-ttu-id="c136f-121">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="c136f-121">Public Methods</span></span>                                                              | <span data-ttu-id="c136f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c136f-122">Description</span></span>                                                        |
| [<span data-ttu-id="c136f-123">**CUnknown**</span><span class="sxs-lookup"><span data-stu-id="c136f-123">**CUnknown**</span></span>](cunknown-cunknown.md)                                       | <span data-ttu-id="c136f-124">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="c136f-124">Constructor method.</span></span>                                                |
| [<span data-ttu-id="c136f-125">**~ CUnknown**</span><span class="sxs-lookup"><span data-stu-id="c136f-125">**~ CUnknown**</span></span>](cunknown--cunknown.md)                                    | <span data-ttu-id="c136f-126">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="c136f-126">Destructor method.</span></span> <span data-ttu-id="c136f-127">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="c136f-127">Virtual.</span></span>                                        |
| [<span data-ttu-id="c136f-128">**GetOwner**</span><span class="sxs-lookup"><span data-stu-id="c136f-128">**GetOwner**</span></span>](cunknown-getowner.md)                                       | <span data-ttu-id="c136f-129">Ottiene un puntatore all' **IUnknown** di controllo.</span><span class="sxs-lookup"><span data-stu-id="c136f-129">Gets a pointer to the controlling **IUnknown**.</span></span>                    |
| <span data-ttu-id="c136f-130">Metodi INonDelegatingUnknown</span><span class="sxs-lookup"><span data-stu-id="c136f-130">INonDelegatingUnknown Methods</span></span>                                               | <span data-ttu-id="c136f-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c136f-131">Description</span></span>                                                        |
| [<span data-ttu-id="c136f-132">**NonDelegatingAddRef**</span><span class="sxs-lookup"><span data-stu-id="c136f-132">**NonDelegatingAddRef**</span></span>](cunknown-nondelegatingaddref.md)                 | <span data-ttu-id="c136f-133">Incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="c136f-133">Increments the reference count.</span></span>                                    |
| [<span data-ttu-id="c136f-134">**NonDelegatingQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="c136f-134">**NonDelegatingQueryInterface**</span></span>](cunknown-nondelegatingqueryinterface.md) | <span data-ttu-id="c136f-135">Recupera un puntatore a interfaccia e incrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="c136f-135">Retrieves an interface pointer and increments the reference count.</span></span> |
| [<span data-ttu-id="c136f-136">**NonDelegatingRelease**</span><span class="sxs-lookup"><span data-stu-id="c136f-136">**NonDelegatingRelease**</span></span>](cunknown-nondelegatingrelease.md)               | <span data-ttu-id="c136f-137">Decrementa il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="c136f-137">Decrements the reference count.</span></span>                                    |



 

## <a name="requirements"></a><span data-ttu-id="c136f-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c136f-138">Requirements</span></span>



| <span data-ttu-id="c136f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c136f-139">Requirement</span></span> | <span data-ttu-id="c136f-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c136f-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c136f-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c136f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="c136f-142"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c136f-142"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c136f-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="c136f-143">Library</span></span><br/> | <dl> <span data-ttu-id="c136f-144"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c136f-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c136f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c136f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c136f-146">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="c136f-146">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




