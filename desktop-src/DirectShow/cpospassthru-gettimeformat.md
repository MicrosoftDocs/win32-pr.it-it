---
description: "Il metodo GetTimeFormat Recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking:: GetTimeFormat."
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Metodo CPosPassThru. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333205"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="ab86a-104">CPosPassThru. GetTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="ab86a-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="ab86a-105">Il `GetTimeFormat` metodo recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ab86a-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="ab86a-106">Questo metodo implementa il metodo [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="ab86a-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab86a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab86a-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="ab86a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab86a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab86a-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="ab86a-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="ab86a-110">Puntatore a una variabile che riceve un GUID del formato dell'ora.</span><span class="sxs-lookup"><span data-stu-id="ab86a-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab86a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab86a-111">Return value</span></span>

<span data-ttu-id="ab86a-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="ab86a-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab86a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab86a-113">Requirements</span></span>



| <span data-ttu-id="ab86a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab86a-114">Requirement</span></span> | <span data-ttu-id="ab86a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ab86a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab86a-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab86a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ab86a-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab86a-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab86a-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab86a-118">Library</span></span><br/> | <dl> <span data-ttu-id="ab86a-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ab86a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab86a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab86a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab86a-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ab86a-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="ab86a-122">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="ab86a-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




