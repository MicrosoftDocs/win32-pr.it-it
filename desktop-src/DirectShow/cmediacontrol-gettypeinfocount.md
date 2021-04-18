---
description: Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Metodo CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332211"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="913c1-103">CMediaControl. GetTypeInfoCount, metodo</span><span class="sxs-lookup"><span data-stu-id="913c1-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="913c1-104">Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="913c1-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="913c1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="913c1-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="913c1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="913c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913c1-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="913c1-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="913c1-108">Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="913c1-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="913c1-109">Se l'oggetto fornisce informazioni sul tipo, questo numero è 1; in caso contrario, il numero è 0.</span><span class="sxs-lookup"><span data-stu-id="913c1-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913c1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="913c1-110">Return value</span></span>

<span data-ttu-id="913c1-111">Restituisce un \_ puntatore E se *pcTInfo* non è valido; in caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="913c1-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="913c1-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="913c1-112">Requirements</span></span>



| <span data-ttu-id="913c1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="913c1-113">Requirement</span></span> | <span data-ttu-id="913c1-114">Valore</span><span class="sxs-lookup"><span data-stu-id="913c1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="913c1-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="913c1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="913c1-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="913c1-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="913c1-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="913c1-117">Library</span></span><br/> | <dl> <span data-ttu-id="913c1-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="913c1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="913c1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="913c1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="913c1-120">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="913c1-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




