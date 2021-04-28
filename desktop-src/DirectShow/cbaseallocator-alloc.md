---
description: 'Metodo CBaseAllocator.Alloc: il metodo Alloc alloca memoria per i buffer.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Metodo CBaseAllocator.Alloc (Amfilter.h)
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
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096368"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="7102a-103">Metodo CBaseAllocator.Alloc</span><span class="sxs-lookup"><span data-stu-id="7102a-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="7102a-104">Il `Alloc` metodo alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="7102a-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7102a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7102a-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="7102a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7102a-106">Parameters</span></span>

<span data-ttu-id="7102a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7102a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7102a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7102a-108">Return value</span></span>

<span data-ttu-id="7102a-109">Restituisce uno dei valori **HRESULT** seguenti.</span><span class="sxs-lookup"><span data-stu-id="7102a-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="7102a-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7102a-110">Return code</span></span>                                                                                       | <span data-ttu-id="7102a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7102a-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7102a-112"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="7102a-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="7102a-113">I requisiti del buffer non sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="7102a-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="7102a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7102a-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="7102a-115">I requisiti del buffer sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="7102a-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="7102a-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="7102a-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="7102a-117">I requisiti del buffer non sono stati impostati.</span><span class="sxs-lookup"><span data-stu-id="7102a-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7102a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7102a-118">Remarks</span></span>

<span data-ttu-id="7102a-119">Questo metodo viene chiamato dal [**metodo CBaseAllocator::Commit.**](cbaseallocator-commit.md)</span><span class="sxs-lookup"><span data-stu-id="7102a-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="7102a-120">Nella classe di base questo metodo non alloca memoria.</span><span class="sxs-lookup"><span data-stu-id="7102a-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="7102a-121">Restituisce un errore se i requisiti del buffer non sono stati impostati, S FALSE se i requisiti non sono stati modificati e S OK se \_ i requisiti sono stati \_ modificati.</span><span class="sxs-lookup"><span data-stu-id="7102a-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="7102a-122">Una classe derivata deve eseguire l'override di questo metodo per eseguire l'allocazione di memoria effettiva.</span><span class="sxs-lookup"><span data-stu-id="7102a-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="7102a-123">In genere, la classe derivata esegue i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7102a-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="7102a-124">Chiamare l'implementazione della classe di base per determinare se la memoria richiede effettivamente l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="7102a-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="7102a-125">Allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="7102a-125">Allocate memory.</span></span>
3.  <span data-ttu-id="7102a-126">Creare [**oggetti CMediaSample**](cmediasample.md) che contengono blocchi di memoria dal passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="7102a-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="7102a-127">Aggiungere ogni **oggetto CMediaSample** all'elenco di esempi gratuiti ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="7102a-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="7102a-128">Per un esempio, vedere [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="7102a-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7102a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7102a-129">Requirements</span></span>



| <span data-ttu-id="7102a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7102a-130">Requirement</span></span> | <span data-ttu-id="7102a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7102a-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7102a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7102a-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7102a-133"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7102a-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7102a-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="7102a-134">Library</span></span><br/> | <dl> <span data-ttu-id="7102a-135"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7102a-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7102a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7102a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7102a-137">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="7102a-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




