---
description: 'Metodo CTransformOutputPin.SetMediaType: il metodo SetMediaType imposta il tipo di supporto per la connessione.'
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Metodo CTransformOutputPin.SetMediaType (Transfrm.h)
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
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084799"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="75241-103">Metodo CTransformOutputPin.SetMediaType</span><span class="sxs-lookup"><span data-stu-id="75241-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="75241-104">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="75241-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75241-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75241-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="75241-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75241-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75241-107">*Monte*</span><span class="sxs-lookup"><span data-stu-id="75241-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="75241-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="75241-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75241-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75241-109">Return value</span></span>

<span data-ttu-id="75241-110">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75241-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="75241-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="75241-111">Remarks</span></span>

<span data-ttu-id="75241-112">Questo metodo esegue l'override [**del metodo CBasePin::SetMediaType.**](cbasepin-setmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="75241-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="75241-113">Chiama il metodo [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) del filtro per informare il filtro.</span><span class="sxs-lookup"><span data-stu-id="75241-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="75241-114">Il pin deve verificare che il tipo di supporto sia accettabile prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="75241-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="75241-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75241-115">Requirements</span></span>



| <span data-ttu-id="75241-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="75241-116">Requirement</span></span> | <span data-ttu-id="75241-117">Valore</span><span class="sxs-lookup"><span data-stu-id="75241-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75241-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75241-118">Header</span></span><br/>  | <dl> <span data-ttu-id="75241-119"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="75241-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75241-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="75241-120">Library</span></span><br/> | <dl> <span data-ttu-id="75241-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="75241-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




