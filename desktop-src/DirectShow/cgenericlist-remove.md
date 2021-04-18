---
description: Il metodo Remove rimuove l'elemento in corrispondenza della posizione specificata.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Metodo CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329795"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="ec5b0-103">Metodo CGenericList. Remove</span><span class="sxs-lookup"><span data-stu-id="ec5b0-103">CGenericList.Remove method</span></span>

<span data-ttu-id="ec5b0-104">Il `Remove` metodo rimuove l'elemento in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ec5b0-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec5b0-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="ec5b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec5b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5b0-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="ec5b0-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="ec5b0-108">Valore di posizione che indica l'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ec5b0-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5b0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec5b0-109">Return value</span></span>

<span data-ttu-id="ec5b0-110">Restituisce un puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="ec5b0-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="ec5b0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec5b0-111">Remarks</span></span>

<span data-ttu-id="ec5b0-112">Questo metodo elimina il nodo dall'elenco, ma non elimina l'elemento contenuto nel nodo.</span><span class="sxs-lookup"><span data-stu-id="ec5b0-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="ec5b0-113">Se *pos* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="ec5b0-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5b0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec5b0-114">Requirements</span></span>



| <span data-ttu-id="ec5b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec5b0-115">Requirement</span></span> | <span data-ttu-id="ec5b0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ec5b0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5b0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec5b0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ec5b0-118"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b0-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ec5b0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="ec5b0-119">Library</span></span><br/> | <dl> <span data-ttu-id="ec5b0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ec5b0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5b0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec5b0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5b0-122">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="ec5b0-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




