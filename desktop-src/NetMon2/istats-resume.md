---
description: "Metodo IStats::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: Metodo IStats::Resume (Netmon.h)
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
ms.openlocfilehash: ee7818da3d8a02e41488d473d3cf26607d3b84ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114619"
---
# <a name="istatsresume-method"></a><span data-ttu-id="60222-103">Metodo IStats::Resume</span><span class="sxs-lookup"><span data-stu-id="60222-103">IStats::Resume method</span></span>

<span data-ttu-id="60222-104">Il **metodo Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="60222-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="60222-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60222-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="60222-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60222-106">Parameters</span></span>

<span data-ttu-id="60222-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="60222-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="60222-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60222-108">Return value</span></span>

<span data-ttu-id="60222-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="60222-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="60222-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="60222-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="60222-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="60222-111">Return code</span></span>                                                                                                | <span data-ttu-id="60222-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60222-112">Description</span></span>                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60222-113"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="60222-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="60222-114">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="60222-114">The NPP is not connected to the network.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="60222-115"><dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="60222-115"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="60222-116">L'acquisizione non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="60222-116">The capture is not paused.</span></span> <span data-ttu-id="60222-117">Chiamare il [metodo IStats::P ause](istats-pause.md) per arrestare temporaneamente l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="60222-117">Call the [IStats::Pause](istats-pause.md) method to temporarily stop the capture.</span></span><br/>                     |
| <dl> <span data-ttu-id="60222-118"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="60222-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="60222-119">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="60222-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="60222-120">Chiamare il [metodo IStats::Connect](istats-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="60222-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="60222-121"><dt>**NMERR \_ NON \_ SOLO \_ STATISTICHE**</dt></span><span class="sxs-lookup"><span data-stu-id="60222-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl>     | <span data-ttu-id="60222-122">Il NPP è connesso alla rete, ma non con [il metodo IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="60222-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="60222-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="60222-123">Remarks</span></span>

<span data-ttu-id="60222-124">Mentre l'acquisizione è sospesa, i nuovi dati non vengono acquisiti fino a quando non viene chiamato il metodo IStats::Resume per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="60222-124">While the capture is in a paused state, new data is not captured until the IStats::Resume method is called to restart the capture.</span></span>

<span data-ttu-id="60222-125">Quando si usano **i metodi Pause** e **Resume** per controllare [](c.md) l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="60222-125">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="60222-126">Per arrestare l'acquisizione, [chiamare IStats::Stop](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="60222-126">To stop the capture, call [IStats::Stop](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60222-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60222-127">Requirements</span></span>



| <span data-ttu-id="60222-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="60222-128">Requirement</span></span> | <span data-ttu-id="60222-129">Valore</span><span class="sxs-lookup"><span data-stu-id="60222-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60222-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60222-130">Minimum supported client</span></span><br/> | <span data-ttu-id="60222-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60222-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="60222-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60222-132">Minimum supported server</span></span><br/> | <span data-ttu-id="60222-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="60222-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="60222-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60222-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="60222-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="60222-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="60222-136">DLL</span><span class="sxs-lookup"><span data-stu-id="60222-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60222-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60222-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60222-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60222-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60222-139">IStat</span><span class="sxs-lookup"><span data-stu-id="60222-139">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="60222-140">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="60222-140">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="60222-141">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="60222-141">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="60222-142">IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="60222-142">IStats::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




