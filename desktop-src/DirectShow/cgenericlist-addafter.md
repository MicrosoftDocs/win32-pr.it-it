---
description: Il metodo AddAfter inserisce un elemento dopo la posizione specificata e usa i parametri "p" e "pObj".
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Metodo CGenericList. AddAfter (Wxlist. h)-p, parametri di pObj
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356154"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="cced7-103">Metodo CGenericList. AddAfter (Wxlist. h)-p, parametri di pObj</span><span class="sxs-lookup"><span data-stu-id="cced7-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="cced7-104">Il `AddAfter` metodo inserisce un elemento dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="cced7-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="cced7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cced7-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="cced7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cced7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cced7-107">*p*</span><span class="sxs-lookup"><span data-stu-id="cced7-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="cced7-108">Posizione dopo la quale aggiungere l'elemento.</span><span class="sxs-lookup"><span data-stu-id="cced7-108">Position after which to add the item.</span></span> <span data-ttu-id="cced7-109">Se *p* è **null**, il metodo aggiunge l'elemento all'inizio dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="cced7-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="cced7-110">*pObj*</span><span class="sxs-lookup"><span data-stu-id="cced7-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="cced7-111">Puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="cced7-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cced7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cced7-112">Return value</span></span>

<span data-ttu-id="cced7-113">Restituisce l'indicatore di posizione dell'elemento inserito.</span><span class="sxs-lookup"><span data-stu-id="cced7-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="cced7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cced7-114">Requirements</span></span>

| <span data-ttu-id="cced7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cced7-115">Requirement</span></span> | <span data-ttu-id="cced7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cced7-116">Value</span></span> |
|-|-|
| <span data-ttu-id="cced7-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cced7-117">Header</span></span> | <span data-ttu-id="cced7-118">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="cced7-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="cced7-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="cced7-119">Library</span></span>| <span data-ttu-id="cced7-120">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="cced7-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="cced7-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cced7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cced7-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="cced7-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




