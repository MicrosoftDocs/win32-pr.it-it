---
description: Il metodo GetSourcePosition recupera la posizione e le dimensioni del rettangolo di origine in un'unica operazione atomica.
ms.assetid: 44356f62-8b14-4b0e-a587-f832adff3bba
title: Metodo CBaseControlVideo. GetSourcePosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourcePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2422845a7b5c64bc07b8e8942b2f19cd10a54d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333799"
---
# <a name="cbasecontrolvideogetsourceposition-method"></a><span data-ttu-id="d03d7-103">CBaseControlVideo. GetSourcePosition, metodo</span><span class="sxs-lookup"><span data-stu-id="d03d7-103">CBaseControlVideo.GetSourcePosition method</span></span>

<span data-ttu-id="d03d7-104">Il `GetSourcePosition` metodo recupera la posizione e le dimensioni del rettangolo di origine in un'unica operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="d03d7-104">The `GetSourcePosition` method retrieves the position and dimensions of the source rectangle in one atomic operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d03d7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d03d7-105">Syntax</span></span>


```C++
HRESULT GetSourcePosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a><span data-ttu-id="d03d7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d03d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d03d7-107">*pLeft*</span><span class="sxs-lookup"><span data-stu-id="d03d7-107">*pLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="d03d7-108">Puntatore alla coordinata sinistra del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="d03d7-108">Pointer to the left coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d03d7-109">*pTop*</span><span class="sxs-lookup"><span data-stu-id="d03d7-109">*pTop*</span></span> 
</dt> <dd>

<span data-ttu-id="d03d7-110">Puntatore alla coordinata superiore del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="d03d7-110">Pointer to the top coordinate of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d03d7-111">*pWidth*</span><span class="sxs-lookup"><span data-stu-id="d03d7-111">*pWidth*</span></span> 
</dt> <dd>

<span data-ttu-id="d03d7-112">Puntatore alla larghezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="d03d7-112">Pointer to the width of the source rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="d03d7-113">*pHeight*</span><span class="sxs-lookup"><span data-stu-id="d03d7-113">*pHeight*</span></span> 
</dt> <dd>

<span data-ttu-id="d03d7-114">Puntatore all'altezza del rettangolo di origine.</span><span class="sxs-lookup"><span data-stu-id="d03d7-114">Pointer to the height of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d03d7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d03d7-115">Return value</span></span>

<span data-ttu-id="d03d7-116">Restituisce un valore **HRESULT** che dipende dall'implementazione di. può essere uno dei valori seguenti oppure altri valori non sono elencati.</span><span class="sxs-lookup"><span data-stu-id="d03d7-116">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="d03d7-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d03d7-117">Return code</span></span>                                                                                           | <span data-ttu-id="d03d7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d03d7-118">Description</span></span>                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d03d7-119"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-119"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="d03d7-120">Esito negativo.</span><span class="sxs-lookup"><span data-stu-id="d03d7-120">Failure.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="d03d7-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-121"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="d03d7-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="d03d7-122">**NULL** pointer argument.</span></span><br/>                                            |
| <dl> <span data-ttu-id="d03d7-123"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-123"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d03d7-124">Impossibile eseguire l'operazione perché i pin non sono connessi.</span><span class="sxs-lookup"><span data-stu-id="d03d7-124">The operation cannot be performed because the pins are not connected.</span></span><br/> |
| <dl> <span data-ttu-id="d03d7-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-125"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="d03d7-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d03d7-126">Success.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d03d7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="d03d7-127">Remarks</span></span>

<span data-ttu-id="d03d7-128">Un'applicazione può modificare i rettangoli di origine e di destinazione per il video tramite l'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="d03d7-128">An application can change the source and destination rectangles for the video through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="d03d7-129">Il rettangolo di origine influiscono sulla sezione dell'origine video nativa che verrà visualizzata nella visualizzazione; il rettangolo di destinazione influiscono sul punto in cui verrà visualizzato il video quando viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="d03d7-129">The source rectangle affects which section of the native video source will appear on the display; the destination rectangle affects where the video will appear when played.</span></span> <span data-ttu-id="d03d7-130">Il rettangolo di destinazione è relativo all'area client della finestra in cui è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d03d7-130">The destination rectangle is relative to the client area of the window in which it is playing.</span></span> <span data-ttu-id="d03d7-131">L'angolo superiore sinistro della finestra è coordinata (0, 0).</span><span class="sxs-lookup"><span data-stu-id="d03d7-131">The upper-left corner of the window is coordinate (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="d03d7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d03d7-132">Requirements</span></span>



| <span data-ttu-id="d03d7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d03d7-133">Requirement</span></span> | <span data-ttu-id="d03d7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d03d7-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d03d7-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d03d7-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d03d7-136"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-136"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d03d7-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="d03d7-137">Library</span></span><br/> | <dl> <span data-ttu-id="d03d7-138"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d03d7-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d03d7-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d03d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03d7-140">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d03d7-140">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




