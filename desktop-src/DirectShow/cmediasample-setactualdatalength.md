---
description: 'Il metodo SetActualDataLength imposta la lunghezza dei dati validi nel buffer. Questo metodo implementa il metodo IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Metodo CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325321"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="333b2-104">CMediaSample. SetActualDataLength, metodo</span><span class="sxs-lookup"><span data-stu-id="333b2-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="333b2-105">Il `SetActualDataLength` metodo imposta la lunghezza dei dati validi nel buffer.</span><span class="sxs-lookup"><span data-stu-id="333b2-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="333b2-106">Questo metodo implementa il metodo [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="333b2-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="333b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="333b2-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="333b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="333b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="333b2-109">*lLen*</span><span class="sxs-lookup"><span data-stu-id="333b2-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="333b2-110">Lunghezza dei dati validi, in byte.</span><span class="sxs-lookup"><span data-stu-id="333b2-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="333b2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="333b2-111">Return value</span></span>

<span data-ttu-id="333b2-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="333b2-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="333b2-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="333b2-113">Return code</span></span>                                                                                             | <span data-ttu-id="333b2-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="333b2-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="333b2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="333b2-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="333b2-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="333b2-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="333b2-117"><dt>**\_overflow del \_ buffer \_ E VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="333b2-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="333b2-118">*lLen* è maggiore della dimensione del buffer allocata.</span><span class="sxs-lookup"><span data-stu-id="333b2-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="333b2-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="333b2-119">Remarks</span></span>

<span data-ttu-id="333b2-120">Questo metodo imposta la variabile membro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="333b2-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="333b2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="333b2-121">Requirements</span></span>



| <span data-ttu-id="333b2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="333b2-122">Requirement</span></span> | <span data-ttu-id="333b2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="333b2-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="333b2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="333b2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="333b2-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="333b2-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="333b2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="333b2-126">Library</span></span><br/> | <dl> <span data-ttu-id="333b2-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="333b2-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="333b2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="333b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="333b2-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="333b2-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




