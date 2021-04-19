---
description: Il \_ metodo Put CurrentPosition imposta la posizione corrente rispetto alla durata totale del flusso. Questo metodo implementa il metodo IMediaPosition::p UT \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: Metodo CPosPassThru.put_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85426636a34d0e197b36496d5a38a847c61b9501
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333195"
---
# <a name="cpospassthruput_currentposition-method"></a><span data-ttu-id="ed3dd-104">CPosPassThru. put \_ CurrentPosition (metodo)</span><span class="sxs-lookup"><span data-stu-id="ed3dd-104">CPosPassThru.put\_CurrentPosition method</span></span>

<span data-ttu-id="ed3dd-105">Il `put_CurrentPosition` metodo imposta la posizione corrente rispetto alla durata totale del flusso.</span><span class="sxs-lookup"><span data-stu-id="ed3dd-105">The `put_CurrentPosition` method sets the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="ed3dd-106">Questo metodo implementa il metodo [**IMediaPosition::p UT \_ currentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) .</span><span class="sxs-lookup"><span data-stu-id="ed3dd-106">This method implements the [**IMediaPosition::put\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed3dd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed3dd-107">Syntax</span></span>


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a><span data-ttu-id="ed3dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed3dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed3dd-109">*llTime*</span><span class="sxs-lookup"><span data-stu-id="ed3dd-109">*llTime*</span></span> 
</dt> <dd>

<span data-ttu-id="ed3dd-110">Nuova posizione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="ed3dd-110">New position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed3dd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed3dd-111">Return value</span></span>

<span data-ttu-id="ed3dd-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="ed3dd-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed3dd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed3dd-113">Requirements</span></span>



| <span data-ttu-id="ed3dd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed3dd-114">Requirement</span></span> | <span data-ttu-id="ed3dd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ed3dd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed3dd-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed3dd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed3dd-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed3dd-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed3dd-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed3dd-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed3dd-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ed3dd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed3dd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed3dd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed3dd-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ed3dd-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




