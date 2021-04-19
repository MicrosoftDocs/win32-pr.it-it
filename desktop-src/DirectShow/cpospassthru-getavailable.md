---
description: "Il metodo GetAvailable recupera l'intervallo di tempo in cui la ricerca è efficiente. Questo metodo implementa il metodo IMediaSeeking:: GetAvailable."
ms.assetid: 5f4af41a-eb7b-4caa-97e0-aaed78467723
title: Metodo CPosPassThru. GetAvailable (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32dbba173caf933185602523dadcf71ce7ca3ef7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327539"
---
# <a name="cpospassthrugetavailable-method"></a><span data-ttu-id="1ec2e-104">Metodo CPosPassThru. GetAvailable</span><span class="sxs-lookup"><span data-stu-id="1ec2e-104">CPosPassThru.GetAvailable method</span></span>

<span data-ttu-id="1ec2e-105">Il `GetAvailable` metodo recupera l'intervallo di tempo in cui la ricerca è efficiente.</span><span class="sxs-lookup"><span data-stu-id="1ec2e-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="1ec2e-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) .</span><span class="sxs-lookup"><span data-stu-id="1ec2e-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec2e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ec2e-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="1ec2e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ec2e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec2e-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="1ec2e-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec2e-110">Puntatore a una variabile che riceve la prima ora per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="1ec2e-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span>

</dd> <dt>

<span data-ttu-id="1ec2e-111">*Piatto*</span><span class="sxs-lookup"><span data-stu-id="1ec2e-111">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="1ec2e-112">Puntatore a una variabile che riceve l'ora più recente per una ricerca efficiente.</span><span class="sxs-lookup"><span data-stu-id="1ec2e-112">Pointer to a variable that receives the latest time for efficient seeking.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec2e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ec2e-113">Return value</span></span>

<span data-ttu-id="1ec2e-114">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="1ec2e-114">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec2e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ec2e-115">Requirements</span></span>



| <span data-ttu-id="1ec2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec2e-116">Requirement</span></span> | <span data-ttu-id="1ec2e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1ec2e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec2e-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ec2e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec2e-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2e-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ec2e-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ec2e-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ec2e-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ec2e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec2e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ec2e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec2e-123">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1ec2e-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




