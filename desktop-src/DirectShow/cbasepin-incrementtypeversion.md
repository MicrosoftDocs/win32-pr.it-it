---
description: Il metodo IncrementTypeVersion incrementa il numero di versione nel set di tipi di supporto preferiti.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Metodo CBasePin. IncrementTypeVersion (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332877"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="e6a01-103">CBasePin. IncrementTypeVersion, metodo</span><span class="sxs-lookup"><span data-stu-id="e6a01-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="e6a01-104">Il `IncrementTypeVersion` metodo incrementa il numero di versione nel set di tipi di supporto preferiti.</span><span class="sxs-lookup"><span data-stu-id="e6a01-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6a01-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="e6a01-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6a01-106">Parameters</span></span>

<span data-ttu-id="e6a01-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e6a01-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6a01-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6a01-108">Return value</span></span>

<span data-ttu-id="e6a01-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e6a01-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a01-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6a01-110">Remarks</span></span>

<span data-ttu-id="e6a01-111">Questo metodo incrementa la variabile membro [**CBasePin:: m \_ TypeVersion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a01-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="e6a01-112">Se il pin modifica in modo dinamico l'elenco dei tipi di supporto preferiti, chiamare questo metodo ogni volta che l'elenco viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e6a01-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="e6a01-113">Per ulteriori informazioni, vedere [**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="e6a01-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a01-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6a01-114">Requirements</span></span>



| <span data-ttu-id="e6a01-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6a01-115">Requirement</span></span> | <span data-ttu-id="e6a01-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e6a01-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a01-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6a01-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6a01-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a01-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6a01-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6a01-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6a01-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6a01-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6a01-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6a01-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a01-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e6a01-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




