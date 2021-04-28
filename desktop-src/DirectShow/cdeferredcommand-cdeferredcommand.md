---
description: Costruttore CDeferredCommand.CDeferredCommand - Metodo costruttore.
ms.assetid: 0b372fa2-78a9-4e38-813c-f18123716c6d
title: Costruttore CDeferredCommand.CDeferredCommand (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.CDeferredCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a10d8bba48902ed2d6fd66da8483cea1ba9aacc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119789"
---
# <a name="cdeferredcommandcdeferredcommand-constructor"></a><span data-ttu-id="8fb44-103">Costruttore CDeferredCommand.CDeferredCommand</span><span class="sxs-lookup"><span data-stu-id="8fb44-103">CDeferredCommand.CDeferredCommand constructor</span></span>

<span data-ttu-id="8fb44-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="8fb44-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb44-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fb44-105">Syntax</span></span>


```C++
CDeferredCommand(
   CCmdQueue *pQ,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   LPUNKNOWN pUnkExecutor,
   REFTIME   time,
   GUID      *iid,
   long      dispidMethod,
   short     wFlags,
   long      cArgs,
   VARIANT   *pDispParams,
   VARIANT   *pvarResult,
   short     *puArgErr,
   BOOL      bStream
);
```



## <a name="parameters"></a><span data-ttu-id="8fb44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fb44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb44-107">*Pq*</span><span class="sxs-lookup"><span data-stu-id="8fb44-107">*pQ*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-108">Puntatore a un oggetto che espone [**l'interfaccia IQueueCommand.**](/windows/desktop/api/Control/nn-control-iqueuecommand)</span><span class="sxs-lookup"><span data-stu-id="8fb44-108">Pointer to an object that exposes the [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="8fb44-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-110">Puntatore all'interfaccia **IUnknown esterna** per l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="8fb44-110">Pointer to the outer **IUnknown** interface for aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="8fb44-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-112">Puntatore a un valore **HRESULT** restituito.</span><span class="sxs-lookup"><span data-stu-id="8fb44-112">Pointer to a returned **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-113">*pUnkExecutor*</span><span class="sxs-lookup"><span data-stu-id="8fb44-113">*pUnkExecutor*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-114">Puntatore all'oggetto che eseererà questo comando.</span><span class="sxs-lookup"><span data-stu-id="8fb44-114">Pointer to the object that will carry out this command.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-115">*time*</span><span class="sxs-lookup"><span data-stu-id="8fb44-115">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-116">Ora in cui verrà eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="8fb44-116">Time at which the command will be run.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-117">*Iid*</span><span class="sxs-lookup"><span data-stu-id="8fb44-117">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-118">Puntatore all'identificatore univoco globale **(GUID)** dell'interfaccia che contiene il metodo.</span><span class="sxs-lookup"><span data-stu-id="8fb44-118">Pointer to the globally unique identifier (**GUID**) of the interface that contains the method.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-119">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="8fb44-119">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-120">Metodo sull'interfaccia da chiamare.</span><span class="sxs-lookup"><span data-stu-id="8fb44-120">Method on the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-121">*Wflags*</span><span class="sxs-lookup"><span data-stu-id="8fb44-121">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-122">Contesto della chiamata.</span><span class="sxs-lookup"><span data-stu-id="8fb44-122">Context of the invocation.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-123">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="8fb44-123">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-124">Numero di argomenti passati.</span><span class="sxs-lookup"><span data-stu-id="8fb44-124">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-125">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="8fb44-125">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-126">Puntatore a un elenco di tipi varianti di argomento.</span><span class="sxs-lookup"><span data-stu-id="8fb44-126">Pointer to a list of argument variant types.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-127">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="8fb44-127">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-128">Puntatore a un elenco di tipi variant restituito, se presente.</span><span class="sxs-lookup"><span data-stu-id="8fb44-128">Pointer to a returned variant type list, if any.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-129">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="8fb44-129">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-130">Puntatore all'ultimo argomento *nell'elenco di parametri pDispParams* con un errore.</span><span class="sxs-lookup"><span data-stu-id="8fb44-130">Pointer to the last argument in the *pDispParams* parameter list with an error.</span></span>

</dd> <dt>

<span data-ttu-id="8fb44-131">*bStream*</span><span class="sxs-lookup"><span data-stu-id="8fb44-131">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="8fb44-132">Valore che indica se l'ora del comando posticipato è nel tempo di flusso (**TRUE**) o nell'ora di presentazione **(FALSE).**</span><span class="sxs-lookup"><span data-stu-id="8fb44-132">Value indicating whether the deferred command time is in stream time (**TRUE**) or presentation time (**FALSE**).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fb44-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8fb44-133">Requirements</span></span>



| <span data-ttu-id="8fb44-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fb44-134">Requirement</span></span> | <span data-ttu-id="8fb44-135">Valore</span><span class="sxs-lookup"><span data-stu-id="8fb44-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fb44-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8fb44-136">Header</span></span><br/>  | <dl> <span data-ttu-id="8fb44-137"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fb44-137"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8fb44-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="8fb44-138">Library</span></span><br/> | <dl> <span data-ttu-id="8fb44-139"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8fb44-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fb44-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fb44-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb44-141">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="8fb44-141">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




