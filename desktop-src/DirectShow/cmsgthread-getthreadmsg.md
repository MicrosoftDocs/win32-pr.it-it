---
description: Recupera un oggetto CMsg in coda contenente una richiesta.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Metodo CMsgThread. GetThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328829"
---
# <a name="cmsgthreadgetthreadmsg-method"></a><span data-ttu-id="07d81-103">CMsgThread. GetThreadMsg, metodo</span><span class="sxs-lookup"><span data-stu-id="07d81-103">CMsgThread.GetThreadMsg method</span></span>

<span data-ttu-id="07d81-104">Recupera un oggetto [**CMsg**](cmsg.md) in coda contenente una richiesta.</span><span class="sxs-lookup"><span data-stu-id="07d81-104">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d81-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d81-105">Syntax</span></span>


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a><span data-ttu-id="07d81-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d81-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d81-107">*msg*</span><span class="sxs-lookup"><span data-stu-id="07d81-107">*msg*</span></span> 
</dt> <dd>

<span data-ttu-id="07d81-108">Puntatore a un oggetto [**CMsg**](cmsg.md) allocato.</span><span class="sxs-lookup"><span data-stu-id="07d81-108">Pointer to an allocated [**CMsg**](cmsg.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d81-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d81-109">Return value</span></span>

<span data-ttu-id="07d81-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="07d81-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07d81-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="07d81-111">Remarks</span></span>

<span data-ttu-id="07d81-112">Questa funzione membro viene chiamata dalla funzione [**ThreadProc**](camthread-threadproc.md) privata del thread di lavoro per recuperare la funzione membro successiva.</span><span class="sxs-lookup"><span data-stu-id="07d81-112">This member function is called from the worker thread's private [**ThreadProc**](camthread-threadproc.md) function to retrieve the next member function.</span></span> <span data-ttu-id="07d81-113">Il parametro *msg* deve puntare a un oggetto [**CMsg**](cmsg.md) allocato che verrà compilato con i parametri della richiesta successiva nella coda.</span><span class="sxs-lookup"><span data-stu-id="07d81-113">The *msg* parameter should point to an allocated [**CMsg**](cmsg.md) object that will be filled with the parameters to the next request in the queue.</span></span> <span data-ttu-id="07d81-114">Se non sono presenti richieste in coda, questa funzione membro si blocca fino a quando la richiesta successiva non viene accodata (tramite una chiamata alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ).</span><span class="sxs-lookup"><span data-stu-id="07d81-114">If there are no queued requests, this member function blocks until the next request is queued (by a call to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function).</span></span>

## <a name="requirements"></a><span data-ttu-id="07d81-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d81-115">Requirements</span></span>



| <span data-ttu-id="07d81-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d81-116">Requirement</span></span> | <span data-ttu-id="07d81-117">Valore</span><span class="sxs-lookup"><span data-stu-id="07d81-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d81-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07d81-118">Header</span></span><br/>  | <dl> <span data-ttu-id="07d81-119"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07d81-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07d81-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="07d81-120">Library</span></span><br/> | <dl> <span data-ttu-id="07d81-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07d81-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d81-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07d81-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d81-123">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="07d81-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




