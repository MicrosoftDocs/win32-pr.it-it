---
description: Il metodo Register aggiunge il filtro al registro di sistema.
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: Metodo CBaseFilter. Register (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bd7ba5a57d670ef28ffda022c95c7dc5b12df77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331660"
---
# <a name="cbasefilterregister-method"></a><span data-ttu-id="4b18c-103">Metodo CBaseFilter. Register</span><span class="sxs-lookup"><span data-stu-id="4b18c-103">CBaseFilter.Register method</span></span>

<span data-ttu-id="4b18c-104">Il `Register` metodo aggiunge il filtro al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b18c-104">The `Register` method adds the filter to the registry.</span></span>

> [!Note]  
> <span data-ttu-id="4b18c-105">Questo metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="4b18c-105">This method is obsolete.</span></span> <span data-ttu-id="4b18c-106">I nuovi filtri devono essere registrati tramite la funzione [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="4b18c-106">New filters should be registered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="4b18c-107">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="4b18c-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4b18c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b18c-108">Syntax</span></span>


```C++
HRESULT Register();
```



## <a name="parameters"></a><span data-ttu-id="4b18c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b18c-109">Parameters</span></span>

<span data-ttu-id="4b18c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4b18c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b18c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b18c-111">Return value</span></span>

<span data-ttu-id="4b18c-112">Restituisce uno dei valori **HRESULT** elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4b18c-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="4b18c-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4b18c-113">Return code</span></span>                                                                             | <span data-ttu-id="4b18c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b18c-114">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4b18c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b18c-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4b18c-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b18c-116">Success.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4b18c-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4b18c-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4b18c-118">Non sono disponibili informazioni sulla registrazione.</span><span class="sxs-lookup"><span data-stu-id="4b18c-118">No registration information is available.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4b18c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b18c-119">Requirements</span></span>



| <span data-ttu-id="4b18c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b18c-120">Requirement</span></span> | <span data-ttu-id="4b18c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4b18c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b18c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b18c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4b18c-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b18c-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4b18c-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4b18c-124">Library</span></span><br/> | <dl> <span data-ttu-id="4b18c-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b18c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b18c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b18c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b18c-127">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4b18c-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




