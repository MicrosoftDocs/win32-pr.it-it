---
description: Puntatore a un oggetto sezione critica che protegge lo stato del filtro.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Membro CBasePin:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331524"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="4419c-103">Membro pLock di CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="4419c-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="4419c-104">Puntatore a un oggetto sezione critica che protegge lo stato del filtro.</span><span class="sxs-lookup"><span data-stu-id="4419c-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4419c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4419c-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="4419c-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4419c-106">Requirements</span></span>



| <span data-ttu-id="4419c-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="4419c-107">Requirement</span></span> | <span data-ttu-id="4419c-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4419c-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4419c-109">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4419c-109">Header</span></span><br/>  | <dl> <span data-ttu-id="4419c-110"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4419c-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4419c-111">Libreria</span><span class="sxs-lookup"><span data-stu-id="4419c-111">Library</span></span><br/> | <dl> <span data-ttu-id="4419c-112"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4419c-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4419c-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4419c-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4419c-114">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="4419c-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="4419c-115">Thread e sezioni critiche</span><span class="sxs-lookup"><span data-stu-id="4419c-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




