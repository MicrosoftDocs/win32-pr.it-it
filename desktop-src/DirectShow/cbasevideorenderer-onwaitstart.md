---
description: Il metodo OnWaitStart aggiorna i tempi di attesa e non in attesa.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Metodo CBaseVideoRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325363"
---
# <a name="cbasevideorendereronwaitstart-method"></a><span data-ttu-id="e6463-103">CBaseVideoRenderer. OnWaitStart, metodo</span><span class="sxs-lookup"><span data-stu-id="e6463-103">CBaseVideoRenderer.OnWaitStart method</span></span>

<span data-ttu-id="e6463-104">Il `OnWaitStart` metodo aggiorna i tempi di attesa e non è in attesa.</span><span class="sxs-lookup"><span data-stu-id="e6463-104">The `OnWaitStart` method updates times spent waiting and not waiting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6463-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6463-105">Syntax</span></span>


```C++
void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="e6463-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6463-106">Parameters</span></span>

<span data-ttu-id="e6463-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e6463-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6463-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6463-108">Return value</span></span>

<span data-ttu-id="e6463-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e6463-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6463-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6463-110">Remarks</span></span>

<span data-ttu-id="e6463-111">Questa funzione membro viene chiamata quando si avvia l'attesa di un evento di rendering.</span><span class="sxs-lookup"><span data-stu-id="e6463-111">This member function is called when starting to wait for a rendering event.</span></span> <span data-ttu-id="e6463-112">Viene usato solo per le misurazioni delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e6463-112">It is used only for performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6463-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6463-113">Requirements</span></span>



| <span data-ttu-id="e6463-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6463-114">Requirement</span></span> | <span data-ttu-id="e6463-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e6463-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6463-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6463-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e6463-117"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6463-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6463-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6463-118">Library</span></span><br/> | <dl> <span data-ttu-id="e6463-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e6463-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6463-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6463-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6463-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e6463-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




