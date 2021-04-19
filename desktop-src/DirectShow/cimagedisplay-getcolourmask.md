---
description: Il metodo GetColourMask recupera le maschere dei colori per il formato di visualizzazione corrente.
ms.assetid: 386d0439-8502-411d-935c-3c2153a8b5b4
title: Metodo CImageDisplay. GetColourMask (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetColourMask
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 499b3677cd68444b58514d692d87cd4f631350b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333074"
---
# <a name="cimagedisplaygetcolourmask-method"></a><span data-ttu-id="72da3-103">CImageDisplay. GetColourMask, metodo</span><span class="sxs-lookup"><span data-stu-id="72da3-103">CImageDisplay.GetColourMask method</span></span>

<span data-ttu-id="72da3-104">Il `GetColourMask` metodo recupera le maschere dei colori per il formato di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="72da3-104">The `GetColourMask` method retrieves the color masks for the current display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="72da3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72da3-105">Syntax</span></span>


```C++
BOOL GetColourMask(
   DWORD *pMaskRed,
   DWORD *pMaskGreen,
   DWORD *pMaskBlue
);
```



## <a name="parameters"></a><span data-ttu-id="72da3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72da3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72da3-107">*pMaskRed*</span><span class="sxs-lookup"><span data-stu-id="72da3-107">*pMaskRed*</span></span> 
</dt> <dd>

<span data-ttu-id="72da3-108">Puntatore a una variabile che riceve la maschera del componente rosso.</span><span class="sxs-lookup"><span data-stu-id="72da3-108">Pointer to a variable that receives the red-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="72da3-109">*pMaskGreen*</span><span class="sxs-lookup"><span data-stu-id="72da3-109">*pMaskGreen*</span></span> 
</dt> <dd>

<span data-ttu-id="72da3-110">Puntatore a una variabile che riceve la maschera del componente verde.</span><span class="sxs-lookup"><span data-stu-id="72da3-110">Pointer to a variable that receives the green-component mask.</span></span>

</dd> <dt>

<span data-ttu-id="72da3-111">*pMaskBlue*</span><span class="sxs-lookup"><span data-stu-id="72da3-111">*pMaskBlue*</span></span> 
</dt> <dd>

<span data-ttu-id="72da3-112">Puntatore a una variabile che riceve la maschera del componente blu.</span><span class="sxs-lookup"><span data-stu-id="72da3-112">Pointer to a variable that receives the blue-component mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72da3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72da3-113">Return value</span></span>

<span data-ttu-id="72da3-114">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="72da3-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="72da3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72da3-115">Requirements</span></span>



| <span data-ttu-id="72da3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72da3-116">Requirement</span></span> | <span data-ttu-id="72da3-117">Valore</span><span class="sxs-lookup"><span data-stu-id="72da3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72da3-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72da3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="72da3-119"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72da3-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72da3-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="72da3-120">Library</span></span><br/> | <dl> <span data-ttu-id="72da3-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72da3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72da3-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72da3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72da3-123">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="72da3-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




