---
description: Il metodo SetSourcePosition imposta una nuova posizione di origine per il video.
ms.assetid: e3c9ce31-9c24-4ef5-9526-ef6b890f5109
title: Metodo CBaseControlVideo. SetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5493779b623108f713f8da252e8696140883395b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333215"
---
# <a name="cbasecontrolvideosetsourceposition-method"></a><span data-ttu-id="6da77-103">CBaseControlVideo. SetSourcePosition, metodo</span><span class="sxs-lookup"><span data-stu-id="6da77-103">CBaseControlVideo.SetSourcePosition method</span></span>

<span data-ttu-id="6da77-104">Il `SetSourcePosition` metodo imposta una nuova posizione di origine per il video.</span><span class="sxs-lookup"><span data-stu-id="6da77-104">The `SetSourcePosition` method sets a new source position for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6da77-105">Syntax</span></span>


```C++
HRESULT SetSourcePosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a><span data-ttu-id="6da77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6da77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da77-107">*Sinistra*</span><span class="sxs-lookup"><span data-stu-id="6da77-107">*Left*</span></span> 
</dt> <dd>

<span data-ttu-id="6da77-108">Nuova coordinata sinistra.</span><span class="sxs-lookup"><span data-stu-id="6da77-108">New left coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6da77-109">*Top*</span><span class="sxs-lookup"><span data-stu-id="6da77-109">*Top*</span></span> 
</dt> <dd>

<span data-ttu-id="6da77-110">Nuova coordinata superiore.</span><span class="sxs-lookup"><span data-stu-id="6da77-110">New top coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="6da77-111">*Larghezza*</span><span class="sxs-lookup"><span data-stu-id="6da77-111">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="6da77-112">Nuova larghezza.</span><span class="sxs-lookup"><span data-stu-id="6da77-112">New width.</span></span>

</dd> <dt>

<span data-ttu-id="6da77-113">*Altezza*</span><span class="sxs-lookup"><span data-stu-id="6da77-113">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="6da77-114">Nuova altezza.</span><span class="sxs-lookup"><span data-stu-id="6da77-114">New height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da77-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6da77-115">Return value</span></span>

<span data-ttu-id="6da77-116">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="6da77-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="6da77-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6da77-117">Return code</span></span>                                                                                           | <span data-ttu-id="6da77-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6da77-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6da77-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="6da77-120">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6da77-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6da77-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="6da77-122">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="6da77-122">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="6da77-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-123"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="6da77-124">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="6da77-124">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="6da77-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="6da77-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6da77-126">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="6da77-127"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-127"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6da77-128">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="6da77-128">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6da77-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="6da77-129">Remarks</span></span>

<span data-ttu-id="6da77-130">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="6da77-130">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="6da77-131">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="6da77-131">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="6da77-132">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6da77-132">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="6da77-133">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="6da77-133">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="6da77-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6da77-134">Requirements</span></span>



| <span data-ttu-id="6da77-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6da77-135">Requirement</span></span> | <span data-ttu-id="6da77-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6da77-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da77-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6da77-137">Header</span></span><br/>  | <dl> <span data-ttu-id="6da77-138"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6da77-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="6da77-139">Library</span></span><br/> | <dl> <span data-ttu-id="6da77-140"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6da77-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6da77-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6da77-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6da77-142">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="6da77-142">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




