---
description: Il metodo RemoveHead rimuove il primo elemento nell'elenco.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Metodo CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329794"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="45798-103">CGenericList. RemoveHead, metodo</span><span class="sxs-lookup"><span data-stu-id="45798-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="45798-104">Il `RemoveHead` metodo rimuove il primo elemento nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="45798-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="45798-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45798-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="45798-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45798-106">Parameters</span></span>

<span data-ttu-id="45798-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="45798-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45798-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45798-108">Return value</span></span>

<span data-ttu-id="45798-109">Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello) o **null** se l'elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="45798-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="45798-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="45798-110">Remarks</span></span>

<span data-ttu-id="45798-111">Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="45798-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="45798-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45798-112">Requirements</span></span>



| <span data-ttu-id="45798-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="45798-113">Requirement</span></span> | <span data-ttu-id="45798-114">Valore</span><span class="sxs-lookup"><span data-stu-id="45798-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45798-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45798-115">Header</span></span><br/>  | <dl> <span data-ttu-id="45798-116"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45798-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="45798-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="45798-117">Library</span></span><br/> | <dl> <span data-ttu-id="45798-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="45798-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45798-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45798-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45798-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="45798-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




