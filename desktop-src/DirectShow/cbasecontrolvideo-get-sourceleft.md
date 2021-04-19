---
description: Il \_ metodo Get SourceLeft recupera la coordinata sinistra del rettangolo di origine corrente.
ms.assetid: dbfb1850-6e49-481c-b26a-22ccb9e4455a
title: Metodo CBaseControlVideo.get_SourceLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2b7ff62617b9fa378511dba2838f0dcbdb25dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327562"
---
# <a name="cbasecontrolvideoget_sourceleft-method"></a><span data-ttu-id="34b61-103">Metodo CBaseControlVideo. Get \_ SourceLeft</span><span class="sxs-lookup"><span data-stu-id="34b61-103">CBaseControlVideo.get\_SourceLeft method</span></span>

<span data-ttu-id="34b61-104">Il `get_SourceLeft` metodo recupera la coordinata sinistra del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="34b61-104">The `get_SourceLeft` method retrieves the left coordinate of the current source rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="34b61-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34b61-105">Syntax</span></span>


```C++
HRESULT get_SourceLeft(
   long *pSourceLeft
);
```



## <a name="parameters"></a><span data-ttu-id="34b61-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34b61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b61-107">*pSourceLeft*</span><span class="sxs-lookup"><span data-stu-id="34b61-107">*pSourceLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="34b61-108">Puntatore alla coordinata sinistra del rettangolo di origine corrente.</span><span class="sxs-lookup"><span data-stu-id="34b61-108">Pointer to the left coordinate of the current source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34b61-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34b61-109">Return value</span></span>

<span data-ttu-id="34b61-110">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="34b61-110">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="34b61-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="34b61-111">Return code</span></span>                                                                                           | <span data-ttu-id="34b61-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34b61-112">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34b61-113"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-113"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="34b61-114">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="34b61-114">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="34b61-115"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-115"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="34b61-116">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="34b61-116">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="34b61-117"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="34b61-118">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="34b61-118">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="34b61-119"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-119"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="34b61-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="34b61-120">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="34b61-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="34b61-121">Remarks</span></span>

<span data-ttu-id="34b61-122">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="34b61-122">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="34b61-123">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="34b61-123">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="34b61-124">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="34b61-124">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="34b61-125">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="34b61-125">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="34b61-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34b61-126">Requirements</span></span>



| <span data-ttu-id="34b61-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b61-127">Requirement</span></span> | <span data-ttu-id="34b61-128">Valore</span><span class="sxs-lookup"><span data-stu-id="34b61-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b61-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34b61-129">Header</span></span><br/>  | <dl> <span data-ttu-id="34b61-130"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34b61-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="34b61-131">Library</span></span><br/> | <dl> <span data-ttu-id="34b61-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34b61-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b61-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34b61-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b61-134">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="34b61-134">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




