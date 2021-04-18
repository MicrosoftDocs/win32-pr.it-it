---
description: Il metodo GetReader restituisce un puntatore all'interfaccia IAsyncReader del PIN di output.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Metodo CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331166"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="580e0-103">CPullPin. GetReader, metodo</span><span class="sxs-lookup"><span data-stu-id="580e0-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="580e0-104">Il `GetReader` metodo restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="580e0-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="580e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="580e0-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="580e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="580e0-106">Parameters</span></span>

<span data-ttu-id="580e0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="580e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="580e0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="580e0-108">Return value</span></span>

<span data-ttu-id="580e0-109">Restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="580e0-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="580e0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="580e0-110">Remarks</span></span>

<span data-ttu-id="580e0-111">Il conteggio dei riferimenti dell'interfaccia restituita è in attesa.</span><span class="sxs-lookup"><span data-stu-id="580e0-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="580e0-112">Il chiamante deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="580e0-112">The caller must release the interface.</span></span>

<span data-ttu-id="580e0-113">Il metodo non verifica il valore del puntatore a interfaccia prima di chiamare **AddRef**, quindi non chiamarlo finché il metodo [**CPullPin:: Connect**](cpullpin-connect.md) non è stato chiamato correttamente.</span><span class="sxs-lookup"><span data-stu-id="580e0-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="580e0-114">In caso contrario, il puntatore a interfaccia potrebbe essere **null** e la chiamata a **AddRef** genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="580e0-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="580e0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="580e0-115">Requirements</span></span>



| <span data-ttu-id="580e0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="580e0-116">Requirement</span></span> | <span data-ttu-id="580e0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="580e0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580e0-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="580e0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="580e0-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="580e0-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="580e0-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="580e0-120">Library</span></span><br/> | <dl> <span data-ttu-id="580e0-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="580e0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580e0-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="580e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580e0-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="580e0-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




