---
description: Il metodo IsValid determina se un tipo principale è stato assegnato a questo oggetto.
ms.assetid: 22d28019-f360-4b93-972c-d1dfe83938f0
title: Metodo CMediaType. IsValid (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.IsValid
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d8e1731060021b61eb5037e1baeeda95021e8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330675"
---
# <a name="cmediatypeisvalid-method"></a><span data-ttu-id="cdf1f-103">Metodo CMediaType. IsValid</span><span class="sxs-lookup"><span data-stu-id="cdf1f-103">CMediaType.IsValid method</span></span>

<span data-ttu-id="cdf1f-104">Il `IsValid` metodo determina se un tipo principale è stato assegnato a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-104">The `IsValid` method determines whether a major type has been assigned to this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf1f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdf1f-105">Syntax</span></span>


```C++
BOOL IsValid() const;
```



## <a name="parameters"></a><span data-ttu-id="cdf1f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdf1f-106">Parameters</span></span>

<span data-ttu-id="cdf1f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdf1f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdf1f-108">Return value</span></span>

<span data-ttu-id="cdf1f-109">Restituisce **true** se è stato assegnato un tipo principale a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-109">Returns **TRUE** if a major type has been assigned to this object.</span></span> <span data-ttu-id="cdf1f-110">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf1f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdf1f-111">Remarks</span></span>

<span data-ttu-id="cdf1f-112">Per impostazione predefinita, gli oggetti [**CMediaType**](cmediatype.md) vengono inizializzati con un tipo principale di GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-112">By default, [**CMediaType**](cmediatype.md) objects are initialized with a major type of GUID\_NULL.</span></span> <span data-ttu-id="cdf1f-113">Chiamare questo metodo per determinare se l'oggetto è stato inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="cdf1f-113">Call this method to determine whether the object has been correctly initialized.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf1f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdf1f-114">Requirements</span></span>



| <span data-ttu-id="cdf1f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf1f-115">Requirement</span></span> | <span data-ttu-id="cdf1f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cdf1f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf1f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdf1f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cdf1f-118"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdf1f-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="cdf1f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdf1f-119">Library</span></span><br/> | <dl> <span data-ttu-id="cdf1f-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="cdf1f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdf1f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf1f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf1f-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="cdf1f-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




