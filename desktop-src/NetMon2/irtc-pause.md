---
description: Il metodo pause sospende l'acquisizione corrente.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: Metodo IRTC::P ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2593c380d0fea52d030586da2f473a3f3fa9446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226965"
---
# <a name="irtcpause-method"></a><span data-ttu-id="d8228-103">IRTC::P metodo ause</span><span class="sxs-lookup"><span data-stu-id="d8228-103">IRTC::Pause method</span></span>

<span data-ttu-id="d8228-104">Il metodo **pause** sospende l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="d8228-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8228-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8228-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="d8228-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8228-106">Parameters</span></span>

<span data-ttu-id="d8228-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d8228-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d8228-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8228-108">Return value</span></span>

<span data-ttu-id="d8228-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d8228-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d8228-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="d8228-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d8228-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d8228-111">Return code</span></span>                                                                                           | <span data-ttu-id="d8228-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8228-112">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8228-113"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="d8228-114">Acquisizione già sospesa.</span><span class="sxs-lookup"><span data-stu-id="d8228-114">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d8228-115"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="d8228-116">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="d8228-116">The NPP is not capturing data.</span></span> <span data-ttu-id="d8228-117">Chiamare [IRTC:: Start](irtc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d8228-117">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="d8228-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="d8228-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d8228-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="d8228-120">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="d8228-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d8228-121"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="d8228-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d8228-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d8228-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8228-123">Remarks</span></span>

<span data-ttu-id="d8228-124">Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi frame non vengono acquisiti fino a quando non viene chiamato il metodo [IRTC:: Resume](irtc-resume.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d8228-124">While the capture is in a paused state, new frames are not captured until the [IRTC::Resume](irtc-resume.md) method is called to restart the capture.</span></span>

<span data-ttu-id="d8228-125">Quando si usano i metodi **IRTC::P ause** e **IRTC:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="d8228-125">When you use the **IRTC::Pause** and **IRTC::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="d8228-126">Per riavviare la chiamata di acquisizione [IRTC:: Resume](irtc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="d8228-126">To restart the capture call [IRTC::Resume](irtc-resume.md).</span></span> <span data-ttu-id="d8228-127">Per arrestare l'acquisizione, chiamare [IRTC:: Stop](irtc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="d8228-127">To stop the capture, call [IRTC::Stop](irtc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8228-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8228-128">Requirements</span></span>



| <span data-ttu-id="d8228-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8228-129">Requirement</span></span> | <span data-ttu-id="d8228-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d8228-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8228-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8228-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d8228-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8228-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d8228-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8228-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d8228-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d8228-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d8228-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8228-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8228-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-136"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d8228-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d8228-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8228-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8228-138"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8228-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8228-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8228-140">IRTC</span><span class="sxs-lookup"><span data-stu-id="d8228-140">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d8228-141">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="d8228-141">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="d8228-142">IRTC:: Resume</span><span class="sxs-lookup"><span data-stu-id="d8228-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="d8228-143">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="d8228-143">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="d8228-144">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="d8228-144">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




