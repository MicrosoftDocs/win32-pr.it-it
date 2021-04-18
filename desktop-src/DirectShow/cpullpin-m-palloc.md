---
description: La \_ variabile membro pAlloc m è un puntatore all'interfaccia IMemAllocator dell'allocatore di memoria.
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Membro CPullPin:: m_pAlloc (Pullpin. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331164"
---
# <a name="cpullpinm_palloc-member"></a><span data-ttu-id="26606-103">Membro pAlloc di CPullPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="26606-103">CPullPin::m\_pAlloc member</span></span>

<span data-ttu-id="26606-104">La `m_pAlloc` variabile membro è un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="26606-104">The `m_pAlloc` member variable is a pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="26606-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26606-105">Syntax</span></span>


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a><span data-ttu-id="26606-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="26606-106">Remarks</span></span>

<span data-ttu-id="26606-107">Il metodo [**CPullPin::D ecideallocator**](cpullpin-decideallocator.md) imposta questa variabile membro.</span><span class="sxs-lookup"><span data-stu-id="26606-107">The [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) method sets this member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="26606-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26606-108">Requirements</span></span>



| <span data-ttu-id="26606-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="26606-109">Requirement</span></span> | <span data-ttu-id="26606-110">Valore</span><span class="sxs-lookup"><span data-stu-id="26606-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26606-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26606-111">Header</span></span><br/>  | <dl> <span data-ttu-id="26606-112"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="26606-112"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="26606-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="26606-113">Library</span></span><br/> | <dl> <span data-ttu-id="26606-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="26606-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26606-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26606-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26606-116">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="26606-116">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




