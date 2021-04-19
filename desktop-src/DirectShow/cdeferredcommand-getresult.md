---
description: Il metodo GetResult recupera l'elenco di argomenti risultante, se disponibile.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Metodo CDeferredCommand. GetResult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333469"
---
# <a name="cdeferredcommandgetresult-method"></a><span data-ttu-id="59226-103">Metodo CDeferredCommand. GetResult</span><span class="sxs-lookup"><span data-stu-id="59226-103">CDeferredCommand.GetResult method</span></span>

<span data-ttu-id="59226-104">Il `GetResult` metodo recupera l'elenco di argomenti risultante, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="59226-104">The `GetResult` method retrieves the resulting argument list, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="59226-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59226-105">Syntax</span></span>


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a><span data-ttu-id="59226-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59226-106">Parameters</span></span>

<span data-ttu-id="59226-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="59226-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59226-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59226-108">Return value</span></span>

<span data-ttu-id="59226-109">Restituisce un puntatore a un **Variant** contenente l'elenco di argomenti del metodo, se esistente.</span><span class="sxs-lookup"><span data-stu-id="59226-109">Returns a pointer to a **VARIANT** containing the method's argument list, if it exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="59226-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59226-110">Requirements</span></span>



| <span data-ttu-id="59226-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="59226-111">Requirement</span></span> | <span data-ttu-id="59226-112">Valore</span><span class="sxs-lookup"><span data-stu-id="59226-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59226-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59226-113">Header</span></span><br/>  | <dl> <span data-ttu-id="59226-114"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59226-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59226-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="59226-115">Library</span></span><br/> | <dl> <span data-ttu-id="59226-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59226-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59226-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59226-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59226-118">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="59226-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




