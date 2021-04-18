---
description: "Il Metodo BeginFlush avvia un'operazione di svuotamento. Questo metodo implementa il metodo IPin:: BeginFlush."
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Metodo CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328479"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="08895-104">CTransformInputPin. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="08895-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="08895-105">Il `BeginFlush` metodo inizia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="08895-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="08895-106">Questo metodo implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="08895-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08895-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08895-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="08895-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08895-108">Parameters</span></span>

<span data-ttu-id="08895-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="08895-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="08895-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08895-110">Return value</span></span>

<span data-ttu-id="08895-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08895-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="08895-112">I valori possibili includono quelli mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="08895-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="08895-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08895-113">Return code</span></span>                                                                                           | <span data-ttu-id="08895-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08895-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="08895-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08895-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="08895-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="08895-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="08895-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="08895-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="08895-118">Il pin di output non è connesso.</span><span class="sxs-lookup"><span data-stu-id="08895-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08895-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="08895-119">Remarks</span></span>

<span data-ttu-id="08895-120">Questo metodo chiama il metodo [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) del PIN.</span><span class="sxs-lookup"><span data-stu-id="08895-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="08895-121">Chiama quindi il metodo [**CTransformFilter:: BeginFlush**](ctransformfilter-beginflush.md) del filtro per recapitare la chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="08895-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="08895-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08895-122">Requirements</span></span>



| <span data-ttu-id="08895-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="08895-123">Requirement</span></span> | <span data-ttu-id="08895-124">Valore</span><span class="sxs-lookup"><span data-stu-id="08895-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08895-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08895-125">Header</span></span><br/>  | <dl> <span data-ttu-id="08895-126"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08895-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="08895-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="08895-127">Library</span></span><br/> | <dl> <span data-ttu-id="08895-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08895-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




