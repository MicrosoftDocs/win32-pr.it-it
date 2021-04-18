---
description: Il metodo SetDefaultDestinationPosition imposta di nuovo il renderer sull'utilizzo della posizione di destinazione predefinita (in genere l'intera area client della finestra).
ms.assetid: 228259d7-2f1f-4528-8c8a-d20d7542523c
title: Metodo CBaseControlVideo. SetDefaultDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a959f462d410b83588fb1a8df87cebffd879d8ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325392"
---
# <a name="cbasecontrolvideosetdefaultdestinationposition-method"></a><span data-ttu-id="43c38-103">CBaseControlVideo. SetDefaultDestinationPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="43c38-103">CBaseControlVideo.SetDefaultDestinationPosition method</span></span>

<span data-ttu-id="43c38-104">Il `SetDefaultDestinationPosition` metodo imposta di nuovo il renderer sull'utilizzo della posizione di destinazione predefinita (in genere l'intera area client della finestra).</span><span class="sxs-lookup"><span data-stu-id="43c38-104">The `SetDefaultDestinationPosition` method sets the renderer back to using the default destination position (typically the entire window client area).</span></span>

## <a name="syntax"></a><span data-ttu-id="43c38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43c38-105">Syntax</span></span>


```C++
HRESULT SetDefaultDestinationPosition();
```



## <a name="parameters"></a><span data-ttu-id="43c38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="43c38-106">Parameters</span></span>

<span data-ttu-id="43c38-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="43c38-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="43c38-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43c38-108">Return value</span></span>

<span data-ttu-id="43c38-109">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="43c38-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="43c38-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="43c38-110">Return code</span></span>                                                                                           | <span data-ttu-id="43c38-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43c38-111">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="43c38-112"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="43c38-112"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="43c38-113">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="43c38-113">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="43c38-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="43c38-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="43c38-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="43c38-115">Success.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="43c38-116"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="43c38-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="43c38-117">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="43c38-117">The operation cannot be performed because the pins are not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43c38-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="43c38-118">Remarks</span></span>

<span data-ttu-id="43c38-119">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="43c38-119">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="43c38-120">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="43c38-120">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="43c38-121">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="43c38-121">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="43c38-122">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="43c38-122">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="43c38-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43c38-123">Requirements</span></span>



| <span data-ttu-id="43c38-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43c38-124">Requirement</span></span> | <span data-ttu-id="43c38-125">Valore</span><span class="sxs-lookup"><span data-stu-id="43c38-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c38-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43c38-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43c38-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43c38-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43c38-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="43c38-128">Library</span></span><br/> | <dl> <span data-ttu-id="43c38-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="43c38-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c38-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43c38-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c38-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="43c38-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




