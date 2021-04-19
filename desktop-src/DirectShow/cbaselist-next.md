---
description: Il metodo successivo recupera la posizione successiva nell'elenco.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Metodo CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328647"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="d7bef-103">Metodo CBaseList. Next</span><span class="sxs-lookup"><span data-stu-id="d7bef-103">CBaseList.Next method</span></span>

<span data-ttu-id="d7bef-104">Il `Next` metodo recupera la posizione successiva nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d7bef-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7bef-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="d7bef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7bef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bef-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="d7bef-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="d7bef-108">Valore della posizione.</span><span class="sxs-lookup"><span data-stu-id="d7bef-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bef-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7bef-109">Return value</span></span>

<span data-ttu-id="d7bef-110">Restituisce l'indicatore di posizione che segue la posizione specificata da *pos*.</span><span class="sxs-lookup"><span data-stu-id="d7bef-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7bef-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7bef-111">Remarks</span></span>

<span data-ttu-id="d7bef-112">Se *pos* è l'ultima posizione nell'elenco, il metodo restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="d7bef-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="d7bef-113">Se *pos* è **null**, il metodo restituisce la prima posizione nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d7bef-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bef-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7bef-114">Requirements</span></span>



| <span data-ttu-id="d7bef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7bef-115">Requirement</span></span> | <span data-ttu-id="d7bef-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d7bef-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bef-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7bef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d7bef-118"><dt>Wxlist. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bef-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d7bef-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d7bef-119">Library</span></span><br/> | <dl> <span data-ttu-id="d7bef-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d7bef-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7bef-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7bef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bef-122">**Classe CBaseList**</span><span class="sxs-lookup"><span data-stu-id="d7bef-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




