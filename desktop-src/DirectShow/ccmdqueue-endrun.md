---
description: Il metodo EndRun passa alla modalità arrestata o sospesa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Metodo CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324485"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="b0289-103">CCmdQueue. EndRun, metodo</span><span class="sxs-lookup"><span data-stu-id="b0289-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="b0289-104">Il `EndRun` metodo passa alla modalità arrestata o sospesa.</span><span class="sxs-lookup"><span data-stu-id="b0289-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0289-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0289-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="b0289-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0289-106">Parameters</span></span>

<span data-ttu-id="b0289-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b0289-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0289-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0289-108">Return value</span></span>

<span data-ttu-id="b0289-109">Restituisce un valore **HRESULT** che dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="b0289-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0289-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0289-110">Remarks</span></span>

<span data-ttu-id="b0289-111">Il mapping dell'ora tra il tempo di flusso e l'ora di presentazione non è noto dopo la chiamata di questa funzione membro.</span><span class="sxs-lookup"><span data-stu-id="b0289-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="b0289-112">Chiamare la funzione membro [**CCmdQueue:: Run**](ccmdqueue-run.md) per eseguire questo mapping.</span><span class="sxs-lookup"><span data-stu-id="b0289-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0289-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0289-113">Requirements</span></span>



| <span data-ttu-id="b0289-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0289-114">Requirement</span></span> | <span data-ttu-id="b0289-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b0289-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0289-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0289-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b0289-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0289-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0289-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0289-118">Library</span></span><br/> | <dl> <span data-ttu-id="b0289-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0289-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0289-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0289-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0289-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="b0289-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




