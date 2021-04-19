---
description: Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Metodo CMediaEvent. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e351d3b8b06bea4f6f9a1a160802972a8fa50f82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332335"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="5aa67-103">CMediaEvent. GetTypeInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="5aa67-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="5aa67-104">Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5aa67-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aa67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5aa67-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="5aa67-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5aa67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa67-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="5aa67-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa67-108">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="5aa67-108">Type information to return.</span></span> <span data-ttu-id="5aa67-109">Passare zero per recuperare le informazioni sul tipo per l'implementazione di **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="5aa67-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="5aa67-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="5aa67-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa67-111">ID delle impostazioni locali per le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="5aa67-111">Locale ID for the type information.</span></span> <span data-ttu-id="5aa67-112">Per le classi che supportano i nomi dei membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per le diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="5aa67-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="5aa67-113">Per le classi che non supportano i nomi dei membri localizzati, questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="5aa67-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5aa67-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="5aa67-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5aa67-115">Indirizzo di un puntatore all'oggetto di informazioni sul tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="5aa67-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa67-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5aa67-116">Return value</span></span>

<span data-ttu-id="5aa67-117">Restituisce un \_ puntatore E se *ppTInfo* non è valido.</span><span class="sxs-lookup"><span data-stu-id="5aa67-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="5aa67-118">Restituisce il tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5aa67-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="5aa67-119">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5aa67-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="5aa67-120">In caso contrario, restituisce un valore **HRESULT** da una delle chiamate per recuperare il tipo.</span><span class="sxs-lookup"><span data-stu-id="5aa67-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5aa67-121">Requirements</span></span>



| <span data-ttu-id="5aa67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aa67-122">Requirement</span></span> | <span data-ttu-id="5aa67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5aa67-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa67-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5aa67-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5aa67-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa67-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5aa67-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="5aa67-126">Library</span></span><br/> | <dl> <span data-ttu-id="5aa67-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa67-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa67-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5aa67-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa67-129">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="5aa67-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




