---
description: Questo operatore verifica la disuguaglianza tra gli oggetti CMediaType.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'Metodo CMediaType. CMediaType:: operator! = (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326401"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="ddf99-103">Metodo CMediaType. CMediaType:: operator! =</span><span class="sxs-lookup"><span data-stu-id="ddf99-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="ddf99-104">Questo operatore verifica la disuguaglianza tra gli oggetti [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="ddf99-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf99-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddf99-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="ddf99-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddf99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddf99-107">*RT* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="ddf99-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ddf99-108">Riferimento all'oggetto **CMediaType** da confrontare.</span><span class="sxs-lookup"><span data-stu-id="ddf99-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddf99-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddf99-109">Return value</span></span>

<span data-ttu-id="ddf99-110">Restituisce **true** se *RT* non è uguale all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddf99-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="ddf99-111">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="ddf99-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf99-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddf99-112">Requirements</span></span>



| <span data-ttu-id="ddf99-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf99-113">Requirement</span></span> | <span data-ttu-id="ddf99-114">Valore</span><span class="sxs-lookup"><span data-stu-id="ddf99-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf99-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddf99-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ddf99-116"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddf99-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ddf99-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddf99-117">Library</span></span><br/> | <dl> <span data-ttu-id="ddf99-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ddf99-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddf99-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddf99-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf99-120">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="ddf99-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




