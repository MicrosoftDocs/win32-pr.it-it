---
description: 'Il metodo IsFormatSupported determina se è supportato un formato di ora specificato. Questo metodo implementa il metodo IMediaSeeking:: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Metodo CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333202"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="1ebc1-104">CPosPassThru. IsFormatSupported, metodo</span><span class="sxs-lookup"><span data-stu-id="1ebc1-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="1ebc1-105">Il `IsFormatSupported` metodo determina se è supportato un formato di ora specificato.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="1ebc1-106">Questo metodo implementa il metodo [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="1ebc1-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ebc1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ebc1-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="1ebc1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ebc1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ebc1-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="1ebc1-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="1ebc1-110">Puntatore a un GUID del formato ora.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ebc1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ebc1-111">Return value</span></span>

<span data-ttu-id="1ebc1-112">Restituisce il valore **HRESULT** dal pin connesso.</span><span class="sxs-lookup"><span data-stu-id="1ebc1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebc1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ebc1-113">Requirements</span></span>



| <span data-ttu-id="1ebc1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ebc1-114">Requirement</span></span> | <span data-ttu-id="1ebc1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1ebc1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebc1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ebc1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1ebc1-117"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebc1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1ebc1-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ebc1-118">Library</span></span><br/> | <dl> <span data-ttu-id="1ebc1-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1ebc1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ebc1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ebc1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebc1-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1ebc1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="1ebc1-122">**GUID del formato dell'ora**</span><span class="sxs-lookup"><span data-stu-id="1ebc1-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




