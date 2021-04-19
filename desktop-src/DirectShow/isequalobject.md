---
description: La funzione IsEqualObject controlla se due interfacce si trovano nello stesso oggetto.
ms.assetid: 51325e05-5a7f-4a80-a12e-2e7dedc028e2
title: Funzione IsEqualObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsEqualObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e959d687d7d6b11dc6055daeda789e728d875d70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326270"
---
# <a name="isequalobject-function"></a><span data-ttu-id="45fb5-103">IsEqualObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="45fb5-103">IsEqualObject function</span></span>

<span data-ttu-id="45fb5-104">La `IsEqualObject` funzione controlla se due interfacce si trovano nello stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="45fb5-104">The `IsEqualObject` function checks if two interfaces are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="45fb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45fb5-105">Syntax</span></span>


```C++
BOOL WINAPI IsEqualObject(
   IUnknown *pFirst,
   IUnknown *pSecond
);
```



## <a name="parameters"></a><span data-ttu-id="45fb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45fb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45fb5-107">*pFirst*</span><span class="sxs-lookup"><span data-stu-id="45fb5-107">*pFirst*</span></span> 
</dt> <dd>

<span data-ttu-id="45fb5-108">Puntatore a un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="45fb5-108">Pointer to one interface.</span></span>

</dd> <dt>

<span data-ttu-id="45fb5-109">*pSecond*</span><span class="sxs-lookup"><span data-stu-id="45fb5-109">*pSecond*</span></span> 
</dt> <dd>

<span data-ttu-id="45fb5-110">Puntatore all'altra interfaccia.</span><span class="sxs-lookup"><span data-stu-id="45fb5-110">Pointer to the other interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45fb5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45fb5-111">Return value</span></span>

<span data-ttu-id="45fb5-112">Restituisce **true** se le interfacce si trovano entrambi nello stesso oggetto. in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="45fb5-112">Returns **TRUE** if the interfaces are both on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fb5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45fb5-113">Requirements</span></span>



| <span data-ttu-id="45fb5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="45fb5-114">Requirement</span></span> | <span data-ttu-id="45fb5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="45fb5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45fb5-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45fb5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="45fb5-117"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45fb5-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="45fb5-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="45fb5-118">Library</span></span><br/> | <dl> <span data-ttu-id="45fb5-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="45fb5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45fb5-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45fb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45fb5-121">Funzioni helper varie</span><span class="sxs-lookup"><span data-stu-id="45fb5-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




