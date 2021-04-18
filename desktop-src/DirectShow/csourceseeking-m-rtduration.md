---
description: 'Durata del flusso. Per impostazione predefinita, il valore viene impostato sul valore della variabile membro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329485"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="b8da4-104">Membro rtDuration di CSourceSeeking:: m \_</span><span class="sxs-lookup"><span data-stu-id="b8da4-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="b8da4-105">Durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="b8da4-105">Duration of the stream.</span></span> <span data-ttu-id="b8da4-106">Per impostazione predefinita, il valore viene impostato sul valore della variabile membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="b8da4-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8da4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8da4-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="b8da4-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b8da4-108">Remarks</span></span>

<span data-ttu-id="b8da4-109">Prima di accedere a questa variabile, mantenere la sezione **\_ pLock critico m** .</span><span class="sxs-lookup"><span data-stu-id="b8da4-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8da4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8da4-110">Requirements</span></span>



| <span data-ttu-id="b8da4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8da4-111">Requirement</span></span> | <span data-ttu-id="b8da4-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b8da4-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8da4-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8da4-113">Header</span></span><br/>  | <dl> <span data-ttu-id="b8da4-114"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8da4-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8da4-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="b8da4-115">Library</span></span><br/> | <dl> <span data-ttu-id="b8da4-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b8da4-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8da4-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8da4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8da4-118">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="b8da4-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




