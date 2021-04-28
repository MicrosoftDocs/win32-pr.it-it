---
description: 'Costruttore CSource.CSource : metodo del costruttore.'
ms.assetid: 94a92c1e-9768-4293-8290-a2b1938cd196
title: Costruttore CSource.CSource (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fab398f3f4e3fdd8c23ce1e1c08f5c130478dfb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085359"
---
# <a name="csourcecsource-constructor"></a><span data-ttu-id="d75b4-103">Costruttore CSource.CSource</span><span class="sxs-lookup"><span data-stu-id="d75b4-103">CSource.CSource constructor</span></span>

<span data-ttu-id="d75b4-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="d75b4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75b4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d75b4-105">Syntax</span></span>


```C++
CSource(
   TCHAR     *pName,
   LPUNKNOWN lpunk,
   CLSID     clsid
);
```



## <a name="parameters"></a><span data-ttu-id="d75b4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d75b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75b4-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="d75b4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d75b4-108">Puntatore a una stringa contenente il nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d75b4-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="d75b4-109">Per altre informazioni, vedere [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d75b4-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="d75b4-110">*lpunk*</span><span class="sxs-lookup"><span data-stu-id="d75b4-110">*lpunk*</span></span> 
</dt> <dd>

<span data-ttu-id="d75b4-111">Puntatore al proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d75b4-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="d75b4-112">Se l'oggetto è aggregato, passare un puntatore all'interfaccia **IUnknown dell'oggetto** di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="d75b4-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="d75b4-113">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="d75b4-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d75b4-114">*Clsid*</span><span class="sxs-lookup"><span data-stu-id="d75b4-114">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="d75b4-115">Identificatore di classe del filtro.</span><span class="sxs-lookup"><span data-stu-id="d75b4-115">Class identifier of the filter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d75b4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d75b4-116">Requirements</span></span>



| <span data-ttu-id="d75b4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75b4-117">Requirement</span></span> | <span data-ttu-id="d75b4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d75b4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d75b4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d75b4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d75b4-120"><dt>Source.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d75b4-120"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d75b4-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="d75b4-121">Library</span></span><br/> | <dl> <span data-ttu-id="d75b4-122"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d75b4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75b4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d75b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75b4-124">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="d75b4-124">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




