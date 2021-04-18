---
description: "Il metodo GetClassID recupera l'identificatore di classe (CLSID) dell'oggetto. Questo metodo implementa il metodo IPersist:: GetClassID."
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Metodo CSystemClock. GetClassID (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333711"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="506c8-104">CSystemClock. GetClassID, metodo</span><span class="sxs-lookup"><span data-stu-id="506c8-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="506c8-105">Il `GetClassID` metodo recupera l'identificatore di classe (CLSID) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="506c8-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="506c8-106">Questo metodo implementa il metodo **IPersist:: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="506c8-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="506c8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="506c8-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="506c8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="506c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="506c8-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="506c8-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="506c8-110">Puntatore a una variabile che riceve il valore CLSID \_ SystemClock.</span><span class="sxs-lookup"><span data-stu-id="506c8-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="506c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="506c8-111">Return value</span></span>

<span data-ttu-id="506c8-112">Restituisce un \_ puntatore S OK o e \_ .</span><span class="sxs-lookup"><span data-stu-id="506c8-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="506c8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="506c8-113">Requirements</span></span>



| <span data-ttu-id="506c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="506c8-114">Requirement</span></span> | <span data-ttu-id="506c8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="506c8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="506c8-116">Versione</span><span class="sxs-lookup"><span data-stu-id="506c8-116">Version</span></span><br/> | <span data-ttu-id="506c8-117">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="506c8-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="506c8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="506c8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="506c8-119"><dt>Sysclock. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="506c8-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="506c8-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="506c8-120">Library</span></span><br/> | <dl> <span data-ttu-id="506c8-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="506c8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




