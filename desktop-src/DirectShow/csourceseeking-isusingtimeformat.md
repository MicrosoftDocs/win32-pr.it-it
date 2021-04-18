---
description: Il metodo IsUsingTimeFormat determina se un formato di ora specificato è il formato attualmente in uso.
ms.assetid: 86965bfc-fc9f-42d3-bcaa-2049195b98bd
title: Metodo CSourceSeeking. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8229387364a061febc7bd825e7bc76ee5d9b4a2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329496"
---
# <a name="csourceseekingisusingtimeformat-method"></a><span data-ttu-id="fc274-103">CSourceSeeking. IsUsingTimeFormat, metodo</span><span class="sxs-lookup"><span data-stu-id="fc274-103">CSourceSeeking.IsUsingTimeFormat method</span></span>

<span data-ttu-id="fc274-104">Il `IsUsingTimeFormat` metodo determina se un formato di ora specificato è il formato attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="fc274-104">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc274-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc274-105">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="fc274-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc274-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc274-107">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="fc274-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="fc274-108">Puntatore a un GUID del formato ora.</span><span class="sxs-lookup"><span data-stu-id="fc274-108">Pointer to a time format GUID.</span></span> <span data-ttu-id="fc274-109">Vedere [**GUID del formato ora**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="fc274-109">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc274-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc274-110">Return value</span></span>

<span data-ttu-id="fc274-111">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fc274-111">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fc274-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fc274-112">Return code</span></span>                                                                               | <span data-ttu-id="fc274-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc274-113">Description</span></span>                                                |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="fc274-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="fc274-114"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="fc274-115">Il formato specificato non è quello corrente.</span><span class="sxs-lookup"><span data-stu-id="fc274-115">The specified format is not the current format.</span></span><br/> |
| <dl> <span data-ttu-id="fc274-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fc274-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fc274-117">Il formato specificato è il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="fc274-117">The specified format is the current format.</span></span><br/>     |
| <dl> <span data-ttu-id="fc274-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="fc274-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fc274-119">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="fc274-119">**NULL** pointer argument.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="fc274-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc274-120">Remarks</span></span>

<span data-ttu-id="fc274-121">L'unico formato di ora supportato dalla classe base è il \_ tempo medio di formato dell'ora \_ \_ (unità 100-nanosecondi).</span><span class="sxs-lookup"><span data-stu-id="fc274-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc274-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc274-122">Requirements</span></span>



| <span data-ttu-id="fc274-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc274-123">Requirement</span></span> | <span data-ttu-id="fc274-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fc274-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc274-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc274-125">Header</span></span><br/>  | <dl> <span data-ttu-id="fc274-126"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc274-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc274-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc274-127">Library</span></span><br/> | <dl> <span data-ttu-id="fc274-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc274-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc274-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc274-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc274-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="fc274-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




