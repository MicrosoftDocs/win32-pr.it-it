---
description: Il metodo Start avvia un'acquisizione.
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'Metodo IStats:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d58821ecc06e0a25d6a260bb2ba9393162dcdca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879678"
---
# <a name="istatsstart-method"></a><span data-ttu-id="a2fdb-103">IStats:: Start (metodo)</span><span class="sxs-lookup"><span data-stu-id="a2fdb-103">IStats::Start method</span></span>

<span data-ttu-id="a2fdb-104">Il metodo **Start** avvia un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-104">The **Start** method starts a capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2fdb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2fdb-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="a2fdb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a2fdb-106">Parameters</span></span>

<span data-ttu-id="a2fdb-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2fdb-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a2fdb-108">Return value</span></span>

<span data-ttu-id="a2fdb-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a2fdb-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2fdb-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a2fdb-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a2fdb-111">Return code</span></span>                                                                                            | <span data-ttu-id="a2fdb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2fdb-112">Description</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2fdb-113"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="a2fdb-114">L'acquisizione è stata sospesa e deve essere arrestata prima di poter essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-114">The capture has paused and must be stopped before it can be restarted.</span></span> <span data-ttu-id="a2fdb-115">Chiamare il metodo [IStats:: Stop](istats-stop.md) per arrestare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-115">Call the [IStats::Stop](istats-stop.md) method to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="a2fdb-116"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="a2fdb-117">Acquisizione già avviata.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-117">The capture has already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="a2fdb-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="a2fdb-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="a2fdb-120">Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/>           |
| <dl> <span data-ttu-id="a2fdb-121"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="a2fdb-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="a2fdb-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="a2fdb-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2fdb-123">Remarks</span></span>

<span data-ttu-id="a2fdb-124">Quando si riavvia l'acquisizione usando i metodi IStats:: Start e [IStats:: Stop](istats-stop.md) , è necessario chiamare il metodo [IStats:: Configure](istats-configure.md) per riconfigurare la connessione ogni volta che si chiama IStats:: Start per riavviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-124">When restarting the capture by using the IStats::Start and [IStats::Stop](istats-stop.md) methods, you must call the [IStats::Configure](istats-configure.md) method to reconfigure the connection each time you call IStats::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="a2fdb-125">È anche possibile avviare e arrestare l'acquisizione usando i metodi [IStats::P ause](istats-pause.md) e [IStats:: Resume](istats-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="a2fdb-125">You can also start and stop the capture by using the [IStats::Pause](istats-pause.md) and [IStats::Resume](istats-resume.md) methods.</span></span> <span data-ttu-id="a2fdb-126">Quando si usano questi metodi, i dati acquisiti vengono archiviati nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a2fdb-126">When you use these methods, the captured data is stored in the same capture file.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2fdb-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2fdb-127">Requirements</span></span>



| <span data-ttu-id="a2fdb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2fdb-128">Requirement</span></span> | <span data-ttu-id="a2fdb-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a2fdb-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2fdb-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2fdb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fdb-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2fdb-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a2fdb-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2fdb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fdb-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2fdb-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a2fdb-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2fdb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2fdb-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a2fdb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a2fdb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2fdb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2fdb-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2fdb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2fdb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2fdb-139">IStats</span><span class="sxs-lookup"><span data-stu-id="a2fdb-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="a2fdb-140">IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="a2fdb-140">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="a2fdb-141">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="a2fdb-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="a2fdb-142">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="a2fdb-142">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="a2fdb-143">IStats:: Resume</span><span class="sxs-lookup"><span data-stu-id="a2fdb-143">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="a2fdb-144">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="a2fdb-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




