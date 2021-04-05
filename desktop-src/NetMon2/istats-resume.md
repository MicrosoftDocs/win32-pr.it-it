---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'Metodo IStats:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883665"
---
# <a name="istatsresume-method"></a><span data-ttu-id="40ef0-103">IStats:: Resume (metodo)</span><span class="sxs-lookup"><span data-stu-id="40ef0-103">IStats::Resume method</span></span>

<span data-ttu-id="40ef0-104">Il metodo **Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="40ef0-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ef0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40ef0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="40ef0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40ef0-106">Parameters</span></span>

<span data-ttu-id="40ef0-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="40ef0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40ef0-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40ef0-108">Return value</span></span>

<span data-ttu-id="40ef0-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="40ef0-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="40ef0-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="40ef0-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="40ef0-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="40ef0-111">Return code</span></span>                                                                                                | <span data-ttu-id="40ef0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40ef0-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40ef0-113"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="40ef0-114">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="40ef0-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="40ef0-115"><dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="40ef0-116">L'acquisizione non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="40ef0-116">The capture is not paused.</span></span> <span data-ttu-id="40ef0-117">Chiamare il metodo [IStats::P ause](istats-pause.md) per arrestare temporaneamente l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="40ef0-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="40ef0-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="40ef0-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="40ef0-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="40ef0-120">Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="40ef0-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="40ef0-121"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="40ef0-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="40ef0-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="40ef0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="40ef0-123">Remarks</span></span>

<span data-ttu-id="40ef0-124">Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono acquisiti fino a quando non viene chiamato il metodo IStats:: Resume per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="40ef0-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="40ef0-125">Quando si utilizzano i metodi di **sospensione** e **ripresa** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="40ef0-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="40ef0-126">Per arrestare l'acquisizione, chiamare [IStats:: Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="40ef0-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40ef0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40ef0-127">Requirements</span></span>



| <span data-ttu-id="40ef0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="40ef0-128">Requirement</span></span> | <span data-ttu-id="40ef0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="40ef0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ef0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ef0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="40ef0-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40ef0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="40ef0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40ef0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="40ef0-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="40ef0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="40ef0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40ef0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ef0-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="40ef0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="40ef0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ef0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ef0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40ef0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40ef0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ef0-139">IStats</span><span class="sxs-lookup"><span data-stu-id="40ef0-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="40ef0-140">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="40ef0-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="40ef0-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="40ef0-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="40ef0-142">IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="40ef0-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




