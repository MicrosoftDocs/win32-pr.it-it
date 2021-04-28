---
description: "Metodo CMediaControl.GetTypeInfo: recupera un oggetto di informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia."
ms.assetid: 2014485f-d937-415d-a2fc-0c69269b5237
title: Metodo CMediaControl.GetTypeInfo (Ctlutil.h)
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
ms.openlocfilehash: 857dbdeee9a2add9ab77cae0ff97d69699d2dd2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099129"
---
# <a name="cmediacontrolgettypeinfo-method"></a><span data-ttu-id="7f308-103">Metodo CMediaControl.GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="7f308-103">CMediaControl.GetTypeInfo method</span></span>

<span data-ttu-id="7f308-104">Recupera un oggetto informazioni sul tipo, che può recuperare le informazioni sul tipo per un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7f308-104">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f308-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f308-105">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a><span data-ttu-id="7f308-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f308-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f308-107">*itinfo*</span><span class="sxs-lookup"><span data-stu-id="7f308-107">*itinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7f308-108">Informazioni sul tipo da restituire.</span><span class="sxs-lookup"><span data-stu-id="7f308-108">Type information to return.</span></span> <span data-ttu-id="7f308-109">Passare zero per recuperare le informazioni sul tipo per **l'implementazione di IDispatch.**</span><span class="sxs-lookup"><span data-stu-id="7f308-109">Pass zero to retrieve type information for the **IDispatch** implementation.</span></span>

</dd> <dt>

<span data-ttu-id="7f308-110">*lcid*</span><span class="sxs-lookup"><span data-stu-id="7f308-110">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="7f308-111">ID delle impostazioni locali per le informazioni sul tipo.</span><span class="sxs-lookup"><span data-stu-id="7f308-111">Locale ID for the type information.</span></span> <span data-ttu-id="7f308-112">Per le classi che supportano nomi di membri localizzati, un oggetto potrebbe essere in grado di restituire informazioni sul tipo diverse per lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="7f308-112">For classes that support localized member names, an object might be able to return different type information for different languages.</span></span> <span data-ttu-id="7f308-113">Per le classi che non supportano nomi di membri localizzati, questo parametro può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="7f308-113">For classes that do not support localized member names, this parameter can be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="7f308-114">*pptinfo*</span><span class="sxs-lookup"><span data-stu-id="7f308-114">*pptinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="7f308-115">Indirizzo di un puntatore all'oggetto informazioni sul tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="7f308-115">Address of a pointer to the type-information object requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f308-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f308-116">Return value</span></span>

<span data-ttu-id="7f308-117">Restituisce un PUNTATORE E \_ se *pptinfo* non è valido.</span><span class="sxs-lookup"><span data-stu-id="7f308-117">Returns an E\_POINTER if *pptinfo* is invalid.</span></span> <span data-ttu-id="7f308-118">Restituisce TYPE \_ E \_ ELEMENTNOTFOUND se *itinfo* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="7f308-118">Returns TYPE\_E\_ELEMENTNOTFOUND if *itinfo* is not zero.</span></span> <span data-ttu-id="7f308-119">Restituisce S \_ OK se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7f308-119">Returns S\_OK if is successful.</span></span> <span data-ttu-id="7f308-120">In caso contrario, **restituisce un HRESULT** da una delle chiamate per recuperare il tipo.</span><span class="sxs-lookup"><span data-stu-id="7f308-120">Otherwise, returns an **HRESULT** from one of the calls to retrieve the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f308-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f308-121">Requirements</span></span>



| <span data-ttu-id="7f308-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f308-122">Requirement</span></span> | <span data-ttu-id="7f308-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7f308-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f308-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f308-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7f308-125"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f308-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f308-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f308-126">Library</span></span><br/> | <dl> <span data-ttu-id="7f308-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f308-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f308-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f308-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f308-129">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="7f308-129">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




