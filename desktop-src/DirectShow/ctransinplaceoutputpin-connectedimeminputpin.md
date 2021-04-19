---
description: 'Il metodo ConnectedIMemInputPin recupera un puntatore al pin di input downstream. Questo metodo restituisce la variabile membro CBaseOutputPin:: m \_ pInputPin.'
ms.assetid: 39a12603-7768-43c3-9558-7caaa8f55108
title: Metodo CTransInPlaceOutputPin. ConnectedIMemInputPin (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.ConnectedIMemInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83f92472e67e1d37a51cd2526b8be65ea9bdbc6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326182"
---
# <a name="ctransinplaceoutputpinconnectedimeminputpin-method"></a><span data-ttu-id="20fa5-104">CTransInPlaceOutputPin. ConnectedIMemInputPin, metodo</span><span class="sxs-lookup"><span data-stu-id="20fa5-104">CTransInPlaceOutputPin.ConnectedIMemInputPin method</span></span>

<span data-ttu-id="20fa5-105">Il `ConnectedIMemInputPin` metodo recupera un puntatore al pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="20fa5-105">The `ConnectedIMemInputPin` method retrieves a pointer to the downstream input pin.</span></span> <span data-ttu-id="20fa5-106">Questo metodo restituisce la variabile membro [**CBaseOutputPin:: m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="20fa5-106">This method returns the [**CBaseOutputPin::m\_pInputPin**](cbaseoutputpin-m-pinputpin.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fa5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20fa5-107">Syntax</span></span>


```C++
IMemInputPin* ConnectedIMemInputPin();
```



## <a name="parameters"></a><span data-ttu-id="20fa5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="20fa5-108">Parameters</span></span>

<span data-ttu-id="20fa5-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="20fa5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20fa5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20fa5-110">Return value</span></span>

<span data-ttu-id="20fa5-111">Restituisce un puntatore all'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sul pin di input downstream.</span><span class="sxs-lookup"><span data-stu-id="20fa5-111">Returns a pointer to the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="20fa5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20fa5-112">Requirements</span></span>



| <span data-ttu-id="20fa5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fa5-113">Requirement</span></span> | <span data-ttu-id="20fa5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="20fa5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fa5-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20fa5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="20fa5-116"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fa5-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="20fa5-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="20fa5-117">Library</span></span><br/> | <dl> <span data-ttu-id="20fa5-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="20fa5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fa5-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20fa5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fa5-120">**Classe CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="20fa5-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




