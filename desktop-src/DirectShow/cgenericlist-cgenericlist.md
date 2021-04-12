---
description: Informazioni sul metodo del costruttore per CGenericList. CGenericList (Wxlist. h). Questo metodo usa i parametri ' pName ' è iItems '.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Costruttore CGenericList. CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356199"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="53671-104">Costruttore CGenericList. CGenericList (Wxlist. h)-pName, parametri iItems</span><span class="sxs-lookup"><span data-stu-id="53671-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="53671-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="53671-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="53671-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53671-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="53671-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="53671-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53671-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="53671-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="53671-109">Puntatore al nome dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="53671-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="53671-110">*iItems*</span><span class="sxs-lookup"><span data-stu-id="53671-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="53671-111">Dimensioni della cache del nodo.</span><span class="sxs-lookup"><span data-stu-id="53671-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="53671-112">*Blocco*</span><span class="sxs-lookup"><span data-stu-id="53671-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="53671-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="53671-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="53671-114">*spbalet*</span><span class="sxs-lookup"><span data-stu-id="53671-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="53671-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="53671-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53671-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="53671-116">Remarks</span></span>

<span data-ttu-id="53671-117">Per migliorare l'efficienza, la `CGenericList` classe mantiene una cache di nodi elenco.</span><span class="sxs-lookup"><span data-stu-id="53671-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="53671-118">Se si conosce approssimativamente il numero di elementi che l'elenco conterrà, usare questa versione del costruttore.</span><span class="sxs-lookup"><span data-stu-id="53671-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="53671-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53671-119">Requirements</span></span>

| <span data-ttu-id="53671-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="53671-120">Requirement</span></span> | <span data-ttu-id="53671-121">Valore</span><span class="sxs-lookup"><span data-stu-id="53671-121">Value</span></span> |
|-|-|
| <span data-ttu-id="53671-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53671-122">Header</span></span> | <span data-ttu-id="53671-123">Wxlist. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="53671-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="53671-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="53671-124">Library</span></span>| <span data-ttu-id="53671-125">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="53671-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="53671-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53671-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53671-127">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="53671-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




