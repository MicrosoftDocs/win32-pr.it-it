---
description: Il metodo AddTail Accoda un elenco alla fine dell'elenco.
ms.assetid: 006cccc5-4fb2-4e3f-9481-5d10c090d24e
title: Metodo CGenericList. AddTail (Wxlist. h)-parametro pList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6695df796e54e85ba32dcd63cce2940e00a0199c
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323798"
---
# <a name="cgenericlistaddtail-method-wxlisth---plist-parameter"></a><span data-ttu-id="eb58a-103">Metodo CGenericList. AddTail (Wxlist. h)-parametro pList</span><span class="sxs-lookup"><span data-stu-id="eb58a-103">CGenericList.AddTail method (Wxlist.h) - pList parameter</span></span>

<span data-ttu-id="eb58a-104">Il `AddTail` Metodo Accoda un elenco alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="eb58a-104">The `AddTail` method appends a list to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb58a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb58a-105">Syntax</span></span>


```C++
BOOL AddTail(
   CGenericList<OBJECT> pList
);
```



## <a name="parameters"></a><span data-ttu-id="eb58a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb58a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb58a-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="eb58a-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="eb58a-108">Puntatore all'elenco da accodare.</span><span class="sxs-lookup"><span data-stu-id="eb58a-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb58a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb58a-109">Return value</span></span>

<span data-ttu-id="eb58a-110">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eb58a-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb58a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb58a-111">Requirements</span></span>

| <span data-ttu-id="eb58a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb58a-112">Requirement</span></span> | <span data-ttu-id="eb58a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="eb58a-113">Value</span></span> |
|-|-|
| <span data-ttu-id="eb58a-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb58a-114">Header</span></span> | <span data-ttu-id="eb58a-115">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="eb58a-115">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="eb58a-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb58a-116">Library</span></span>| <span data-ttu-id="eb58a-117">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="eb58a-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="eb58a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb58a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb58a-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="eb58a-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




