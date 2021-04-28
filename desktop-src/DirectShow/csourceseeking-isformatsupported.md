---
description: 'Metodo CSourceSeeking.IsFormatSupported: il metodo IsFormatSupported determina se è supportato un formato di ora specificato. Questo metodo implementa il metodo IMediaSeeking::IsFormatSupported.'
ms.assetid: 79b6dfd4-7f03-479b-b855-8f389bf6cbc7
title: Metodo CSourceSeeking.IsFormatSupported (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c58e8edd908c101c3045e221cc86420cbb5cb94
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098749"
---
# <a name="csourceseekingisformatsupported-method"></a><span data-ttu-id="e8a40-104">Metodo CSourceSeeking.IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="e8a40-104">CSourceSeeking.IsFormatSupported method</span></span>

<span data-ttu-id="e8a40-105">Il `IsFormatSupported` metodo determina se è supportato un formato di ora specificato.</span><span class="sxs-lookup"><span data-stu-id="e8a40-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="e8a40-106">Questo metodo implementa il [**metodo IMediaSeeking::IsFormatSupported.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)</span><span class="sxs-lookup"><span data-stu-id="e8a40-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a40-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8a40-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="e8a40-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8a40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a40-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="e8a40-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a40-110">Puntatore a un GUID di formato ora.</span><span class="sxs-lookup"><span data-stu-id="e8a40-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="e8a40-111">Vedere [**GUID di formato dell'ora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="e8a40-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a40-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8a40-112">Return value</span></span>

<span data-ttu-id="e8a40-113">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e8a40-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="e8a40-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8a40-114">Return code</span></span>                                                                               | <span data-ttu-id="e8a40-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8a40-115">Description</span></span>                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e8a40-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="e8a40-116"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="e8a40-117">Il formato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e8a40-117">The format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="e8a40-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8a40-118"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="e8a40-119">Il formato è supportato.</span><span class="sxs-lookup"><span data-stu-id="e8a40-119">The format is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="e8a40-120"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="e8a40-120"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="e8a40-121">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e8a40-121">**NULL** pointer argument.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="e8a40-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8a40-122">Remarks</span></span>

<span data-ttu-id="e8a40-123">L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità di 100 nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="e8a40-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a40-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8a40-124">Requirements</span></span>



| <span data-ttu-id="e8a40-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a40-125">Requirement</span></span> | <span data-ttu-id="e8a40-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e8a40-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a40-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8a40-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e8a40-128"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a40-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e8a40-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e8a40-129">Library</span></span><br/> | <dl> <span data-ttu-id="e8a40-130"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a40-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a40-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8a40-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a40-132">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="e8a40-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




