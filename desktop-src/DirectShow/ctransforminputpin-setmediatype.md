---
description: Il metodo SetMediaType imposta il tipo di supporto per la connessione.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Metodo CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333310"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="ae318-103">CTransformInputPin. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="ae318-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="ae318-104">Il `SetMediaType` metodo imposta il tipo di supporto per la connessione.</span><span class="sxs-lookup"><span data-stu-id="ae318-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae318-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae318-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="ae318-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae318-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae318-107">*Mt*</span><span class="sxs-lookup"><span data-stu-id="ae318-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="ae318-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="ae318-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae318-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae318-109">Return value</span></span>

<span data-ttu-id="ae318-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ae318-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae318-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae318-111">Remarks</span></span>

<span data-ttu-id="ae318-112">Questo metodo esegue l'override del metodo [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae318-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="ae318-113">Chiama il metodo [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) del filtro per informare il filtro.</span><span class="sxs-lookup"><span data-stu-id="ae318-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="ae318-114">Il PIN deve verificare che il tipo di supporto sia accettabile prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ae318-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae318-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae318-115">Requirements</span></span>



| <span data-ttu-id="ae318-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae318-116">Requirement</span></span> | <span data-ttu-id="ae318-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ae318-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae318-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae318-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ae318-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae318-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae318-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae318-120">Library</span></span><br/> | <dl> <span data-ttu-id="ae318-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ae318-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




