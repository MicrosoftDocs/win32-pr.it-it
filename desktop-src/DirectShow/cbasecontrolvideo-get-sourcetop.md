---
description: Il \_ metodo Get SourceTop recupera la coordinata superiore del rettangolo di origine corrente.
ms.assetid: 78dbd1e6-f591-487e-b9fe-fcbda55f5338
title: Metodo CBaseControlVideo.get_SourceTop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceTop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1c2a2a90b441571a23bfa4210002b352e388a98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327560"
---
# <a name="cbasecontrolvideoget_sourcetop-method"></a><span data-ttu-id="d3d38-103">Metodo CBaseControlVideo. Get \_ SourceTop</span><span class="sxs-lookup"><span data-stu-id="d3d38-103">CBaseControlVideo.get\_SourceTop method</span></span>

<span data-ttu-id="d3d38-104">Il `get_SourceTop` metodo recupera la coordinata superiore del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="d3d38-104">The `get_SourceTop` method retrieves the top coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3d38-105">Syntax</span></span>


```C++
HRESULT get_SourceTop(
   long *pSourceTop
);
```



## <a name="parameters"></a><span data-ttu-id="d3d38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3d38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d38-107">*pSourceTop*</span><span class="sxs-lookup"><span data-stu-id="d3d38-107">*pSourceTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d3d38-108">Puntatore alla coordinata superiore del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="d3d38-108">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d38-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3d38-109">Return value</span></span>

<span data-ttu-id="d3d38-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="d3d38-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="d3d38-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d3d38-111">Return code</span></span>                                                                                           | <span data-ttu-id="d3d38-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3d38-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3d38-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="d3d38-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d3d38-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d3d38-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="d3d38-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d3d38-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d3d38-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d3d38-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="d3d38-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d3d38-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="d3d38-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d3d38-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d3d38-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3d38-121">Remarks</span></span>

<span data-ttu-id="d3d38-122">Questa funzione membro implementa il metodo [**IBasicVideo:: Get \_ SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) .</span><span class="sxs-lookup"><span data-stu-id="d3d38-122">This member function implements the [**IBasicVideo::get\_SourceTop**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcetop) method.</span></span>

<span data-ttu-id="d3d38-123">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="d3d38-123">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="d3d38-124">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="d3d38-124">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="d3d38-125">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d3d38-125">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="d3d38-126">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="d3d38-126">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3d38-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3d38-127">Requirements</span></span>



| <span data-ttu-id="d3d38-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d38-128">Requirement</span></span> | <span data-ttu-id="d3d38-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d3d38-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d38-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3d38-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d3d38-131"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3d38-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d3d38-132">Library</span></span><br/> | <dl> <span data-ttu-id="d3d38-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d3d38-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3d38-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3d38-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d38-135">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d3d38-135">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




