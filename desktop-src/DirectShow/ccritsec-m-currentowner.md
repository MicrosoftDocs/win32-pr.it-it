---
description: Identificatore del thread proprietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Membro CCritSec:: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332585"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="c3088-103">Membro currentOwner di CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="c3088-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="c3088-104">Identificatore del thread proprietario.</span><span class="sxs-lookup"><span data-stu-id="c3088-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3088-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3088-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="c3088-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c3088-106">Remarks</span></span>

<span data-ttu-id="c3088-107">Questa variabile membro viene definita solo nella versione di debug della classe di base.</span><span class="sxs-lookup"><span data-stu-id="c3088-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="c3088-108">Il membro viene usato dalle [funzioni di debug della sezione critica](critical-section-debugging-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="c3088-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3088-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3088-109">Requirements</span></span>



| <span data-ttu-id="c3088-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3088-110">Requirement</span></span> | <span data-ttu-id="c3088-111">Valore</span><span class="sxs-lookup"><span data-stu-id="c3088-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3088-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3088-112">Header</span></span><br/>  | <dl> <span data-ttu-id="c3088-113"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3088-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c3088-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="c3088-114">Library</span></span><br/> | <dl> <span data-ttu-id="c3088-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c3088-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3088-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3088-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3088-117">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="c3088-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




