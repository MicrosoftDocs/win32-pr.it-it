---
description: Il metodo GetEvent recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Metodo CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328360"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="2c0ad-103">Metodo CAMSchedule. GetEvent</span><span class="sxs-lookup"><span data-stu-id="2c0ad-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="2c0ad-104">Il `GetEvent` metodo recupera un handle di evento, che viene usato per segnalare una modifica nel tempo di notifica successivo.</span><span class="sxs-lookup"><span data-stu-id="2c0ad-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c0ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c0ad-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="2c0ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c0ad-106">Parameters</span></span>

<span data-ttu-id="2c0ad-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2c0ad-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2c0ad-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c0ad-108">Return value</span></span>

<span data-ttu-id="2c0ad-109">Restituisce un handle a un evento.</span><span class="sxs-lookup"><span data-stu-id="2c0ad-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0ad-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c0ad-110">Remarks</span></span>

<span data-ttu-id="2c0ad-111">Se il successivo avviso cambia in altre parole, se viene aggiunta una nuova richiesta di notifica all'inizio dell'elenco, l'utilità di pianificazione segnala l'evento.</span><span class="sxs-lookup"><span data-stu-id="2c0ad-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="2c0ad-112">L'orologio deve chiamare il metodo [**CAMSchedule:: Advise**](camschedule-advise.md) per determinare il tempo di notifica successivo.</span><span class="sxs-lookup"><span data-stu-id="2c0ad-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0ad-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c0ad-113">Requirements</span></span>



| <span data-ttu-id="2c0ad-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c0ad-114">Requirement</span></span> | <span data-ttu-id="2c0ad-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2c0ad-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0ad-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c0ad-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2c0ad-117"><dt>Dsschedule. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ad-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="2c0ad-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="2c0ad-118">Library</span></span><br/> | <dl> <span data-ttu-id="2c0ad-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2c0ad-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0ad-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c0ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0ad-121">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="2c0ad-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




