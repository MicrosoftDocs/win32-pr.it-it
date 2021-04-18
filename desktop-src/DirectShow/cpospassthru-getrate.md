---
description: 'Il metodo getrate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaSeeking:: getrate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Metodo CPosPassThru. getrate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e96bb231eb3e5c41f8cdf18c649f20955ba5cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325512"
---
# <a name="cpospassthrugetrate-method"></a><span data-ttu-id="6031e-104">CPosPassThru. getrate, metodo</span><span class="sxs-lookup"><span data-stu-id="6031e-104">CPosPassThru.GetRate method</span></span>

<span data-ttu-id="6031e-105">Il `GetRate` metodo recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6031e-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="6031e-106">Questo metodo implementa il metodo [**IMediaSeeking:: getrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .</span><span class="sxs-lookup"><span data-stu-id="6031e-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6031e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6031e-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="6031e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6031e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6031e-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="6031e-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="6031e-110">Puntatore a una variabile che riceve la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="6031e-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6031e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6031e-111">Return value</span></span>

<span data-ttu-id="6031e-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="6031e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="6031e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6031e-113">Requirements</span></span>



| <span data-ttu-id="6031e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6031e-114">Requirement</span></span> | <span data-ttu-id="6031e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6031e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6031e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6031e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6031e-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6031e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6031e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="6031e-118">Library</span></span><br/> | <dl> <span data-ttu-id="6031e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6031e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6031e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6031e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6031e-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="6031e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




