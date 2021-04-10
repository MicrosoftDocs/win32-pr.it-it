---
description: Il metodo AddBefore inserisce un elenco prima della posizione specificata. Questo metodo usa i parametri "pos" e "pList".
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: Metodo CGenericList. AddBefore (Wxlist. h)-pos, parametri pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103762424"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="25359-104">Metodo CGenericList. AddBefore (Wxlist. h)-pos, parametri pList</span><span class="sxs-lookup"><span data-stu-id="25359-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="25359-105">Il `AddBefore` metodo inserisce un elenco prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="25359-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="25359-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25359-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="25359-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="25359-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25359-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="25359-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="25359-109">Posizione in cui inserire l'elenco.</span><span class="sxs-lookup"><span data-stu-id="25359-109">Position to insert the list.</span></span> <span data-ttu-id="25359-110">L'elenco viene inserito prima di questa posizione.</span><span class="sxs-lookup"><span data-stu-id="25359-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="25359-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="25359-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="25359-112">Puntatore all'elenco da inserire.</span><span class="sxs-lookup"><span data-stu-id="25359-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25359-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25359-113">Return value</span></span>

<span data-ttu-id="25359-114">Restituisce **true** se l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="25359-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="25359-115">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="25359-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="25359-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25359-116">Requirements</span></span>

| <span data-ttu-id="25359-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="25359-117">Requirement</span></span> | <span data-ttu-id="25359-118">Valore</span><span class="sxs-lookup"><span data-stu-id="25359-118">Value</span></span> |
|-|-|
| <span data-ttu-id="25359-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25359-119">Header</span></span> | <span data-ttu-id="25359-120">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="25359-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="25359-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="25359-121">Library</span></span>| <span data-ttu-id="25359-122">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="25359-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="25359-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25359-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25359-124">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="25359-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




