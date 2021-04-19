---
description: Il metodo CheckStreamState determina se un campione multimediale deve essere recapitato o rimosso.
ms.assetid: 1533f4b9-e13e-458b-9614-96d733cef4ed
title: Metodo CBaseStreamControl. CheckStreamState (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CheckStreamState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e469e288e853ca88a0cf15c209882a8114e33509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326565"
---
# <a name="cbasestreamcontrolcheckstreamstate-method"></a><span data-ttu-id="6d7cc-103">CBaseStreamControl. CheckStreamState, metodo</span><span class="sxs-lookup"><span data-stu-id="6d7cc-103">CBaseStreamControl.CheckStreamState method</span></span>

<span data-ttu-id="6d7cc-104">Il `CheckStreamState` metodo determina se un campione multimediale deve essere recapitato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-104">The `CheckStreamState` method determines whether a media sample should be delivered or discarded.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d7cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d7cc-105">Syntax</span></span>


```C++
enum CheckStreamState(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="6d7cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d7cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d7cc-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="6d7cc-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="6d7cc-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d7cc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d7cc-109">Return value</span></span>

<span data-ttu-id="6d7cc-110">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-110">Returns one of the following values.</span></span>



| <span data-ttu-id="6d7cc-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6d7cc-111">Return code</span></span>                                                                                       | <span data-ttu-id="6d7cc-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d7cc-112">Description</span></span>                     |
|---------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="6d7cc-113"><dt>**ELIMINAZIONE di flussi \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cc-113"><dt>**STREAM\_DISCARDING**</dt></span></span> </dl> | <span data-ttu-id="6d7cc-114">Rimuovere l'esempio.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-114">Discard this sample.</span></span><br/> |
| <dl> <span data-ttu-id="6d7cc-115"><dt>**flusso di flusso \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cc-115"><dt>**STREAM\_FLOWING**</dt></span></span> </dl>    | <span data-ttu-id="6d7cc-116">Fornire questo esempio.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-116">Deliver this sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d7cc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d7cc-117">Remarks</span></span>

<span data-ttu-id="6d7cc-118">Chiamare questo metodo quando il pin riceve un campione.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-118">Call this method when your pin receives a sample.</span></span> <span data-ttu-id="6d7cc-119">Recapitare l'esempio solo se il valore restituito è flusso di flusso \_ .</span><span class="sxs-lookup"><span data-stu-id="6d7cc-119">Deliver the sample only if the return value is STREAM\_FLOWING.</span></span> <span data-ttu-id="6d7cc-120">Se il valore restituito è il flusso che viene \_ ignorato, eliminare l'esempio.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-120">If the return value is STREAM\_DISCARDING, discard the sample.</span></span>

<span data-ttu-id="6d7cc-121">Se il pin Elimina tutti gli esempi, deve contrassegnare l'esempio successivo che recapita come discontinuità, chiamando il metodo [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="6d7cc-121">If the pin discards any samples, it should mark the next sample that it delivers as a discontinuity, by calling the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="6d7cc-122">Se il filtro implementa l'interfaccia [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) per contare il numero di frame eliminati, non contare un frame scartato come frame eliminato.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-122">If your filter implements the [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes) interface to count how many frames it drops, do not count a discarded frame as a dropped frame.</span></span>

<span data-ttu-id="6d7cc-123">Quando il valore restituito è il flusso che viene \_ ignorato, il metodo si blocca fino a quando non viene raggiunta l'ora di inizio del campione.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-123">When the return value is STREAM\_DISCARDING, the method blocks until the reference time reaches the sample's start time.</span></span> <span data-ttu-id="6d7cc-124">In questo modo si impedisce al pin di ignorare troppo rapidamente i campioni.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-124">This prevents your pin from discarding samples too quickly.</span></span> <span data-ttu-id="6d7cc-125">Se il filtro è sospeso, il tempo di attesa è infinito, fino a quando il filtro non viene eseguito, interrompe o Scarica i dati.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-125">If the filter is paused, the wait time is infinite, until the filter runs, stops, or flushes data.</span></span> <span data-ttu-id="6d7cc-126">(Le modifiche allo stato del filtro e lo streaming avvengono su thread separati, quindi non viene generato alcun deadlock).</span><span class="sxs-lookup"><span data-stu-id="6d7cc-126">(Filter state changes and streaming happen on separate threads, so this does not cause any deadlock.)</span></span>

<span data-ttu-id="6d7cc-127">L'enumerazione **CBaseStreamControl:: StreamControlState** viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="6d7cc-127">The **CBaseStreamControl::StreamControlState** enumeration is defined as follows:</span></span>


```C++
enum StreamControlState{ 
    STREAM_FLOWING = 0x1000,
    STREAM_DISCARDING
};
```



## <a name="examples"></a><span data-ttu-id="6d7cc-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="6d7cc-128">Examples</span></span>

<span data-ttu-id="6d7cc-129">Nell'esempio seguente si presuppone che il pin usi una variabile membro denominata m \_ fLastSampleDiscarded per tenere traccia delle discontinuità.</span><span class="sxs-lookup"><span data-stu-id="6d7cc-129">The following example assumes that the pin uses a member variable named m\_fLastSampleDiscarded to keep track of discontinuities.</span></span>


```C++
CMyPin::Receive(IMediaSample *pSample)
{
    if (!pSample) return E_POINTER;

    int iStreamState = CheckStreamState(pSample);
    if (iStreamState == STREAM_FLOWING) 
    {
        if (m_fLastSampleDiscarded)
            pSample->SetDiscontinuity(TRUE);
        m_fLastSampleDiscarded = FALSE;
        /* Deliver the sample. */
    } 
    else 
    {
        m_fLastSampleDiscarded = TRUE;  
       // Discard this sample. Do not deliver it.
    }
}
```



## <a name="requirements"></a><span data-ttu-id="6d7cc-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d7cc-130">Requirements</span></span>



| <span data-ttu-id="6d7cc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d7cc-131">Requirement</span></span> | <span data-ttu-id="6d7cc-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6d7cc-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d7cc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d7cc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="6d7cc-134"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cc-134"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6d7cc-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d7cc-135">Library</span></span><br/> | <dl> <span data-ttu-id="6d7cc-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6d7cc-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d7cc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d7cc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d7cc-138">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="6d7cc-138">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




