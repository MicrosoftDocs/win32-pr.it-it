---
description: Questo operatore verifica l'uguaglianza tra gli oggetti CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'Metodo CMediaType. CMediaType:: operator = = (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330670"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="e276e-103">Metodo CMediaType. CMediaType:: operator = =</span><span class="sxs-lookup"><span data-stu-id="e276e-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="e276e-104">Questo operatore verifica l'uguaglianza tra gli oggetti [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="e276e-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e276e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e276e-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="e276e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e276e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e276e-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="e276e-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e276e-108">Riferimento all'oggetto **CMediaType** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="e276e-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e276e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e276e-109">Return value</span></span>

<span data-ttu-id="e276e-110">Restituisce **true** se *RT* è uguale a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e276e-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="e276e-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="e276e-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e276e-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e276e-112">Requirements</span></span>



| <span data-ttu-id="e276e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e276e-113">Requirement</span></span> | <span data-ttu-id="e276e-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e276e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e276e-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e276e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e276e-116"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e276e-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e276e-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e276e-117">Library</span></span><br/> | <dl> <span data-ttu-id="e276e-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e276e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e276e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e276e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e276e-120">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e276e-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




