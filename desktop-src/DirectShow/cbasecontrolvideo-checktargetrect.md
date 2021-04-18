---
description: Il metodo CheckTargetRect determina se un rettangolo di destinazione è valido.
ms.assetid: a16e7faf-6421-4f78-bbb1-40d38f1a5525
title: Metodo CBaseControlVideo. CheckTargetRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94f8d50aea58f556634e7f20b3880aecad72cc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327582"
---
# <a name="cbasecontrolvideochecktargetrect-method"></a><span data-ttu-id="98c5a-103">CBaseControlVideo. CheckTargetRect, metodo</span><span class="sxs-lookup"><span data-stu-id="98c5a-103">CBaseControlVideo.CheckTargetRect method</span></span>

<span data-ttu-id="98c5a-104">Il `CheckTargetRect` metodo determina se un rettangolo di destinazione è valido.</span><span class="sxs-lookup"><span data-stu-id="98c5a-104">The `CheckTargetRect` method determines if a target rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="98c5a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98c5a-105">Syntax</span></span>


```C++
virtual HRESULT CheckTargetRect(
   RECT *pTargetRect
);
```



## <a name="parameters"></a><span data-ttu-id="98c5a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98c5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c5a-107">*pTargetRect*</span><span class="sxs-lookup"><span data-stu-id="98c5a-107">*pTargetRect*</span></span> 
</dt> <dd>

<span data-ttu-id="98c5a-108">Puntatore al rettangolo di destinazione da controllare.</span><span class="sxs-lookup"><span data-stu-id="98c5a-108">Pointer to the target rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c5a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98c5a-109">Return value</span></span>

<span data-ttu-id="98c5a-110">Restituisce E \_ INVALIDARG se non è valido; in caso contrario, restituisce NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="98c5a-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="98c5a-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="98c5a-111">Remarks</span></span>

<span data-ttu-id="98c5a-112">Questa funzione membro determina se il rettangolo di destinazione richiesto è valido.</span><span class="sxs-lookup"><span data-stu-id="98c5a-112">This member function determines if the target rectangle requested is valid.</span></span> <span data-ttu-id="98c5a-113">Poiché il rettangolo di destinazione specifica una posizione nel client logico della finestra, le coordinate possono essere negative, anche se la larghezza e l'altezza complessive non possono essere pari a zero o a un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="98c5a-113">Because the destination rectangle specifies a position in the logical client of the window, the coordinates can be negative, although the overall width and height cannot be zero or a negative value.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c5a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98c5a-114">Requirements</span></span>



| <span data-ttu-id="98c5a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c5a-115">Requirement</span></span> | <span data-ttu-id="98c5a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98c5a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c5a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98c5a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98c5a-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c5a-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="98c5a-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="98c5a-119">Library</span></span><br/> | <dl> <span data-ttu-id="98c5a-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98c5a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c5a-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98c5a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98c5a-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="98c5a-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




