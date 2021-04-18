---
description: "Il metodo GetClassID recupera l'identificatore di classe del filtro. Questo metodo implementa il metodo IPersist:: GetClassID."
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: Metodo CBaseFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328949"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="65f16-104">CBaseFilter. GetClassID, metodo</span><span class="sxs-lookup"><span data-stu-id="65f16-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="65f16-105">Il `GetClassID` metodo recupera l'identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="65f16-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="65f16-106">Questo metodo implementa il metodo **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="65f16-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f16-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65f16-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="65f16-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="65f16-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f16-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="65f16-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="65f16-110">Puntatore a una variabile che riceve l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="65f16-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f16-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65f16-111">Return value</span></span>

<span data-ttu-id="65f16-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="65f16-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="65f16-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65f16-113">Requirements</span></span>



| <span data-ttu-id="65f16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f16-114">Requirement</span></span> | <span data-ttu-id="65f16-115">Valore</span><span class="sxs-lookup"><span data-stu-id="65f16-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65f16-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65f16-116">Header</span></span><br/>  | <dl> <span data-ttu-id="65f16-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65f16-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="65f16-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="65f16-118">Library</span></span><br/> | <dl> <span data-ttu-id="65f16-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="65f16-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f16-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65f16-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f16-121">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="65f16-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




