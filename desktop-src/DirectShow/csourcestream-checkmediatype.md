---
description: 'Il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico. Questo metodo implementa il Metodo CBasePin:: CheckMediaType virtuale puro.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Metodo CSourceStream. CheckMediaType (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329032"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="6bbea-104">CSourceStream. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="6bbea-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="6bbea-105">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="6bbea-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="6bbea-106">Questo metodo implementa il metodo [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="6bbea-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bbea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bbea-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="6bbea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bbea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bbea-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="6bbea-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6bbea-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="6bbea-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bbea-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bbea-111">Return value</span></span>

<span data-ttu-id="6bbea-112">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6bbea-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6bbea-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6bbea-113">Return code</span></span>                                                                            | <span data-ttu-id="6bbea-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6bbea-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6bbea-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbea-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6bbea-116">Questo pin supporta questo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6bbea-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="6bbea-117"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="6bbea-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6bbea-118">Il PIN non supporta questo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6bbea-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6bbea-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bbea-119">Remarks</span></span>

<span data-ttu-id="6bbea-120">Per impostazione predefinita, il pin supporta un solo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6bbea-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="6bbea-121">Questo metodo recupera il tipo supportato chiamando la versione a parametro singolo del metodo [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e lo confronta con il tipo proposto.</span><span class="sxs-lookup"><span data-stu-id="6bbea-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="6bbea-122">Se il pin supporta più di un tipo di supporto, eseguire l'override di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="6bbea-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bbea-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bbea-123">Requirements</span></span>



| <span data-ttu-id="6bbea-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bbea-124">Requirement</span></span> | <span data-ttu-id="6bbea-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6bbea-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bbea-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bbea-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6bbea-127"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bbea-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6bbea-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6bbea-128">Library</span></span><br/> | <dl> <span data-ttu-id="6bbea-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6bbea-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bbea-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bbea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bbea-131">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="6bbea-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




