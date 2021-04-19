---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione.
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Metodo CTransformOutputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45bd16f0c0e5ea9cd1e719518fab15180177fd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332983"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="4c5b5-103">CTransformOutputPin. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="4c5b5-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="4c5b5-104">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="4c5b5-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c5b5-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="4c5b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c5b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5b5-107">*Mt*</span><span class="sxs-lookup"><span data-stu-id="4c5b5-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="4c5b5-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="4c5b5-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5b5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c5b5-109">Return value</span></span>

<span data-ttu-id="4c5b5-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c5b5-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c5b5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c5b5-111">Remarks</span></span>

<span data-ttu-id="4c5b5-112">Questo metodo esegue l'override del metodo [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="4c5b5-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="4c5b5-113">Chiama il metodo [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) del filtro per informare il filtro.</span><span class="sxs-lookup"><span data-stu-id="4c5b5-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="4c5b5-114">Il PIN deve verificare che il tipo di supporto sia accettabile prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4c5b5-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5b5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c5b5-115">Requirements</span></span>



| <span data-ttu-id="4c5b5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5b5-116">Requirement</span></span> | <span data-ttu-id="4c5b5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4c5b5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5b5-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c5b5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4c5b5-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c5b5-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4c5b5-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c5b5-120">Library</span></span><br/> | <dl> <span data-ttu-id="4c5b5-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4c5b5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




