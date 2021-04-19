---
description: La funzione EqualPins controlla se due pin si trovano nello stesso oggetto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Funzione EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325181"
---
# <a name="equalpins-function"></a><span data-ttu-id="7faff-103">EqualPins (funzione)</span><span class="sxs-lookup"><span data-stu-id="7faff-103">EqualPins function</span></span>

<span data-ttu-id="7faff-104">La funzione EqualPins controlla se due pin si trovano nello stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="7faff-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7faff-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="7faff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7faff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7faff-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="7faff-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="7faff-108">Puntatore a un PIN.</span><span class="sxs-lookup"><span data-stu-id="7faff-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="7faff-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="7faff-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="7faff-110">Puntatore all'altro pin.</span><span class="sxs-lookup"><span data-stu-id="7faff-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7faff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7faff-111">Return value</span></span>

<span data-ttu-id="7faff-112">Restituisce **true** se entrambi i pin si trovano nello stesso oggetto. in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="7faff-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7faff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7faff-113">Requirements</span></span>



| <span data-ttu-id="7faff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7faff-114">Requirement</span></span> | <span data-ttu-id="7faff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7faff-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7faff-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7faff-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7faff-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7faff-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7faff-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="7faff-118">Library</span></span><br/> | <dl> <span data-ttu-id="7faff-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7faff-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7faff-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7faff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7faff-121">Funzioni helper varie</span><span class="sxs-lookup"><span data-stu-id="7faff-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




