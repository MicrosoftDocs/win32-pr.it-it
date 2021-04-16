---
description: Il metodo AddAfter inserisce un elenco dopo la posizione specificata e usa i parametri "pos" e "plist".
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: Metodo CGenericList. AddAfter (Wxlist. h)-pos, parametri plist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104531105"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="46c92-103">Metodo CGenericList. AddAfter (Wxlist. h)-pos, parametri plist</span><span class="sxs-lookup"><span data-stu-id="46c92-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="46c92-104">Il `AddAfter` metodo inserisce un elenco dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="46c92-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c92-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46c92-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="46c92-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46c92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c92-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="46c92-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="46c92-108">Posizione in cui inserire l'elenco.</span><span class="sxs-lookup"><span data-stu-id="46c92-108">Position to insert the list.</span></span> <span data-ttu-id="46c92-109">L'elenco viene inserito dopo questa posizione.</span><span class="sxs-lookup"><span data-stu-id="46c92-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="46c92-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="46c92-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="46c92-111">Puntatore all'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="46c92-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c92-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46c92-112">Return value</span></span>

<span data-ttu-id="46c92-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="46c92-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="46c92-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46c92-114">Requirements</span></span>

| <span data-ttu-id="46c92-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="46c92-115">Requirement</span></span> | <span data-ttu-id="46c92-116">Valore</span><span class="sxs-lookup"><span data-stu-id="46c92-116">Value</span></span> |
|-|-|
| <span data-ttu-id="46c92-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46c92-117">Header</span></span> | <span data-ttu-id="46c92-118">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="46c92-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="46c92-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="46c92-119">Library</span></span>| <span data-ttu-id="46c92-120">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="46c92-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="46c92-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46c92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46c92-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="46c92-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




