---
description: Il metodo Get recupera l'elemento in corrispondenza della posizione specificata.
ms.assetid: cafa4083-96e6-4ed3-afbc-5828b7f1c5be
title: Metodo CGenericList. Get (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Get
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02af7d57d2219e6eb0506a8ab11521b4cf3570eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329811"
---
# <a name="cgenericlistget-method"></a><span data-ttu-id="93446-103">Metodo CGenericList. Get</span><span class="sxs-lookup"><span data-stu-id="93446-103">CGenericList.Get method</span></span>

<span data-ttu-id="93446-104">Il `Get` metodo recupera l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="93446-104">The `Get` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="93446-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93446-105">Syntax</span></span>


```C++
OBJECT* Get(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="93446-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93446-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="93446-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="93446-108">Indicatore di posizione per l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="93446-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93446-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93446-109">Return value</span></span>

<span data-ttu-id="93446-110">Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="93446-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="93446-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="93446-111">Remarks</span></span>

<span data-ttu-id="93446-112">Se *pos* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="93446-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="93446-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93446-113">Requirements</span></span>



| <span data-ttu-id="93446-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="93446-114">Requirement</span></span> | <span data-ttu-id="93446-115">Valore</span><span class="sxs-lookup"><span data-stu-id="93446-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93446-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93446-116">Header</span></span><br/>  | <dl> <span data-ttu-id="93446-117"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93446-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="93446-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="93446-118">Library</span></span><br/> | <dl> <span data-ttu-id="93446-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="93446-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93446-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93446-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93446-121">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="93446-121">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




