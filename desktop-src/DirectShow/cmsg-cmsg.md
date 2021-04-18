---
description: Costruisce un oggetto CMsg.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: Costruttore CMsg. CMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328839"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="8c0e5-103">Costruttore CMsg. CMsg</span><span class="sxs-lookup"><span data-stu-id="8c0e5-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="8c0e5-104">Costruisce un oggetto [**CMsg**](cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="8c0e5-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c0e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c0e5-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="8c0e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c0e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c0e5-107">*u*</span><span class="sxs-lookup"><span data-stu-id="8c0e5-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0e5-108">Codice della richiesta, definito dal client della classe thread e riconosciuto dalla funzione thread di lavoro sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="8c0e5-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="8c0e5-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0e5-110">Parametro del flag per il codice della richiesta.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="8c0e5-111">*LP*</span><span class="sxs-lookup"><span data-stu-id="8c0e5-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0e5-112">Puntatore ai dati richiesti dal thread di lavoro come parametri o valori restituiti.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="8c0e5-113">Questi dati non devono essere basati su stack, in quanto verrà fatto riferimento a un po' di tempo dopo il completamento dell'operazione di Accodamento.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="8c0e5-114">*pEvent*</span><span class="sxs-lookup"><span data-stu-id="8c0e5-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="8c0e5-115">Puntatore all'oggetto evento che un thread di lavoro può segnalare per indicare il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c0e5-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c0e5-116">Remarks</span></span>

<span data-ttu-id="8c0e5-117">Questa funzione membro contiene una richiesta di intervento di un thread di lavoro di [**CMsgThread**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="8c0e5-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="8c0e5-118">Tutti i parametri vengono passati alla funzione thread di lavoro come parametri quando il messaggio viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="8c0e5-119">I significati dei parametri sono definiti dalla funzione client che chiama il thread di lavoro e la classe derivata che fornisce la funzione di esecuzione del thread di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8c0e5-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c0e5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c0e5-120">Requirements</span></span>



| <span data-ttu-id="8c0e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c0e5-121">Requirement</span></span> | <span data-ttu-id="8c0e5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8c0e5-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c0e5-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c0e5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8c0e5-124"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c0e5-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8c0e5-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c0e5-125">Library</span></span><br/> | <dl> <span data-ttu-id="8c0e5-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8c0e5-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




