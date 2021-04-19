---
description: Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Metodo CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332592"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="98fb8-103">CBasePin. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="98fb8-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="98fb8-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="98fb8-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="98fb8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98fb8-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="98fb8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98fb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98fb8-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="98fb8-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="98fb8-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="98fb8-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98fb8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98fb8-109">Return value</span></span>

<span data-ttu-id="98fb8-110">Restituisce \_ OK se il tipo di supporto proposto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="98fb8-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="98fb8-111">In caso contrario, restituisce \_ false o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="98fb8-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98fb8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="98fb8-112">Remarks</span></span>

<span data-ttu-id="98fb8-113">La classe derivata deve eseguire l'override di questo metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="98fb8-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98fb8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98fb8-114">Requirements</span></span>



| <span data-ttu-id="98fb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98fb8-115">Requirement</span></span> | <span data-ttu-id="98fb8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98fb8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98fb8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98fb8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98fb8-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98fb8-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98fb8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="98fb8-119">Library</span></span><br/> | <dl> <span data-ttu-id="98fb8-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98fb8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98fb8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98fb8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98fb8-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="98fb8-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




