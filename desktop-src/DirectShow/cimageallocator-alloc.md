---
description: "Il metodo Alloc alloca memoria per i buffer. Questo metodo esegue l'override del metodo CBaseAllocator:: Alloc."
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Metodo CImageAllocator. Alloc (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329775"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="cba89-104">CImageAllocator. Alloc, metodo</span><span class="sxs-lookup"><span data-stu-id="cba89-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="cba89-105">Il `Alloc` metodo alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="cba89-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="cba89-106">Questo metodo esegue l'override del metodo [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="cba89-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba89-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cba89-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="cba89-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cba89-108">Parameters</span></span>

<span data-ttu-id="cba89-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cba89-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cba89-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cba89-110">Return value</span></span>

<span data-ttu-id="cba89-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cba89-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cba89-112">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="cba89-112">Possible values include the following.</span></span>



| <span data-ttu-id="cba89-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cba89-113">Return code</span></span>                                                                                   | <span data-ttu-id="cba89-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cba89-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="cba89-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cba89-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cba89-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="cba89-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="cba89-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="cba89-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cba89-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="cba89-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cba89-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cba89-119">Remarks</span></span>

<span data-ttu-id="cba89-120">Questo metodo viene chiamato dal metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) , quando il filtro esegue il commit dell'allocatore.</span><span class="sxs-lookup"><span data-stu-id="cba89-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="cba89-121">Questo metodo crea un elenco di esempi di supporti, implementati come oggetti [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="cba89-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="cba89-122">Ogni esempio contiene una bitmap indipendente dal dispositivo GDI, usando la funzione **CreateDIBSection** di GDI.</span><span class="sxs-lookup"><span data-stu-id="cba89-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="cba89-123">Internamente questo metodo chiama [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) per creare ogni DIB e [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) per creare ogni campione.</span><span class="sxs-lookup"><span data-stu-id="cba89-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba89-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cba89-124">Requirements</span></span>



| <span data-ttu-id="cba89-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba89-125">Requirement</span></span> | <span data-ttu-id="cba89-126">Valore</span><span class="sxs-lookup"><span data-stu-id="cba89-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cba89-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cba89-127">Header</span></span><br/>  | <dl> <span data-ttu-id="cba89-128"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cba89-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cba89-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="cba89-129">Library</span></span><br/> | <dl> <span data-ttu-id="cba89-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cba89-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba89-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cba89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba89-132">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="cba89-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




