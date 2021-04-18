---
description: Il metodo AlignDown tronca un valore in un limite di allineamento specificato.
ms.assetid: f0efdedb-67ec-49d6-92a8-54485aa04e15
title: Metodo CPullPin. AlignDown (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignDown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1383517f4931fa153fd141878475cc8775a61045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328492"
---
# <a name="cpullpinaligndown-method"></a><span data-ttu-id="24cc5-103">CPullPin. AlignDown, metodo</span><span class="sxs-lookup"><span data-stu-id="24cc5-103">CPullPin.AlignDown method</span></span>

<span data-ttu-id="24cc5-104">Il `AlignDown` Metodo tronca un valore in un limite di allineamento specificato.</span><span class="sxs-lookup"><span data-stu-id="24cc5-104">The `AlignDown` method truncates a value to a specified alignment boundary.</span></span>

## <a name="syntax"></a><span data-ttu-id="24cc5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24cc5-105">Syntax</span></span>


```C++
LONGLONG AlignDown(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="24cc5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24cc5-107">*ll*</span><span class="sxs-lookup"><span data-stu-id="24cc5-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="24cc5-108">Specifica il numero da allineare.</span><span class="sxs-lookup"><span data-stu-id="24cc5-108">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="24cc5-109">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="24cc5-109">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="24cc5-110">Specifica il limite di allineamento.</span><span class="sxs-lookup"><span data-stu-id="24cc5-110">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24cc5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24cc5-111">Return value</span></span>

<span data-ttu-id="24cc5-112">Restituisce il risultato allineato.</span><span class="sxs-lookup"><span data-stu-id="24cc5-112">Returns the aligned result.</span></span>

## <a name="requirements"></a><span data-ttu-id="24cc5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24cc5-113">Requirements</span></span>



| <span data-ttu-id="24cc5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="24cc5-114">Requirement</span></span> | <span data-ttu-id="24cc5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="24cc5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24cc5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24cc5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="24cc5-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="24cc5-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="24cc5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="24cc5-118">Library</span></span><br/> | <dl> <span data-ttu-id="24cc5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24cc5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24cc5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24cc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24cc5-121">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="24cc5-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




