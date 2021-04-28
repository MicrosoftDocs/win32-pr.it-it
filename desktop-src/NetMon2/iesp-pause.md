---
description: "Metodo IESP::P ause: il metodo Pause sospende l'acquisizione corrente."
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: Metodo IESP::P ause (Netmon.h)
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
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084239"
---
# <a name="iesppause-method"></a><span data-ttu-id="dfd23-103">Metodo IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="dfd23-103">IESP::Pause method</span></span>

<span data-ttu-id="dfd23-104">Il **metodo Pause** sospende l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfd23-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfd23-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="dfd23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfd23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfd23-107">*lpStats*</span><span class="sxs-lookup"><span data-stu-id="dfd23-107">*lpStats*</span></span> 
</dt> <dd>

<span data-ttu-id="dfd23-108">Obsoleta.</span><span class="sxs-lookup"><span data-stu-id="dfd23-108">Obsolete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfd23-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfd23-109">Return value</span></span>

<span data-ttu-id="dfd23-110">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="dfd23-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dfd23-111">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfd23-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dfd23-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dfd23-112">Return code</span></span>                                                                                           | <span data-ttu-id="dfd23-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfd23-113">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfd23-114"><dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-114"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="dfd23-115">L'acquisizione è già sospesa.</span><span class="sxs-lookup"><span data-stu-id="dfd23-115">The capture is already paused.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="dfd23-116"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="dfd23-117">Il NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="dfd23-117">The NPP is not capturing data.</span></span> <span data-ttu-id="dfd23-118">Chiamare [IESP::Start](iesp-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfd23-118">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="dfd23-119"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-119"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="dfd23-120">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="dfd23-120">The NPP is not connected to the network.</span></span> <span data-ttu-id="dfd23-121">Chiamare [IESP::Connect](iesp-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="dfd23-121">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dfd23-122"><dt>**NMERR \_ NON \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-122"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>        | <span data-ttu-id="dfd23-123">Il NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="dfd23-123">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="dfd23-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfd23-124">Remarks</span></span>

<span data-ttu-id="dfd23-125">Mentre l'acquisizione è in pausa, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non si chiama il metodo [IESP::Resume](iesp-resume.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfd23-125">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until you call the [IESP::Resume](iesp-resume.md) method to restart the capture.</span></span> <span data-ttu-id="dfd23-126">Quando **sospendi** **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="dfd23-126">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="dfd23-127">Quando si usano i metodi **IESP::P ause** e **IESP::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="dfd23-127">When you use the **IESP::Pause** and **IESP::Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="dfd23-128">Per riavviare l'acquisizione, chiamare [IESP::Resume](iesp-resume.md).</span><span class="sxs-lookup"><span data-stu-id="dfd23-128">To restart the capture, call [IESP::Resume](iesp-resume.md).</span></span> <span data-ttu-id="dfd23-129">Per arrestare l'acquisizione, chiamare [IESP::Stop](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="dfd23-129">To stop the capture, call [IESP::Stop](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd23-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfd23-130">Requirements</span></span>



| <span data-ttu-id="dfd23-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd23-131">Requirement</span></span> | <span data-ttu-id="dfd23-132">Valore</span><span class="sxs-lookup"><span data-stu-id="dfd23-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd23-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd23-133">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd23-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfd23-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dfd23-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfd23-135">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd23-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfd23-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dfd23-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfd23-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfd23-138"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dfd23-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dfd23-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfd23-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfd23-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfd23-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfd23-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd23-142">IESP</span><span class="sxs-lookup"><span data-stu-id="dfd23-142">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="dfd23-143">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="dfd23-143">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="dfd23-144">IESP::Resume</span><span class="sxs-lookup"><span data-stu-id="dfd23-144">IESP::Resume</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="dfd23-145">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="dfd23-145">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="dfd23-146">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="dfd23-146">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




