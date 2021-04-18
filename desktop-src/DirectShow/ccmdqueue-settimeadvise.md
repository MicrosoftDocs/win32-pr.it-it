---
description: Il metodo SetTimeAdvise imposta un evento timer con l'orologio di riferimento.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Metodo CCmdQueue. SetTimeAdvise (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324025"
---
# <a name="ccmdqueuesettimeadvise-method"></a><span data-ttu-id="f2913-103">CCmdQueue. SetTimeAdvise, metodo</span><span class="sxs-lookup"><span data-stu-id="f2913-103">CCmdQueue.SetTimeAdvise method</span></span>

<span data-ttu-id="f2913-104">Il `SetTimeAdvise` metodo configura un evento timer con l'orologio di riferimento.</span><span class="sxs-lookup"><span data-stu-id="f2913-104">The `SetTimeAdvise` method sets up a timer event with the reference clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2913-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2913-105">Syntax</span></span>


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a><span data-ttu-id="f2913-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2913-106">Parameters</span></span>

<span data-ttu-id="f2913-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f2913-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2913-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2913-108">Return value</span></span>

<span data-ttu-id="f2913-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f2913-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2913-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2913-110">Remarks</span></span>

<span data-ttu-id="f2913-111">Questa funzione membro chiama il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) per impostare una notifica per la prima ora necessaria nella coda.</span><span class="sxs-lookup"><span data-stu-id="f2913-111">This member function calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method to set up a notification for the earliest time required in the queue.</span></span> <span data-ttu-id="f2913-112">I comandi per la fase di presentazione posticipati vengono sempre controllati.</span><span class="sxs-lookup"><span data-stu-id="f2913-112">Presentation-time commands that are deferred are always checked.</span></span> <span data-ttu-id="f2913-113">Se il grafico del filtro è in modalità di esecuzione, vengono controllati anche i comandi posticipati che usano il tempo di flusso.</span><span class="sxs-lookup"><span data-stu-id="f2913-113">If the filter graph is in running mode, deferred commands using stream time are also checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2913-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2913-114">Requirements</span></span>



| <span data-ttu-id="f2913-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2913-115">Requirement</span></span> | <span data-ttu-id="f2913-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f2913-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2913-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f2913-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f2913-118"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2913-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2913-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="f2913-119">Library</span></span><br/> | <dl> <span data-ttu-id="f2913-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f2913-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2913-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2913-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2913-122">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="f2913-122">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




