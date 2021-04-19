---
description: Il metodo SetDrawContext imposta i contesti di dispositivo usati per il disegno.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Metodo CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326826"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="165c9-103">CDrawImage. SetDrawContext, metodo</span><span class="sxs-lookup"><span data-stu-id="165c9-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="165c9-104">Il `SetDrawContext` metodo imposta i contesti di dispositivo usati per il disegno.</span><span class="sxs-lookup"><span data-stu-id="165c9-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="165c9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="165c9-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="165c9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="165c9-106">Parameters</span></span>

<span data-ttu-id="165c9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="165c9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="165c9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="165c9-108">Return value</span></span>

<span data-ttu-id="165c9-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="165c9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="165c9-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="165c9-110">Remarks</span></span>

<span data-ttu-id="165c9-111">Questo metodo recupera i contesti di dispositivo della finestra e memoria dall'oggetto [**CBaseWindow**](cbasewindow.md) proprietario.</span><span class="sxs-lookup"><span data-stu-id="165c9-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="165c9-112">Chiamare questo metodo dopo l'inizializzazione della finestra, ma prima di iniziare il disegno.</span><span class="sxs-lookup"><span data-stu-id="165c9-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="165c9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="165c9-113">Requirements</span></span>



| <span data-ttu-id="165c9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="165c9-114">Requirement</span></span> | <span data-ttu-id="165c9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="165c9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="165c9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="165c9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="165c9-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="165c9-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="165c9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="165c9-118">Library</span></span><br/> | <dl> <span data-ttu-id="165c9-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="165c9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="165c9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="165c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="165c9-121">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="165c9-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




