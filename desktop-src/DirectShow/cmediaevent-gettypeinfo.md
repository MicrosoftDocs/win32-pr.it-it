---
description: "Metodo CMediaEvent.GetTypeInfo: recupera un oggetto di informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia."
ms.assetid: d54042d5-e9d3-415c-b90d-1fe7d38164f5
title: Metodo CMediaEvent.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: f93e3227051729f9d16e1f9ef8de464a14cca33b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095569"
---
# <a name="cmediaeventgettypeinfo-method"></a><span data-ttu-id="63082-103">Metodo CMediaEvent.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="63082-103">CMediaEvent.GetTypeInfo method</span></span>

<span data-ttu-id="63082-104">Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="63082-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="63082-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63082-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="63082-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63082-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63082-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="63082-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="63082-108">Digitare le informazioni da restituire.</span><span class="sxs-lookup"><span data-stu-id="63082-108">Type information to return.</span></span> <span data-ttu-id="63082-109">Passare zero per recuperare le informazioni sul tipo per **l'implementazione di IDispatch.**</span><span class="sxs-lookup"><span data-stu-id="63082-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="63082-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="63082-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="63082-111">ID delle impostazioni locali per le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="63082-111">Locale ID for the type information.</span></span> <span data-ttu-id="63082-112">Per le classi che supportano nomi di membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="63082-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="63082-113">Per le classi che non supportano nomi di membri localizzati, questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="63082-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="63082-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="63082-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="63082-115">Indirizzo di un puntatore all'oggetto informazioni sul tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="63082-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63082-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63082-116">Return value</span></span>

<span data-ttu-id="63082-117">Restituisce un puntatore E \_ se *pptinfo* non è valido.</span><span class="sxs-lookup"><span data-stu-id="63082-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="63082-118">Restituisce TYPE \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="63082-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="63082-119">Restituisce S \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="63082-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="63082-120">In caso contrario, restituisce **un HRESULT** da una delle chiamate per recuperare il tipo.</span><span class="sxs-lookup"><span data-stu-id="63082-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="63082-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63082-121">Requirements</span></span>



| <span data-ttu-id="63082-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63082-122">Requirement</span></span> | <span data-ttu-id="63082-123">Valore</span><span class="sxs-lookup"><span data-stu-id="63082-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63082-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63082-124">Header</span></span><br/>  | <dl> <span data-ttu-id="63082-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="63082-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63082-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="63082-126">Library</span></span><br/> | <dl> <span data-ttu-id="63082-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="63082-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63082-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63082-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63082-129">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="63082-129">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




