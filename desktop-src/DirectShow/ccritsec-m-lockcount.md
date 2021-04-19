---
description: Numero di blocchi in attesa su questo oggetto.
ms.assetid: 27506c1d-6a9a-4410-80fb-6d4f2fd2f824
title: 'Membro CCritSec:: m_lockCount (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lockCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88098a8ded025a899e2092a96308bd6c54750758
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329861"
---
# <a name="ccritsecm_lockcount-member"></a><span data-ttu-id="2ed13-103">Membro lockCount di CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="2ed13-103">CCritSec::m\_lockCount member</span></span>

<span data-ttu-id="2ed13-104">Numero di blocchi in attesa su questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2ed13-104">Number of outstanding locks on this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ed13-105">Syntax</span></span>


```C++
DWORD m_lockCount;
```



## <a name="remarks"></a><span data-ttu-id="2ed13-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="2ed13-106">Remarks</span></span>

<span data-ttu-id="2ed13-107">Questa variabile membro viene definita solo nella versione di debug della classe di base.</span><span class="sxs-lookup"><span data-stu-id="2ed13-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="2ed13-108">Il membro viene usato dalle funzioni di [debug della sezione critica](critical-section-debugging-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed13-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) functions use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed13-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ed13-109">Requirements</span></span>



| <span data-ttu-id="2ed13-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed13-110">Requirement</span></span> | <span data-ttu-id="2ed13-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2ed13-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed13-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ed13-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2ed13-113"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed13-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2ed13-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ed13-114">Library</span></span><br/> | <dl> <span data-ttu-id="2ed13-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2ed13-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed13-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ed13-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed13-117">**Classe CCritSec**</span><span class="sxs-lookup"><span data-stu-id="2ed13-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




