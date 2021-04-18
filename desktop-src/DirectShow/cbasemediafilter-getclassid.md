---
description: "Il metodo GetClassID recupera l'identificatore di classe. Questo metodo implementa il metodo IPersist:: GetClassID."
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: Metodo CBaseMediaFilter. GetClassID (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325383"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="3a1fd-104">CBaseMediaFilter. GetClassID, metodo</span><span class="sxs-lookup"><span data-stu-id="3a1fd-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="3a1fd-105">Il `GetClassID` metodo recupera l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="3a1fd-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="3a1fd-106">Questo metodo implementa il metodo **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="3a1fd-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a1fd-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="3a1fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a1fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a1fd-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="3a1fd-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="3a1fd-110">Puntatore a una variabile che riceve l'identificatore di classe.</span><span class="sxs-lookup"><span data-stu-id="3a1fd-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a1fd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a1fd-111">Return value</span></span>

<span data-ttu-id="3a1fd-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="3a1fd-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1fd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a1fd-113">Requirements</span></span>



| <span data-ttu-id="3a1fd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a1fd-114">Requirement</span></span> | <span data-ttu-id="3a1fd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3a1fd-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1fd-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a1fd-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1fd-117"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1fd-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3a1fd-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3a1fd-118">Library</span></span><br/> | <dl> <span data-ttu-id="3a1fd-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1fd-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1fd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3a1fd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1fd-121">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="3a1fd-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




