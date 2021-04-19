---
description: 'Identificatore del thread che ha chiamato per ultimo il metodo IPinFlowControl:: Block su questo pin. Questa variabile membro è valida solo quando il PIN è bloccato.'
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: 'Membro CDynamicOutputPin:: m_dwBlockCallerThreadID (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9aa2de66f1afe690715ab658483c01cdfeb3f451
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333448"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a><span data-ttu-id="b2f13-104">Membro dwBlockCallerThreadID di CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="b2f13-104">CDynamicOutputPin::m\_dwBlockCallerThreadID member</span></span>

<span data-ttu-id="b2f13-105">Identificatore del thread che ha chiamato per ultimo il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) su questo pin.</span><span class="sxs-lookup"><span data-stu-id="b2f13-105">The identifier of the thread that last called the [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) method on this pin.</span></span> <span data-ttu-id="b2f13-106">Questa variabile membro è valida solo quando il PIN è bloccato.</span><span class="sxs-lookup"><span data-stu-id="b2f13-106">This member variable is only valid while the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f13-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2f13-107">Syntax</span></span>


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a><span data-ttu-id="b2f13-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b2f13-108">Remarks</span></span>

<span data-ttu-id="b2f13-109">Prima di accedere a questa variabile, conservare la sezione [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical.</span><span class="sxs-lookup"><span data-stu-id="b2f13-109">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f13-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2f13-110">Requirements</span></span>



| <span data-ttu-id="b2f13-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f13-111">Requirement</span></span> | <span data-ttu-id="b2f13-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b2f13-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f13-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2f13-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b2f13-114"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f13-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2f13-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="b2f13-115">Library</span></span><br/> | <dl> <span data-ttu-id="b2f13-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f13-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f13-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2f13-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f13-118">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b2f13-118">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




