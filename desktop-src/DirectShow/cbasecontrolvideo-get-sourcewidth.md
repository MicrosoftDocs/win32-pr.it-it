---
description: Il \_ metodo Get SourceWidth recupera la larghezza del rettangolo di origine corrente.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: Metodo CBaseControlVideo.get_SourceWidth (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60a78fe647ebf488a47907c058962f13790f2538
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327559"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a><span data-ttu-id="1faba-103">Metodo CBaseControlVideo. Get \_ SourceWidth</span><span class="sxs-lookup"><span data-stu-id="1faba-103">CBaseControlVideo.get\_SourceWidth method</span></span>

<span data-ttu-id="1faba-104">Il `get_SourceWidth` metodo recupera la larghezza del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="1faba-104">The `get_SourceWidth` method retrieves the width of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1faba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1faba-105">Syntax</span></span>


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a><span data-ttu-id="1faba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1faba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1faba-107">*pSourceWidth*</span><span class="sxs-lookup"><span data-stu-id="1faba-107">*pSourceWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="1faba-108">Puntatore alla larghezza del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="1faba-108">Pointer to the width of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1faba-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1faba-109">Return value</span></span>

<span data-ttu-id="1faba-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="1faba-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="1faba-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1faba-111">Return code</span></span>                                                                                           | <span data-ttu-id="1faba-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1faba-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1faba-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="1faba-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="1faba-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="1faba-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1faba-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="1faba-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1faba-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1faba-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="1faba-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="1faba-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="1faba-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1faba-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="1faba-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1faba-121">Remarks</span></span>

<span data-ttu-id="1faba-122">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) .</span><span class="sxs-lookup"><span data-stu-id="1faba-122">This member function implements the [**IBasicVideo::get\_SourceWidth**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth) method.</span></span>

<span data-ttu-id="1faba-123">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="1faba-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="1faba-124">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="1faba-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="1faba-125">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="1faba-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="1faba-126">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="1faba-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1faba-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1faba-127">Requirements</span></span>



| <span data-ttu-id="1faba-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1faba-128">Requirement</span></span> | <span data-ttu-id="1faba-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1faba-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faba-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1faba-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1faba-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1faba-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="1faba-132">Library</span></span><br/> | <dl> <span data-ttu-id="1faba-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1faba-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1faba-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1faba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1faba-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="1faba-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




