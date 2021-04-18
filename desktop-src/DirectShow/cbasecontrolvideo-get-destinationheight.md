---
description: Il \_ metodo Get DestinationHeight recupera l'altezza del rettangolo di destinazione corrente.
ms.assetid: 0001d98a-3a5c-47f1-8f5e-ce464d64131a
title: Metodo CBaseControlVideo.get_DestinationHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9dc4fc63e63adbc42b75ae9a24d1c47e7d985c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327568"
---
# <a name="cbasecontrolvideoget_destinationheight-method"></a><span data-ttu-id="23e1d-103">Metodo CBaseControlVideo. Get \_ DestinationHeight</span><span class="sxs-lookup"><span data-stu-id="23e1d-103">CBaseControlVideo.get\_DestinationHeight method</span></span>

<span data-ttu-id="23e1d-104">Il `get_DestinationHeight` metodo recupera l'altezza del rettangolo di destinazione corrente.</span><span class="sxs-lookup"><span data-stu-id="23e1d-104">The `get_DestinationHeight` method retrieves the current destination rectangle height.</span></span>

## <a name="syntax"></a><span data-ttu-id="23e1d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23e1d-105">Syntax</span></span>


```C++
HRESULT get_DestinationHeight(
   long *pDestinationHeight
);
```



## <a name="parameters"></a><span data-ttu-id="23e1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23e1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e1d-107">*pDestinationHeight*</span><span class="sxs-lookup"><span data-stu-id="23e1d-107">*pDestinationHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="23e1d-108">Puntatore all'altezza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="23e1d-108">Pointer to the destination height.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e1d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23e1d-109">Return value</span></span>

<span data-ttu-id="23e1d-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="23e1d-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="23e1d-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="23e1d-111">Return code</span></span>                                                                                           | <span data-ttu-id="23e1d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23e1d-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23e1d-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="23e1d-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="23e1d-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="23e1d-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="23e1d-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="23e1d-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="23e1d-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="23e1d-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="23e1d-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="23e1d-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="23e1d-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="23e1d-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="23e1d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="23e1d-121">Remarks</span></span>

<span data-ttu-id="23e1d-122">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) .</span><span class="sxs-lookup"><span data-stu-id="23e1d-122">This member function implements the [**IBasicVideo::get\_DestinationHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationheight) method.</span></span>

<span data-ttu-id="23e1d-123">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="23e1d-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="23e1d-124">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sulla posizione in cui verrà riprodotto.</span><span class="sxs-lookup"><span data-stu-id="23e1d-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where it will be played.</span></span> <span data-ttu-id="23e1d-125">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="23e1d-125">The destination rectangle is relative to the client area of the window that it is playing in.</span></span> <span data-ttu-id="23e1d-126">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="23e1d-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="23e1d-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23e1d-127">Requirements</span></span>



| <span data-ttu-id="23e1d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e1d-128">Requirement</span></span> | <span data-ttu-id="23e1d-129">Valore</span><span class="sxs-lookup"><span data-stu-id="23e1d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23e1d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23e1d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="23e1d-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="23e1d-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="23e1d-132">Library</span></span><br/> | <dl> <span data-ttu-id="23e1d-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23e1d-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23e1d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23e1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23e1d-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="23e1d-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




