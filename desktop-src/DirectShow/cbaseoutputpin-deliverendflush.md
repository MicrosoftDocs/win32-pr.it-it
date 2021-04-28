---
description: "Metodo CBaseOutputPin.DeliverEndFlush: il metodo DeliverEndFlush richiede al pin di input connesso di terminare un'operazione di scaricamento."
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Metodo CBaseOutputPin.DeliverEndFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096179"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="9829e-103">Metodo CBaseOutputPin.DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="9829e-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="9829e-104">Il `DeliverEndFlush` metodo richiede al pin di input connesso di terminare un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="9829e-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9829e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9829e-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="9829e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9829e-106">Parameters</span></span>

<span data-ttu-id="9829e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9829e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9829e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9829e-108">Return value</span></span>

<span data-ttu-id="9829e-109">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9829e-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9829e-110">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="9829e-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9829e-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9829e-111">Return code</span></span>                                                                                           | <span data-ttu-id="9829e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9829e-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9829e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9829e-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="9829e-114">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="9829e-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="9829e-115"><dt>**VFW \_ E \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="9829e-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="9829e-116">Il pin non è connesso.</span><span class="sxs-lookup"><span data-stu-id="9829e-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9829e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9829e-117">Remarks</span></span>

<span data-ttu-id="9829e-118">Questo metodo chiama il [**metodo IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input.</span><span class="sxs-lookup"><span data-stu-id="9829e-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9829e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9829e-119">Requirements</span></span>



| <span data-ttu-id="9829e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9829e-120">Requirement</span></span> | <span data-ttu-id="9829e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9829e-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9829e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9829e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9829e-123"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9829e-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9829e-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9829e-124">Library</span></span><br/> | <dl> <span data-ttu-id="9829e-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9829e-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9829e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9829e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9829e-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="9829e-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




