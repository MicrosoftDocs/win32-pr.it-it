---
description: 'Il \_ metodo Get rate recupera la velocità di riproduzione. Questo metodo implementa il metodo IMediaPosition:: Get \_ rate.'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Metodo CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327842"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="c6c7b-104">Metodo CPosPassThru. Get \_ rate</span><span class="sxs-lookup"><span data-stu-id="c6c7b-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="c6c7b-105">Il `get_Rate` metodo recupera la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="c6c7b-106">Questo metodo implementa il metodo [**IMediaPosition:: Get \_ rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .</span><span class="sxs-lookup"><span data-stu-id="c6c7b-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c7b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6c7b-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="c6c7b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6c7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c7b-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="c6c7b-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="c6c7b-110">Puntatore a una variabile che riceve la velocità di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c7b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6c7b-111">Return value</span></span>

<span data-ttu-id="c6c7b-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="c6c7b-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c7b-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6c7b-113">Requirements</span></span>



| <span data-ttu-id="c6c7b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6c7b-114">Requirement</span></span> | <span data-ttu-id="c6c7b-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c6c7b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c7b-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6c7b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c6c7b-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c7b-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6c7b-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6c7b-118">Library</span></span><br/> | <dl> <span data-ttu-id="c6c7b-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c6c7b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6c7b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6c7b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c7b-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="c6c7b-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




