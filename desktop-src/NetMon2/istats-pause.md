---
description: Il metodo pause interrompe temporaneamente l'acquisizione corrente.
ms.assetid: 43176e9e-1502-484c-a8af-4e7bbf5f6474
title: IStats::P metodo ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d9e9f04ce3d25399866c711dad7a853f2c43c2ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319940"
---
# <a name="istatspause-method"></a><span data-ttu-id="564c5-103">IStats::P metodo ause</span><span class="sxs-lookup"><span data-stu-id="564c5-103">IStats::Pause method</span></span>

<span data-ttu-id="564c5-104">Il metodo **pause** interrompe temporaneamente l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="564c5-104">The **Pause** method temporarily stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="564c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="564c5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="564c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="564c5-106">Parameters</span></span>

<span data-ttu-id="564c5-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="564c5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="564c5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="564c5-108">Return value</span></span>

<span data-ttu-id="564c5-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="564c5-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="564c5-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="564c5-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="564c5-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="564c5-111">Return code</span></span>                                                                                            | <span data-ttu-id="564c5-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="564c5-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="564c5-113"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl>  | <span data-ttu-id="564c5-114">Acquisizione già sospesa.</span><span class="sxs-lookup"><span data-stu-id="564c5-114">The capture is already paused.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="564c5-115"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="564c5-116">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="564c5-116">The NPP is not capturing data.</span></span> <span data-ttu-id="564c5-117">Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="564c5-117">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="564c5-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="564c5-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="564c5-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="564c5-120">Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="564c5-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="564c5-121"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="564c5-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="564c5-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="564c5-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="564c5-123">Remarks</span></span>

<span data-ttu-id="564c5-124">Quando l'acquisizione viene sospesa, i nuovi frame non vengono acquisiti fino a quando una chiamata al metodo [IStats:: Resume](istats-resume.md) riavvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="564c5-124">While the capture is paused, new frames are not captured until a call to the [IStats::Resume](istats-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="564c5-125">Quando si usano i metodi **IStats::P ause** e **IStats:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="564c5-125">When you use the **IStats::Pause** and **IStats::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="564c5-126">Per riavviare la chiamata di acquisizione [IStats:: Resume](istats-resume.md).</span><span class="sxs-lookup"><span data-stu-id="564c5-126">To restart the capture call [IStats::Resume](istats-resume.md).</span></span> <span data-ttu-id="564c5-127">Per arrestare l'acquisizione, chiamare [IStats:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="564c5-127">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="564c5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="564c5-128">Requirements</span></span>



| <span data-ttu-id="564c5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="564c5-129">Requirement</span></span> | <span data-ttu-id="564c5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="564c5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="564c5-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="564c5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="564c5-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="564c5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="564c5-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="564c5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="564c5-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="564c5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="564c5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="564c5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="564c5-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="564c5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="564c5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="564c5-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="564c5-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="564c5-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="564c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="564c5-140">IStats</span><span class="sxs-lookup"><span data-stu-id="564c5-140">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="564c5-141">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="564c5-141">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="564c5-142">IStats:: Resume</span><span class="sxs-lookup"><span data-stu-id="564c5-142">IStats::Resume</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="564c5-143">IStats:: Start</span><span class="sxs-lookup"><span data-stu-id="564c5-143">IStats::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="564c5-144">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="564c5-144">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




