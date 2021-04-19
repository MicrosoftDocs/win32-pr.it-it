---
description: Il metodo Invoke consente di accedere ai metodi e alle proprietà esposti da un oggetto.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Metodo CDeferredCommand. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329635"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="c92ce-103">Metodo CDeferredCommand. Invoke</span><span class="sxs-lookup"><span data-stu-id="c92ce-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="c92ce-104">Il `Invoke` metodo fornisce l'accesso ai metodi e alle proprietà esposti da un oggetto.</span><span class="sxs-lookup"><span data-stu-id="c92ce-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92ce-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c92ce-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="c92ce-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c92ce-106">Parameters</span></span>

<span data-ttu-id="c92ce-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c92ce-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c92ce-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c92ce-108">Return value</span></span>

<span data-ttu-id="c92ce-109">Restituisce VFW \_ E \_ già \_ annullato se **m \_ pQueue** è **null**.</span><span class="sxs-lookup"><span data-stu-id="c92ce-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="c92ce-110">In caso contrario, restituisce il valore **HRESULT** risultante da una chiamata a **IDispatch:: GetTypeInfo** o **IUnknown:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c92ce-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c92ce-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c92ce-111">Requirements</span></span>



| <span data-ttu-id="c92ce-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c92ce-112">Requirement</span></span> | <span data-ttu-id="c92ce-113">Valore</span><span class="sxs-lookup"><span data-stu-id="c92ce-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c92ce-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c92ce-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c92ce-115"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ce-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c92ce-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="c92ce-116">Library</span></span><br/> | <dl> <span data-ttu-id="c92ce-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c92ce-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c92ce-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c92ce-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92ce-119">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="c92ce-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




