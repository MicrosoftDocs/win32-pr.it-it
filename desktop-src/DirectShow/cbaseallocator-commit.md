---
description: 'Il metodo commit alloca la memoria per i buffer. Questo metodo implementa il metodo IMemAllocator:: commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Metodo CBaseAllocator. Commit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328271"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="842ec-104">Metodo CBaseAllocator. commit</span><span class="sxs-lookup"><span data-stu-id="842ec-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="842ec-105">Il `Commit` metodo alloca la memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="842ec-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="842ec-106">Questo metodo implementa il metodo [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .</span><span class="sxs-lookup"><span data-stu-id="842ec-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="842ec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="842ec-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="842ec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="842ec-108">Parameters</span></span>

<span data-ttu-id="842ec-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="842ec-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="842ec-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="842ec-110">Return value</span></span>

<span data-ttu-id="842ec-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="842ec-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="842ec-112">I valori possibili includono quelli elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="842ec-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="842ec-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="842ec-113">Return code</span></span>                                                                                       | <span data-ttu-id="842ec-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="842ec-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="842ec-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="842ec-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="842ec-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="842ec-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="842ec-117"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="842ec-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="842ec-118">I requisiti del buffer non sono stati specificati.</span><span class="sxs-lookup"><span data-stu-id="842ec-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="842ec-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="842ec-119">Remarks</span></span>

<span data-ttu-id="842ec-120">Prima di chiamare questo metodo, chiamare il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) per specificare i requisiti del buffer.</span><span class="sxs-lookup"><span data-stu-id="842ec-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="842ec-121">Questo metodo chiama il metodo virtuale [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) per allocare la memoria per i buffer.</span><span class="sxs-lookup"><span data-stu-id="842ec-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="842ec-122">Le classi derivate possono eseguire l'override di **Alloc**.</span><span class="sxs-lookup"><span data-stu-id="842ec-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="842ec-123">Se un'operazione di decommit è in sospeso, viene annullata.</span><span class="sxs-lookup"><span data-stu-id="842ec-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="842ec-124">È necessario chiamare questo metodo prima di chiamare il metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="842ec-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="842ec-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842ec-125">Requirements</span></span>



| <span data-ttu-id="842ec-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="842ec-126">Requirement</span></span> | <span data-ttu-id="842ec-127">Valore</span><span class="sxs-lookup"><span data-stu-id="842ec-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842ec-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="842ec-128">Header</span></span><br/>  | <dl> <span data-ttu-id="842ec-129"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="842ec-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="842ec-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="842ec-130">Library</span></span><br/> | <dl> <span data-ttu-id="842ec-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="842ec-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842ec-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="842ec-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842ec-133">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="842ec-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




