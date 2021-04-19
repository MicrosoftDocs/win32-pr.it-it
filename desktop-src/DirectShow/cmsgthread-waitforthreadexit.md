---
description: Si blocca fino alla chiusura del thread.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Metodo CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330220"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a><span data-ttu-id="b7908-103">CMsgThread. WaitForThreadExit, metodo</span><span class="sxs-lookup"><span data-stu-id="b7908-103">CMsgThread.WaitForThreadExit method</span></span>

<span data-ttu-id="b7908-104">Si blocca fino alla chiusura del thread.</span><span class="sxs-lookup"><span data-stu-id="b7908-104">Blocks until the thread exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7908-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7908-105">Syntax</span></span>


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a><span data-ttu-id="b7908-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7908-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7908-107">*lpdwExitCode*</span><span class="sxs-lookup"><span data-stu-id="b7908-107">*lpdwExitCode*</span></span> 
</dt> <dd>

<span data-ttu-id="b7908-108">Puntatore al codice di uscita restituito dal thread.</span><span class="sxs-lookup"><span data-stu-id="b7908-108">Pointer to the exit code returned by the thread.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7908-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7908-109">Return value</span></span>

<span data-ttu-id="b7908-110">Restituisce **true** o **false**, il cui significato è determinato dalla classe che fornisce la funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) sottoposta a override e la funzione membro chiamante.</span><span class="sxs-lookup"><span data-stu-id="b7908-110">Returns either **TRUE** or **FALSE**, the meaning of which is determined by the class supplying the overridden [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function and the calling member function.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7908-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7908-111">Remarks</span></span>

<span data-ttu-id="b7908-112">Verificare che il thread di lavoro sia stato chiuso completamente prima di completare la distruzione della classe derivata; in caso contrario, il thread potrebbe essere ancora eseguito dopo che la libreria di collegamento dinamico (DLL) è stata scaricata dallo spazio degli indirizzi del processo.</span><span class="sxs-lookup"><span data-stu-id="b7908-112">Ensure that the worker thread has exited completely before completing the destruction of your derived class; otherwise, the thread might still execute after your dynamic-link library (DLL) has been unloaded from the address space of the process.</span></span> <span data-ttu-id="b7908-113">Anche se l'unica istruzione lasciata per uscire è un'istruzione a singolo ritorno, si verificherà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="b7908-113">Even if the only instruction left to exit is a single-return instruction, this would cause an exception.</span></span> <span data-ttu-id="b7908-114">L'unico modo affidabile per assicurarsi che il thread sia stato terminato consiste nel segnalare al thread di uscire (usando un oggetto [**CMsg**](cmsg.md) negoziato privatamente inviato alla funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e quindi chiamare questa funzione membro.</span><span class="sxs-lookup"><span data-stu-id="b7908-114">The only reliable way to ensure that the thread has exited is to signal the thread to exit (using a privately negotiated [**CMsg**](cmsg.md) object sent to the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then call this member function.</span></span> <span data-ttu-id="b7908-115">Questa operazione deve essere eseguita nel distruttore per la classe derivata.</span><span class="sxs-lookup"><span data-stu-id="b7908-115">You should do this in the destructor for your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7908-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7908-116">Requirements</span></span>



| <span data-ttu-id="b7908-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7908-117">Requirement</span></span> | <span data-ttu-id="b7908-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b7908-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7908-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7908-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b7908-120"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b7908-120"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b7908-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7908-121">Library</span></span><br/> | <dl> <span data-ttu-id="b7908-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b7908-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7908-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7908-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7908-124">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="b7908-124">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




