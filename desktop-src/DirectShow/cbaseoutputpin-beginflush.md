---
description: "Il Metodo BeginFlush avvia un'operazione di svuotamento. Implementa il metodo IPin:: BeginFlush."
ms.assetid: f16c8337-5b7f-47e8-810d-00ffb3b5a1b4
title: Metodo CBaseOutputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0216f74094d0c024d9b354dc594ff8d65315efbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329555"
---
# <a name="cbaseoutputpinbeginflush-method"></a><span data-ttu-id="35877-104">CBaseOutputPin. BeginFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="35877-104">CBaseOutputPin.BeginFlush method</span></span>

<span data-ttu-id="35877-105">Il `BeginFlush` metodo inizia un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="35877-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="35877-106">Implementa il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="35877-106">Implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="35877-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35877-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="35877-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="35877-108">Parameters</span></span>

<span data-ttu-id="35877-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="35877-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35877-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35877-110">Return value</span></span>

<span data-ttu-id="35877-111">Restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="35877-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="35877-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="35877-112">Remarks</span></span>

<span data-ttu-id="35877-113">Questo metodo deve essere chiamato solo sui pin di input, pertanto l'implementazione di **CBaseOutputPin** restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="35877-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="35877-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35877-114">Requirements</span></span>



| <span data-ttu-id="35877-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35877-115">Requirement</span></span> | <span data-ttu-id="35877-116">Valore</span><span class="sxs-lookup"><span data-stu-id="35877-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35877-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35877-117">Header</span></span><br/>  | <dl> <span data-ttu-id="35877-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35877-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="35877-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="35877-119">Library</span></span><br/> | <dl> <span data-ttu-id="35877-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="35877-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35877-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35877-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35877-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="35877-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




