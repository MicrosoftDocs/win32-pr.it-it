---
description: Modello di classe CGenericList che implementa un elenco specifico del tipo. Per ulteriori informazioni, vedere CBaseList.
ms.assetid: 69067530-3a7d-4731-8ac6-9d02dbba8440
title: Classe CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6de3a2dde8d4549221ef4f13decab167fcf6d560
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329792"
---
# <a name="cgenericlist-class"></a><span data-ttu-id="58e92-104">Classe CGenericList</span><span class="sxs-lookup"><span data-stu-id="58e92-104">CGenericList class</span></span>

![gerarchia di classi cgenericlist](images/list01.png)

<span data-ttu-id="58e92-106">`CGenericList`Modello di classe che implementa un elenco specifico del tipo.</span><span class="sxs-lookup"><span data-stu-id="58e92-106">The `CGenericList` class template that implements a type-specific list.</span></span> <span data-ttu-id="58e92-107">Per ulteriori informazioni, vedere [**CBaseList**](cbaselist.md).</span><span class="sxs-lookup"><span data-stu-id="58e92-107">For more information, see [**CBaseList**](cbaselist.md).</span></span>

<span data-ttu-id="58e92-108">Per usare questo modello, dichiarare una variabile di tipo `CGenericList` con un argomento di modello che definisce il tipo di oggetto nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-108">To use this template, declare a variable of type `CGenericList` with a template argument that defines the type of object in the list.</span></span> <span data-ttu-id="58e92-109">L'istruzione seguente, ad esempio, dichiara un elenco di oggetti [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="58e92-109">For example, the following statement declares a list of [**CBaseFilter**](cbasefilter.md) objects:</span></span>


```
CGenericList<CBaseFilter> myFilterList("Filters"); 
```



<span data-ttu-id="58e92-110">Per praticità, Wxlist. h definisce i tipi di elenco seguenti:</span><span class="sxs-lookup"><span data-stu-id="58e92-110">For convenience, Wxlist.h defines the following list types:</span></span>

``` syntax
typedef CGenericList<CBaseObject> CBaseObjectList;
typedef CGenericList<IUnknown> CBaseInterfaceList;
```



| <span data-ttu-id="58e92-111">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="58e92-111">Public Methods</span></span>                                          | <span data-ttu-id="58e92-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e92-112">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="58e92-113">**CGenericList**</span><span class="sxs-lookup"><span data-stu-id="58e92-113">**CGenericList**</span></span>](cgenericlist-cgenericlist.md)       | <span data-ttu-id="58e92-114">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="58e92-114">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="58e92-115">**~ CGenericList**</span><span class="sxs-lookup"><span data-stu-id="58e92-115">**~CGenericList**</span></span>](cgenericlist--cgenericlist.md)     | <span data-ttu-id="58e92-116">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="58e92-116">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="58e92-117">**GetHeadPosition**</span><span class="sxs-lookup"><span data-stu-id="58e92-117">**GetHeadPosition**</span></span>](cgenericlist-getheadposition.md) | <span data-ttu-id="58e92-118">Recupera la posizione del primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-118">Retrieves the position of the first item in the list.</span></span>                    |
| [<span data-ttu-id="58e92-119">**GetTailPosition**</span><span class="sxs-lookup"><span data-stu-id="58e92-119">**GetTailPosition**</span></span>](cgenericlist-gettailposition.md) | <span data-ttu-id="58e92-120">Recupera la posizione dell'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-120">Retrieves the position of the last item of the list.</span></span>                     |
| [<span data-ttu-id="58e92-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="58e92-121">**GetCount**</span></span>](cgenericlist-getcount.md)               | <span data-ttu-id="58e92-122">Recupera il numero di elementi nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-122">Retrieves the number of items in the list.</span></span>                               |
| [<span data-ttu-id="58e92-123">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="58e92-123">**GetNext**</span></span>](cgenericlist-getnext.md)                 | <span data-ttu-id="58e92-124">Recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.</span><span class="sxs-lookup"><span data-stu-id="58e92-124">Retrieves the item at the specified position, and advances the position.</span></span> |
| [<span data-ttu-id="58e92-125">**Recupero**</span><span class="sxs-lookup"><span data-stu-id="58e92-125">**Get**</span></span>](cgenericlist-get.md)                         | <span data-ttu-id="58e92-126">Recupera l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="58e92-126">Retrieves the item at the specified position.</span></span>                            |
| [<span data-ttu-id="58e92-127">**GetHead**</span><span class="sxs-lookup"><span data-stu-id="58e92-127">**GetHead**</span></span>](cgenericlist-gethead.md)                 | <span data-ttu-id="58e92-128">Recupera l'elemento all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-128">Retrieves the item at the head of the list.</span></span>                              |
| [<span data-ttu-id="58e92-129">**RemoveHead**</span><span class="sxs-lookup"><span data-stu-id="58e92-129">**RemoveHead**</span></span>](cgenericlist-removehead.md)           | <span data-ttu-id="58e92-130">Rimuove il primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-130">Removes the first item in the list.</span></span>                                      |
| [<span data-ttu-id="58e92-131">**RemoveTail**</span><span class="sxs-lookup"><span data-stu-id="58e92-131">**RemoveTail**</span></span>](cgenericlist-removetail.md)           | <span data-ttu-id="58e92-132">Rimuove l'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-132">Removes the last item in the list.</span></span>                                       |
| [<span data-ttu-id="58e92-133">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="58e92-133">**Remove**</span></span>](cgenericlist-remove.md)                   | <span data-ttu-id="58e92-134">Rimuove l'elemento nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="58e92-134">Removes the item at the specified position.</span></span>                              |
| [<span data-ttu-id="58e92-135">**AddBefore**</span><span class="sxs-lookup"><span data-stu-id="58e92-135">**AddBefore**</span></span>](cgenericlist-addbefore.md)             | <span data-ttu-id="58e92-136">Inserisce un elemento o un elenco prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="58e92-136">Inserts an item or list before the specified position.</span></span>                   |
| [<span data-ttu-id="58e92-137">**AddAfter**</span><span class="sxs-lookup"><span data-stu-id="58e92-137">**AddAfter**</span></span>](cgenericlist-addafter.md)               | <span data-ttu-id="58e92-138">Inserisce un elemento o un elenco dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="58e92-138">Inserts an item or list after the specified position.</span></span>                    |
| [<span data-ttu-id="58e92-139">**AddHead**</span><span class="sxs-lookup"><span data-stu-id="58e92-139">**AddHead**</span></span>](cgenericlist-addhead.md)                 | <span data-ttu-id="58e92-140">Aggiunge un elemento o un elenco all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-140">Adds an item or list to the front of the list.</span></span>                           |
| [<span data-ttu-id="58e92-141">**AddTail**</span><span class="sxs-lookup"><span data-stu-id="58e92-141">**AddTail**</span></span>](cgenericlist-addtail.md)                 | <span data-ttu-id="58e92-142">Accoda un elemento o un elenco alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58e92-142">Appends an item or list to the end of the list.</span></span>                          |
| [<span data-ttu-id="58e92-143">**Find**</span><span class="sxs-lookup"><span data-stu-id="58e92-143">**Find**</span></span>](cgenericlist-find.md)                       | <span data-ttu-id="58e92-144">Recupera la prima posizione che include l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="58e92-144">Retrieves the first position that holds the specified item.</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="58e92-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e92-145">Requirements</span></span>



| <span data-ttu-id="58e92-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e92-146">Requirement</span></span> | <span data-ttu-id="58e92-147">Valore</span><span class="sxs-lookup"><span data-stu-id="58e92-147">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e92-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58e92-148">Header</span></span><br/>  | <dl> <span data-ttu-id="58e92-149"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58e92-149"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="58e92-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="58e92-150">Library</span></span><br/> | <dl> <span data-ttu-id="58e92-151"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="58e92-151"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




