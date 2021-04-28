---
description: 'Metodo CTransInPlaceFilter.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito per il pin di output.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Metodo CTransInPlaceFilter.GetMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094809"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="dacc4-103">Metodo CTransInPlaceFilter.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="dacc4-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="dacc4-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito per il pin di output.</span><span class="sxs-lookup"><span data-stu-id="dacc4-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="dacc4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dacc4-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="dacc4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dacc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dacc4-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="dacc4-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="dacc4-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="dacc4-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="dacc4-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="dacc4-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="dacc4-110">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="dacc4-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dacc4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dacc4-111">Return value</span></span>

<span data-ttu-id="dacc4-112">Restituisce E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="dacc4-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="dacc4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dacc4-113">Remarks</span></span>

<span data-ttu-id="dacc4-114">Questo metodo esegue l'override [**del metodo CTransformFilter::GetMediaType.**](ctransformfilter-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="dacc4-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="dacc4-115">Nella classe **CTransInPlaceFilter** ogni pin chiama il pin connesso opposto per enumerare i tipi di supporti preferiti.</span><span class="sxs-lookup"><span data-stu-id="dacc4-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="dacc4-116">Il pin di input chiama il pin di input del filtro downstream e il pin di output chiama il pin di output del filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="dacc4-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="dacc4-117">Pertanto, il metodo del `GetMediaType` filtro non viene mai chiamato.</span><span class="sxs-lookup"><span data-stu-id="dacc4-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="dacc4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dacc4-118">Requirements</span></span>



| <span data-ttu-id="dacc4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dacc4-119">Requirement</span></span> | <span data-ttu-id="dacc4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="dacc4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dacc4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dacc4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dacc4-122"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dacc4-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dacc4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="dacc4-123">Library</span></span><br/> | <dl> <span data-ttu-id="dacc4-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dacc4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dacc4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dacc4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dacc4-126">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="dacc4-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




