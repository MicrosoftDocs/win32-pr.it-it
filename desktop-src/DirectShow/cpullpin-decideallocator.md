---
description: Il metodo DecideAllocator negozia un allocatore con il pin di output.
ms.assetid: 5c04f440-b177-4caa-989f-3aa783c4b348
title: Metodo CPullPin. DecideAllocator (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91ffa139b916b1594e0729a0f8d52f07c62eda12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331177"
---
# <a name="cpullpindecideallocator-method"></a><span data-ttu-id="829b2-103">CPullPin. DecideAllocator, metodo</span><span class="sxs-lookup"><span data-stu-id="829b2-103">CPullPin.DecideAllocator method</span></span>

<span data-ttu-id="829b2-104">Il `DecideAllocator` Metodo negozia un allocatore con il pin di output.</span><span class="sxs-lookup"><span data-stu-id="829b2-104">The `DecideAllocator` method negotiates an allocator with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="829b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="829b2-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="829b2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="829b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="829b2-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="829b2-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="829b2-108">Puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore preferito del PIN di input o **null**.</span><span class="sxs-lookup"><span data-stu-id="829b2-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="829b2-109">*pProps*</span><span class="sxs-lookup"><span data-stu-id="829b2-109">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="829b2-110">Puntatore a una struttura [**di \_ Proprietà allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) facoltativa che contiene i requisiti del buffer del PIN di input.</span><span class="sxs-lookup"><span data-stu-id="829b2-110">Pointer to an optional [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="829b2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="829b2-111">Return value</span></span>

<span data-ttu-id="829b2-112">Restituisce \_ OK se l'esito è positivo o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="829b2-112">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="829b2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="829b2-113">Remarks</span></span>

<span data-ttu-id="829b2-114">Questo metodo chiama il metodo [**IAsyncReader:: RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) per negoziare un allocatore.</span><span class="sxs-lookup"><span data-stu-id="829b2-114">This method calls the [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method to negotiate an allocator.</span></span> <span data-ttu-id="829b2-115">Passa il parametro *pAlloc* direttamente al metodo **RequestAllocator** .</span><span class="sxs-lookup"><span data-stu-id="829b2-115">It passes the *pAlloc* parameter directly to the **RequestAllocator** method.</span></span> <span data-ttu-id="829b2-116">Passa il parametro *pProps* a **RequestAllocator** se *pProps* è diverso da **null**; in caso contrario, viene creata una struttura di **\_ proprietà dell'allocatore** con una richiesta predefinita di tre buffer 64K.</span><span class="sxs-lookup"><span data-stu-id="829b2-116">It passes the *pProps* parameter to **RequestAllocator** if *pProps* is non-**NULL**; otherwise, it creates an **ALLOCATOR\_PROPERTIES** structure with a default request of three 64K buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="829b2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="829b2-117">Requirements</span></span>



| <span data-ttu-id="829b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="829b2-118">Requirement</span></span> | <span data-ttu-id="829b2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="829b2-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="829b2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="829b2-120">Header</span></span><br/>  | <dl> <span data-ttu-id="829b2-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="829b2-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="829b2-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="829b2-122">Library</span></span><br/> | <dl> <span data-ttu-id="829b2-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="829b2-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="829b2-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="829b2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="829b2-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="829b2-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> <dt>

[<span data-ttu-id="829b2-126">**CPullPin:: Connect**</span><span class="sxs-lookup"><span data-stu-id="829b2-126">**CPullPin::Connect**</span></span>](cpullpin-connect.md)
</dt> </dl>

 

 




