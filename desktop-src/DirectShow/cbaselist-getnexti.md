---
description: Il metodo getnexti recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Metodo CBaseList. getnexto (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328659"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="20943-103">CBaseList. getnexti (metodo)</span><span class="sxs-lookup"><span data-stu-id="20943-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="20943-104">Il `GetNextI` metodo recupera l'elemento in corrispondenza della posizione specificata e fa avanzare la posizione.</span><span class="sxs-lookup"><span data-stu-id="20943-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="20943-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20943-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="20943-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="20943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20943-107">*componente* \[ di Ref\]</span><span class="sxs-lookup"><span data-stu-id="20943-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="20943-108">Riferimento a un valore di posizione.</span><span class="sxs-lookup"><span data-stu-id="20943-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20943-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20943-109">Return value</span></span>

<span data-ttu-id="20943-110">Restituisce un puntatore all'elemento.</span><span class="sxs-lookup"><span data-stu-id="20943-110">Returns a pointer to the item.</span></span> <span data-ttu-id="20943-111">Se *RP* è **null**, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="20943-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="20943-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="20943-112">Remarks</span></span>

<span data-ttu-id="20943-113">Questo metodo sposta l'indicatore di posizione nella posizione successiva.</span><span class="sxs-lookup"><span data-stu-id="20943-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="20943-114">Se l'indicatore di posizione si sposta oltre la fine dell'elenco, il metodo lo imposta su **null**.</span><span class="sxs-lookup"><span data-stu-id="20943-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="20943-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20943-115">Requirements</span></span>



| <span data-ttu-id="20943-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="20943-116">Requirement</span></span> | <span data-ttu-id="20943-117">Valore</span><span class="sxs-lookup"><span data-stu-id="20943-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20943-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20943-118">Header</span></span><br/>  | <dl> <span data-ttu-id="20943-119"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20943-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="20943-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="20943-120">Library</span></span><br/> | <dl> <span data-ttu-id="20943-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="20943-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20943-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20943-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20943-123">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="20943-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




