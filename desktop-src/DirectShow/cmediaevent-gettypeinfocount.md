---
description: 'Metodo CMediaEvent.GetTypeInfoCount: recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto.'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Metodo CMediaEvent.GetTypeInfoCount (Ctlutil.h)
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
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099119"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="61f53-103">Metodo CMediaEvent.GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="61f53-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="61f53-104">Recupera il numero di interfacce di informazioni sul tipo fornite da un oggetto .</span><span class="sxs-lookup"><span data-stu-id="61f53-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61f53-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="61f53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61f53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f53-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="61f53-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="61f53-108">Puntatore al numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61f53-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="61f53-109">Se l'oggetto fornisce informazioni sul tipo, questo numero è 1. In caso contrario, il numero è 0.</span><span class="sxs-lookup"><span data-stu-id="61f53-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f53-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61f53-110">Return value</span></span>

<span data-ttu-id="61f53-111">Restituisce E \_ POINTER se *pctinfo non è* valido; in caso contrario, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="61f53-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f53-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61f53-112">Requirements</span></span>



| <span data-ttu-id="61f53-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="61f53-113">Requirement</span></span> | <span data-ttu-id="61f53-114">Valore</span><span class="sxs-lookup"><span data-stu-id="61f53-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f53-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61f53-115">Header</span></span><br/>  | <dl> <span data-ttu-id="61f53-116"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="61f53-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61f53-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="61f53-117">Library</span></span><br/> | <dl> <span data-ttu-id="61f53-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="61f53-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f53-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61f53-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f53-120">**Classe CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="61f53-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




