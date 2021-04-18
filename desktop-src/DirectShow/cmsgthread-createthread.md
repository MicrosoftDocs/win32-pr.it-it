---
description: Crea un thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Metodo CMsgThread. CreateThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328834"
---
# <a name="cmsgthreadcreatethread-method"></a><span data-ttu-id="b0817-103">CMsgThread. CreateThread, metodo</span><span class="sxs-lookup"><span data-stu-id="b0817-103">CMsgThread.CreateThread method</span></span>

<span data-ttu-id="b0817-104">Crea un thread.</span><span class="sxs-lookup"><span data-stu-id="b0817-104">Creates a thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0817-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0817-105">Syntax</span></span>


```C++
BOOL CreateThread();
```



## <a name="parameters"></a><span data-ttu-id="b0817-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0817-106">Parameters</span></span>

<span data-ttu-id="b0817-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="b0817-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0817-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0817-108">Return value</span></span>

<span data-ttu-id="b0817-109">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0817-109">Returns one of the following values.</span></span>



| <span data-ttu-id="b0817-110">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b0817-110">Return code</span></span>                                                                              | <span data-ttu-id="b0817-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0817-111">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="b0817-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b0817-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>  | <span data-ttu-id="b0817-113">Creazione thread completata.</span><span class="sxs-lookup"><span data-stu-id="b0817-113">Thread was successfully created.</span></span><br/>     |
| <dl> <span data-ttu-id="b0817-114"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b0817-114"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="b0817-115">Creazione del thread non riuscita.</span><span class="sxs-lookup"><span data-stu-id="b0817-115">Thread was not successfully created.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0817-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0817-116">Remarks</span></span>

<span data-ttu-id="b0817-117">Il thread effettuerà il ciclo, bloccando la coda di una richiesta (tramite la funzione membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e quindi chiamando la funzione membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) con ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="b0817-117">The thread will loop, blocking until a request is queued (through the [**CMsgThread::PutThreadMsg**](cmsgthread-putthreadmsg.md) member function) and then calling the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function with each message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0817-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0817-118">Requirements</span></span>



| <span data-ttu-id="b0817-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0817-119">Requirement</span></span> | <span data-ttu-id="b0817-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b0817-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0817-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0817-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b0817-122"><dt>Msgthrd. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0817-122"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0817-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0817-123">Library</span></span><br/> | <dl> <span data-ttu-id="b0817-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b0817-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0817-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0817-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0817-126">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="b0817-126">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




