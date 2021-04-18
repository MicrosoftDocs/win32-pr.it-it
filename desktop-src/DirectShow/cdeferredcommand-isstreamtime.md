---
description: Il metodo IsStreamTime specifica se è necessario eseguire il comando in fase di flusso o di presentazione.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Metodo CDeferredCommand. IsStreamTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333729"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="fa0b3-103">CDeferredCommand. IsStreamTime, metodo</span><span class="sxs-lookup"><span data-stu-id="fa0b3-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="fa0b3-104">Il `IsStreamTime` metodo specifica se il comando deve essere eseguito in fase di flusso o di presentazione.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa0b3-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="fa0b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa0b3-106">Parameters</span></span>

<span data-ttu-id="fa0b3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa0b3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa0b3-108">Return value</span></span>

<span data-ttu-id="fa0b3-109">Restituisce **true** se impostato sull'ora del flusso; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="fa0b3-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0b3-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa0b3-110">Requirements</span></span>



| <span data-ttu-id="fa0b3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa0b3-111">Requirement</span></span> | <span data-ttu-id="fa0b3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="fa0b3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0b3-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa0b3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="fa0b3-114"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b3-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fa0b3-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa0b3-115">Library</span></span><br/> | <dl> <span data-ttu-id="fa0b3-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0b3-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa0b3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0b3-118">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="fa0b3-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




