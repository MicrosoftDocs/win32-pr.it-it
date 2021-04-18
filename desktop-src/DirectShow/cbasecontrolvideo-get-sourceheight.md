---
description: Il \_ metodo Get SourceHeight recupera l'altezza del rettangolo di origine corrente.
ms.assetid: bf727cf6-9143-41f0-a482-782a4178ea92
title: Metodo CBaseControlVideo.get_SourceHeight (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b724f63907c8372867095b059ff728b4c646df21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327563"
---
# <a name="cbasecontrolvideoget_sourceheight-method"></a><span data-ttu-id="124ec-103">Metodo CBaseControlVideo. Get \_ SourceHeight</span><span class="sxs-lookup"><span data-stu-id="124ec-103">CBaseControlVideo.get\_SourceHeight method</span></span>

<span data-ttu-id="124ec-104">Il `get_SourceHeight` metodo recupera l'altezza del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="124ec-104">The `get_SourceHeight` method retrieves the height of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="124ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="124ec-105">Syntax</span></span>


```C++
HRESULT get_SourceHeight(
   long *pSourceHeight
);
```



## <a name="parameters"></a><span data-ttu-id="124ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="124ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="124ec-107">*pSourceHeight*</span><span class="sxs-lookup"><span data-stu-id="124ec-107">*pSourceHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="124ec-108">Puntatore all'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="124ec-108">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="124ec-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="124ec-109">Return value</span></span>

<span data-ttu-id="124ec-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="124ec-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="124ec-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="124ec-111">Return code</span></span>                                                                                           | <span data-ttu-id="124ec-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="124ec-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="124ec-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="124ec-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="124ec-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="124ec-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="124ec-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="124ec-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="124ec-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="124ec-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="124ec-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="124ec-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="124ec-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="124ec-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="124ec-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="124ec-121">Remarks</span></span>

<span data-ttu-id="124ec-122">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) .</span><span class="sxs-lookup"><span data-stu-id="124ec-122">This member function implements the [**IBasicVideo::get\_SourceHeight**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourceheight) method.</span></span>

<span data-ttu-id="124ec-123">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="124ec-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="124ec-124">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="124ec-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="124ec-125">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="124ec-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="124ec-126">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="124ec-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="124ec-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="124ec-127">Requirements</span></span>



| <span data-ttu-id="124ec-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="124ec-128">Requirement</span></span> | <span data-ttu-id="124ec-129">Valore</span><span class="sxs-lookup"><span data-stu-id="124ec-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="124ec-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="124ec-130">Header</span></span><br/>  | <dl> <span data-ttu-id="124ec-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="124ec-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="124ec-132">Library</span></span><br/> | <dl> <span data-ttu-id="124ec-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="124ec-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="124ec-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="124ec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="124ec-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="124ec-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




