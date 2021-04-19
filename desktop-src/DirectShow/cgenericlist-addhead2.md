---
description: Il metodo AddHead aggiunge un elenco all'inizio dell'elenco.
ms.assetid: 9a344bed-d871-4082-9bbb-330f2ff42cca
title: Metodo CGenericList. AddHead (Wxlist. h)-parametro pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0039566f111033062bca080cb24924c7ea4324ac
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323803"
---
# <a name="cgenericlistaddhead-method-wxlisth---plist-parameter"></a><span data-ttu-id="58139-103">Metodo CGenericList. AddHead (Wxlist. h)-parametro pList</span><span class="sxs-lookup"><span data-stu-id="58139-103">CGenericList.AddHead method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="58139-104">Il `AddHead` metodo aggiunge un elenco all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="58139-104">The `AddHead` method adds a list to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="58139-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58139-105">Syntax</span></span>


```C++
BOOL AddHead(
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="58139-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58139-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58139-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="58139-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="58139-108">Puntatore all'elenco di elementi da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="58139-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58139-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58139-109">Return value</span></span>

<span data-ttu-id="58139-110">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="58139-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="58139-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58139-111">Requirements</span></span>

| <span data-ttu-id="58139-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="58139-112">Requirement</span></span> | <span data-ttu-id="58139-113">Valore</span><span class="sxs-lookup"><span data-stu-id="58139-113">Value</span></span> |
|-|-|
| <span data-ttu-id="58139-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58139-114">Header</span></span> | <span data-ttu-id="58139-115">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="58139-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="58139-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="58139-116">Library</span></span>| <span data-ttu-id="58139-117">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="58139-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="58139-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58139-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58139-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="58139-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




