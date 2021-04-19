---
description: Il metodo seTYPE specifica il tipo principale.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Metodo CMediaType. seTYPE (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332209"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="5cbd1-103">Metodo CMediaType. seTYPE</span><span class="sxs-lookup"><span data-stu-id="5cbd1-103">CMediaType.SetType method</span></span>

<span data-ttu-id="5cbd1-104">Il `SetType` metodo specifica il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5cbd1-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cbd1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cbd1-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="5cbd1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cbd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cbd1-107">*pType*</span><span class="sxs-lookup"><span data-stu-id="5cbd1-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="5cbd1-108">Puntatore a un **GUID** che specifica il tipo principale.</span><span class="sxs-lookup"><span data-stu-id="5cbd1-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cbd1-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cbd1-109">Return value</span></span>

<span data-ttu-id="5cbd1-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5cbd1-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cbd1-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cbd1-111">Requirements</span></span>



| <span data-ttu-id="5cbd1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cbd1-112">Requirement</span></span> | <span data-ttu-id="5cbd1-113">Valore</span><span class="sxs-lookup"><span data-stu-id="5cbd1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cbd1-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cbd1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5cbd1-115"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5cbd1-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5cbd1-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="5cbd1-116">Library</span></span><br/> | <dl> <span data-ttu-id="5cbd1-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5cbd1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cbd1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cbd1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cbd1-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="5cbd1-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




