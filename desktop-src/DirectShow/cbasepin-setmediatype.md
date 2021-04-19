---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Metodo CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330312"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="43352-103">CBasePin. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="43352-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="43352-104">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="43352-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="43352-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43352-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="43352-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43352-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="43352-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="43352-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="43352-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43352-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43352-109">Return value</span></span>

<span data-ttu-id="43352-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43352-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43352-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="43352-111">Remarks</span></span>

<span data-ttu-id="43352-112">Questo metodo stabilisce il formato per una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="43352-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="43352-113">Prima di chiamare questo metodo, il pin chiama il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il tipo di supporto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="43352-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="43352-114">Pertanto, si presuppone che il parametro *PMT* sia un tipo di supporto accettabile.</span><span class="sxs-lookup"><span data-stu-id="43352-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="43352-115">Nella classe di base, questo metodo imposta la variabile membro [**CBasePin:: m \_ mt**](cbasepin-m-mt.md) e restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43352-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="43352-116">Una classe derivata può eseguire l'override di questo metodo se è necessaria una notifica quando è impostato il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="43352-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="43352-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43352-117">Requirements</span></span>



| <span data-ttu-id="43352-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43352-118">Requirement</span></span> | <span data-ttu-id="43352-119">Valore</span><span class="sxs-lookup"><span data-stu-id="43352-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43352-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43352-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43352-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43352-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="43352-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="43352-122">Library</span></span><br/> | <dl> <span data-ttu-id="43352-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43352-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43352-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43352-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43352-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="43352-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




