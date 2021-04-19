---
description: La classe CTransInPlaceInputPin implementa un pin di input usato dalla classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326185"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="83e69-103">Classe CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="83e69-103">CTransInPlaceInputPin class</span></span>

![gerarchia di classi ctransinplaceinputpin](images/tsip01.png)

<span data-ttu-id="83e69-105">La `CTransInPlaceInputPin` classe implementa un pin di input usato dalla classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="83e69-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="83e69-106">In genere, non è necessario derivare da questa classe.</span><span class="sxs-lookup"><span data-stu-id="83e69-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="83e69-107">In tal caso, è necessario eseguire l'override del metodo [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) del filtro per creare istanze della classe derivata.</span><span class="sxs-lookup"><span data-stu-id="83e69-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="83e69-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="83e69-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="83e69-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e69-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="83e69-110">**\_bReadOnly m**</span><span class="sxs-lookup"><span data-stu-id="83e69-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="83e69-111">Flag che specifica se il flusso di input è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="83e69-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="83e69-112">**\_pTIPFilter m**</span><span class="sxs-lookup"><span data-stu-id="83e69-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="83e69-113">Puntatore al filtro che ha creato questo pin.</span><span class="sxs-lookup"><span data-stu-id="83e69-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="83e69-114">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="83e69-114">Public Methods</span></span>                                                                      | <span data-ttu-id="83e69-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e69-115">Description</span></span>                                                |
| [<span data-ttu-id="83e69-116">**CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="83e69-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="83e69-117">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="83e69-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="83e69-118">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="83e69-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="83e69-119">Determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="83e69-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="83e69-120">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="83e69-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="83e69-121">Recupera un puntatore all'allocatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="83e69-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="83e69-122">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="83e69-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="83e69-123">Indica se il flusso di input è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="83e69-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="83e69-124">Metodi IPin</span><span class="sxs-lookup"><span data-stu-id="83e69-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="83e69-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e69-125">Description</span></span>                                                |
| [<span data-ttu-id="83e69-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="83e69-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="83e69-127">Enumera i tipi di supporto preferiti del PIN.</span><span class="sxs-lookup"><span data-stu-id="83e69-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="83e69-128">Metodi IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="83e69-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="83e69-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83e69-129">Description</span></span>                                                |
| [<span data-ttu-id="83e69-130">**Getallocator**</span><span class="sxs-lookup"><span data-stu-id="83e69-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="83e69-131">Recupera l'allocatore di memoria proposto da questo pin.</span><span class="sxs-lookup"><span data-stu-id="83e69-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="83e69-132">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="83e69-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="83e69-133">Specifica un allocatore per la connessione.</span><span class="sxs-lookup"><span data-stu-id="83e69-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="83e69-134">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="83e69-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="83e69-135">Recupera le proprietà dell'allocatore richieste dal pin.</span><span class="sxs-lookup"><span data-stu-id="83e69-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="83e69-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e69-136">Requirements</span></span>



| <span data-ttu-id="83e69-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e69-137">Requirement</span></span> | <span data-ttu-id="83e69-138">Valore</span><span class="sxs-lookup"><span data-stu-id="83e69-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e69-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83e69-139">Header</span></span><br/>  | <dl> <span data-ttu-id="83e69-140"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83e69-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="83e69-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="83e69-141">Library</span></span><br/> | <dl> <span data-ttu-id="83e69-142"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="83e69-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




