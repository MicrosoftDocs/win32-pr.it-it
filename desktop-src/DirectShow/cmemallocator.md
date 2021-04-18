---
description: Implementa un allocatore che supporta l'interfaccia IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Classe CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328841"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="45fe6-103">Classe CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="45fe6-103">CMemAllocator class</span></span>

![gerarchia di classi cmemallocator](images/filter10.png)

<span data-ttu-id="45fe6-105">Implementa un allocatore che supporta l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="45fe6-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="45fe6-106">Questa classe deriva da [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="45fe6-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="45fe6-107">Per ulteriori informazioni sugli allocatori, vedere la documentazione relativa a [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="45fe6-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="45fe6-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="45fe6-108">Protected Member Variables</span></span>                              | <span data-ttu-id="45fe6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45fe6-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="45fe6-110">**\_pbuffer m**</span><span class="sxs-lookup"><span data-stu-id="45fe6-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="45fe6-111">Puntatore al blocco di memoria che contiene i buffer.</span><span class="sxs-lookup"><span data-stu-id="45fe6-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="45fe6-112">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="45fe6-112">Protected Methods</span></span>                                       | <span data-ttu-id="45fe6-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45fe6-113">Description</span></span>                                                              |
| [<span data-ttu-id="45fe6-114">**Libero**</span><span class="sxs-lookup"><span data-stu-id="45fe6-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="45fe6-115">Metodo segnaposto; chiamato durante un'operazione di decommit.</span><span class="sxs-lookup"><span data-stu-id="45fe6-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="45fe6-116">**ReallyFree**</span><span class="sxs-lookup"><span data-stu-id="45fe6-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="45fe6-117">Rilascia la memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="45fe6-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="45fe6-118">**Alloc**</span><span class="sxs-lookup"><span data-stu-id="45fe6-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="45fe6-119">Alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="45fe6-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="45fe6-120">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="45fe6-120">Public Methods</span></span>                                          | <span data-ttu-id="45fe6-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45fe6-121">Description</span></span>                                                              |
| [<span data-ttu-id="45fe6-122">**CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="45fe6-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="45fe6-123">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="45fe6-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="45fe6-124">**~ CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="45fe6-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="45fe6-125">Metodo del distruttore.</span><span class="sxs-lookup"><span data-stu-id="45fe6-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="45fe6-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="45fe6-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="45fe6-127">Crea una nuova istanza della classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="45fe6-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="45fe6-128">Metodi IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="45fe6-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="45fe6-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45fe6-129">Description</span></span>                                                              |
| [<span data-ttu-id="45fe6-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="45fe6-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="45fe6-131">Specifica il numero di buffer da allocare e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="45fe6-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="45fe6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45fe6-132">Requirements</span></span>



| <span data-ttu-id="45fe6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fe6-133">Requirement</span></span> | <span data-ttu-id="45fe6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="45fe6-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fe6-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45fe6-135">Header</span></span><br/>  | <dl> <span data-ttu-id="45fe6-136"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45fe6-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45fe6-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="45fe6-137">Library</span></span><br/> | <dl> <span data-ttu-id="45fe6-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="45fe6-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fe6-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45fe6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45fe6-140">Fornire un allocatore personalizzato</span><span class="sxs-lookup"><span data-stu-id="45fe6-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




