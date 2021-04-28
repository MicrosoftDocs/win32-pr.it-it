---
description: "Metodo CSourceSeeking.SetTimeFormat: il metodo SetTimeFormat imposta il formato dell'ora. Questo metodo implementa il metodo IMediaSeeking::SetTimeFormat."
ms.assetid: dbc7c950-8cc2-4f8e-adfa-8f5cdc1b56c7
title: Metodo CSourceSeeking.SetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fdb3889ecfa5bdcd49b4054822a2b2d09df58fa6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085199"
---
# <a name="csourceseekingsettimeformat-method"></a><span data-ttu-id="ab564-104">Metodo CSourceSeeking.SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ab564-104">CSourceSeeking.SetTimeFormat method</span></span>

<span data-ttu-id="ab564-105">Il `SetTimeFormat` metodo imposta il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="ab564-105">The `SetTimeFormat` method sets the time format.</span></span> <span data-ttu-id="ab564-106">Questo metodo implementa il [**metodo IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)</span><span class="sxs-lookup"><span data-stu-id="ab564-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab564-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab564-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="ab564-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab564-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab564-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="ab564-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="ab564-110">Puntatore a un GUID di formato ora.</span><span class="sxs-lookup"><span data-stu-id="ab564-110">Pointer to a time format GUID.</span></span> <span data-ttu-id="ab564-111">Vedere [**GUID di formato dell'ora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="ab564-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab564-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab564-112">Return value</span></span>

<span data-ttu-id="ab564-113">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ab564-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="ab564-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ab564-114">Return code</span></span>                                                                                  | <span data-ttu-id="ab564-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab564-115">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="ab564-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab564-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ab564-117">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="ab564-117">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="ab564-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ab564-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ab564-119">Il formato specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ab564-119">Specified format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="ab564-120"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab564-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ab564-121">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ab564-121">**NULL** pointer argument.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="ab564-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab564-122">Remarks</span></span>

<span data-ttu-id="ab564-123">L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità di 100 nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="ab564-123">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab564-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab564-124">Requirements</span></span>



| <span data-ttu-id="ab564-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab564-125">Requirement</span></span> | <span data-ttu-id="ab564-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ab564-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab564-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab564-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ab564-128"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab564-128"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab564-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab564-129">Library</span></span><br/> | <dl> <span data-ttu-id="ab564-130"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab564-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab564-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab564-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab564-132">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="ab564-132">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




