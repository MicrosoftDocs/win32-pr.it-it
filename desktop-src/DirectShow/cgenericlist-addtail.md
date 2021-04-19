---
description: Il metodo AddTail aggiunge un elemento alla fine dell'elenco.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: Metodo CGenericList. AddTail (Wxlist. h)-parametro pObj
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
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "106323799"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="28fa0-103">Metodo CGenericList. AddTail (Wxlist. h)-parametro pObj</span><span class="sxs-lookup"><span data-stu-id="28fa0-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="28fa0-104">Il `AddTail` metodo aggiunge un elemento alla fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="28fa0-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fa0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28fa0-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="28fa0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="28fa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fa0-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="28fa0-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="28fa0-108">Puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="28fa0-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fa0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28fa0-109">Return value</span></span>

<span data-ttu-id="28fa0-110">Restituisce un valore di posizione per la nuova posizione della coda.</span><span class="sxs-lookup"><span data-stu-id="28fa0-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="28fa0-111">Se il metodo ha esito negativo, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="28fa0-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fa0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28fa0-112">Requirements</span></span>

| <span data-ttu-id="28fa0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="28fa0-113">Requirement</span></span> | <span data-ttu-id="28fa0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="28fa0-114">Value</span></span> |
|-|-|
| <span data-ttu-id="28fa0-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28fa0-115">Header</span></span> | <span data-ttu-id="28fa0-116">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="28fa0-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="28fa0-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="28fa0-117">Library</span></span>| <span data-ttu-id="28fa0-118">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="28fa0-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="28fa0-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28fa0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fa0-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="28fa0-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




