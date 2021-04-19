---
description: Il metodo GetMediaType recupera un tipo di supporto preferito.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: Metodo CSourceStream. GetMediaType (source. h)-parametro pMediaType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389184"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="10382-103">Metodo CSourceStream. GetMediaType (source. h)</span><span class="sxs-lookup"><span data-stu-id="10382-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="10382-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito.</span><span class="sxs-lookup"><span data-stu-id="10382-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="10382-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10382-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="10382-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="10382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10382-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="10382-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="10382-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="10382-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10382-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10382-109">Return value</span></span>

<span data-ttu-id="10382-110">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="10382-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="10382-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="10382-111">Return code</span></span>                                                                                            | <span data-ttu-id="10382-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10382-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="10382-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="10382-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="10382-114">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="10382-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="10382-115"><dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="10382-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="10382-116">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="10382-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="10382-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="10382-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="10382-118">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="10382-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="10382-119"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="10382-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="10382-120">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="10382-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="10382-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="10382-121">Remarks</span></span>

<span data-ttu-id="10382-122">Sono disponibili due versioni di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="10382-122">There are two versions of this method.</span></span> <span data-ttu-id="10382-123">Una versione esegue l'override del metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e accetta un valore di indice come parametro.</span><span class="sxs-lookup"><span data-stu-id="10382-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="10382-124">L'altra versione è progettata per recuperare un solo tipo di supporto, pertanto non dispone del parametro index.</span><span class="sxs-lookup"><span data-stu-id="10382-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="10382-125">Il metodo a parametro singolo restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="10382-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="10382-126">Il metodo a due parametri verifica che il parametro *iPosition* sia zero, quindi chiama la versione a parametro singolo.</span><span class="sxs-lookup"><span data-stu-id="10382-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="10382-127">A seconda del numero di tipi di supporto supportati dal pin, è necessario eseguire l'override di uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="10382-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="10382-128">Se il pin supporta esattamente un tipo di supporto, eseguire l'override della versione a parametro singolo.</span><span class="sxs-lookup"><span data-stu-id="10382-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="10382-129">Compilare il tipo di supporto supportato dal pin.</span><span class="sxs-lookup"><span data-stu-id="10382-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="10382-130">Se il pin supporta più di un tipo di supporto, eseguire l'override della versione a due parametri.</span><span class="sxs-lookup"><span data-stu-id="10382-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="10382-131">Eseguire anche l'override del metodo [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="10382-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="10382-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10382-132">Requirements</span></span>



| <span data-ttu-id="10382-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="10382-133">Requirement</span></span> | <span data-ttu-id="10382-134">Valore</span><span class="sxs-lookup"><span data-stu-id="10382-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10382-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10382-135">Header</span></span><br/>  | <dl> <span data-ttu-id="10382-136"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10382-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="10382-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="10382-137">Library</span></span><br/> | <dl> <span data-ttu-id="10382-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="10382-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10382-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10382-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10382-140">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="10382-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




