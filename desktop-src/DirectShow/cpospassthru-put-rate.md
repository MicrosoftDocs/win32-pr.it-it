---
description: Il \_ metodo Put rate imposta la velocità di riproduzione. Questo metodo implementa il metodo IMediaPosition::p UT \_ rate.
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Metodo CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21e7e654233f78adcda2addf73b87a178654872e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324181"
---
# <a name="cpospassthruput_rate-method"></a><span data-ttu-id="50029-104">Metodo di frequenza CPosPassThru. put \_</span><span class="sxs-lookup"><span data-stu-id="50029-104">CPosPassThru.put\_Rate method</span></span>

<span data-ttu-id="50029-105">Il `put_Rate` metodo imposta la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="50029-105">The `put_Rate` method sets the playback rate.</span></span> <span data-ttu-id="50029-106">Questo metodo implementa il metodo [**IMediaPosition::p UT \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .</span><span class="sxs-lookup"><span data-stu-id="50029-106">This method implements the [**IMediaPosition::put\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="50029-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50029-107">Syntax</span></span>


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="50029-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="50029-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50029-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="50029-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="50029-110">Velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="50029-110">Playback rate.</span></span> <span data-ttu-id="50029-111">Non deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="50029-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50029-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50029-112">Return value</span></span>

<span data-ttu-id="50029-113">Restituisce E \_ INVALIDARG se *drate* è zero.</span><span class="sxs-lookup"><span data-stu-id="50029-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="50029-114">In caso contrario, restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="50029-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="50029-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="50029-115">Remarks</span></span>

<span data-ttu-id="50029-116">Le frequenze negative indicano la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="50029-116">Negative rates indicate reverse play.</span></span> <span data-ttu-id="50029-117">Non tutti i supporti supporteranno la riproduzione inversa.</span><span class="sxs-lookup"><span data-stu-id="50029-117">Not all media will support reverse play.</span></span>

## <a name="requirements"></a><span data-ttu-id="50029-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50029-118">Requirements</span></span>



| <span data-ttu-id="50029-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50029-119">Requirement</span></span> | <span data-ttu-id="50029-120">Valore</span><span class="sxs-lookup"><span data-stu-id="50029-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50029-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50029-121">Header</span></span><br/>  | <dl> <span data-ttu-id="50029-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50029-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50029-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="50029-123">Library</span></span><br/> | <dl> <span data-ttu-id="50029-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="50029-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50029-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50029-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50029-126">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="50029-126">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




