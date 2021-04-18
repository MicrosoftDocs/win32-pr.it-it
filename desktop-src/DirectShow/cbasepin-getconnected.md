---
description: Il metodo getconnected Recupera il pin connesso a questo pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Metodo CBasePin. getconnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328847"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="7ba61-103">Metodo CBasePin. getconnected</span><span class="sxs-lookup"><span data-stu-id="7ba61-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="7ba61-104">Il `GetConnected` metodo recupera il pin connesso a questo pin.</span><span class="sxs-lookup"><span data-stu-id="7ba61-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ba61-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="7ba61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ba61-106">Parameters</span></span>

<span data-ttu-id="7ba61-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7ba61-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ba61-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ba61-108">Return value</span></span>

<span data-ttu-id="7ba61-109">Restituisce un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.</span><span class="sxs-lookup"><span data-stu-id="7ba61-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ba61-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ba61-110">Remarks</span></span>

<span data-ttu-id="7ba61-111">Se il PIN non è connesso, questo metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="7ba61-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="7ba61-112">Chiamare il metodo [**CBasePin:: disconnected**](cbasepin-isconnected.md) per determinare se il PIN è connesso.</span><span class="sxs-lookup"><span data-stu-id="7ba61-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="7ba61-113">Il metodo non chiama **AddRef** sull'interfaccia **Ipin** , pertanto il chiamante non deve rilasciare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7ba61-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="7ba61-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="7ba61-114">Examples</span></span>

<span data-ttu-id="7ba61-115">Poiché il conteggio dei riferimenti non viene incrementato nel puntatore restituito, è possibile concatenare le chiamate al metodo:</span><span class="sxs-lookup"><span data-stu-id="7ba61-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="7ba61-116">Questo modello di codifica è molto utile. Tuttavia, come illustrato nell'esempio, è necessario prestare attenzione a non dereferenziare un puntatore **null** quando il PIN è scollegato.</span><span class="sxs-lookup"><span data-stu-id="7ba61-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba61-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ba61-117">Requirements</span></span>



| <span data-ttu-id="7ba61-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba61-118">Requirement</span></span> | <span data-ttu-id="7ba61-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7ba61-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba61-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ba61-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ba61-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ba61-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ba61-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ba61-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ba61-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7ba61-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ba61-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ba61-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba61-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7ba61-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




