---
description: Il Metodo BeginFlush avvia un'operazione di svuotamento.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Metodo CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329406"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="b16c3-103">CBaseRenderer. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="b16c3-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="b16c3-104">Il `BeginFlush` metodo inizia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="b16c3-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b16c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b16c3-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="b16c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b16c3-106">Parameters</span></span>

<span data-ttu-id="b16c3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b16c3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b16c3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b16c3-108">Return value</span></span>

<span data-ttu-id="b16c3-109">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b16c3-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b16c3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b16c3-110">Remarks</span></span>

<span data-ttu-id="b16c3-111">Il pin di input del filtro chiama questo metodo quando riceve una chiamata al metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="b16c3-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="b16c3-112">Il filtro rilascia il thread di streaming e rilascia qualsiasi campione che era in attesa di rendering.</span><span class="sxs-lookup"><span data-stu-id="b16c3-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="b16c3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b16c3-113">Requirements</span></span>



| <span data-ttu-id="b16c3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b16c3-114">Requirement</span></span> | <span data-ttu-id="b16c3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b16c3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16c3-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b16c3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b16c3-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b16c3-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b16c3-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b16c3-118">Library</span></span><br/> | <dl> <span data-ttu-id="b16c3-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b16c3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b16c3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b16c3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b16c3-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b16c3-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




