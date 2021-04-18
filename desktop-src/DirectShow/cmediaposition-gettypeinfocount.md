---
description: Il metodo GetTypeInfoCount Recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Metodo CMediaPosition. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329379"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="3a6e4-103">CMediaPosition. GetTypeInfoCount, metodo</span><span class="sxs-lookup"><span data-stu-id="3a6e4-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="3a6e4-104">Il `GetTypeInfoCount` metodo recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a6e4-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a6e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a6e4-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="3a6e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a6e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a6e4-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="3a6e4-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="3a6e4-108">Puntatore a una variabile che riceve il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3a6e4-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="3a6e4-109">Quando il metodo restituisce, il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="3a6e4-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a6e4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a6e4-110">Return value</span></span>

<span data-ttu-id="3a6e4-111">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3a6e4-111">Returns one of the following values.</span></span>



| <span data-ttu-id="3a6e4-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3a6e4-112">Return code</span></span>                                                                               | <span data-ttu-id="3a6e4-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a6e4-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3a6e4-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e4-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3a6e4-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3a6e4-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3a6e4-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e4-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3a6e4-117">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="3a6e4-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3a6e4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a6e4-118">Requirements</span></span>



| <span data-ttu-id="3a6e4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a6e4-119">Requirement</span></span> | <span data-ttu-id="3a6e4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3a6e4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a6e4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a6e4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3a6e4-122"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e4-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3a6e4-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a6e4-123">Library</span></span><br/> | <dl> <span data-ttu-id="3a6e4-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a6e4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a6e4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a6e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a6e4-126">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="3a6e4-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




