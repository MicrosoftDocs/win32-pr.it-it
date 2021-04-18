---
description: Puntatore all'allocatore che ha creato l'esempio.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membro CMediaSample:: m_pAllocator (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324933"
---
# <a name="cmediasamplem_pallocator-member"></a><span data-ttu-id="77679-103">Membro pAllocator di CMediaSample:: m \_</span><span class="sxs-lookup"><span data-stu-id="77679-103">CMediaSample::m\_pAllocator member</span></span>

<span data-ttu-id="77679-104">Puntatore all'allocatore che ha creato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="77679-104">Pointer to the allocator that created this sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="77679-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77679-105">Syntax</span></span>


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a><span data-ttu-id="77679-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="77679-106">Remarks</span></span>

<span data-ttu-id="77679-107">Sebbene nell'esempio venga mantenuto un puntatore all'allocatore, non viene mantenuto un conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="77679-107">Although the sample keeps a pointer to the allocator, it does not hold a reference count.</span></span> <span data-ttu-id="77679-108">Al contrario, l'allocatore incrementa il proprio conteggio dei riferimenti nel metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) e rilascia se stesso nel metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="77679-108">Instead, the allocator increments its own reference count in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method, and releases itself in the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span> <span data-ttu-id="77679-109">Ciò garantisce che l'allocatore sarà disponibile purché un altro oggetto stia usando l'esempio.</span><span class="sxs-lookup"><span data-stu-id="77679-109">This guarantees that the allocator will be available as long as another object is using the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="77679-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77679-110">Requirements</span></span>



| <span data-ttu-id="77679-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="77679-111">Requirement</span></span> | <span data-ttu-id="77679-112">Valore</span><span class="sxs-lookup"><span data-stu-id="77679-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77679-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="77679-113">Header</span></span><br/>  | <dl> <span data-ttu-id="77679-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77679-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="77679-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="77679-115">Library</span></span><br/> | <dl> <span data-ttu-id="77679-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="77679-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77679-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77679-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77679-118">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="77679-118">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




