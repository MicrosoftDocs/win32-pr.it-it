---
description: Il metodo posticipate specifica una nuova ora di presentazione per un comando accodato in precedenza.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Metodo CDeferredCommand. posticipate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333725"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="fc3ed-103">Metodo CDeferredCommand. posporre</span><span class="sxs-lookup"><span data-stu-id="fc3ed-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="fc3ed-104">Il `Postpone` metodo specifica una nuova ora di presentazione per un comando accodato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fc3ed-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc3ed-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="fc3ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc3ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc3ed-107">*newTime*</span><span class="sxs-lookup"><span data-stu-id="fc3ed-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="fc3ed-108">Ora della nuova presentazione.</span><span class="sxs-lookup"><span data-stu-id="fc3ed-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc3ed-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc3ed-109">Return value</span></span>

<span data-ttu-id="fc3ed-110">Restituisce l' \_ ora di VFW E \_ \_ è già stata \_ passata se *newTime* è già stato superato.</span><span class="sxs-lookup"><span data-stu-id="fc3ed-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="fc3ed-111">In caso contrario, restituisce un **HRESULT** risultante da una chiamata a [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (quando si estrae dall'elenco) o [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (durante il reinserimento con l'ora di modifica).</span><span class="sxs-lookup"><span data-stu-id="fc3ed-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3ed-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc3ed-112">Remarks</span></span>

<span data-ttu-id="fc3ed-113">Questa funzione membro implementa il metodo [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .</span><span class="sxs-lookup"><span data-stu-id="fc3ed-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc3ed-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc3ed-114">Requirements</span></span>



| <span data-ttu-id="fc3ed-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc3ed-115">Requirement</span></span> | <span data-ttu-id="fc3ed-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fc3ed-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc3ed-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc3ed-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fc3ed-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc3ed-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fc3ed-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc3ed-119">Library</span></span><br/> | <dl> <span data-ttu-id="fc3ed-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fc3ed-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc3ed-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc3ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc3ed-122">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="fc3ed-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




