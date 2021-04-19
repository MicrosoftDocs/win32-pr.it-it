---
description: "Il metodo SetTimeFormat imposta il formato dell'ora. Questo metodo implementa il metodo IMediaSeeking:: SetTimeFormat."
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Metodo CPosPassThru. SetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b843e67a827e4bbd7471bb42df31033e314d9158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328498"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="9a38c-104">CPosPassThru. SetTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="9a38c-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="9a38c-105">Il metodo SetTimeFormat imposta il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="9a38c-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="9a38c-106">Questo metodo implementa il metodo [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="9a38c-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a38c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a38c-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="9a38c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a38c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a38c-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="9a38c-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="9a38c-110">Puntatore a un GUID del formato ora.</span><span class="sxs-lookup"><span data-stu-id="9a38c-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a38c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a38c-111">Return value</span></span>

<span data-ttu-id="9a38c-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="9a38c-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a38c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a38c-113">Requirements</span></span>



| <span data-ttu-id="9a38c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a38c-114">Requirement</span></span> | <span data-ttu-id="9a38c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="9a38c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a38c-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9a38c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9a38c-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a38c-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a38c-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="9a38c-118">Library</span></span><br/> | <dl> <span data-ttu-id="9a38c-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a38c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a38c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a38c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a38c-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="9a38c-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="9a38c-122">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="9a38c-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




