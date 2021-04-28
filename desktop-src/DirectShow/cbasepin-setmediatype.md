---
description: 'Metodo CBasePin.SetMediaType: il metodo SetMediaType imposta il tipo di supporto per la connessione.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Metodo CBasePin.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095988"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="531da-103">Metodo CBasePin.SetMediaType</span><span class="sxs-lookup"><span data-stu-id="531da-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="531da-104">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="531da-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="531da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="531da-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="531da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="531da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="531da-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="531da-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="531da-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="531da-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="531da-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="531da-109">Return value</span></span>

<span data-ttu-id="531da-110">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="531da-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="531da-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="531da-111">Remarks</span></span>

<span data-ttu-id="531da-112">Questo metodo stabilisce il formato per una connessione pin.</span><span class="sxs-lookup"><span data-stu-id="531da-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="531da-113">Prima di chiamare questo metodo, il pin chiama il [**metodo CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) per determinare se il tipo di supporto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="531da-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="531da-114">Si presuppone pertanto *che il parametro pmt* sia un tipo di supporto accettabile.</span><span class="sxs-lookup"><span data-stu-id="531da-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="531da-115">Nella classe di base questo metodo imposta la variabile membro [**CBasePin::m \_ mt**](cbasepin-m-mt.md) e restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="531da-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="531da-116">Una classe derivata può eseguire l'override di questo metodo se richiede una notifica quando viene impostato il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="531da-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="531da-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="531da-117">Requirements</span></span>



| <span data-ttu-id="531da-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="531da-118">Requirement</span></span> | <span data-ttu-id="531da-119">Valore</span><span class="sxs-lookup"><span data-stu-id="531da-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531da-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="531da-120">Header</span></span><br/>  | <dl> <span data-ttu-id="531da-121"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="531da-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="531da-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="531da-122">Library</span></span><br/> | <dl> <span data-ttu-id="531da-123"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="531da-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531da-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="531da-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531da-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="531da-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




