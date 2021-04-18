---
description: La classe CImageAllocator implementa un allocatore che gestisce le bitmap (DIB) indipendenti dal dispositivo GDI. Questa classe deriva dalla classe CBaseAllocator. Crea esempi di supporti che vengono implementati usando la classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325326"
---
# <a name="cimageallocator-class"></a><span data-ttu-id="a72d1-105">Classe CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="a72d1-105">CImageAllocator class</span></span>

![gerarchia di classi cimageallocator](images/wutil04.png)

<span data-ttu-id="a72d1-107">La `CImageAllocator` classe implementa un allocatore che gestisce le bitmap (DIB) indipendenti dal dispositivo GDI.</span><span class="sxs-lookup"><span data-stu-id="a72d1-107">The `CImageAllocator` class implements an allocator that manages GDI device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="a72d1-108">Questa classe deriva dalla classe [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="a72d1-108">This class derives from the [**CBaseAllocator**](cbaseallocator.md) class.</span></span> <span data-ttu-id="a72d1-109">Crea esempi di supporti che vengono implementati usando la classe [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="a72d1-109">It creates media samples that are implemented using the [**CImageSample**](cimagesample.md) class.</span></span>

<span data-ttu-id="a72d1-110">Un allocatore è condiviso da due pin connessi, ma è sempre di proprietà di uno dei filtri nella connessione.</span><span class="sxs-lookup"><span data-stu-id="a72d1-110">An allocator is shared by two connected pins, but is always owned by one of the filters in the connection.</span></span> <span data-ttu-id="a72d1-111">Un filtro che usa `CImageAllocator` deve tenere traccia del fatto che l'allocatore sia stato fornito da solo o dall'altro filtro.</span><span class="sxs-lookup"><span data-stu-id="a72d1-111">A filter that uses `CImageAllocator` must keep track of whether the allocator was provided by itself or by the other filter.</span></span> <span data-ttu-id="a72d1-112">Se l'allocatore è stato fornito da solo, il filtro proprietario può basarsi sul fatto che tutti gli esempi di supporti dell'allocatore sono oggetti **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="a72d1-112">If the allocator was provided by itself, the owning filter can rely on the fact that all media samples from the allocator are **CImageSample** objects.</span></span> <span data-ttu-id="a72d1-113">Può quindi usare l'oggetto **CImageSample** per ottenere informazioni su DIB, memorizzato in una struttura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="a72d1-113">It can therefore use the **CImageSample** object to obtain information about the DIB, which is stored in a [**DIBDATA**](dibdata.md) structure.</span></span>

<span data-ttu-id="a72d1-114">Il filtro proprietario deve chiamare **NotifyMediaType** ogni volta che viene modificato il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a72d1-114">The owning filter should call **NotifyMediaType** whenever the media type changes.</span></span>



| <span data-ttu-id="a72d1-115">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="a72d1-115">Protected Member Variables</span></span>                                     | <span data-ttu-id="a72d1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a72d1-116">Description</span></span>                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="a72d1-117">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="a72d1-117">**m\_pFilter**</span></span>](cimageallocator-m-pfilter.md)                | <span data-ttu-id="a72d1-118">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="a72d1-118">Pointer to the owning filter.</span></span>                                            |
| [<span data-ttu-id="a72d1-119">**\_pMediaType m**</span><span class="sxs-lookup"><span data-stu-id="a72d1-119">**m\_pMediaType**</span></span>](cimageallocator-m-pmediatype.md)          | <span data-ttu-id="a72d1-120">Puntatore al tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="a72d1-120">Pointer to the current media type.</span></span>                                       |
| <span data-ttu-id="a72d1-121">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="a72d1-121">Protected Methods</span></span>                                              | <span data-ttu-id="a72d1-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a72d1-122">Description</span></span>                                                              |
| [<span data-ttu-id="a72d1-123">**Alloc**</span><span class="sxs-lookup"><span data-stu-id="a72d1-123">**Alloc**</span></span>](cimageallocator-alloc.md)                         | <span data-ttu-id="a72d1-124">Alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="a72d1-124">Allocates memory for the buffers.</span></span>                                        |
| [<span data-ttu-id="a72d1-125">**CheckSizes**</span><span class="sxs-lookup"><span data-stu-id="a72d1-125">**CheckSizes**</span></span>](cimageallocator-checksizes.md)               | <span data-ttu-id="a72d1-126">Verifica le proprietà dell'allocatore rispetto al tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="a72d1-126">Checks allocator properties against the current media type.</span></span>              |
| [<span data-ttu-id="a72d1-127">**CreateDIB**</span><span class="sxs-lookup"><span data-stu-id="a72d1-127">**CreateDIB**</span></span>](cimageallocator-createdib.md)                 | <span data-ttu-id="a72d1-128">Crea una DIB.</span><span class="sxs-lookup"><span data-stu-id="a72d1-128">Creates a DIB.</span></span>                                                           |
| [<span data-ttu-id="a72d1-129">**CreateImageSample**</span><span class="sxs-lookup"><span data-stu-id="a72d1-129">**CreateImageSample**</span></span>](cimageallocator-createimagesample.md) | <span data-ttu-id="a72d1-130">Crea un esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="a72d1-130">Creates a media sample.</span></span> <span data-ttu-id="a72d1-131">Virtuale.</span><span class="sxs-lookup"><span data-stu-id="a72d1-131">Virtual.</span></span>                                         |
| [<span data-ttu-id="a72d1-132">**Gratuito**</span><span class="sxs-lookup"><span data-stu-id="a72d1-132">**Free**</span></span>](cimageallocator-free.md)                           | <span data-ttu-id="a72d1-133">Rilascia tutta la memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="a72d1-133">Releases all of the buffer memory.</span></span>                                       |
| <span data-ttu-id="a72d1-134">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="a72d1-134">Public Methods</span></span>                                                 | <span data-ttu-id="a72d1-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a72d1-135">Description</span></span>                                                              |
| [<span data-ttu-id="a72d1-136">**CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="a72d1-136">**CImageAllocator**</span></span>](cimageallocator-cimageallocator.md)     | <span data-ttu-id="a72d1-137">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="a72d1-137">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="a72d1-138">**NotifyMediaType**</span><span class="sxs-lookup"><span data-stu-id="a72d1-138">**NotifyMediaType**</span></span>](cimageallocator-notifymediatype.md)     | <span data-ttu-id="a72d1-139">Informa l'oggetto del tipo di supporto corrente.</span><span class="sxs-lookup"><span data-stu-id="a72d1-139">Informs the object of the current media type.</span></span>                            |
| <span data-ttu-id="a72d1-140">Metodi IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="a72d1-140">IMemAllocator Methods</span></span>                                          | <span data-ttu-id="a72d1-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a72d1-141">Description</span></span>                                                              |
| [<span data-ttu-id="a72d1-142">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="a72d1-142">**SetProperties**</span></span>](cimageallocator-setproperties.md)         | <span data-ttu-id="a72d1-143">Specifica il numero di buffer da allocare e le dimensioni di ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="a72d1-143">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a72d1-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a72d1-144">Requirements</span></span>



| <span data-ttu-id="a72d1-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a72d1-145">Requirement</span></span> | <span data-ttu-id="a72d1-146">Valore</span><span class="sxs-lookup"><span data-stu-id="a72d1-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a72d1-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a72d1-147">Header</span></span><br/>  | <dl> <span data-ttu-id="a72d1-148"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a72d1-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a72d1-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="a72d1-149">Library</span></span><br/> | <dl> <span data-ttu-id="a72d1-150"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a72d1-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a72d1-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a72d1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a72d1-152">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a72d1-152">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




