---
description: "Metodo CPosPassThru.GetTimeFormat: il metodo GetTimeFormat recupera il formato dell'ora corrente. Questo metodo implementa il metodo IMediaSeeking::GetTimeFormat."
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Metodo CPosPassThru.GetTimeFormat (Ctlutil.h)
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
ms.openlocfilehash: 903d1c6163d4cad5c5b9ca22213b02542bb3da49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085589"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="304e1-104">Metodo CPosPassThru.GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="304e1-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="304e1-105">Il `GetTimeFormat` metodo recupera il formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="304e1-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="304e1-106">Questo metodo implementa il [**metodo IMediaSeeking::GetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)</span><span class="sxs-lookup"><span data-stu-id="304e1-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="304e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="304e1-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="304e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="304e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="304e1-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="304e1-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="304e1-110">Puntatore a una variabile che riceve un GUID di formato ora.</span><span class="sxs-lookup"><span data-stu-id="304e1-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="304e1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="304e1-111">Return value</span></span>

<span data-ttu-id="304e1-112">Restituisce il **valore HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="304e1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="304e1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="304e1-113">Requirements</span></span>



| <span data-ttu-id="304e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="304e1-114">Requirement</span></span> | <span data-ttu-id="304e1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="304e1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="304e1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="304e1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="304e1-117"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="304e1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="304e1-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="304e1-118">Library</span></span><br/> | <dl> <span data-ttu-id="304e1-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="304e1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="304e1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="304e1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="304e1-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="304e1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="304e1-122">**GUID di formato ora**</span><span class="sxs-lookup"><span data-stu-id="304e1-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




