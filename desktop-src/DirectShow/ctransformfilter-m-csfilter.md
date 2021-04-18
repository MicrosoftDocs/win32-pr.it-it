---
description: Sezione critica che protegge lo stato del filtro. Per ulteriori informazioni, vedere flusso di dati per gli sviluppatori di filtri.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Membro CTransformFilter:: m_csFilter (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331141"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="d4287-104">Membro csFilter di CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="d4287-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="d4287-105">Sezione critica che protegge lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="d4287-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="d4287-106">Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="d4287-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d4287-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4287-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="d4287-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4287-108">Requirements</span></span>



| <span data-ttu-id="d4287-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4287-109">Requirement</span></span> | <span data-ttu-id="d4287-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d4287-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4287-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4287-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d4287-112"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4287-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d4287-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4287-113">Library</span></span><br/> | <dl> <span data-ttu-id="d4287-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4287-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4287-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4287-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4287-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d4287-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




