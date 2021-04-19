---
description: Puntatore al blocco di memoria che contiene i buffer.
ms.assetid: b9d08f5b-8616-4f68-869a-e8ebb77ccdc1
title: 'Membro CMemAllocator:: m_pBuffer (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pBuffer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ae988474196e323cde24305b0e389ac69f0f10d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333601"
---
# <a name="cmemallocatorm_pbuffer-member"></a><span data-ttu-id="cc568-103">Membro pBuffer di CMemAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="cc568-103">CMemAllocator::m\_pBuffer member</span></span>

<span data-ttu-id="cc568-104">Puntatore al blocco di memoria che contiene i buffer.</span><span class="sxs-lookup"><span data-stu-id="cc568-104">Pointer to the memory block that contains the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc568-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc568-105">Syntax</span></span>


```C++
LPBYTE m_pBuffer;
```



## <a name="remarks"></a><span data-ttu-id="cc568-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="cc568-106">Remarks</span></span>

<span data-ttu-id="cc568-107">I buffer di esempio vengono calcolati come offset da questo puntatore.</span><span class="sxs-lookup"><span data-stu-id="cc568-107">Sample buffers are calculated as offsets from this pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc568-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc568-108">Requirements</span></span>



| <span data-ttu-id="cc568-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc568-109">Requirement</span></span> | <span data-ttu-id="cc568-110">Valore</span><span class="sxs-lookup"><span data-stu-id="cc568-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc568-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc568-111">Header</span></span><br/>  | <dl> <span data-ttu-id="cc568-112"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc568-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc568-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc568-113">Library</span></span><br/> | <dl> <span data-ttu-id="cc568-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cc568-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc568-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc568-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc568-116">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="cc568-116">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




