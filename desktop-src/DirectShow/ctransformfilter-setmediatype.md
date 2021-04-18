---
description: Il metodo SetMediaType viene chiamato quando il tipo di supporto è impostato su uno dei pin del filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Metodo CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331126"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="e62f7-103">CTransformFilter. SetMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="e62f7-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="e62f7-104">Il `SetMediaType` metodo viene chiamato quando il tipo di supporto è impostato su uno dei pin del filtro.</span><span class="sxs-lookup"><span data-stu-id="e62f7-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="e62f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e62f7-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="e62f7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e62f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62f7-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="e62f7-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="e62f7-108">Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica un pin sul filtro (input o output).</span><span class="sxs-lookup"><span data-stu-id="e62f7-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="e62f7-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="e62f7-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e62f7-110">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che specifica il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e62f7-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62f7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e62f7-111">Return value</span></span>

<span data-ttu-id="e62f7-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e62f7-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e62f7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e62f7-113">Remarks</span></span>

<span data-ttu-id="e62f7-114">I metodi [**CTransformInputPin:: SetMediaType**](ctransforminputpin-setmediatype.md) e [**CTransformOutputPin:: SetMediaType**](ctransformoutputpin-setmediatype.md) chiamano questo metodo quando è impostato il tipo di supporto di un PIN.</span><span class="sxs-lookup"><span data-stu-id="e62f7-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="e62f7-115">Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.</span><span class="sxs-lookup"><span data-stu-id="e62f7-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e62f7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e62f7-116">Requirements</span></span>



| <span data-ttu-id="e62f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e62f7-117">Requirement</span></span> | <span data-ttu-id="e62f7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e62f7-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e62f7-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e62f7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e62f7-120"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e62f7-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e62f7-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="e62f7-121">Library</span></span><br/> | <dl> <span data-ttu-id="e62f7-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e62f7-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e62f7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e62f7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e62f7-124">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="e62f7-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




