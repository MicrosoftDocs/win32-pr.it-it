---
description: Il metodo ScaleSourceRect ridimensiona un rettangolo, se esiste una differenza tra la dimensione del video nativa e il formato del tipo di supporto.
ms.assetid: 7bd4d555-5782-4ce5-9f0d-928b199ef897
title: Metodo CDrawImage. ScaleSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ScaleSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9800f405c0002fb58ca68ebd2369eb068f6319a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325327"
---
# <a name="cdrawimagescalesourcerect-method"></a><span data-ttu-id="ce498-103">CDrawImage. ScaleSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="ce498-103">CDrawImage.ScaleSourceRect method</span></span>

<span data-ttu-id="ce498-104">Il `ScaleSourceRect` metodo ridimensiona un rettangolo, se esiste una differenza tra la dimensione del video nativa e il formato del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="ce498-104">The `ScaleSourceRect` method scales a rectangle, if there is a difference between the native video size and the media type format.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce498-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce498-105">Syntax</span></span>


```C++
virtual RECT ScaleSourceRect(
   const RECT *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="ce498-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce498-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce498-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="ce498-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="ce498-108">Puntatore a un rettangolo non ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="ce498-108">Pointer to an unscaled rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce498-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce498-109">Return value</span></span>

<span data-ttu-id="ce498-110">Restituisce il rettangolo ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="ce498-110">Returns the scaled rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce498-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce498-111">Remarks</span></span>

<span data-ttu-id="ce498-112">Nella classe **CDrawImage** , questo metodo restituisce *pSource* senza alcuna modifica.</span><span class="sxs-lookup"><span data-stu-id="ce498-112">In the **CDrawImage** class, this method returns *pSource* without any change.</span></span> <span data-ttu-id="ce498-113">È possibile eseguire l'override di questo metodo se il filtro estende l'immagine video in arrivo.</span><span class="sxs-lookup"><span data-stu-id="ce498-113">You can override this method if the filter stretches the incoming video image.</span></span> <span data-ttu-id="ce498-114">Ad esempio, le dimensioni del video nativo potrebbero essere 320 240, ma il tipo di supporto del PIN di input potrebbe essere 640 480.</span><span class="sxs-lookup"><span data-stu-id="ce498-114">For example, the native video size might be 320   240, but the media type on the input pin might be 640   480.</span></span> <span data-ttu-id="ce498-115">In tal caso, è necessario che il filtro Ridimensiona il rettangolo di origine in base a un fattore di 2.</span><span class="sxs-lookup"><span data-stu-id="ce498-115">In that case the filter would need to scale the source rectangle by a factor of 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce498-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce498-116">Requirements</span></span>



| <span data-ttu-id="ce498-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce498-117">Requirement</span></span> | <span data-ttu-id="ce498-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ce498-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce498-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce498-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ce498-120"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce498-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce498-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce498-121">Library</span></span><br/> | <dl> <span data-ttu-id="ce498-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce498-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce498-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce498-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce498-124">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="ce498-124">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




