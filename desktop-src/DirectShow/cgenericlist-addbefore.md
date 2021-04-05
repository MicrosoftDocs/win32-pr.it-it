---
description: Il metodo AddBefore inserisce un elemento prima della posizione specificata. Questo metodo usa i parametri "p" e "pObj".
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Metodo CGenericList. AddBefore (Wxlist. h)-p, parametri di pObj
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969538"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="c6bee-104">Metodo CGenericList. AddBefore (Wxlist. h)-p, parametri di pObj</span><span class="sxs-lookup"><span data-stu-id="c6bee-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="c6bee-105">Il `AddBefore` metodo inserisce un elemento prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c6bee-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6bee-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6bee-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c6bee-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6bee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6bee-108">*p*</span><span class="sxs-lookup"><span data-stu-id="c6bee-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="c6bee-109">Posizione prima della quale inserire l'elenco.</span><span class="sxs-lookup"><span data-stu-id="c6bee-109">Position before which to insert the list.</span></span> <span data-ttu-id="c6bee-110">Se *p* è **null**, questo metodo aggiunge l'elemento alla parte finale dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="c6bee-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="c6bee-111">*pObj*</span><span class="sxs-lookup"><span data-stu-id="c6bee-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c6bee-112">Puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="c6bee-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6bee-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6bee-113">Return value</span></span>

<span data-ttu-id="c6bee-114">Restituisce l'indicatore di posizione per l'elemento inserito.</span><span class="sxs-lookup"><span data-stu-id="c6bee-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6bee-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6bee-115">Requirements</span></span>

| <span data-ttu-id="c6bee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6bee-116">Requirement</span></span> | <span data-ttu-id="c6bee-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c6bee-117">Value</span></span> |
|-|-|
| <span data-ttu-id="c6bee-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6bee-118">Header</span></span> | <span data-ttu-id="c6bee-119">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c6bee-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="c6bee-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="c6bee-120">Library</span></span>| <span data-ttu-id="c6bee-121">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="c6bee-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c6bee-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6bee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6bee-123">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="c6bee-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




