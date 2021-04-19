---
description: Il metodo Alloc alloca memoria per i buffer.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Metodo CBaseAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324042"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="b6f83-103">CBaseAllocator. Alloc, metodo</span><span class="sxs-lookup"><span data-stu-id="b6f83-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="b6f83-104">Il `Alloc` metodo alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="b6f83-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6f83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6f83-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="b6f83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6f83-106">Parameters</span></span>

<span data-ttu-id="b6f83-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b6f83-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6f83-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6f83-108">Return value</span></span>

<span data-ttu-id="b6f83-109">Restituisce uno dei seguenti valori **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b6f83-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="b6f83-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b6f83-110">Return code</span></span>                                                                                       | <span data-ttu-id="b6f83-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6f83-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="b6f83-112"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f83-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="b6f83-113">I requisiti del buffer non sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="b6f83-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="b6f83-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f83-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="b6f83-115">I requisiti del buffer sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="b6f83-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="b6f83-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="b6f83-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="b6f83-117">I requisiti del buffer non sono stati impostati.</span><span class="sxs-lookup"><span data-stu-id="b6f83-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b6f83-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6f83-118">Remarks</span></span>

<span data-ttu-id="b6f83-119">Questo metodo viene chiamato dal metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="b6f83-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="b6f83-120">Nella classe di base, questo metodo non alloca memoria.</span><span class="sxs-lookup"><span data-stu-id="b6f83-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="b6f83-121">Restituisce un errore se i requisiti del buffer non sono stati impostati, S \_ false se i requisiti non sono stati modificati e s \_ OK se i requisiti sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="b6f83-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="b6f83-122">Una classe derivata deve eseguire l'override di questo metodo per eseguire l'allocazione di memoria effettiva.</span><span class="sxs-lookup"><span data-stu-id="b6f83-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="b6f83-123">In genere, la classe derivata eseguirà i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6f83-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="b6f83-124">Chiamare l'implementazione della classe di base per determinare se la memoria richiede effettivamente l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="b6f83-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="b6f83-125">Allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="b6f83-125">Allocate memory.</span></span>
3.  <span data-ttu-id="b6f83-126">Creare oggetti [**CMediaSample**](cmediasample.md) che contengono blocchi di memoria dal passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="b6f83-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="b6f83-127">Aggiungere ogni oggetto **CMediaSample** all'elenco di esempi gratuiti ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="b6f83-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="b6f83-128">Per un esempio, vedere [**CMemAllocator:: Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="b6f83-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6f83-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6f83-129">Requirements</span></span>



| <span data-ttu-id="b6f83-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6f83-130">Requirement</span></span> | <span data-ttu-id="b6f83-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b6f83-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6f83-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6f83-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b6f83-133"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f83-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b6f83-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6f83-134">Library</span></span><br/> | <dl> <span data-ttu-id="b6f83-135"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b6f83-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6f83-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6f83-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6f83-137">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="b6f83-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




