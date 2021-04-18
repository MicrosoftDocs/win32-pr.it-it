---
description: Il metodo Alloc alloca memoria per i buffer.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Metodo CMemAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327445"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="a68ce-103">CMemAllocator. Alloc, metodo</span><span class="sxs-lookup"><span data-stu-id="a68ce-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="a68ce-104">Il `Alloc` metodo alloca memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="a68ce-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a68ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a68ce-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="a68ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a68ce-106">Parameters</span></span>

<span data-ttu-id="a68ce-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a68ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a68ce-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a68ce-108">Return value</span></span>

<span data-ttu-id="a68ce-109">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a68ce-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a68ce-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a68ce-110">Return code</span></span>                                                                                       | <span data-ttu-id="a68ce-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a68ce-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a68ce-112"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a68ce-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a68ce-113">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a68ce-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="a68ce-114"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="a68ce-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="a68ce-115">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="a68ce-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="a68ce-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="a68ce-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="a68ce-117">I requisiti del buffer non sono stati impostati.</span><span class="sxs-lookup"><span data-stu-id="a68ce-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a68ce-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a68ce-118">Remarks</span></span>

<span data-ttu-id="a68ce-119">Questo metodo viene chiamato dal metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="a68ce-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="a68ce-120">Alloca un blocco di memoria contiguo sufficiente per i requisiti del buffer specificati nel metodo [**CMemAllocator:: seproperties**](cmemallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a68ce-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a68ce-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a68ce-121">Requirements</span></span>



| <span data-ttu-id="a68ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a68ce-122">Requirement</span></span> | <span data-ttu-id="a68ce-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a68ce-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a68ce-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a68ce-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a68ce-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a68ce-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a68ce-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a68ce-126">Library</span></span><br/> | <dl> <span data-ttu-id="a68ce-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a68ce-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a68ce-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a68ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a68ce-129">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="a68ce-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




