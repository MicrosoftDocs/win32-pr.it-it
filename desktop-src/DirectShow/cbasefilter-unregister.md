---
description: Il metodo Unregister rimuove il filtro dal registro di sistema.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Metodo CBaseFilter. Unregister (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326939"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="88e6d-103">Metodo CBaseFilter. Unregister</span><span class="sxs-lookup"><span data-stu-id="88e6d-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="88e6d-104">Il `Unregister` metodo rimuove il filtro dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="88e6d-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="88e6d-105">Questo metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="88e6d-105">This method is obsolete.</span></span> <span data-ttu-id="88e6d-106">È necessario annullare la registrazione dei nuovi filtri tramite la funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="88e6d-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="88e6d-107">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="88e6d-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="88e6d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88e6d-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="88e6d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88e6d-109">Parameters</span></span>

<span data-ttu-id="88e6d-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="88e6d-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88e6d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88e6d-111">Return value</span></span>

<span data-ttu-id="88e6d-112">Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="88e6d-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e6d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88e6d-113">Requirements</span></span>



| <span data-ttu-id="88e6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e6d-114">Requirement</span></span> | <span data-ttu-id="88e6d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="88e6d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e6d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88e6d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="88e6d-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="88e6d-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="88e6d-118">Library</span></span><br/> | <dl> <span data-ttu-id="88e6d-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="88e6d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88e6d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88e6d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88e6d-121">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="88e6d-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




