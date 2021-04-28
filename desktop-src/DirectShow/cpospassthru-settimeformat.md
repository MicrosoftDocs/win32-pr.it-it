---
description: "Metodo CPosPassThru.SetTimeFormat: il metodo SetTimeFormat imposta il formato dell'ora. Questo metodo implementa il metodo IMediaSeeking::SetTimeFormat."
ms.assetid: f6fc456d-51cf-4b2e-9248-afed9073d440
title: Metodo CPosPassThru.SetTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: 81798ccbb51056353c62cd94f821b3567d78a484
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085469"
---
# <a name="cpospassthrusettimeformat-method"></a><span data-ttu-id="908ca-104">Metodo CPosPassThru.SetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="908ca-104">CPosPassThru.SetTimeFormat method</span></span>

<span data-ttu-id="908ca-105">Il metodo SetTimeFormat imposta il formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="908ca-105">The SetTimeFormat method sets the time format.</span></span> <span data-ttu-id="908ca-106">Questo metodo implementa il [**metodo IMediaSeeking::SetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)</span><span class="sxs-lookup"><span data-stu-id="908ca-106">This method implements the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="908ca-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="908ca-107">Syntax</span></span>


```C++
HRESULT SetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="908ca-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="908ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="908ca-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="908ca-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="908ca-110">Puntatore a un GUID di formato ora.</span><span class="sxs-lookup"><span data-stu-id="908ca-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="908ca-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="908ca-111">Return value</span></span>

<span data-ttu-id="908ca-112">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="908ca-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="908ca-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="908ca-113">Requirements</span></span>



| <span data-ttu-id="908ca-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="908ca-114">Requirement</span></span> | <span data-ttu-id="908ca-115">Valore</span><span class="sxs-lookup"><span data-stu-id="908ca-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="908ca-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="908ca-116">Header</span></span><br/>  | <dl> <span data-ttu-id="908ca-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="908ca-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="908ca-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="908ca-118">Library</span></span><br/> | <dl> <span data-ttu-id="908ca-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="908ca-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="908ca-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="908ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="908ca-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="908ca-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="908ca-122">**GUID di formato ora**</span><span class="sxs-lookup"><span data-stu-id="908ca-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




