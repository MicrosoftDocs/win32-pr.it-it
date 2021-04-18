---
description: Il metodo GetMediaType recupera un tipo di supporto preferito. Questo metodo usa i parametri *iPosition* e *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: Metodo CSourceStream. GetMediaType (source. h)-parametri iPosition e pMediaType
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2021
ms.locfileid: "106334365"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="b58ed-104">Metodo CSourceStream. GetMediaType (source. h)-parametri iPosition e pMediaType</span><span class="sxs-lookup"><span data-stu-id="b58ed-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="b58ed-105">Il metodo **GetMediaType** recupera un tipo di supporto preferito.</span><span class="sxs-lookup"><span data-stu-id="b58ed-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58ed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b58ed-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="b58ed-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b58ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b58ed-108">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="b58ed-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="b58ed-109">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="b58ed-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="b58ed-110">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="b58ed-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="b58ed-111">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="b58ed-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b58ed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b58ed-112">Return value</span></span>

<span data-ttu-id="b58ed-113">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b58ed-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b58ed-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b58ed-114">Return code</span></span>                                                                                            | <span data-ttu-id="b58ed-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b58ed-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b58ed-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b58ed-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="b58ed-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b58ed-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="b58ed-118"><dt>**\_non ci \_ sono \_ altri \_ elementi di VFW**</dt></span><span class="sxs-lookup"><span data-stu-id="b58ed-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="b58ed-119">Indice non compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="b58ed-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="b58ed-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b58ed-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="b58ed-121">Indice minore di zero.</span><span class="sxs-lookup"><span data-stu-id="b58ed-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="b58ed-122"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="b58ed-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="b58ed-123">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b58ed-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b58ed-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b58ed-124">Remarks</span></span>

<span data-ttu-id="b58ed-125">Sono disponibili due versioni di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b58ed-125">There are two versions of this method.</span></span> <span data-ttu-id="b58ed-126">Una versione esegue l'override del metodo [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) e accetta un valore di indice come parametro.</span><span class="sxs-lookup"><span data-stu-id="b58ed-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="b58ed-127">L'altra versione è progettata per recuperare un solo tipo di supporto, pertanto non dispone del parametro index.</span><span class="sxs-lookup"><span data-stu-id="b58ed-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="b58ed-128">Il metodo a parametro singolo restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b58ed-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="b58ed-129">Il metodo a due parametri verifica che il parametro *iPosition* sia zero, quindi chiama la versione a parametro singolo.</span><span class="sxs-lookup"><span data-stu-id="b58ed-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="b58ed-130">A seconda del numero di tipi di supporto supportati dal pin, è necessario eseguire l'override di uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="b58ed-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="b58ed-131">Se il pin supporta esattamente un tipo di supporto, eseguire l'override della versione a parametro singolo.</span><span class="sxs-lookup"><span data-stu-id="b58ed-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="b58ed-132">Compilare il tipo di supporto supportato dal pin.</span><span class="sxs-lookup"><span data-stu-id="b58ed-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="b58ed-133">Se il pin supporta più di un tipo di supporto, eseguire l'override della versione a due parametri.</span><span class="sxs-lookup"><span data-stu-id="b58ed-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="b58ed-134">Eseguire anche l'override del metodo [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="b58ed-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b58ed-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b58ed-135">Requirements</span></span>



| <span data-ttu-id="b58ed-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58ed-136">Requirement</span></span> | <span data-ttu-id="b58ed-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b58ed-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58ed-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b58ed-138">Header</span></span>  | <span data-ttu-id="b58ed-139">Source. h (Includi Streams. h)</span><span class="sxs-lookup"><span data-stu-id="b58ed-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="b58ed-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="b58ed-140">Library</span></span> | <span data-ttu-id="b58ed-141">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="b58ed-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b58ed-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b58ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58ed-143">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="b58ed-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




