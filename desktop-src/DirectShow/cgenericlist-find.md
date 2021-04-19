---
description: Il metodo Find recupera la prima posizione che contiene l'elemento specificato.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Metodo CGenericList. Find (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329812"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="3d528-103">Metodo CGenericList. Find</span><span class="sxs-lookup"><span data-stu-id="3d528-103">CGenericList.Find method</span></span>

<span data-ttu-id="3d528-104">Il `Find` metodo recupera la prima posizione che include l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="3d528-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d528-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d528-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="3d528-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d528-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d528-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="3d528-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="3d528-108">Puntatore a un oggetto di tipo **Object** (il tipo di modello).</span><span class="sxs-lookup"><span data-stu-id="3d528-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d528-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d528-109">Return value</span></span>

<span data-ttu-id="3d528-110">Restituisce un valore di posizione oppure **null** se l'elemento non è presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="3d528-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d528-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d528-111">Requirements</span></span>



| <span data-ttu-id="3d528-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d528-112">Requirement</span></span> | <span data-ttu-id="3d528-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3d528-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d528-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d528-114">Header</span></span><br/>  | <dl> <span data-ttu-id="3d528-115"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d528-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3d528-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d528-116">Library</span></span><br/> | <dl> <span data-ttu-id="3d528-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3d528-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d528-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d528-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d528-119">**Classe CGenericList**</span><span class="sxs-lookup"><span data-stu-id="3d528-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




