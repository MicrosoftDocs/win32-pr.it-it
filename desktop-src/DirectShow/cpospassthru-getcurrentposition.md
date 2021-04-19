---
description: 'Il metodo GetCurrentPosition recupera la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaSeeking:: GetCurrentPosition.'
ms.assetid: 07020182-2199-4153-9bab-f30d112bc09f
title: Metodo CPosPassThru. GetCurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5cdbd93edf7630499f6585fbbf6e34a70bed68c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329374"
---
# <a name="cpospassthrugetcurrentposition-method"></a><span data-ttu-id="4b930-104">CPosPassThru. GetCurrentPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="4b930-104">CPosPassThru.GetCurrentPosition method</span></span>

<span data-ttu-id="4b930-105">Il `GetCurrentPosition` metodo recupera la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="4b930-105">The `GetCurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="4b930-106">Questo metodo implementa il metodo [**IMediaSeeking:: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) .</span><span class="sxs-lookup"><span data-stu-id="4b930-106">This method implements the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b930-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b930-107">Syntax</span></span>


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a><span data-ttu-id="4b930-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b930-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b930-109">*pCurrent*</span><span class="sxs-lookup"><span data-stu-id="4b930-109">*pCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="4b930-110">Puntatore a una variabile che riceve la posizione corrente, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="4b930-110">Pointer to a variable that receives the current position, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b930-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b930-111">Return value</span></span>

<span data-ttu-id="4b930-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b930-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4b930-113">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4b930-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4b930-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4b930-114">Return code</span></span>                                                                               | <span data-ttu-id="4b930-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b930-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4b930-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b930-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4b930-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b930-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="4b930-118"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4b930-118"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="4b930-119">Il metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4b930-119">Method is not supported.</span></span><br/>   |
| <dl> <span data-ttu-id="4b930-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="4b930-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="4b930-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="4b930-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b930-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b930-122">Remarks</span></span>

<span data-ttu-id="4b930-123">Questo metodo chiama il metodo [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) per recuperare la posizione più recente.</span><span class="sxs-lookup"><span data-stu-id="4b930-123">This method calls the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method to retrieve the most recent position.</span></span> <span data-ttu-id="4b930-124">Se **GetMediaTime** ha esito negativo, il metodo chiama **IMediaSeeking:: getCurrentPosition** sul pin connesso.</span><span class="sxs-lookup"><span data-stu-id="4b930-124">If **GetMediaTime** fails, the method calls **IMediaSeeking::GetCurrentPosition** on the connected pin.</span></span>

<span data-ttu-id="4b930-125">Il metodo **GetMediaTime** ha esito negativo per impostazione predefinita nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="4b930-125">The **GetMediaTime** method fails by default in the base class.</span></span> <span data-ttu-id="4b930-126">Se il filtro memorizza nella cache la posizione corrente, eseguire l'override di **GetMediaTime** per restituire il valore memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="4b930-126">If your filter caches the current position, override **GetMediaTime** to return the cached value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b930-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b930-127">Requirements</span></span>



| <span data-ttu-id="4b930-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b930-128">Requirement</span></span> | <span data-ttu-id="4b930-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4b930-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b930-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b930-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4b930-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b930-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b930-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b930-132">Library</span></span><br/> | <dl> <span data-ttu-id="4b930-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b930-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b930-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b930-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b930-135">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="4b930-135">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




