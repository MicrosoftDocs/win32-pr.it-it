---
description: Il metodo CheckTime determina se è previsto un periodo di tempo specificato.
ms.assetid: 522bc7ae-f998-4a7d-8bc3-caf09b4108a6
title: Metodo CCmdQueue. CheckTime (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.CheckTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17fd67973e122830e53d93d1d8db17046f716507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333484"
---
# <a name="ccmdqueuechecktime-method"></a><span data-ttu-id="d0fe1-103">CCmdQueue. CheckTime, metodo</span><span class="sxs-lookup"><span data-stu-id="d0fe1-103">CCmdQueue.CheckTime method</span></span>

<span data-ttu-id="d0fe1-104">Il `CheckTime` metodo determina se è previsto un periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-104">The `CheckTime` method determines if a specified time is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0fe1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0fe1-105">Syntax</span></span>


```C++
BOOL CheckTime(
   CRefTime time,
   BOOL     bStream
);
```



## <a name="parameters"></a><span data-ttu-id="d0fe1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0fe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0fe1-107">*time*</span><span class="sxs-lookup"><span data-stu-id="d0fe1-107">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fe1-108">Tempo da verificare.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-108">Time to check.</span></span>

</dd> <dt>

<span data-ttu-id="d0fe1-109">*bStream*</span><span class="sxs-lookup"><span data-stu-id="d0fe1-109">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="d0fe1-110">**True** se il parametro *Time* è un valore del flusso di tempo; **False** se *Time* è un valore in fase di presentazione.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-110">**TRUE** if the *time* parameter is a stream-time value; **FALSE** if *time* is a presentation-time value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0fe1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0fe1-111">Return value</span></span>

<span data-ttu-id="d0fe1-112">Restituisce **true** se l'ora specificata non è stata ancora superata.</span><span class="sxs-lookup"><span data-stu-id="d0fe1-112">Returns **TRUE** if the specified time has not yet passed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0fe1-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0fe1-113">Requirements</span></span>



| <span data-ttu-id="d0fe1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0fe1-114">Requirement</span></span> | <span data-ttu-id="d0fe1-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d0fe1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fe1-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0fe1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d0fe1-117"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe1-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0fe1-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0fe1-118">Library</span></span><br/> | <dl> <span data-ttu-id="d0fe1-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d0fe1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0fe1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0fe1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0fe1-121">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="d0fe1-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




