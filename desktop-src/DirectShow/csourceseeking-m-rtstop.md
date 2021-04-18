---
description: Ora di arresto. Per impostazione predefinita, il valore è impostato su un numero molto elevato. La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.
ms.assetid: 1fddcf84-fd9a-4dad-892c-1b0abbb0ca55
title: 'Membro CSourceSeeking:: m_rtStop (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtStop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28031f245ef877eca38129df2a86210f90093db4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330201"
---
# <a name="csourceseekingm_rtstop-member"></a><span data-ttu-id="8b5b3-105">Membro rtStop di CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="8b5b3-105">CSourceSeeking::m\_rtStop member</span></span>

<span data-ttu-id="8b5b3-106">Ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-106">Stop time.</span></span> <span data-ttu-id="8b5b3-107">Per impostazione predefinita, il valore è impostato su un numero molto elevato.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-107">By default, the value is set to a very large number.</span></span> <span data-ttu-id="8b5b3-108">La classe derivata può reimpostare il valore nel costruttore o quando il filtro viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="8b5b3-108">The derived class can reset the value in its constructor, or when the filter is initialized.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5b3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b5b3-109">Syntax</span></span>


```C++
CRefTime m_rtStop;
```



## <a name="remarks"></a><span data-ttu-id="8b5b3-110">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8b5b3-110">Remarks</span></span>

<span data-ttu-id="8b5b3-111">Prima di accedere a questa variabile, mantenere la sezione **\_ pLock critico m** .</span><span class="sxs-lookup"><span data-stu-id="8b5b3-111">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b5b3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b5b3-112">Requirements</span></span>



| <span data-ttu-id="8b5b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b5b3-113">Requirement</span></span> | <span data-ttu-id="8b5b3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8b5b3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5b3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8b5b3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8b5b3-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b5b3-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b5b3-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="8b5b3-117">Library</span></span><br/> | <dl> <span data-ttu-id="8b5b3-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8b5b3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b5b3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b5b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5b3-120">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="8b5b3-120">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




