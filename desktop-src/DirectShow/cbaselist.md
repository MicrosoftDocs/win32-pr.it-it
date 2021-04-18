---
description: Il metodo CBaseList implementa un elenco di Abtract. Il modello di classe CGenericList, che deriva da CBaseList, fornisce il controllo del tipo e un'interfaccia più semplice rispetto alla classe CBaseList.
ms.assetid: 372ee6f7-be0c-469f-92b3-673970ebd6da
title: Classe CBaseList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6aa4a3c80cd583bd3cc83a2a0adedecb6caaf7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325673"
---
# <a name="cbaselist-class"></a><span data-ttu-id="b3fdd-104">Classe CBaseList</span><span class="sxs-lookup"><span data-stu-id="b3fdd-104">CBaseList class</span></span>

![gerarchia di classi cbaselist](images/list01.png)

<span data-ttu-id="b3fdd-106">Il metodo **CBaseList** implementa un elenco di Abtract.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-106">The **CBaseList** method implements an abtract list.</span></span> <span data-ttu-id="b3fdd-107">Il modello di classe [**CGenericList**](cgenericlist.md) , che deriva da **CBaseList**, fornisce il controllo del tipo e un'interfaccia più semplice rispetto alla classe **CBaseList** .</span><span class="sxs-lookup"><span data-stu-id="b3fdd-107">The [**CGenericList**](cgenericlist.md) class template, which derives from **CBaseList**, provides type checking and a simpler interface than the **CBaseList** class.</span></span>

<span data-ttu-id="b3fdd-108">La classe **CBaseList** viene modellata dopo la classe **CObList** nella libreria Microsoft Foundation Classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="b3fdd-108">The **CBaseList** class is modeled after the **CObList** class in the Microsoft Foundation Classes (MFC) library.</span></span> <span data-ttu-id="b3fdd-109">Le posizioni all'interno dell'elenco sono rappresentate da una struttura di posizione.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-109">Positions within the list are represented by a POSITION structure.</span></span> <span data-ttu-id="b3fdd-110">Il chiamante non deve accedere ai membri interni della struttura di posizione; considerarlo come un puntatore a un nodo elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-110">The caller should not access the internal members of the POSITION structure; treat it as a pointer to a list node.</span></span> <span data-ttu-id="b3fdd-111">La posizione di un oggetto nell'elenco rimane valida fino a quando l'oggetto non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-111">The position of an object in the list remains valid until the object is deleted.</span></span>

<span data-ttu-id="b3fdd-112">L'elenco non richiede alcun supporto per gli oggetti in esso contenuti.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-112">The list does not require any support by the objects it contains.</span></span> <span data-ttu-id="b3fdd-113">Non esegue alcuna gestione dell'archiviazione o copia sugli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-113">It performs no storage management or copying on the objects.</span></span> <span data-ttu-id="b3fdd-114">Gli oggetti possono trovarsi in più elenchi.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-114">Objects can be in multiple lists.</span></span>

<span data-ttu-id="b3fdd-115">Approssimativamente la metà dei metodi in questa classe agisce su singoli oggetti.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-115">Roughly half of the methods in this class act on single objects.</span></span> <span data-ttu-id="b3fdd-116">Questi metodi hanno il suffisso-I nel nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-116">These methods have the suffix - I in the method name.</span></span> <span data-ttu-id="b3fdd-117">Gli altri metodi agiscono su interi elenchi.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-117">The other methods act on entire lists.</span></span> <span data-ttu-id="b3fdd-118">Ad esempio, il metodo [**CBaseList:: AddAfter**](cbaselist-addafter.md) Accoda un elenco a un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-118">For example, the [**CBaseList::AddAfter**](cbaselist-addafter.md) method appends a list to another list.</span></span> <span data-ttu-id="b3fdd-119">Le operazioni a oggetto singolo restituiscono valori di posizione o **null** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-119">Single-object operations return POSITION values, or **NULL** on failure.</span></span> <span data-ttu-id="b3fdd-120">Le operazioni di elenco restituiscono **true** in caso di esito positivo o **falso** .</span><span class="sxs-lookup"><span data-stu-id="b3fdd-120">List operations return **TRUE** if successful or **FALSE** otherwise.</span></span>



| <span data-ttu-id="b3fdd-121">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="b3fdd-121">Protected Member Variables</span></span>                             | <span data-ttu-id="b3fdd-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3fdd-122">Description</span></span>                                                               |
|--------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="b3fdd-123">**\_conteggio m**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-123">**m\_Count**</span></span>](cbaselist-m-count.md)                  | <span data-ttu-id="b3fdd-124">Numero di elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-124">Number of items in the list.</span></span>                                              |
| [<span data-ttu-id="b3fdd-125">**\_pFirst m**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-125">**m\_pFirst**</span></span>](cbaselist-m-pfirst.md)                | <span data-ttu-id="b3fdd-126">Puntatore al primo nodo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-126">Pointer to the first node in the list.</span></span>                                    |
| [<span data-ttu-id="b3fdd-127">**m \_ pLast**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-127">**m\_pLast**</span></span>](cbaselist-m-plast.md)                  | <span data-ttu-id="b3fdd-128">Puntatore all'ultimo nodo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-128">Pointer to the last node in the list.</span></span>                                     |
| <span data-ttu-id="b3fdd-129">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="b3fdd-129">Protected Methods</span></span>                                      | <span data-ttu-id="b3fdd-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3fdd-130">Description</span></span>                                                               |
| [<span data-ttu-id="b3fdd-131">**Getnexti**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-131">**GetNextI**</span></span>](cbaselist-getnexti.md)                 | <span data-ttu-id="b3fdd-132">Recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-132">Retrieves the item at the specified position, and advances the position.</span></span>  |
| [<span data-ttu-id="b3fdd-133">**GetI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-133">**GetI**</span></span>](cbaselist-geti.md)                         | <span data-ttu-id="b3fdd-134">Recupera l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-134">Retrieves the item at the specified position.</span></span>                             |
| [<span data-ttu-id="b3fdd-135">**FindI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-135">**FindI**</span></span>](cbaselist-findi.md)                       | <span data-ttu-id="b3fdd-136">Recupera la prima posizione che include l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-136">Retrieves the first position that holds the specified item.</span></span>               |
| [<span data-ttu-id="b3fdd-137">**RemoveHeadI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-137">**RemoveHeadI**</span></span>](cbaselist-removeheadi.md)           | <span data-ttu-id="b3fdd-138">Rimuove il primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-138">Removes the first item in the list.</span></span>                                       |
| [<span data-ttu-id="b3fdd-139">**RemoveTailI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-139">**RemoveTailI**</span></span>](cbaselist-removetaili.md)           | <span data-ttu-id="b3fdd-140">Rimuove l'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-140">Removes the last item in the list.</span></span>                                        |
| [<span data-ttu-id="b3fdd-141">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-141">**RemoveI**</span></span>](cbaselist-removei.md)                   | <span data-ttu-id="b3fdd-142">Rimuove l'elemento nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-142">Removes the item at the specified position.</span></span>                               |
| [<span data-ttu-id="b3fdd-143">**AddTailI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-143">**AddTailI**</span></span>](cbaselist-addtaili.md)                 | <span data-ttu-id="b3fdd-144">Aggiunge un elemento alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-144">Adds an item to the end of the list.</span></span>                                      |
| [<span data-ttu-id="b3fdd-145">**AddHeadI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-145">**AddHeadI**</span></span>](cbaselist-addheadi.md)                 | <span data-ttu-id="b3fdd-146">Aggiunge un elemento all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-146">Adds an item to the front of the list.</span></span>                                    |
| [<span data-ttu-id="b3fdd-147">**AddAfterI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-147">**AddAfterI**</span></span>](cbaselist-addafteri.md)               | <span data-ttu-id="b3fdd-148">Inserisce un elemento dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-148">Inserts an item after the specified position.</span></span>                             |
| [<span data-ttu-id="b3fdd-149">**AddBeforeI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-149">**AddBeforeI**</span></span>](cbaselist-addbeforei.md)             | <span data-ttu-id="b3fdd-150">Inserisce un elemento prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-150">Inserts an item before the specified position.</span></span>                            |
| <span data-ttu-id="b3fdd-151">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="b3fdd-151">Public Methods</span></span>                                         | <span data-ttu-id="b3fdd-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3fdd-152">Description</span></span>                                                               |
| [<span data-ttu-id="b3fdd-153">**CBaseList**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-153">**CBaseList**</span></span>](cbaselist-cbaselist.md)               | <span data-ttu-id="b3fdd-154">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-154">Constructor method.</span></span>                                                       |
| [<span data-ttu-id="b3fdd-155">**~ CBaseList**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-155">**~ CBaseList**</span></span>](cbaselist--cbaselist.md)            | <span data-ttu-id="b3fdd-156">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-156">Destructor method.</span></span>                                                        |
| [<span data-ttu-id="b3fdd-157">**RemoveAll**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-157">**RemoveAll**</span></span>](cbaselist-removeall.md)               | <span data-ttu-id="b3fdd-158">Rimuove tutti i nodi dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-158">Removes all nodes from the list.</span></span>                                          |
| [<span data-ttu-id="b3fdd-159">**GetHeadPositionI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-159">**GetHeadPositionI**</span></span>](cbaselist-getheadpositioni.md) | <span data-ttu-id="b3fdd-160">Recupera la posizione del primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-160">Retrieves the position of the first item in the list.</span></span>                     |
| [<span data-ttu-id="b3fdd-161">**GetTailPositionI**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-161">**GetTailPositionI**</span></span>](cbaselist-gettailpositioni.md) | <span data-ttu-id="b3fdd-162">Recupera la posizione dell'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-162">Retrieves the position of the last item of the list.</span></span>                      |
| [<span data-ttu-id="b3fdd-163">**Getcounti**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-163">**GetCountI**</span></span>](cbaselist-getcounti.md)               | <span data-ttu-id="b3fdd-164">Recupera il numero di elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-164">Retrieves the number of items in the list.</span></span>                                |
| [<span data-ttu-id="b3fdd-165">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-165">**Next**</span></span>](cbaselist-next.md)                         | <span data-ttu-id="b3fdd-166">Recupera la posizione successiva nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-166">Retrieves the next position in the list.</span></span>                                  |
| [<span data-ttu-id="b3fdd-167">**Prev**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-167">**Prev**</span></span>](cbaselist-prev.md)                         | <span data-ttu-id="b3fdd-168">Recupera la posizione precedente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-168">Retrieves the previous position in the list.</span></span>                              |
| [<span data-ttu-id="b3fdd-169">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-169">**AddHead**</span></span>](cbaselist-addhead.md)                   | <span data-ttu-id="b3fdd-170">Inserisce un altro elenco all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-170">Inserts another list at the front of this list.</span></span>                           |
| [<span data-ttu-id="b3fdd-171">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-171">**AddTail**</span></span>](cbaselist-addtail.md)                   | <span data-ttu-id="b3fdd-172">Accoda un altro elenco alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-172">Appends another list to the end of this list.</span></span>                             |
| [<span data-ttu-id="b3fdd-173">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-173">**AddAfter**</span></span>](cbaselist-addafter.md)                 | <span data-ttu-id="b3fdd-174">Inserisce un elenco dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-174">Inserts a list after the specified position.</span></span>                              |
| [<span data-ttu-id="b3fdd-175">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-175">**AddBefore**</span></span>](cbaselist-addbefore.md)               | <span data-ttu-id="b3fdd-176">Inserisce un elenco prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-176">Inserts a list before the specified position.</span></span>                             |
| [<span data-ttu-id="b3fdd-177">**MoveToTail**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-177">**MoveToTail**</span></span>](cbaselist-movetotail.md)             | <span data-ttu-id="b3fdd-178">Suddivide l'elenco e aggiunge la parte Head alla parte finale di un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-178">Splits the list and appends the head portion to the tail of another list.</span></span> |
| [<span data-ttu-id="b3fdd-179">**MoveToHead**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-179">**MoveToHead**</span></span>](cbaselist-movetohead.md)             | <span data-ttu-id="b3fdd-180">Suddivide l'elenco e inserisce la parte finale all'inizio di un altro elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-180">Splits the list and inserts the tail portion at the head of another list.</span></span> |
| [<span data-ttu-id="b3fdd-181">**Inverso**</span><span class="sxs-lookup"><span data-stu-id="b3fdd-181">**Reverse**</span></span>](cbaselist-reverse.md)                   | <span data-ttu-id="b3fdd-182">Inverte l'ordine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b3fdd-182">Reverses the order of the list.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="b3fdd-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3fdd-183">Requirements</span></span>



| <span data-ttu-id="b3fdd-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3fdd-184">Requirement</span></span> | <span data-ttu-id="b3fdd-185">Valore</span><span class="sxs-lookup"><span data-stu-id="b3fdd-185">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3fdd-186">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3fdd-186">Header</span></span><br/>  | <dl> <span data-ttu-id="b3fdd-187"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3fdd-187"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b3fdd-188">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3fdd-188">Library</span></span><br/> | <dl> <span data-ttu-id="b3fdd-189"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b3fdd-189"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3fdd-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3fdd-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3fdd-191">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="b3fdd-191">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




