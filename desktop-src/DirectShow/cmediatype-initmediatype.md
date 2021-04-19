---
description: Il metodo InitMediaType Inizializza il tipo di supporto.
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: Metodo CMediaType.InitMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324005"
---
# <a name="cmediatypeinitmediatype-method"></a><span data-ttu-id="e35da-103">Metodo tMediaType CMediaType.Ini</span><span class="sxs-lookup"><span data-stu-id="e35da-103">CMediaType.InitMediaType method</span></span>

<span data-ttu-id="e35da-104">Il `InitMediaType` metodo inizializza il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e35da-104">The `InitMediaType` method initializes the media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e35da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e35da-105">Syntax</span></span>


```C++
void InitMediaType();
```



## <a name="parameters"></a><span data-ttu-id="e35da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e35da-106">Parameters</span></span>

<span data-ttu-id="e35da-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e35da-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e35da-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e35da-108">Return value</span></span>

<span data-ttu-id="e35da-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e35da-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e35da-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e35da-110">Remarks</span></span>

<span data-ttu-id="e35da-111">Questo metodo Azzera la memoria dell'oggetto, imposta la proprietà Fixed-sample-size su **true** e imposta le dimensioni del campione su 1.</span><span class="sxs-lookup"><span data-stu-id="e35da-111">This method zeroes the object's memory, sets the fixed-sample-size property to **TRUE**, and sets the sample size to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="e35da-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e35da-112">Requirements</span></span>



| <span data-ttu-id="e35da-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e35da-113">Requirement</span></span> | <span data-ttu-id="e35da-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e35da-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e35da-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e35da-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e35da-116"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e35da-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e35da-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e35da-117">Library</span></span><br/> | <dl> <span data-ttu-id="e35da-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e35da-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e35da-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e35da-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e35da-120">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e35da-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




