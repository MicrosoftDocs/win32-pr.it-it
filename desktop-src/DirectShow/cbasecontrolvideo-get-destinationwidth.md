---
description: Il \_ metodo Get DestinationWidth recupera la larghezza del rettangolo di destinazione corrente.
ms.assetid: 7d466d61-1768-48b4-8460-b15d28a294f3
title: Metodo CBaseControlVideo.get_DestinationWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95fc5ccdf0c2b0dd6d198686e12edb3185489b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327565"
---
# <a name="cbasecontrolvideoget_destinationwidth-method"></a><span data-ttu-id="1cab0-103">Metodo CBaseControlVideo. Get \_ DestinationWidth</span><span class="sxs-lookup"><span data-stu-id="1cab0-103">CBaseControlVideo.get\_DestinationWidth method</span></span>

<span data-ttu-id="1cab0-104">Il `get_DestinationWidth` metodo recupera la larghezza del rettangolo di destinazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1cab0-104">The `get_DestinationWidth` method retrieves the width of the current destination rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cab0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cab0-105">Syntax</span></span>


```C++
HRESULT get_DestinationWidth(
   long *pDestinationWidth
);
```



## <a name="parameters"></a><span data-ttu-id="1cab0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cab0-107">*pDestinationWidth*</span><span class="sxs-lookup"><span data-stu-id="1cab0-107">*pDestinationWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="1cab0-108">Puntatore alla larghezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1cab0-108">Pointer to the destination width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cab0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cab0-109">Return value</span></span>

<span data-ttu-id="1cab0-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="1cab0-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1cab0-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1cab0-111">Return code</span></span>                                                                                           | <span data-ttu-id="1cab0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cab0-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cab0-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1cab0-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1cab0-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1cab0-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1cab0-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="1cab0-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1cab0-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1cab0-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="1cab0-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="1cab0-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1cab0-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1cab0-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="1cab0-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cab0-121">Remarks</span></span>

<span data-ttu-id="1cab0-122">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ DestinationWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationwidth) .</span><span class="sxs-lookup"><span data-stu-id="1cab0-122">This member function implements the [**IBasicVideo::get\_DestinationWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationwidth) method.</span></span>

<span data-ttu-id="1cab0-123">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="1cab0-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1cab0-124">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="1cab0-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1cab0-125">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1cab0-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1cab0-126">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="1cab0-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cab0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cab0-127">Requirements</span></span>



| <span data-ttu-id="1cab0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cab0-128">Requirement</span></span> | <span data-ttu-id="1cab0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1cab0-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cab0-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cab0-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1cab0-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1cab0-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cab0-132">Library</span></span><br/> | <dl> <span data-ttu-id="1cab0-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1cab0-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cab0-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cab0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cab0-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1cab0-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




