---
description: 'Il metodo IsUsingTimeFormat determina se un formato di ora specificato è il formato attualmente in uso. Questo metodo implementa il metodo IMediaSeeking:: IsUsingTimeFormat.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Metodo CPosPassThru. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333199"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="af99e-104">CPosPassThru. IsUsingTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="af99e-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="af99e-105">Il `IsUsingTimeFormat` metodo determina se un formato di ora specificato è il formato attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="af99e-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="af99e-106">Questo metodo implementa il metodo [**IMediaSeeking:: IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .</span><span class="sxs-lookup"><span data-stu-id="af99e-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="af99e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af99e-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="af99e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af99e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af99e-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="af99e-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="af99e-110">Puntatore a un GUID del formato ora.</span><span class="sxs-lookup"><span data-stu-id="af99e-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af99e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af99e-111">Return value</span></span>

<span data-ttu-id="af99e-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="af99e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="af99e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af99e-113">Requirements</span></span>



| <span data-ttu-id="af99e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="af99e-114">Requirement</span></span> | <span data-ttu-id="af99e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="af99e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af99e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af99e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="af99e-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af99e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af99e-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="af99e-118">Library</span></span><br/> | <dl> <span data-ttu-id="af99e-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af99e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af99e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af99e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af99e-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="af99e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="af99e-122">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="af99e-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




