---
description: Il metodo GetSourceRect Recupera il rettangolo di origine corrente.
ms.assetid: e9ca091f-3fd7-4e42-90e9-b7831dd488a9
title: Metodo CDrawImage. GetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8a2188a183794b94a5d6d05ac237f91dbcb5d6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329163"
---
# <a name="cdrawimagegetsourcerect-method"></a><span data-ttu-id="f004d-103">CDrawImage. GetSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="f004d-103">CDrawImage.GetSourceRect method</span></span>

<span data-ttu-id="f004d-104">Il `GetSourceRect` metodo recupera il rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="f004d-104">The `GetSourceRect` method retrieves the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f004d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f004d-105">Syntax</span></span>


```C++
void GetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="f004d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f004d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f004d-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="f004d-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="f004d-108">Puntatore a una struttura **Rect** che riceve il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="f004d-108">Pointer to a **RECT** structure that receives the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f004d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f004d-109">Return value</span></span>

<span data-ttu-id="f004d-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f004d-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f004d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f004d-111">Requirements</span></span>



| <span data-ttu-id="f004d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f004d-112">Requirement</span></span> | <span data-ttu-id="f004d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f004d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f004d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f004d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f004d-115"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f004d-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f004d-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="f004d-116">Library</span></span><br/> | <dl> <span data-ttu-id="f004d-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f004d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f004d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f004d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f004d-119">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="f004d-119">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




