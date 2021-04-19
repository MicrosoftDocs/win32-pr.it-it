---
description: Il \_ metodo Put SourceTop imposta la coordinata superiore del rettangolo di origine.
ms.assetid: 8891771d-5a0b-4dfa-b961-9f375f13b4f7
title: Metodo CBaseControlVideo.put_SourceTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76786290609026da44ada7cae962fd7d4b09c358
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325400"
---
# <a name="cbasecontrolvideoput_sourcetop-method"></a><span data-ttu-id="e0baa-103">CBaseControlVideo. put \_ SourceTop (metodo)</span><span class="sxs-lookup"><span data-stu-id="e0baa-103">CBaseControlVideo.put\_SourceTop method</span></span>

<span data-ttu-id="e0baa-104">Il `put_SourceTop` metodo imposta la coordinata superiore del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="e0baa-104">The `put_SourceTop` method sets the top coordinate of the source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0baa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0baa-105">Syntax</span></span>


```C++
HRESULT put_SourceTop(
   long SourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="e0baa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0baa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0baa-107">*SourceTop*</span><span class="sxs-lookup"><span data-stu-id="e0baa-107">*SourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="e0baa-108">Nuova coordinata superiore del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="e0baa-108">New top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0baa-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0baa-109">Return value</span></span>

<span data-ttu-id="e0baa-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="e0baa-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="e0baa-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e0baa-111">Return code</span></span>                                                                                           | <span data-ttu-id="e0baa-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0baa-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0baa-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="e0baa-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e0baa-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="e0baa-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="e0baa-116">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="e0baa-116">Invalid argument.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="e0baa-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-117"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="e0baa-118">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="e0baa-118">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="e0baa-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="e0baa-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e0baa-120">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="e0baa-121"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-121"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e0baa-122">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="e0baa-122">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0baa-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0baa-123">Remarks</span></span>

<span data-ttu-id="e0baa-124">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="e0baa-124">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="e0baa-125">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="e0baa-125">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="e0baa-126">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e0baa-126">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="e0baa-127">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="e0baa-127">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0baa-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0baa-128">Requirements</span></span>



| <span data-ttu-id="e0baa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0baa-129">Requirement</span></span> | <span data-ttu-id="e0baa-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e0baa-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0baa-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0baa-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e0baa-132"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0baa-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0baa-133">Library</span></span><br/> | <dl> <span data-ttu-id="e0baa-134"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e0baa-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0baa-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0baa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0baa-136">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="e0baa-136">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




