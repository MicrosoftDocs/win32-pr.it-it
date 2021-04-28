---
description: "Metodo CBaseRenderer.EndFlush: il metodo EndFlush termina un'operazione di scaricamento."
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Metodo CBaseRenderer.EndFlush (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 87e29f405430ca87943773d19793ffc1941ec42c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095909"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="e0a33-103">Metodo CBaseRenderer.EndFlush</span><span class="sxs-lookup"><span data-stu-id="e0a33-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="e0a33-104">Il `EndFlush` metodo termina un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="e0a33-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0a33-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0a33-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="e0a33-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0a33-106">Parameters</span></span>

<span data-ttu-id="e0a33-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e0a33-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e0a33-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0a33-108">Return value</span></span>

<span data-ttu-id="e0a33-109">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0a33-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0a33-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0a33-110">Remarks</span></span>

<span data-ttu-id="e0a33-111">Il pin di input del filtro chiama questo metodo quando riceve una chiamata al [**metodo IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="e0a33-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0a33-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0a33-112">Requirements</span></span>



| <span data-ttu-id="e0a33-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0a33-113">Requirement</span></span> | <span data-ttu-id="e0a33-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e0a33-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0a33-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0a33-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e0a33-116"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0a33-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0a33-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0a33-117">Library</span></span><br/> | <dl> <span data-ttu-id="e0a33-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e0a33-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0a33-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0a33-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0a33-120">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e0a33-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




