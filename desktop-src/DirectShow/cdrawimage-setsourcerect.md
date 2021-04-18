---
description: Il metodo SetSourceRect imposta il rettangolo di origine.
ms.assetid: 982636fe-73ea-4f13-9f2b-7ae8df839ab1
title: Metodo CDrawImage. SetSourceRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64fb8729b694d38eac2d6321f92904292d99bd38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325194"
---
# <a name="cdrawimagesetsourcerect-method"></a><span data-ttu-id="fade0-103">CDrawImage. SetSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="fade0-103">CDrawImage.SetSourceRect method</span></span>

<span data-ttu-id="fade0-104">Il `SetSourceRect` metodo imposta il rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="fade0-104">The `SetSourceRect` method sets the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="fade0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fade0-105">Syntax</span></span>


```C++
void SetSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="fade0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fade0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fade0-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="fade0-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="fade0-108">Puntatore a una struttura **Rect** che definisce il nuovo rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="fade0-108">Pointer to a **RECT** structure that defines the new source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fade0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fade0-109">Return value</span></span>

<span data-ttu-id="fade0-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fade0-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fade0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="fade0-111">Remarks</span></span>

<span data-ttu-id="fade0-112">Il filtro proprietario deve chiamare questo metodo se il rettangolo di origine viene modificato; ad esempio, in risposta a una chiamata [**IBasicVideo:: SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) .</span><span class="sxs-lookup"><span data-stu-id="fade0-112">The owning filter should call this method if the source rectangle changes; for example, in response to an [**IBasicVideo::SetSourcePosition**](/windows/desktop/api/Control/nf-control-ibasicvideo-setsourceposition) call.</span></span>

<span data-ttu-id="fade0-113">Verificare il rettangolo specificato in *pSourceRect* prima di chiamare questo metodo, per assicurarsi che non si estenda oltre le dimensioni del video nativo.</span><span class="sxs-lookup"><span data-stu-id="fade0-113">Validate the rectangle given in *pSourceRect* before calling this method, to make sure it does not extend beyond the native video size.</span></span>

## <a name="requirements"></a><span data-ttu-id="fade0-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fade0-114">Requirements</span></span>



| <span data-ttu-id="fade0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fade0-115">Requirement</span></span> | <span data-ttu-id="fade0-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fade0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fade0-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fade0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fade0-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fade0-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fade0-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fade0-119">Library</span></span><br/> | <dl> <span data-ttu-id="fade0-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fade0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fade0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fade0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fade0-122">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="fade0-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




