---
description: "Metodo CBaseRenderer.BeginFlush: il metodo BeginFlush avvia un'operazione di scaricamento."
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Metodo CBaseRenderer.BeginFlush (Renbase.h)
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
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095939"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="3fda0-103">Metodo CBaseRenderer.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="3fda0-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="3fda0-104">Il `BeginFlush` metodo avvia un'operazione di scaricamento.</span><span class="sxs-lookup"><span data-stu-id="3fda0-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fda0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fda0-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="3fda0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fda0-106">Parameters</span></span>

<span data-ttu-id="3fda0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3fda0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fda0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fda0-108">Return value</span></span>

<span data-ttu-id="3fda0-109">Restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3fda0-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fda0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fda0-110">Remarks</span></span>

<span data-ttu-id="3fda0-111">Il pin di input del filtro chiama questo metodo quando riceve una chiamata al metodo [**IPin::BeginFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)</span><span class="sxs-lookup"><span data-stu-id="3fda0-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="3fda0-112">Il filtro rilascia il thread di streaming e rilascia qualsiasi esempio contenuto per il rendering.</span><span class="sxs-lookup"><span data-stu-id="3fda0-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fda0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fda0-113">Requirements</span></span>



| <span data-ttu-id="3fda0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fda0-114">Requirement</span></span> | <span data-ttu-id="3fda0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3fda0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fda0-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fda0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3fda0-117"><dt>Renbase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fda0-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3fda0-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3fda0-118">Library</span></span><br/> | <dl> <span data-ttu-id="3fda0-119"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3fda0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fda0-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fda0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fda0-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3fda0-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




