---
description: Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Metodo CMediaControl. GetTypeInfo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe393922206744c23b534bf8d701d6292736c65a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328346"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="e6edb-103">CMediaControl. GetTypeInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="e6edb-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="e6edb-104">Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e6edb-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6edb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6edb-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="e6edb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6edb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6edb-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="e6edb-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e6edb-108">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="e6edb-108">Type information to return.</span></span> <span data-ttu-id="e6edb-109">Passare zero per recuperare le informazioni sul tipo per l'implementazione di **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="e6edb-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="e6edb-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="e6edb-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="e6edb-111">ID delle impostazioni locali per le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="e6edb-111">Locale ID for the type information.</span></span> <span data-ttu-id="e6edb-112">Per le classi che supportano i nomi dei membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per le diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="e6edb-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="e6edb-113">Per le classi che non supportano i nomi dei membri localizzati, questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="e6edb-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="e6edb-114">*ppTInfo*</span><span class="sxs-lookup"><span data-stu-id="e6edb-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e6edb-115">Indirizzo di un puntatore all'oggetto di informazioni sul tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="e6edb-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6edb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6edb-116">Return value</span></span>

<span data-ttu-id="e6edb-117">Restituisce un \_ puntatore E se *ppTInfo* non è valido.</span><span class="sxs-lookup"><span data-stu-id="e6edb-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="e6edb-118">Restituisce il tipo \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e6edb-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="e6edb-119">Restituisce \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e6edb-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="e6edb-120">In caso contrario, restituisce un valore **HRESULT** da una delle chiamate per recuperare il tipo.</span><span class="sxs-lookup"><span data-stu-id="e6edb-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6edb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6edb-121">Requirements</span></span>



| <span data-ttu-id="e6edb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6edb-122">Requirement</span></span> | <span data-ttu-id="e6edb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e6edb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6edb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6edb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e6edb-125"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6edb-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6edb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6edb-126">Library</span></span><br/> | <dl> <span data-ttu-id="e6edb-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6edb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6edb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6edb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6edb-129">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="e6edb-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




