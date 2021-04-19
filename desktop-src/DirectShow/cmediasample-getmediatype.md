---
description: "Il metodo GetMediaType Recupera il tipo di supporto, se il tipo di supporto è diverso rispetto all'esempio precedente. Questo metodo implementa il metodo IMediaSample:: GetMediaType."
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Metodo CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326405"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="8cfd8-104">CMediaSample. GetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="8cfd8-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="8cfd8-105">Il `GetMediaType` metodo recupera il tipo di supporto, se il tipo di supporto è diverso rispetto all'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="8cfd8-106">Questo metodo implementa il metodo [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="8cfd8-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cfd8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8cfd8-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="8cfd8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8cfd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cfd8-109">*ppMediaType*</span><span class="sxs-lookup"><span data-stu-id="8cfd8-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="8cfd8-110">Indirizzo di una variabile che riceve un puntatore a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="8cfd8-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="8cfd8-111">Se il tipo di supporto non è stato modificato rispetto all'esempio precedente, *\* ppMediaType* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cfd8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8cfd8-112">Return value</span></span>

<span data-ttu-id="8cfd8-113">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="8cfd8-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8cfd8-114">Return code</span></span>                                                                                   | <span data-ttu-id="8cfd8-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cfd8-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cfd8-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd8-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="8cfd8-117">Il tipo di supporto non è stato modificato rispetto all'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="8cfd8-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8cfd8-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="8cfd8-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd8-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8cfd8-121">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="8cfd8-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8cfd8-122">Remarks</span></span>

<span data-ttu-id="8cfd8-123">Al termine del tipo di supporto, liberare il blocco di memoria chiamando la funzione di utilità [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="8cfd8-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="8cfd8-124">La variabile membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="8cfd8-125">La variabile membro [**\_ dwFlags CMediaSample:: m**](cmediasample-m-dwflags.md) specifica se il tipo di supporto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="8cfd8-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cfd8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8cfd8-126">Requirements</span></span>



| <span data-ttu-id="8cfd8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cfd8-127">Requirement</span></span> | <span data-ttu-id="8cfd8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8cfd8-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cfd8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8cfd8-129">Header</span></span><br/>  | <dl> <span data-ttu-id="8cfd8-130"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd8-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8cfd8-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="8cfd8-131">Library</span></span><br/> | <dl> <span data-ttu-id="8cfd8-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8cfd8-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cfd8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cfd8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cfd8-134">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="8cfd8-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




