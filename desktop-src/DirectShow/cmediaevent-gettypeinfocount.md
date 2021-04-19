---
description: Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Metodo CMediaEvent. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326411"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="6decb-103">CMediaEvent. GetTypeInfoCount, metodo</span><span class="sxs-lookup"><span data-stu-id="6decb-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="6decb-104">Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6decb-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6decb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6decb-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="6decb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6decb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6decb-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="6decb-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6decb-108">Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6decb-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="6decb-109">Se l'oggetto fornisce informazioni sul tipo, questo numero è 1; in caso contrario, il numero è 0.</span><span class="sxs-lookup"><span data-stu-id="6decb-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6decb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6decb-110">Return value</span></span>

<span data-ttu-id="6decb-111">Restituisce un \_ puntatore E se *pcTInfo* non è valido; in caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6decb-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="6decb-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6decb-112">Requirements</span></span>



| <span data-ttu-id="6decb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6decb-113">Requirement</span></span> | <span data-ttu-id="6decb-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6decb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6decb-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6decb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6decb-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6decb-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6decb-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="6decb-117">Library</span></span><br/> | <dl> <span data-ttu-id="6decb-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6decb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6decb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6decb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6decb-120">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="6decb-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




