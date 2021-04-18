---
description: Passa un \_ \_ \_ messaggio di modifica delle dimensioni del video EC al gestore del grafico dei filtri.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Metodo CBaseControlVideo. OnVideoSizeChange (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324493"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a><span data-ttu-id="f0d4d-103">CBaseControlVideo. OnVideoSizeChange, metodo</span><span class="sxs-lookup"><span data-stu-id="f0d4d-103">CBaseControlVideo.OnVideoSizeChange method</span></span>

<span data-ttu-id="f0d4d-104">Passa un \_ \_ \_ messaggio di modifica delle dimensioni del video EC al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-104">Passes an EC\_VIDEO\_SIZE\_CHANGED message to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f0d4d-105">Syntax</span></span>


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a><span data-ttu-id="f0d4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0d4d-106">Parameters</span></span>

<span data-ttu-id="f0d4d-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f0d4d-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0d4d-108">Return value</span></span>

<span data-ttu-id="f0d4d-109">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-109">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="f0d4d-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f0d4d-110">Return code</span></span>                                                                                   | <span data-ttu-id="f0d4d-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f0d4d-111">Description</span></span>               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="f0d4d-112"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d4d-112"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f0d4d-113">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-113">Failure.</span></span><br/>       |
| <dl> <span data-ttu-id="f0d4d-114"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f0d4d-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f0d4d-115">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-115">Out of memory.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f0d4d-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0d4d-116">Remarks</span></span>

<span data-ttu-id="f0d4d-117">Un renderer video deve chiamare questa funzione membro ogni volta che viene modificata la dimensione del video; Questa operazione viene in genere chiamata una volta dopo la connessione iniziale.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-117">A video renderer should call this member function each time the video size is changed; this will typically be called once after initial connection.</span></span> <span data-ttu-id="f0d4d-118">Se il renderer è in grado di supportare le modifiche del formato dinamico (da 320 x 240 a 160 x 120), dovrebbe chiamarlo anche dopo ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="f0d4d-118">If the renderer can support dynamic format changes (from 320 x 240 to 160 x 120), it should also call it after each change.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0d4d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0d4d-119">Requirements</span></span>



| <span data-ttu-id="f0d4d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0d4d-120">Requirement</span></span> | <span data-ttu-id="f0d4d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f0d4d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0d4d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0d4d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f0d4d-123"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0d4d-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f0d4d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="f0d4d-124">Library</span></span><br/> | <dl> <span data-ttu-id="f0d4d-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f0d4d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0d4d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0d4d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0d4d-127">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="f0d4d-127">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




