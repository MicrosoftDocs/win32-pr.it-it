---
description: "Il metodo GetTimeFormat Recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking:: GetTimeFormat."
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Metodo CSourceSeeking. GetTimeFormat (Ctlutil. h)
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
ms.openlocfilehash: ce53f4a6cabcc5face6c332666701dc208c3f8bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329500"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="bf2bb-104">CSourceSeeking. GetTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="bf2bb-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="bf2bb-105">Il `GetTimeFormat` metodo recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="bf2bb-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="bf2bb-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="bf2bb-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2bb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf2bb-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="bf2bb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf2bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf2bb-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="bf2bb-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="bf2bb-110">Puntatore a una variabile che riceve un GUID del formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="bf2bb-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="bf2bb-111">Vedere [**GUID del formato ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="bf2bb-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf2bb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf2bb-112">Return value</span></span>

<span data-ttu-id="bf2bb-113">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bf2bb-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="bf2bb-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bf2bb-114">Return code</span></span>                                                                               | <span data-ttu-id="bf2bb-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf2bb-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="bf2bb-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bb-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="bf2bb-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="bf2bb-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="bf2bb-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bb-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="bf2bb-119">Valore del puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="bf2bb-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf2bb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf2bb-120">Remarks</span></span>

<span data-ttu-id="bf2bb-121">L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="bf2bb-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2bb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf2bb-122">Requirements</span></span>



| <span data-ttu-id="bf2bb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf2bb-123">Requirement</span></span> | <span data-ttu-id="bf2bb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bf2bb-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2bb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf2bb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bf2bb-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bb-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf2bb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="bf2bb-127">Library</span></span><br/> | <dl> <span data-ttu-id="bf2bb-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bf2bb-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2bb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf2bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2bb-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="bf2bb-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




