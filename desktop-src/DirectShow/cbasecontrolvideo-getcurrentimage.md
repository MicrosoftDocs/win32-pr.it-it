---
description: Il metodo GetCurrentImage recupera una copia dell'immagine corrente nel renderer.
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: Metodo CBaseControlVideo. GetCurrentImage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333802"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="9e3e4-103">CBaseControlVideo. GetCurrentImage, metodo</span><span class="sxs-lookup"><span data-stu-id="9e3e4-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="9e3e4-104">Il `GetCurrentImage` metodo recupera una copia dell'immagine corrente nel renderer.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e3e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e3e4-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="9e3e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e3e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e3e4-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="9e3e4-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9e3e4-108">Puntatore alla dimensione del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9e3e4-109">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="9e3e4-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="9e3e4-110">Puntatore al buffer di output per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e3e4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e3e4-111">Return value</span></span>

<span data-ttu-id="9e3e4-112">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="9e3e4-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9e3e4-113">Return code</span></span>                                                                                        | <span data-ttu-id="9e3e4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e3e4-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e3e4-115"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="9e3e4-116">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9e3e4-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="9e3e4-118">Argomento non valido.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="9e3e4-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="9e3e4-120">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-120">Out of memory.</span></span> <span data-ttu-id="9e3e4-121">Restituito quando il parametro *pVideoInfo* è **null**.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="9e3e4-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="9e3e4-123">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="9e3e4-124"><dt>**VFW \_ E \_ non \_ sospeso**</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="9e3e4-125">Non è stato possibile eseguire l'operazione perché il filtro non è sospeso.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e3e4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e3e4-126">Remarks</span></span>

<span data-ttu-id="9e3e4-127">Questa funzione membro recupera l'immagine dall'esempio e la copia nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="9e3e4-128">La sezione del video copiato nel buffer di output riflette il rettangolo di origine impostato tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="9e3e4-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="9e3e4-129">Non riflette il rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9e3e4-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e3e4-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e3e4-130">Requirements</span></span>



| <span data-ttu-id="9e3e4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e3e4-131">Requirement</span></span> | <span data-ttu-id="9e3e4-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9e3e4-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e3e4-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e3e4-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9e3e4-134"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e3e4-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e3e4-135">Library</span></span><br/> | <dl> <span data-ttu-id="9e3e4-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9e3e4-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e3e4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e3e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e3e4-138">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="9e3e4-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




