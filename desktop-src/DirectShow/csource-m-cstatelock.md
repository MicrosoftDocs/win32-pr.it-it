---
description: Oggetto sezione critica che protegge lo stato del filtro. Il metodo helper CSource::p StateLock restituisce un puntatore a questa variabile membro.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: 'Membro CSource:: m_cStateLock (source. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325745"
---
# <a name="csourcem_cstatelock-member"></a><span data-ttu-id="88ad7-104">Membro cStateLock di CSource:: m \_</span><span class="sxs-lookup"><span data-stu-id="88ad7-104">CSource::m\_cStateLock member</span></span>

<span data-ttu-id="88ad7-105">Oggetto sezione critica che protegge lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="88ad7-105">Critical section object that protects the filter state.</span></span> <span data-ttu-id="88ad7-106">Il metodo helper [**CSource::P stateLock**](csource--pstatelock.md) restituisce un puntatore a questa variabile membro.</span><span class="sxs-lookup"><span data-stu-id="88ad7-106">The [**CSource::pStateLock**](csource--pstatelock.md) helper method returns a pointer to this member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ad7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88ad7-107">Syntax</span></span>


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a><span data-ttu-id="88ad7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88ad7-108">Requirements</span></span>



| <span data-ttu-id="88ad7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ad7-109">Requirement</span></span> | <span data-ttu-id="88ad7-110">Valore</span><span class="sxs-lookup"><span data-stu-id="88ad7-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ad7-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88ad7-111">Header</span></span><br/>  | <dl> <span data-ttu-id="88ad7-112"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88ad7-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="88ad7-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="88ad7-113">Library</span></span><br/> | <dl> <span data-ttu-id="88ad7-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88ad7-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ad7-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88ad7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ad7-116">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="88ad7-116">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




