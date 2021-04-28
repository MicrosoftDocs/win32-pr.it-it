---
description: 'Metodo CTransformOutputPin.GetMediaType: il metodo GetMediaType recupera un tipo di supporto preferito, in base al valore di indice.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Metodo CTransformOutputPin.GetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094899"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="69a2f-103">Metodo CTransformOutputPin.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="69a2f-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="69a2f-104">Il `GetMediaType` metodo recupera un tipo di supporto preferito, in base al valore di indice.</span><span class="sxs-lookup"><span data-stu-id="69a2f-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a2f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69a2f-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="69a2f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a2f-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="69a2f-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="69a2f-108">Valore di indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="69a2f-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="69a2f-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="69a2f-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="69a2f-110">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che riceve il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="69a2f-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a2f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69a2f-111">Return value</span></span>

<span data-ttu-id="69a2f-112">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="69a2f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="69a2f-113">I valori possibili includono quelli illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="69a2f-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="69a2f-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="69a2f-114">Return code</span></span>                                                                                            | <span data-ttu-id="69a2f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69a2f-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="69a2f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="69a2f-117">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="69a2f-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="69a2f-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="69a2f-119">Indice non compreso nell'intervallo</span><span class="sxs-lookup"><span data-stu-id="69a2f-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69a2f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="69a2f-120">Remarks</span></span>

<span data-ttu-id="69a2f-121">Questo metodo esegue l'override [**del metodo CBasePin::GetMediaType.**](cbasepin-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="69a2f-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="69a2f-122">Se il pin di input del filtro non è connesso, il metodo restituisce VFW \_ S \_ NO MORE \_ \_ ITEMS.</span><span class="sxs-lookup"><span data-stu-id="69a2f-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="69a2f-123">In caso contrario, chiama il metodo [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) del filtro per recuperare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="69a2f-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="69a2f-124">Il **metodo CTransformFilter::GetMediaType** è virtuale puro. La classe derivata del filtro deve eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="69a2f-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="69a2f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69a2f-125">Requirements</span></span>



| <span data-ttu-id="69a2f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a2f-126">Requirement</span></span> | <span data-ttu-id="69a2f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="69a2f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a2f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69a2f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="69a2f-129"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="69a2f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="69a2f-130">Library</span></span><br/> | <dl> <span data-ttu-id="69a2f-131"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="69a2f-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




