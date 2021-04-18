---
description: Il metodo SESINK imposta l'oggetto IQualityControl che riceverà i messaggi di qualità.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Metodo CBaseVideoRenderer. SESINK (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325347"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="de4e9-103">Metodo CBaseVideoRenderer. SESINK</span><span class="sxs-lookup"><span data-stu-id="de4e9-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="de4e9-104">Il `SetSink` metodo imposta l'oggetto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) che riceverà i messaggi di qualità.</span><span class="sxs-lookup"><span data-stu-id="de4e9-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="de4e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de4e9-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="de4e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de4e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de4e9-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="de4e9-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="de4e9-108">Puntatore all'oggetto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) a cui devono essere inviate le notifiche.</span><span class="sxs-lookup"><span data-stu-id="de4e9-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de4e9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de4e9-109">Return value</span></span>

<span data-ttu-id="de4e9-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de4e9-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de4e9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="de4e9-111">Remarks</span></span>

<span data-ttu-id="de4e9-112">Questa funzione membro implementa il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue nel renderer video.</span><span class="sxs-lookup"><span data-stu-id="de4e9-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="de4e9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de4e9-113">Requirements</span></span>



| <span data-ttu-id="de4e9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="de4e9-114">Requirement</span></span> | <span data-ttu-id="de4e9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="de4e9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de4e9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de4e9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="de4e9-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de4e9-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de4e9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="de4e9-118">Library</span></span><br/> | <dl> <span data-ttu-id="de4e9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="de4e9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de4e9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de4e9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de4e9-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="de4e9-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




