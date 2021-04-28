---
description: "Metodo CSourceSeeking.GetTimeFormat: il metodo GetTimeFormat recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking::GetTimeFormat."
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Metodo CSourceSeeking.GetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085219"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="d0c1d-104">Metodo CSourceSeeking.GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="d0c1d-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="d0c1d-105">Il `GetTimeFormat` metodo recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="d0c1d-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="d0c1d-106">Questo metodo implementa il [**metodo IMediaSeeking::GetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)</span><span class="sxs-lookup"><span data-stu-id="d0c1d-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0c1d-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d0c1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0c1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0c1d-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d0c1d-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d0c1d-110">Puntatore a una variabile che riceve un GUID di formato ora.</span><span class="sxs-lookup"><span data-stu-id="d0c1d-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="d0c1d-111">Vedere [**GUID di formato ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="d0c1d-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0c1d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0c1d-112">Return value</span></span>

<span data-ttu-id="d0c1d-113">Restituisce uno dei **valori HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d0c1d-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="d0c1d-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d0c1d-114">Return code</span></span>                                                                               | <span data-ttu-id="d0c1d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0c1d-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="d0c1d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1d-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d0c1d-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="d0c1d-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="d0c1d-118"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1d-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d0c1d-119">**Valore del** puntatore NULL</span><span class="sxs-lookup"><span data-stu-id="d0c1d-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0c1d-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0c1d-120">Remarks</span></span>

<span data-ttu-id="d0c1d-121">L'unico formato di ora supportato dalla classe di base è TIME \_ FORMAT \_ MEDIA TIME \_ (unità da 100 nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="d0c1d-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c1d-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0c1d-122">Requirements</span></span>



| <span data-ttu-id="d0c1d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0c1d-123">Requirement</span></span> | <span data-ttu-id="d0c1d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d0c1d-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c1d-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0c1d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c1d-126"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1d-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0c1d-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0c1d-127">Library</span></span><br/> | <dl> <span data-ttu-id="d0c1d-128"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0c1d-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c1d-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0c1d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c1d-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="d0c1d-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




