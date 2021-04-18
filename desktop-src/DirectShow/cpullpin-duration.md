---
description: Il metodo Duration recupera la durata del flusso.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Metodo CPullPin. Duration (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331173"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="a28e9-103">Metodo CPullPin. Duration</span><span class="sxs-lookup"><span data-stu-id="a28e9-103">CPullPin.Duration method</span></span>

<span data-ttu-id="a28e9-104">Il `Duration` metodo recupera la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="a28e9-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="a28e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a28e9-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="a28e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a28e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28e9-107">*ptDuration*</span><span class="sxs-lookup"><span data-stu-id="a28e9-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="a28e9-108">Puntatore a una variabile che riceve la durata, in byte, moltiplicata per 10 milioni.</span><span class="sxs-lookup"><span data-stu-id="a28e9-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28e9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a28e9-109">Return value</span></span>

<span data-ttu-id="a28e9-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a28e9-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28e9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a28e9-111">Remarks</span></span>

<span data-ttu-id="a28e9-112">La durata è indeterminata fino a quando non viene chiamato il metodo [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="a28e9-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28e9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a28e9-113">Requirements</span></span>



| <span data-ttu-id="a28e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a28e9-114">Requirement</span></span> | <span data-ttu-id="a28e9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a28e9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a28e9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a28e9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a28e9-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a28e9-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a28e9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="a28e9-118">Library</span></span><br/> | <dl> <span data-ttu-id="a28e9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a28e9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28e9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a28e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28e9-121">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="a28e9-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




