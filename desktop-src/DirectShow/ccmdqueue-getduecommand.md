---
description: Il metodo GetDueCommand recupera un puntatore al comando successivo che è dovuto a.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: Metodo CCmdQueue. GetDueCommand (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a1297a3f0d514215270acf7e73b18cba46fca1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324481"
---
# <a name="ccmdqueuegetduecommand-method"></a><span data-ttu-id="a2c27-103">CCmdQueue. GetDueCommand, metodo</span><span class="sxs-lookup"><span data-stu-id="a2c27-103">CCmdQueue.GetDueCommand method</span></span>

<span data-ttu-id="a2c27-104">Il `GetDueCommand` metodo recupera un puntatore al comando successivo che è dovuto a.</span><span class="sxs-lookup"><span data-stu-id="a2c27-104">The `GetDueCommand` method retrieves a pointer to the next command that is due.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c27-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2c27-105">Syntax</span></span>


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="a2c27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2c27-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="a2c27-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c27-108">Indirizzo di un puntatore al comando posticipato.</span><span class="sxs-lookup"><span data-stu-id="a2c27-108">Address of a pointer to the deferred command.</span></span>

</dd> <dt>

<span data-ttu-id="a2c27-109">*msTimeout*</span><span class="sxs-lookup"><span data-stu-id="a2c27-109">*msTimeout*</span></span> 
</dt> <dd>

<span data-ttu-id="a2c27-110">Tempo di attesa prima dell'esecuzione del timeout.</span><span class="sxs-lookup"><span data-stu-id="a2c27-110">Amount of time to wait before carrying out the time-out.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2c27-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2c27-111">Return value</span></span>

<span data-ttu-id="a2c27-112">Restituisce E \_ Interrompi se si verifica un timeout.</span><span class="sxs-lookup"><span data-stu-id="a2c27-112">Returns E\_ABORT if a time-out occurs.</span></span> <span data-ttu-id="a2c27-113">Restituisce \_ OK se ha esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a2c27-113">Returns S\_OK if successful; otherwise, returns an error.</span></span> <span data-ttu-id="a2c27-114">Restituisce un oggetto che è stato incrementato utilizzando **IUnknown:: AddRef**.</span><span class="sxs-lookup"><span data-stu-id="a2c27-114">Returns an object that has been incremented using **IUnknown::AddRef**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2c27-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2c27-115">Remarks</span></span>

<span data-ttu-id="a2c27-116">Questa funzione membro si blocca fino a quando non è previsto un comando in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a2c27-116">This member function blocks until a pending command is due.</span></span> <span data-ttu-id="a2c27-117">La funzione membro blocca per la quantità di tempo, in millisecondi, specificata nel parametro *msTimeout* .</span><span class="sxs-lookup"><span data-stu-id="a2c27-117">The member function blocks for the amount of time, in milliseconds, specified in the *msTimeout* parameter.</span></span> <span data-ttu-id="a2c27-118">I comandi in fase di flusso diventano dovuti solo tra le funzioni membro [**CCmdQueue:: Run**](ccmdqueue-run.md) e [**CCmdQueue:: EndRun**](ccmdqueue-endrun.md) .</span><span class="sxs-lookup"><span data-stu-id="a2c27-118">Stream-time commands become due only between the [**CCmdQueue::Run**](ccmdqueue-run.md) and [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) member functions.</span></span> <span data-ttu-id="a2c27-119">Il comando rimane in coda fino a quando non viene eseguito o annullato.</span><span class="sxs-lookup"><span data-stu-id="a2c27-119">The command remains queued until run or canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2c27-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2c27-120">Requirements</span></span>



| <span data-ttu-id="a2c27-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c27-121">Requirement</span></span> | <span data-ttu-id="a2c27-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a2c27-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c27-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2c27-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a2c27-124"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c27-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2c27-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a2c27-125">Library</span></span><br/> | <dl> <span data-ttu-id="a2c27-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c27-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c27-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2c27-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c27-128">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="a2c27-128">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




