---
description: "Il metodo QueryPreferredFormat Recupera il formato ora preferito dell'oggetto. Questo metodo implementa il metodo IMediaSeeking:: QueryPreferredFormat."
ms.assetid: 3b73b7cf-1ba7-47c5-8442-5f138b74f335
title: Metodo CSourceSeeking. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8916e23756279dd30eaf177ef839944a4c68d61a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328488"
---
# <a name="csourceseekingquerypreferredformat-method"></a><span data-ttu-id="5717c-104">CSourceSeeking. QueryPreferredFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="5717c-104">CSourceSeeking.QueryPreferredFormat method</span></span>

<span data-ttu-id="5717c-105">Il `QueryPreferredFormat` metodo recupera il formato ora preferito dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5717c-105">The `QueryPreferredFormat` method retrieves the object's preferred time format.</span></span> <span data-ttu-id="5717c-106">Questo metodo implementa il metodo [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="5717c-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5717c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5717c-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="5717c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5717c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5717c-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="5717c-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5717c-110">Puntatore a una variabile che riceve un GUID del formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="5717c-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="5717c-111">Vedere [**GUID del formato ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="5717c-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5717c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5717c-112">Return value</span></span>

<span data-ttu-id="5717c-113">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5717c-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="5717c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5717c-114">Return code</span></span>                                                                               | <span data-ttu-id="5717c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5717c-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="5717c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5717c-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5717c-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="5717c-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="5717c-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5717c-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5717c-119">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="5717c-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5717c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5717c-120">Remarks</span></span>

<span data-ttu-id="5717c-121">L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="5717c-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="5717c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5717c-122">Requirements</span></span>



| <span data-ttu-id="5717c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5717c-123">Requirement</span></span> | <span data-ttu-id="5717c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="5717c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5717c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5717c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5717c-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5717c-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5717c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="5717c-127">Library</span></span><br/> | <dl> <span data-ttu-id="5717c-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5717c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5717c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5717c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5717c-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="5717c-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




