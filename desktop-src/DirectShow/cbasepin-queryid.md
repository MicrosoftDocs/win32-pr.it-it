---
description: "Il metodo QueryId recupera l'identificatore del PIN. Questo metodo implementa il metodo IPin:: QueryId."
ms.assetid: b365a574-61b4-454c-b062-8826cbe10f03
title: Metodo CBasePin. QueryId (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa14fb933c89da0b0b6d2eebfab480b5508a3666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328262"
---
# <a name="cbasepinqueryid-method"></a><span data-ttu-id="b20a9-104">CBasePin. QueryId, metodo</span><span class="sxs-lookup"><span data-stu-id="b20a9-104">CBasePin.QueryId method</span></span>

<span data-ttu-id="b20a9-105">Il `QueryId` metodo recupera l'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="b20a9-105">The `QueryId` method retrieves the pin identifier.</span></span> <span data-ttu-id="b20a9-106">Questo metodo implementa il metodo [**Ipin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="b20a9-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b20a9-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="b20a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b20a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20a9-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="b20a9-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="b20a9-110">Puntatore all'identificatore del PIN.</span><span class="sxs-lookup"><span data-stu-id="b20a9-110">Pointer to the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20a9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b20a9-111">Return value</span></span>

<span data-ttu-id="b20a9-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b20a9-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b20a9-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b20a9-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="b20a9-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b20a9-114">Return code</span></span>                                                                                   | <span data-ttu-id="b20a9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b20a9-115">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="b20a9-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b20a9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b20a9-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b20a9-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="b20a9-118"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="b20a9-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b20a9-119">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="b20a9-119">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="b20a9-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="b20a9-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b20a9-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="b20a9-121">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b20a9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="b20a9-122">Remarks</span></span>

<span data-ttu-id="b20a9-123">Questo metodo restituisce una copia della variabile membro [**CBasePin:: m \_ pname**](cbasepin-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="b20a9-123">This method returns a copy of the [**CBasePin::m\_pName**](cbasepin-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20a9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b20a9-124">Requirements</span></span>



| <span data-ttu-id="b20a9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20a9-125">Requirement</span></span> | <span data-ttu-id="b20a9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b20a9-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20a9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b20a9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b20a9-128"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b20a9-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b20a9-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="b20a9-129">Library</span></span><br/> | <dl> <span data-ttu-id="b20a9-130"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b20a9-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b20a9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b20a9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20a9-132">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="b20a9-132">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




