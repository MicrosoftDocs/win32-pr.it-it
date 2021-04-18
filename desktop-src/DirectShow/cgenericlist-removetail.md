---
description: Il metodo RemoveTail rimuove l'ultimo elemento dell'elenco.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Metodo CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329793"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="30f63-103">CGenericList. RemoveTail, metodo</span><span class="sxs-lookup"><span data-stu-id="30f63-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="30f63-104">Il `RemoveTail` metodo rimuove l'ultimo elemento dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="30f63-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f63-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30f63-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="30f63-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30f63-106">Parameters</span></span>

<span data-ttu-id="30f63-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="30f63-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30f63-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30f63-108">Return value</span></span>

<span data-ttu-id="30f63-109">Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello) o **null** se l'elenco è vuoto.</span><span class="sxs-lookup"><span data-stu-id="30f63-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f63-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="30f63-110">Remarks</span></span>

<span data-ttu-id="30f63-111">Questo metodo elimina il nodo elenco, ma non l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="30f63-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f63-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30f63-112">Requirements</span></span>



| <span data-ttu-id="30f63-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f63-113">Requirement</span></span> | <span data-ttu-id="30f63-114">Valore</span><span class="sxs-lookup"><span data-stu-id="30f63-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f63-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30f63-115">Header</span></span><br/>  | <dl> <span data-ttu-id="30f63-116"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30f63-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="30f63-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="30f63-117">Library</span></span><br/> | <dl> <span data-ttu-id="30f63-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="30f63-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30f63-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30f63-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30f63-120">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="30f63-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




