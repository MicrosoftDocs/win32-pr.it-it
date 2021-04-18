---
description: Il metodo GetDestinationPosition Recupera il rettangolo di destinazione in un'unica operazione atomica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Metodo CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333801"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a><span data-ttu-id="5a04c-103">CBaseControlVideo. GetDestinationPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="5a04c-103">CBaseControlVideo.GetDestinationPosition method</span></span>

<span data-ttu-id="5a04c-104">Il `GetDestinationPosition` metodo recupera il rettangolo di destinazione in un'unica operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="5a04c-104">The `GetDestinationPosition` method retrieves the destination rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a04c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a04c-105">Syntax</span></span>


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="5a04c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a04c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a04c-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="5a04c-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="5a04c-108">Puntatore alla coordinata sinistra del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a04c-108">Pointer to the left coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5a04c-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="5a04c-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="5a04c-110">Puntatore alla coordinata superiore del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a04c-110">Pointer to the top coordinate of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5a04c-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="5a04c-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="5a04c-112">Puntatore alla larghezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a04c-112">Pointer to the width of the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5a04c-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="5a04c-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="5a04c-114">Puntatore all'altezza del rettangolo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a04c-114">Pointer to the height of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a04c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a04c-115">Return value</span></span>

<span data-ttu-id="5a04c-116">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="5a04c-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="5a04c-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a04c-117">Return code</span></span>                                                                                           | <span data-ttu-id="5a04c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a04c-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a04c-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="5a04c-120">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5a04c-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="5a04c-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="5a04c-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="5a04c-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5a04c-123"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5a04c-124">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="5a04c-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="5a04c-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="5a04c-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a04c-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="5a04c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a04c-127">Remarks</span></span>

<span data-ttu-id="5a04c-128">Questa funzione membro può essere usata al posto di chiamate separate alle funzioni [**membro CBaseControlVideo:: Get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo:: Get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo:: Get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)e [**CBaseControlVideo:: Get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) .</span><span class="sxs-lookup"><span data-stu-id="5a04c-128">This member function can be used in place of separate calls to the [**CBaseControlVideo::get\_DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get\_DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get\_DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md), and [**CBaseControlVideo::get\_DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) member functions.</span></span> <span data-ttu-id="5a04c-129">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="5a04c-129">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="5a04c-130">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="5a04c-130">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="5a04c-131">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5a04c-131">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="5a04c-132">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="5a04c-132">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a04c-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a04c-133">Requirements</span></span>



| <span data-ttu-id="5a04c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a04c-134">Requirement</span></span> | <span data-ttu-id="5a04c-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5a04c-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a04c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a04c-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5a04c-137"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a04c-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="5a04c-138">Library</span></span><br/> | <dl> <span data-ttu-id="5a04c-139"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5a04c-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a04c-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a04c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a04c-141">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="5a04c-141">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




