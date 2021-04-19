---
description: Il metodo GetMediaTypeVersion recupera un numero di versione per il set di tipi di supporto preferiti.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Metodo CBasePin. GetMediaTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333604"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="723e9-103">CBasePin. GetMediaTypeVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="723e9-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="723e9-104">Il `GetMediaTypeVersion` metodo recupera un numero di versione per il set di tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="723e9-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="723e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="723e9-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="723e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="723e9-106">Parameters</span></span>

<span data-ttu-id="723e9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="723e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="723e9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="723e9-108">Return value</span></span>

<span data-ttu-id="723e9-109">Restituisce la variabile membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="723e9-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="723e9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="723e9-110">Remarks</span></span>

<span data-ttu-id="723e9-111">Il costruttore **CBasePin** Inizializza il numero di versione su 1.</span><span class="sxs-lookup"><span data-stu-id="723e9-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="723e9-112">Nella classe base questo numero non viene mai modificato.</span><span class="sxs-lookup"><span data-stu-id="723e9-112">In the base class, this number never changes.</span></span> <span data-ttu-id="723e9-113">Se il pin modifica dinamicamente l'elenco dei tipi di supporto preferiti, deve incrementare il numero di versione ogni volta che l'elenco viene modificato.</span><span class="sxs-lookup"><span data-stu-id="723e9-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="723e9-114">Per incrementare il numero di versione, chiamare il metodo [**CBasePin:: IncrementTypeVersion**](cbasepin-incrementtypeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="723e9-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="723e9-115">L'enumeratore Media Type, implementato dalla classe [**CEnumMediaTypes**](cenummediatypes.md) , usa il numero di versione per mantenersi sincronizzato con il PIN.</span><span class="sxs-lookup"><span data-stu-id="723e9-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="723e9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="723e9-116">Requirements</span></span>



| <span data-ttu-id="723e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="723e9-117">Requirement</span></span> | <span data-ttu-id="723e9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="723e9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723e9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="723e9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="723e9-120"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="723e9-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="723e9-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="723e9-121">Library</span></span><br/> | <dl> <span data-ttu-id="723e9-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="723e9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723e9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="723e9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723e9-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="723e9-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




