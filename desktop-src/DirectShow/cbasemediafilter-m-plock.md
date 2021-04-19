---
description: Puntatore a una sezione critica.
ms.assetid: 7d949b7f-a6a7-4ab5-b651-f85b70d55065
title: 'Membro CBaseMediaFilter:: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 126aa213004dd032eea43b28198b6f8b49fe7f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330234"
---
# <a name="cbasemediafilterm_plock-member"></a><span data-ttu-id="fd516-103">Membro pLock di CBaseMediaFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="fd516-103">CBaseMediaFilter::m\_pLock member</span></span>

<span data-ttu-id="fd516-104">Puntatore a una sezione critica.</span><span class="sxs-lookup"><span data-stu-id="fd516-104">Pointer to a critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd516-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd516-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="fd516-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="fd516-106">Remarks</span></span>

<span data-ttu-id="fd516-107">La sezione critica viene mantenuta durante le transizioni di stato ([**CBaseMediaFilter:: Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::P ause**](cbasemediafilter-pause.md), [**CBaseMediaFilter:: Stop**](cbasemediafilter-stop.md)), quando si accede al clock di riferimento ([**CBaseMediaFilter:: SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter:: GetSyncSource**](cbasemediafilter-getsyncsource.md)) e nel metodo [**CBaseMediaFilter::**](cbasemediafilter-isactive.md) IsValid.</span><span class="sxs-lookup"><span data-stu-id="fd516-107">The critical section is held during state transitions ([**CBaseMediaFilter::Run**](cbasemediafilter-run.md), [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md), [**CBaseMediaFilter::Stop**](cbasemediafilter-stop.md)), when accessing the reference clock ([**CBaseMediaFilter::SetSyncSource**](cbasemediafilter-setsyncsource.md), [**CBaseMediaFilter::GetSyncSource**](cbasemediafilter-getsyncsource.md)), and in the [**CBaseMediaFilter::IsActive**](cbasemediafilter-isactive.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd516-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd516-108">Requirements</span></span>



| <span data-ttu-id="fd516-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd516-109">Requirement</span></span> | <span data-ttu-id="fd516-110">Valore</span><span class="sxs-lookup"><span data-stu-id="fd516-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd516-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd516-111">Header</span></span><br/>  | <dl> <span data-ttu-id="fd516-112"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd516-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fd516-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd516-113">Library</span></span><br/> | <dl> <span data-ttu-id="fd516-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fd516-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd516-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd516-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd516-116">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="fd516-116">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




