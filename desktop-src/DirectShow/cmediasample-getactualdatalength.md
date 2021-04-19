---
description: 'Il metodo GetActualDataLength recupera la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample:: GetActualDataLength.'
ms.assetid: bdb8c2b9-7be4-494b-bb96-34a9936d4a2f
title: Metodo CMediaSample. GetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e65b72c1e0b6db85a271c10f76e5630b0799b78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332327"
---
# <a name="cmediasamplegetactualdatalength-method"></a><span data-ttu-id="29210-104">CMediaSample. GetActualDataLength, metodo</span><span class="sxs-lookup"><span data-stu-id="29210-104">CMediaSample.GetActualDataLength method</span></span>

<span data-ttu-id="29210-105">Il `GetActualDataLength` metodo recupera la lunghezza dei dati validi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="29210-105">The `GetActualDataLength` method retrieves the length of the valid data in the buffer.</span></span> <span data-ttu-id="29210-106">Questo metodo implementa il metodo [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="29210-106">This method implements the [**IMediaSample::GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="29210-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29210-107">Syntax</span></span>


```C++
LONG GetActualDataLength();
```



## <a name="parameters"></a><span data-ttu-id="29210-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29210-108">Parameters</span></span>

<span data-ttu-id="29210-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="29210-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29210-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29210-110">Return value</span></span>

<span data-ttu-id="29210-111">Restituisce la lunghezza in byte dei dati validi.</span><span class="sxs-lookup"><span data-stu-id="29210-111">Returns the length of the valid data, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="29210-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="29210-112">Remarks</span></span>

<span data-ttu-id="29210-113">La variabile membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) specifica questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="29210-113">The [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable specifies this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="29210-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29210-114">Requirements</span></span>



| <span data-ttu-id="29210-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29210-115">Requirement</span></span> | <span data-ttu-id="29210-116">Valore</span><span class="sxs-lookup"><span data-stu-id="29210-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29210-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29210-117">Header</span></span><br/>  | <dl> <span data-ttu-id="29210-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29210-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="29210-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="29210-119">Library</span></span><br/> | <dl> <span data-ttu-id="29210-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="29210-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29210-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29210-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29210-122">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="29210-122">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

