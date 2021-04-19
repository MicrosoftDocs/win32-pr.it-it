---
description: Il metodo SetMediaType viene chiamato quando è impostato il tipo di supporto del PIN.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Metodo CBaseRenderer. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333003"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="1fbf2-103">CBaseRenderer. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="1fbf2-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="1fbf2-104">Il `SetMediaType` metodo viene chiamato quando è impostato il tipo di supporto del PIN.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbf2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fbf2-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="1fbf2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fbf2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fbf2-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="1fbf2-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="1fbf2-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fbf2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fbf2-109">Return value</span></span>

<span data-ttu-id="1fbf2-110">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fbf2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fbf2-111">Remarks</span></span>

<span data-ttu-id="1fbf2-112">Il pin di input chiama questo metodo dal proprio metodo [**CRendererInputPin:: SetMediaType**](crendererinputpin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="1fbf2-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="1fbf2-113">Questo metodo non esegue alcuna operazione nella classe di base.</span><span class="sxs-lookup"><span data-stu-id="1fbf2-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fbf2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fbf2-114">Requirements</span></span>



| <span data-ttu-id="1fbf2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fbf2-115">Requirement</span></span> | <span data-ttu-id="1fbf2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1fbf2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbf2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fbf2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1fbf2-118"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fbf2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fbf2-119">Library</span></span><br/> | <dl> <span data-ttu-id="1fbf2-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1fbf2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fbf2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fbf2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbf2-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="1fbf2-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




