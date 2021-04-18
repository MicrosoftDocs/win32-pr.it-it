---
description: 'Il metodo ConnectedTo recupera un puntatore al pin connesso, se disponibile. Questo metodo implementa il metodo IPin:: ConnectedTo.'
ms.assetid: d8978c9a-e498-4411-a052-f3c2fca570ef
title: Metodo CBasePin. ConnectedTo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectedTo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5003154011f93b2b70ddd49dab00dcc1659eb2f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328081"
---
# <a name="cbasepinconnectedto-method"></a><span data-ttu-id="5ad26-104">CBasePin. ConnectedTo, metodo</span><span class="sxs-lookup"><span data-stu-id="5ad26-104">CBasePin.ConnectedTo method</span></span>

<span data-ttu-id="5ad26-105">Il `ConnectedTo` metodo recupera un puntatore al pin connesso, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="5ad26-105">The `ConnectedTo` method retrieves a pointer to the connected pin, if any.</span></span> <span data-ttu-id="5ad26-106">Questo metodo implementa il metodo [**Ipin:: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) .</span><span class="sxs-lookup"><span data-stu-id="5ad26-106">This method implements the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad26-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ad26-107">Syntax</span></span>


```C++
HRESULT ConnectedTo(
   IPin **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="5ad26-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ad26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad26-109">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="5ad26-109">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="5ad26-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="5ad26-110">Address of a variable that receives a pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad26-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ad26-111">Return value</span></span>

<span data-ttu-id="5ad26-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ad26-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5ad26-113">I valori possibili includono quelli nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5ad26-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="5ad26-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5ad26-114">Return code</span></span>                                                                                           | <span data-ttu-id="5ad26-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ad26-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5ad26-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad26-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5ad26-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5ad26-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5ad26-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad26-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5ad26-119">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="5ad26-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="5ad26-120"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="5ad26-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5ad26-121">Il PIN non è connesso.</span><span class="sxs-lookup"><span data-stu-id="5ad26-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="5ad26-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ad26-122">Remarks</span></span>

<span data-ttu-id="5ad26-123">Se il metodo ha esito positivo, l'interfaccia **Ipin** restituita presenta un conteggio dei riferimenti in attesa.</span><span class="sxs-lookup"><span data-stu-id="5ad26-123">If the method succeeds, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="5ad26-124">Assicurarsi di rilasciarlo al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ad26-124">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ad26-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ad26-125">Requirements</span></span>



| <span data-ttu-id="5ad26-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad26-126">Requirement</span></span> | <span data-ttu-id="5ad26-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5ad26-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad26-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ad26-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5ad26-129"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad26-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5ad26-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ad26-130">Library</span></span><br/> | <dl> <span data-ttu-id="5ad26-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad26-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ad26-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ad26-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ad26-133">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5ad26-133">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




