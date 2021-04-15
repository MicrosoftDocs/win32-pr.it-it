---
description: Il metodo pause sospende l'acquisizione corrente.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: Metodo IESP::P ause (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0558c5dfe36f26e3aad9f31101364d2e8e5c4967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525117"
---
# <a name="iesppause-method"></a><span data-ttu-id="80b7c-103">IESP::P metodo ause</span><span class="sxs-lookup"><span data-stu-id="80b7c-103">IESP::Pause method</span></span>

<span data-ttu-id="80b7c-104">Il metodo **pause** sospende l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="80b7c-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80b7c-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="80b7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80b7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80b7c-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="80b7c-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="80b7c-108">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="80b7c-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80b7c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80b7c-109">Return value</span></span>

<span data-ttu-id="80b7c-110">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="80b7c-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="80b7c-111">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="80b7c-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="80b7c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="80b7c-112">Return code</span></span>                                                                                           | <span data-ttu-id="80b7c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80b7c-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80b7c-114"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="80b7c-115">Acquisizione già sospesa.</span><span class="sxs-lookup"><span data-stu-id="80b7c-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="80b7c-116"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="80b7c-117">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="80b7c-117">The NPP is not capturing data.</span></span> <span data-ttu-id="80b7c-118">Chiamare [IESP:: Start](iesp-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="80b7c-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="80b7c-119"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="80b7c-120">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="80b7c-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="80b7c-121">Chiamare [IESP:: Connect](iesp-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="80b7c-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="80b7c-122"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="80b7c-123">L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="80b7c-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="80b7c-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="80b7c-124">Remarks</span></span>

<span data-ttu-id="80b7c-125">Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato il metodo [IESP:: Resume](iesp-resume.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="80b7c-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="80b7c-126">Quando si utilizzano **pause** e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="80b7c-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="80b7c-127">Quando si usano i metodi **IESP::P ause** e **IESP:: Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) ogni volta che viene eseguita l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="80b7c-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="80b7c-128">Per riavviare l'acquisizione, chiamare [IESP:: Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="80b7c-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="80b7c-129">Per arrestare l'acquisizione, chiamare [IESP:: Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="80b7c-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80b7c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80b7c-130">Requirements</span></span>



| <span data-ttu-id="80b7c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="80b7c-131">Requirement</span></span> | <span data-ttu-id="80b7c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="80b7c-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80b7c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80b7c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="80b7c-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80b7c-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="80b7c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80b7c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="80b7c-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80b7c-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="80b7c-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80b7c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b7c-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="80b7c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="80b7c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b7c-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b7c-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b7c-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80b7c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b7c-142">IESP</span><span class="sxs-lookup"><span data-stu-id="80b7c-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="80b7c-143">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="80b7c-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="80b7c-144">IESP:: Resume</span><span class="sxs-lookup"><span data-stu-id="80b7c-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="80b7c-145">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="80b7c-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="80b7c-146">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="80b7c-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




