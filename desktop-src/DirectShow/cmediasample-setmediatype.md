---
description: "Il metodo SetMediaType imposta il tipo di supporto per l'esempio. Questo metodo implementa il metodo IMediaSample:: SetMediaType."
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Metodo CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325309"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="ef6ee-104">CMediaSample. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="ef6ee-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="ef6ee-105">Il `SetMediaType` metodo imposta il tipo di supporto per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="ef6ee-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="ef6ee-106">Questo metodo implementa il metodo [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .</span><span class="sxs-lookup"><span data-stu-id="ef6ee-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef6ee-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef6ee-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ef6ee-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef6ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6ee-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="ef6ee-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="ef6ee-110">Puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="ef6ee-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6ee-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef6ee-111">Return value</span></span>

<span data-ttu-id="ef6ee-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ef6ee-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ef6ee-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ef6ee-113">Return code</span></span>                                                                                   | <span data-ttu-id="ef6ee-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef6ee-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="ef6ee-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef6ee-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ef6ee-116">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="ef6ee-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="ef6ee-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="ef6ee-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ef6ee-118">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="ef6ee-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef6ee-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef6ee-119">Remarks</span></span>

<span data-ttu-id="ef6ee-120">Questo metodo imposta la variabile membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , che specifica il tipo di supporto e la variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) , che specifica se il tipo di supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="ef6ee-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="ef6ee-121">Questo metodo crea una copia della struttura del \_ tipo di supporto am \_ .</span><span class="sxs-lookup"><span data-stu-id="ef6ee-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef6ee-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef6ee-122">Requirements</span></span>



| <span data-ttu-id="ef6ee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef6ee-123">Requirement</span></span> | <span data-ttu-id="ef6ee-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ef6ee-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6ee-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef6ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ef6ee-126"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef6ee-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef6ee-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef6ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="ef6ee-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef6ee-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef6ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef6ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef6ee-130">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="ef6ee-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




