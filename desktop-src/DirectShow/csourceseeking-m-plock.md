---
description: Puntatore a un oggetto sezione critica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membro CSourceSeeking:: m_pLock (Ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329488"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="35647-103">Membro pLock di CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="35647-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="35647-104">Puntatore a un oggetto sezione critica.</span><span class="sxs-lookup"><span data-stu-id="35647-104">Pointer to a critical section object.</span></span> <span data-ttu-id="35647-105">La `CSourceSeeking` classe usa questa sezione critica per sincronizzare l'accesso all'ora di inizio e di fine, alla durata e alle variabili di frequenza.</span><span class="sxs-lookup"><span data-stu-id="35647-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="35647-106">Questa variabile viene inizializzata nel metodo del costruttore. vedere [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="35647-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35647-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35647-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="35647-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35647-108">Requirements</span></span>



| <span data-ttu-id="35647-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="35647-109">Requirement</span></span> | <span data-ttu-id="35647-110">Valore</span><span class="sxs-lookup"><span data-stu-id="35647-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35647-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35647-111">Header</span></span><br/>  | <dl> <span data-ttu-id="35647-112"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35647-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35647-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="35647-113">Library</span></span><br/> | <dl> <span data-ttu-id="35647-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35647-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35647-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35647-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35647-116">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="35647-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




