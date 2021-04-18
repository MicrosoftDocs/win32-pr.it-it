---
description: Il metodo GetOwner recupera un puntatore all'interfaccia IUnknown del componente proprietario. Per un componente aggregato, il proprietario è il componente esterno. In caso contrario, il componente è proprietario.
ms.assetid: 7d8af9d1-52c0-4f2b-9d05-6ddff85ab508
title: Metodo CUnknown. GetOwner (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.GetOwner
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e3cb1cd1d5b183857b6d75db79ee0fcdc6cb2d30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331451"
---
# <a name="cunknowngetowner-method"></a><span data-ttu-id="0243f-105">Metodo CUnknown. GetOwner</span><span class="sxs-lookup"><span data-stu-id="0243f-105">CUnknown.GetOwner method</span></span>

<span data-ttu-id="0243f-106">Il `GetOwner` metodo recupera un puntatore all'interfaccia **IUnknown** del componente proprietario.</span><span class="sxs-lookup"><span data-stu-id="0243f-106">The `GetOwner` method retrieves a pointer to the **IUnknown** interface of the owning component.</span></span> <span data-ttu-id="0243f-107">Per un componente aggregato, il proprietario è il componente esterno.</span><span class="sxs-lookup"><span data-stu-id="0243f-107">For an aggregated component, the owner is the outer component.</span></span> <span data-ttu-id="0243f-108">In caso contrario, il componente è proprietario.</span><span class="sxs-lookup"><span data-stu-id="0243f-108">Otherwise, the component owns itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="0243f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0243f-109">Syntax</span></span>


```C++
LPUNKNOWN GetOwner();
```



## <a name="parameters"></a><span data-ttu-id="0243f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0243f-110">Parameters</span></span>

<span data-ttu-id="0243f-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0243f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0243f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0243f-112">Return value</span></span>

<span data-ttu-id="0243f-113">Restituisce un puntatore all'interfaccia **IUnknown** di controllo.</span><span class="sxs-lookup"><span data-stu-id="0243f-113">Returns a pointer to the controlling **IUnknown** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0243f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0243f-114">Requirements</span></span>



| <span data-ttu-id="0243f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0243f-115">Requirement</span></span> | <span data-ttu-id="0243f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0243f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0243f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0243f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0243f-118"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0243f-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0243f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="0243f-119">Library</span></span><br/> | <dl> <span data-ttu-id="0243f-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0243f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




